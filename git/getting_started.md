### **Git Tutorial in Simple Terms**  
Git is a **version control system** that helps you track changes in your code, collaborate with others, and revert to older versions if something breaks.  

---

## **1. Basic Git Commands**  

### **① Initialize a Git Repository**  
```bash
git init
```  
- Turns your folder into a Git-tracked project.  

**Use Case:** Starting a new project.  

---

### **② Check File Status**  
```bash
git status
```  
- Shows which files are **new/modified/deleted**.  

**Use Case:** Before committing, check what changes you made.  

---

### **③ Stage Changes (Add to "Ready to Commit" List)**  
```bash
git add <file>       # Add a specific file
git add .            # Add all changes
```  
- Prepares changes for saving (commit).  

**Use Case:** You fixed a bug and want to save it.  

---

### **④ Commit (Save Changes with a Message)**  
```bash
git commit -m "Fixed the login bug"
```  
- Takes a "snapshot" of your changes.  

**Use Case:** After testing a feature, save it permanently.  

---

### **⑤ View Commit History**  
```bash
git log
```  
- Shows all past commits (who, when, what).  

**Use Case:** Find when a bug was introduced.  

---

## **2. Working with Remote Repositories (GitHub/GitLab)**  

### **⑥ Connect to a Remote Repository**  
```bash
git remote add origin <repo-url>
```  
- Links your local Git to a cloud repo (like GitHub).  

**Use Case:** Uploading your project to GitHub for backup/collaboration.  

---

### **⑦ Push Changes to Remote**  
```bash
git push origin main
```  
- Uploads your commits to GitHub/GitLab.  

**Use Case:** Sharing your code with teammates.  

---

### **⑧ Pull Latest Changes**  
```bash
git pull origin main
```  
- Downloads updates from the remote repo.  

**Use Case:** Getting the latest code from your team.  

---

### **⑨ Clone a Repository (Download a Project)**  
```bash
git clone <repo-url>
```  
- Copies a remote repo to your computer.  

**Use Case:** Starting work on an existing project.  

---

## **3. Branching (Working on Features Safely)**  

### **⑩ Create & Switch to a New Branch**  
```bash
git checkout -b new-feature
```  
- Creates a separate workspace for testing new code.  

**Use Case:** Developing a new feature without breaking the main code.  

---

### **⑪ Merge a Branch**  
```bash
git checkout main
git merge new-feature
```  
- Combines changes from `new-feature` into `main`.  

**Use Case:** After testing, adding the feature to the main project.  

---

## **4. Undoing Mistakes**  

### **⑫ Undo Unstaged Changes**  
```bash
git restore <file>
```  
- Reverts a file to its last committed state.  

**Use Case:** You messed up and want to discard recent edits.  

---

### **⑬ Undo a Commit (Soft Reset)**  
```bash
git reset --soft HEAD~1
```  
- Removes the last commit but keeps changes.  

**Use Case:** You committed too early and want to fix the message.  

---

### **⑭ Revert a Commit (Safe Undo)**  
```bash
git revert <commit-hash>
```  
- Creates a new commit that reverses an old one.  

**Use Case:** You pushed a bug and need to roll back safely.  

---

## **Real-World Use Cases**  
1. **Personal Project** – Track changes and revert if something breaks.  
2. **Team Collaboration** – Work on features in branches and merge safely.  
3. **Open Source Contributions** – Fork, edit, and submit pull requests.  
4. **Bug Fixes** – Use `git log` to find when a bug was introduced.  

---

### **Next Steps**  
- Try these commands in a test folder.  
- Create a free GitHub account and push a project.  

Want a deeper dive into any part? 😊