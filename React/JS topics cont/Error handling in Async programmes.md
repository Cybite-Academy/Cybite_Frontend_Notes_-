# Error Handling in Asynchronous JavaScript

Error handling is crucial in asynchronous operations because things can go wrong in many ways - network failures, server errors, invalid data, timeouts, etc. Let me explain how to handle errors in different async patterns.

## 1. Callback Pattern Error Handling

In the callback pattern, errors are typically handled using the "error-first" convention:

```javascript
function fetchData(callback) {
    // Simulate an async operation that might fail
    setTimeout(() => {
        const success = Math.random() > 0.5; // 50% chance of success
        if (success) {
            callback(null, 'Data received!'); // First parameter is for errors
        } else {
            callback('Error: Failed to fetch data', null);
        }
    }, 1000);
}

// Usage
fetchData((error, data) => {
    if (error) {
        console.error('Something went wrong:', error);
        return;
    }
    console.log('Success:', data);
});
```

**Key Points:**
- First parameter is reserved for error
- Second parameter is for successful result
- Always check for error first

## 2. Promise Error Handling

Promises provide cleaner error handling with `.catch()`:

```javascript
function fetchData() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const success = Math.random() > 0.5;
            if (success) {
                resolve('Data received!');
            } else {
                reject('Error: Failed to fetch data');
            }
        }, 1000);
    });
}

// Usage
fetchData()
    .then(data => console.log('Success:', data))
    .catch(error => console.error('Something went wrong:', error));
```

**Alternative Approach (chaining):**
```javascript
fetchData()
    .then(data => {
        console.log('Success:', data);
        return processData(data); // can chain more operations
    })
    .catch(error => {
        console.error('Error in chain:', error);
    });
```

## 3. Async/Await Error Handling

The cleanest way is using try/catch blocks:

```javascript
async function getData() {
    try {
        const data = await fetchData();
        console.log('Success:', data);
    } catch (error) {
        console.error('Something went wrong:', error);
    }
}

getData();
```

**Important Notes:**
1. `await` must be inside an `async` function
2. `try/catch` works just like with synchronous code
3. Uncaught errors in async functions will reject their promise

## Advanced Error Handling Techniques

### 1. Handling Multiple Async Operations

```javascript
async function fetchAllData() {
    try {
        const [users, posts] = await Promise.all([
            fetch('/api/users'),
            fetch('/api/posts')
        ]);
        
        // Additional processing
    } catch (error) {
        console.error('Failed to fetch all data:', error);
        // Maybe implement retry logic here
    }
}
```

### 2. Retry Mechanism

```javascript
async function fetchWithRetry(url, retries = 3) {
    try {
        const response = await fetch(url);
        return await response.json();
    } catch (err) {
        if (retries <= 0) {
            throw new Error('Max retries reached');
        }
        console.log(`Retrying... (${retries} left)`);
        return fetchWithRetry(url, retries - 1);
    }
}
```

### 3. Error Wrapping

```javascript
class NetworkError extends Error {
    constructor(message) {
        super(message);
        this.name = 'NetworkError';
    }
}

async function fetchData() {
    try {
        const response = await fetch('api/data');
        if (!response.ok) {
            throw new NetworkError('Bad response');
        }
        return response.json();
    } catch (err) {
        // Convert generic errors to specific ones
        if (err.message.includes('Failed to fetch')) {
            throw new NetworkError('Connection failed');
        }
        throw err; // rethrow other errors
    }
}
```

## Common Pitfalls

1. **Unhandled Promise Rejections**
   - Always include `.catch()` or try/catch
   - In Node.js, listen for `unhandledRejection` event

2. **Forgetting await**
   ```javascript
   // BAD - error won't be caught
   async function example() {
       try {
           return fetchData(); // missing await!
       } catch (err) {
           console.error(err); // never reached
       }
   }
   ```

3. **Over-nesting Error Handling**
   - Avoid nesting try/catch blocks too deeply
   - Consider error handling at appropriate levels

## Best Practices

1. Be specific with error types
2. Fail fast and loud in development
3. Graceful degradation in production
4. Log errors with context (stack traces, request IDs)
5. Consider centralized error handling for larger apps

Remember: Good error handling makes your application more robust and easier to debug!