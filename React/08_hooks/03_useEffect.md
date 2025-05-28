# **useEffect Hook - Simple Tutorial with Practical Use Cases**

`useEffect` is like a Swiss Army knife for side effects in React components. It lets you perform actions when your component renders or when specific data changes.

## **How useEffect Works**
```jsx
useEffect(() => {
  // Your side effect code here
  return () => {
    // Cleanup (optional)
  };
}, [dependencies]); // Dependency array
```

### **The 3 Main Use Patterns**:
1. **Run on every render** (no dependency array)
   ```jsx
   useEffect(() => { console.log("I run every time") });
   ```
2. **Run once on mount** (empty array)
   ```jsx
   useEffect(() => { console.log("I run only once") }, []);
   ```
3. **Run when dependencies change**
   ```jsx
   useEffect(() => { console.log("I run when 'count' changes") }, [count]);
   ```

---

## **5 Practical Use Cases**

### 1️⃣ **Fetching Data (API Calls)**
```jsx
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    fetch(`https://api.example.com/users/${userId}`)
      .then(response => response.json())
      .then(data => setUser(data));
  }, [userId]); // Re-fetch when userId changes

  if (!user) return <p>Loading...</p>;

  return <h1>{user.name}</h1>;
}
```
**When to use:** Loading user data, products, posts

---

### 2️⃣ **Updating Document Title**
```jsx
function PageTracker() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  }, [count]); // Update when count changes

  return <button onClick={() => setCount(c => c + 1)}>Click me</button>;
}
```
**When to use:** Dynamic page titles, analytics tracking

---

### 3️⃣ **Event Listeners**
```jsx
function WindowSizeTracker() {
  const [size, setSize] = useState({
    width: window.innerWidth,
    height: window.innerHeight
  });

  useEffect(() => {
    const handleResize = () => {
      setSize({
        width: window.innerWidth,
        height: window.innerHeight
      });
    };

    window.addEventListener('resize', handleResize);
    
    return () => {
      window.removeEventListener('resize', handleResize); // Cleanup
    };
  }, []); // Only run once on mount

  return <p>Window size: {size.width}x{size.height}</p>;
}
```
**When to use:** Keyboard shortcuts, scroll events, resize handling

---

### 4️⃣ **Timer/Interval**
```jsx
function Timer() {
  const [seconds, setSeconds] = useState(0);

  useEffect(() => {
    const interval = setInterval(() => {
      setSeconds(s => s + 1);
    }, 1000);

    return () => clearInterval(interval); // Cleanup
  }, []); // Run once on mount

  return <p>Seconds: {seconds}</p>;
}
```
**When to use:** Countdowns, auto-refreshing data

---

### 5️⃣ **Form Validation**
```jsx
function EmailForm() {
  const [email, setEmail] = useState("");
  const [isValid, setIsValid] = useState(false);

  useEffect(() => {
    const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    setIsValid(regex.test(email));
  }, [email]); // Validate on email change

  return (
    <form>
      <input 
        type="email" 
        value={email}
        onChange={(e) => setEmail(e.target.value)}
      />
      {!isValid && <p>Please enter a valid email</p>}
    </form>
  );
}
```
**When to use:** Real-time validation, dependent fields

---

## **Key Rules to Remember**
1. **Clean up after yourself** (return cleanup function)
   ```jsx
   useEffect(() => {
     const subscription = someAPI.subscribe();
     return () => subscription.unsubscribe();
   }, []);
   ```
2. **Don't forget dependencies** (or you'll get stale values)
3. **Multiple effects are okay** (separate concerns)
   ```jsx
   useEffect(() => { /* API call */ }, [userId]);
   useEffect(() => { /* Analytics */ }, [pageView]);
   ```

---

## **When NOT to Use useEffect**
❌ For state transformations (use `useMemo` instead)  
❌ For event handlers (just put logic in the handler)  
❌ As a "watch everything" solution (be specific with dependencies)  

---

## **Real-World Examples**
- **Chat App:** Fetch new messages every 5 seconds
- **E-commerce:** Update recommendations when category changes
- **Dashboard:** Subscribe to real-time data streams
- **Form:** Auto-save draft every minute
- **Game:** Clean up animations when component unmounts

**Try this exercise:** Create a component that:
1. Fetches a random joke from an API on mount
2. Has a button to fetch a new joke
3. Shows loading state while fetching

```jsx
function JokeGenerator() {
  const [joke, setJoke] = useState(null);
  const [loading, setLoading] = useState(false);

  const fetchJoke = async () => {
    setLoading(true);
    const response = await fetch("https://official-joke-api.appspot.com/random_joke");
    const data = await response.json();
    setJoke(data);
    setLoading(false);
  };

  useEffect(() => {
    fetchJoke();
  }, []);

  return (
    <div>
      {loading ? <p>Loading...</p> : (
        joke && <p>{joke.setup} - {joke.punchline}</p>
      )}
      <button onClick={fetchJoke}>New Joke</button>
    </div>
  );
}
```

`useEffect` is your go-to for anything that happens "outside" React's render cycle. What side effect will you implement first? 🚀