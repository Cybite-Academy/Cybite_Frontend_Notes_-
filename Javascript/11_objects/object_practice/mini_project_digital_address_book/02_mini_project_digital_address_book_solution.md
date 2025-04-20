# Solution
<br>
<br>

### ✅ Step 1: Create One Contact Object

```js
const contact1 = {
  name: "Amaka",
  phone: "08123456789",
  email: "amaka@example.com",
};
```

---

### ✅ Step 2: Store Multiple Contacts in an Array

```js
const contacts = [
  {
    name: "Amaka",
    phone: "08123456789",
    email: "amaka@example.com",
  },
  {
    name: "Tunde",
    phone: "08098765432",
    email: "tunde@example.com",
  },
];
```

---

### ✅ Step 3: Display All Contacts

```js
function showContacts() {
  console.log("📇 Contact List:");
  contacts.forEach((contact, index) => {
    console.log(
      `${index + 1}. ${contact.name} - ${contact.phone} - ${contact.email}`
    );
  });
}

showContacts();
```

---

### ✅ Step 4: Add a New Contact

```js
function addContact(name, phone, email) {
  const newContact = {
    name: name,
    phone: phone,
    email: email,
  };
  contacts.push(newContact);
  console.log(`✅ ${name} was added to your contacts!`);
}

addContact("Chidi", "07011223344", "chidi@example.com");
showContacts();
```

<br>
<br>
<br>

## 🧠 Extra Challenges
Perfect! Let’s level up your **Digital Address Book** project by adding:

1. 🔍 **Search** for a contact by name  
2. ❌ **Delete** a contact by name

<br>

### 🔍 1. Search Contact by Name

We'll loop through the contacts and find a match.

```js
function searchContact(name) {
  const found = contacts.find(contact => contact.name.toLowerCase() === name.toLowerCase());

  if (found) {
    console.log("🔎 Contact Found:");
    console.log(`${found.name} - ${found.phone} - ${found.email}`);
  } else {
    console.log("❌ Contact not found.");
  }
}

// Example usage:
searchContact("Tunde");
```

---

### ❌ 2. Delete Contact by Name

We’ll filter out the contact and update the list.

```js
function deleteContact(name) {
  const initialLength = contacts.length;

  const updatedContacts = contacts.filter(
    contact => contact.name.toLowerCase() !== name.toLowerCase()
  );

  if (updatedContacts.length === initialLength) {
    console.log("❌ No contact deleted. Name not found.");
  } else {
    contacts.length = 0; // Clear the original array
    contacts.push(...updatedContacts); // Refill with updated list
    console.log(`🗑️ Contact "${name}" has been deleted.`);
  }
}

// Example usage:
deleteContact("Chidi");
showContacts();
```

---

### 📦 Full Features Now Included:
- Add new contacts
- Display all contacts
- Search for a contact
- Delete a contact




<br>
<br>
<br>
<br>

Here's your **complete runnable script** 🧑‍💻 — all in one place — to practice creating, adding, searching, and deleting contacts using **JavaScript objects**.

You can run this in your browser console or in any online JS playground like [jsfiddle.net](https://jsfiddle.net/) or [codepen.io](https://codepen.io/).

---

### ✅ **Digital Address Book - Practice Script**

```js
// Initial contacts
const contacts = [
  {
    name: "Amaka",
    phone: "08123456789",
    email: "amaka@example.com"
  },
  {
    name: "Tunde",
    phone: "08098765432",
    email: "tunde@example.com"
  }
];

// Show all contacts
function showContacts() {
  console.log("📇 Contact List:");
  if (contacts.length === 0) {
    console.log("No contacts found.");
    return;
  }

  contacts.forEach((contact, index) => {
    console.log(`${index + 1}. ${contact.name} - ${contact.phone} - ${contact.email}`);
  });
}

// Add a new contact
function addContact(name, phone, email) {
  const newContact = { name, phone, email };
  contacts.push(newContact);
  console.log(`✅ ${name} was added to your contacts!`);
}

// Search for a contact by name
function searchContact(name) {
  const found = contacts.find(contact => contact.name.toLowerCase() === name.toLowerCase());

  if (found) {
    console.log("🔍 Contact Found:");
    console.log(`${found.name} - ${found.phone} - ${found.email}`);
  } else {
    console.log("❌ Contact not found.");
  }
}

// Delete a contact by name
function deleteContact(name) {
  const initialLength = contacts.length;

  const updatedContacts = contacts.filter(
    contact => contact.name.toLowerCase() !== name.toLowerCase()
  );

  if (updatedContacts.length === initialLength) {
    console.log("❌ No contact deleted. Name not found.");
  } else {
    contacts.length = 0; // clear original
    contacts.push(...updatedContacts); // refill
    console.log(`🗑️ Contact "${name}" has been deleted.`);
  }
}

// === TRY IT OUT ===

// Show initial contacts
showContacts();

// Add a new contact
addContact("Chidi", "07011223344", "chidi@example.com");

// Search for someone
searchContact("tunde");

// Delete a contact
deleteContact("amaka");

// Final contact list
showContacts();
```

---

### 💡 You Can Now:
- Run the script
- Edit names, emails, etc.
- Practice modifying it
- Try adding birthdays, addresses, or even a "favorite" tag


