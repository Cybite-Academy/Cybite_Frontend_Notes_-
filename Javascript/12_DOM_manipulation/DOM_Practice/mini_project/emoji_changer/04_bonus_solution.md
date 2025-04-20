## ✅ **Full Working Version (HTML + CSS + JS Combined)**

students can copy-paste this into a single `.html` file or test it on [CodePen](https://codepen.io/), [JSFiddle](https://jsfiddle.net/), or Live Server.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Emoji Mood Changer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 40px;
    }

    #mood-box {
      padding: 30px;
      text-align: center;
      border: 2px solid #ccc;
      border-radius: 10px;
      margin-bottom: 20px;
      transition: background-color 0.3s ease;
    }

    .buttons button, #custom-emoji + button {
      margin: 5px;
      padding: 10px 15px;
      font-size: 16px;
      cursor: pointer;
    }

    #custom-emoji {
      padding: 8px;
      width: 220px;
      font-size: 14px;
      margin-top: 10px;
    }
  </style>
</head>
<body>

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

  <hr />

  <h3>Custom Mood</h3>
  <input type="text" id="custom-emoji" placeholder="Type mood + emoji e.g. Sleepy 🥱" />
  <button onclick="setCustomMood()">Set Mood</button>

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

    function setCustomMood() {
      const customInput = document.getElementById("custom-emoji").value.trim();

      if (customInput !== "") {
        emoji.textContent = extractEmoji(customInput);
        message.textContent = customInput;
        box.style.backgroundColor = getRandomColor();
        document.getElementById("custom-emoji").value = "";
      }
    }

    function extractEmoji(text) {
      // Matches last emoji or non-word character
      const match = text.match(/[\p{Emoji_Presentation}\p{Emoji}\uFE0F]$/gu);
      return match ? match[0] : "😐";
    }

    function getRandomColor() {
      const hue = Math.floor(Math.random() * 360);
      return `hsl(${hue}, 100%, 90%)`;
    }
  </script>

</body>
</html>
```