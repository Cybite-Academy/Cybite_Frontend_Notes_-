# Async/Await vs. Promises - Explained Like You're 12

Imagine you're ordering pizza for you and your friends. I'll explain both concepts using this pizza example:

## Promises (The Old Way)

With promises, it's like this:
1. You call the pizza place and say "I want a pizza" (this starts the promise)
2. They say "Okay, we'll make it and call you back when it's ready" (this is the promise)
3. You can do other things while waiting (play video games)
4. When the pizza arrives, your phone rings and you say ".then() I'll eat the pizza!"

```javascript
orderPizza()
  .then(pizza => {
    eatPizza(pizza);
  })
  .catch(error => {
    console.log("Oh no! They burned the pizza!", error);
  });
```

## Async/Await (The Newer, Cleaner Way)

With async/await, it's more like:
1. You call the pizza place and say "I want a pizza" (this is the async function)
2. You say "I'll wait right here until it's ready" (this is the await)
3. The pizza arrives and you eat it right away

```javascript
async function haveDinner() {
  try {
    const pizza = await orderPizza(); // Waits here until pizza arrives
    eatPizza(pizza);
  } catch (error) {
    console.log("Oh no! They burned the pizza!", error);
  }
}
```

## Key Differences:

1. **Looks like normal code** - Async/await looks like regular step-by-step code
2. **Waiting is built-in** - The `await` keyword pauses the function until the pizza (or data) arrives
3. **Same power** - Under the hood, async/await still uses promises
4. **Easier error handling** - You can use normal try/catch blocks

## Real Code Example:

**With Promises:**
```javascript
function getData() {
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));
}
```

**With Async/Await:**
```javascript
async function getData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}
```

Async/await is like writing normal code that happens to wait for things when needed, while promises are more like setting up a chain of events that will happen in the future. Both get you pizza (data), but async/await makes it easier to follow the recipe!