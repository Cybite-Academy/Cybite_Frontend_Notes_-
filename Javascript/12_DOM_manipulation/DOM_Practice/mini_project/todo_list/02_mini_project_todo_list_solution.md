## Solution

<br>

#### **HTML**

```html
<h2>My Todo List</h2>
<input type="text" id="todo-input" placeholder="Enter a task" />
<button id="add-btn">Add Task</button>

<ul id="todo-list"></ul>
```

<br>

#### **CSS (optional styling)**

```html
<style>
  body {
    font-family: Arial;
  }
  li {
    margin: 5px 0;
  }
  .delete-btn {
    margin-left: 10px;
    color: red;
    cursor: pointer;
  }
</style>
```

<br>

#### **JavaScript**

```html
<script>
  const input = document.getElementById("todo-input");
  const addBtn = document.getElementById("add-btn");
  const todoList = document.getElementById("todo-list");

  addBtn.addEventListener("click", () => {
    const task = input.value.trim();

    if (task !== "") {
      const li = document.createElement("li");
      li.textContent = task;

      const deleteBtn = document.createElement("span");
      deleteBtn.textContent = "❌";
      deleteBtn.classList.add("delete-btn");

      deleteBtn.addEventListener("click", () => {
        li.remove();
      });

      li.appendChild(deleteBtn);
      todoList.appendChild(li);

      input.value = ""; // clear input
    }
  });
</script>
```

<br>

### **How This Uses DOM Manipulation**

- `getElementById` selects the input, button, and list.
- `createElement` makes a new task (`li`) and delete button (`span`).
- `appendChild` adds the new elements to the page.
- `addEventListener` allows interactions (add & delete).
- `remove()` deletes an item from the DOM.

<br>
<br>

## **Adding to Local Storage**

Great! Let’s upgrade the Todo List by **saving tasks to local storage** so they **stay even after refreshing the page**.

<br>

### **Updated JavaScript (with Local Storage)**

```html
<script>
  const input = document.getElementById("todo-input");
  const addBtn = document.getElementById("add-btn");
  const todoList = document.getElementById("todo-list");

  // Load tasks from local storage when page loads
  window.addEventListener("load", () => {
    const savedTasks = JSON.parse(localStorage.getItem("todos")) || [];
    savedTasks.forEach((task) => addTaskToDOM(task));
  });

  addBtn.addEventListener("click", () => {
    const task = input.value.trim();
    if (task !== "") {
      addTaskToDOM(task);
      saveTask(task);
      input.value = "";
    }
  });

  function addTaskToDOM(task) {
    const li = document.createElement("li");
    li.textContent = task;

    const deleteBtn = document.createElement("span");
    deleteBtn.textContent = "❌";
    deleteBtn.classList.add("delete-btn");

    deleteBtn.addEventListener("click", () => {
      li.remove();
      deleteTask(task);
    });

    li.appendChild(deleteBtn);
    todoList.appendChild(li);
  }

  function saveTask(task) {
    const tasks = JSON.parse(localStorage.getItem("todos")) || [];
    tasks.push(task);
    localStorage.setItem("todos", JSON.stringify(tasks));
  }

  function deleteTask(taskToDelete) {
    const tasks = JSON.parse(localStorage.getItem("todos")) || [];
    const filtered = tasks.filter((task) => task !== taskToDelete);
    localStorage.setItem("todos", JSON.stringify(filtered));
  }
</script>
```

---

### **How It Works Now:**

- When you **add a task**, it’s stored in your browser.
- When the page **reloads**, it reads and shows all saved tasks.
- When you **delete a task**, it also removes it from storage.
