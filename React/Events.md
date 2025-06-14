# React Events in Simple Terms

Events in React are how you handle user interactions like clicks, typing, hovering, etc. They work similarly to regular HTML events but with some React-specific differences.

## Basic Concepts

1. **Event Handling**: React events are named using camelCase (like `onClick`) rather than lowercase (like `onclick`).
2. **Synthetic Events**: React wraps browser events in its own event system for consistency across browsers.
3. **JSX Syntax**: You pass functions as event handlers directly in JSX.

## Common Event Examples

### 1. onClick - Handling Clicks
```jsx
function Button() {
  const handleClick = () => {
    alert('Button was clicked!');
  };

  return <button onClick={handleClick}>Click Me</button>;
}
```

**Use Case**: 
- Submit buttons
- Navigation menu toggles
- Like/upvote buttons

### 2. onChange - Handling Input Changes
```jsx
function InputField() {
  const [value, setValue] = useState('');

  const handleChange = (e) => {
    setValue(e.target.value);
  };

  return <input type="text" value={value} onChange={handleChange} />;
}
```

**Use Case**: 
- Form inputs
- Search bars
- Settings toggles

### 3. onSubmit - Handling Form Submissions
```jsx
function ContactForm() {
  const handleSubmit = (e) => {
    e.preventDefault();
    // Process form data
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* form fields */}
      <button type="submit">Submit</button>
    </form>
  );
}
```

**Use Case**: 
- Contact forms
- Login/registration forms
- Any data submission

### 4. onMouseEnter/onMouseLeave - Hover Effects
```jsx
function HoverBox() {
  const [isHovered, setIsHovered] = useState(false);

  return (
    <div 
      onMouseEnter={() => setIsHovered(true)}
      onMouseLeave={() => setIsHovered(false)}
      style={{ background: isHovered ? 'lightblue' : 'white' }}
    >
      Hover over me!
    </div>
  );
}
```

**Use Case**: 
- Tooltips
- Interactive menus
- Highlighting elements

### 5. onKeyDown - Keyboard Inputs
```jsx
function SearchBox() {
  const handleKeyDown = (e) => {
    if (e.key === 'Enter') {
      // Perform search
    }
  };

  return <input type="text" onKeyDown={handleKeyDown} />;
}
```

**Use Case**: 
- Keyboard shortcuts
- Handling Enter key in forms
- Game controls

## Important Notes

1. Always pass the function reference, don't call it immediately:
   - ✅ Correct: `onClick={handleClick}`
   - ❌ Incorrect: `onClick={handleClick()}` (this calls it during render)

2. To pass parameters, use an arrow function:
   ```jsx
   <button onClick={() => handleItemClick(item.id)}>Delete</button>
   ```

3. Prevent default behavior with `e.preventDefault()` when needed (like in forms).

4. Event propagation works the same as in DOM (bubbling up), but you can stop it with `e.stopPropagation()`.