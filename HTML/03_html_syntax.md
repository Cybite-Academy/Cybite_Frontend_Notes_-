# 📌Table of Contents

1. [HTML Syntax](#html-syntax-in-simple-terms)
2. [HTML Comment Syntax](#html-comment-syntax)

   - [Things to Know About HTML Syntax](#things-to-know-about-html-syntax)

3. [HTML Elements, Attributes and More – Explained Simply](#html-elements-attributes-and-more)

<br>
<br>
<br>

## **HTML Syntax in Simple Terms**

HTML (HyperText Markup Language) is the standard language for creating web pages. It uses **tags** enclosed in angle brackets (`< >`) to structure content.

#### **Basic Structure of an HTML Page**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Page</title>
  </head>
  <body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

<br>

### **Use Case Scenarios**

1. **Creating Web Pages** – HTML is used to structure content for websites.
2. **Building Forms** – Used for login pages, registrations, and data collection.
3. **Embedding Media** – Used to display images, videos, and audio.
4. **Hyperlinking Pages** – Enables navigation between web pages using links.

<br>

### **Things to Know About HTML Syntax**

✅ **Tags Come in Pairs** – Most elements have an opening tag (`<tag>`) and a closing tag (`</tag>`), e.g., `<p>Hello</p>`.  
✅ **Self-Closing Tags** – Some tags don’t need a closing tag, e.g., `<img>` and `<br>`.  
✅ **Case Insensitive** – HTML is not case-sensitive, but lowercase is recommended (`<HTML>` is the same as `<html>`).  
✅ **Attributes Add Extra Information** – Attributes like `src`, `href`, and `alt` modify elements, e.g.:

```html
<img src="image.jpg" alt="Description" />
```

✅ **Nesting Matters** – Tags should be properly nested to avoid errors:

```html
<!-- Correct nesting -->
<div><p>Text</p></div>

<!-- Incorrect nesting -->
<div><p>Text</div></p>
```

<br>
<br>
<br>
<br>

## **HTML Comment Syntax**

HTML comments are written using `<!--` to start and `-->` to end the comment.

#### **Example:**

```html
<!-- This is an HTML comment -->
<p>This is visible content.</p>
<!-- <p>This content is hidden and won't appear on the webpage.</p> -->
```

#### **Use Cases of HTML Comments**

1. **Code Explanation** – Helps explain the purpose of sections in the code.
2. **Temporary Debugging** – You can comment out sections of code without deleting them.
3. **Hiding Elements** – Prevents certain elements from being displayed on the webpage.
4. **To-Do Notes** – Helps developers leave reminders for future edits.

### **Things to Know about HTML Comments**

- They do **not** appear on the webpage but are visible in the source code.
- They can be used inside `<!-- -->`, but you **cannot** nest them (`<!-- <!-- Nested comment --> -->` is invalid).
- Browsers ignore comments, so they do not affect page rendering.

<br>
<br>
<br>
<br>

## **HTML Elements, Attributes and More**

### **1️⃣ HTML Elements**

An **HTML element** consists of an opening tag, content, and a closing tag.

#### **Example:**

```html
<p>This is a paragraph.</p>
```

📌 **Parts of an HTML Element:**

- `<p>` → Opening tag
- `This is a paragraph.` → Content
- `</p>` → Closing tag

#### **Types of HTML Elements:**

✅ **Block-level Elements** – Take up the full width of the page. Examples: `<div>`, `<p>`, `<h1>` - `<h6>`, `<section>`, `<article>`.  
✅ **Inline Elements** – Only take up as much space as needed. Examples: `<span>`, `<a>`, `<strong>`, `<em>`.  
✅ **Self-closing Elements** – Don't need a closing tag. Examples: `<img>`, `<br>`, `<hr>`, `<input>`.

<br>

### **2️⃣ HTML Attributes**

Attributes **add extra information** to elements. They are always included in the **opening tag** and follow a `name="value"` format.

#### **Example:**

```html
<img src="image.jpg" alt="A sample image" width="300" />
```

📌 **Common Attributes:**

- `src` – Specifies the image source (`<img>`).
- `alt` – Provides alternative text for images (`<img>`).
- `href` – Specifies a link destination (`<a>`).
- `id` – Assigns a unique identifier (`<div id="header">`).
- `class` – Groups elements for styling (`<p class="text-style">`).
- `style` – Adds inline CSS (`<p style="color: red;">Red Text</p>`).

#### **More Attribute Examples:**

```html
<a href="https://example.com" target="_blank">Visit Example</a>
<input type="text" placeholder="Enter your name" />
<button disabled>Click Me</button>
```

<br>

### **3️⃣ HTML Tags vs. Elements vs. Attributes**

| Feature       | Description                                                      | Example                          |
| ------------- | ---------------------------------------------------------------- | -------------------------------- |
| **Tag**       | The actual HTML command enclosed in `< >`                        | `<p>`                            |
| **Element**   | A complete structure with an opening & closing tag, plus content | `<p>Hello</p>`                   |
| **Attribute** | Extra information inside an opening tag                          | `<a href="https://example.com">` |
