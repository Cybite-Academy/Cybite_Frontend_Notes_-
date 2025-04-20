## Solution
#### 📄 **Basic HTML:**

```html
<h2>Mood Changer 😎</h2>

<div id="mood-box">
  <div id="emoji" style="font-size: 80px;">😐</div>
  <p id="message">Click a mood to change how I feel!</p>
</div>

<div class="buttons">
  <button onclick="changeMood('happy')">Happy 😊</button>
  <button onclick="changeMood('sad')">Sad 😢</button>
  <button onclick="changeMood('angry')">Angry 😠</button>
  <button onclick="changeMood('excited')">Excited 🤩</button>
</div>
```

<br>

#### 🎨 **Simple CSS (Optional):**

```html
<style>
  #mood-box {
    padding: 30px;
    text-align: center;
    border: 2px solid #ccc;
    border-radius: 10px;
    margin-bottom: 20px;
    transition: background-color 0.3s ease;
  }
  .buttons button {
    margin: 5px;
    padding: 10px 15px;
    font-size: 16px;
    cursor: pointer;
  }
</style>
```

<br>

#### 🧠 **JavaScript:**

```html
<script>
  const emoji = document.getElementById("emoji");
  const message = document.getElementById("message");
  const box = document.getElementById("mood-box");

  function changeMood(mood) {
    if (mood === "happy") {
      emoji.textContent = "😊";
      message.textContent = "I'm feeling happy!";
      box.style.backgroundColor = "#e0ffcc";
    } else if (mood === "sad") {
      emoji.textContent = "😢";
      message.textContent = "Feeling kinda blue...";
      box.style.backgroundColor = "#cce0ff";
    } else if (mood === "angry") {
      emoji.textContent = "😠";
      message.textContent = "I'm really angry!";
      box.style.backgroundColor = "#ffc1c1";
    } else if (mood === "excited") {
      emoji.textContent = "🤩";
      message.textContent = "Woohoo! Let’s go!";
      box.style.backgroundColor = "#ffe680";
    }
  }
</script>
```

<br>

### 💪 **Why This Is Great for Beginners:**

- It’s visual and fun (emojis + colors).
- Teaches the core of DOM manipulation: selecting elements, changing text/content, styling, and event handling.
- Easy to extend — students can add more moods, use `switch` instead of `if`, or add sound later on.