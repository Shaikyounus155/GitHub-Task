# GitHub-Task

# 🚀 TASK 4: Build a Version-Controlled DevOps Project with Git

## 🎯 Objective
Manage a DevOps project using Git best practices for collaboration, traceability, and automation.

---

## 🧰 Tools
- Git
- GitHub

---

## ✅ Deliverables
- Project repository on GitHub  
- Proper commit messages and version history  
- Branching strategy (`main`, `dev`, `feature/*`)  
- Pull requests for all merges  
- `README.md` explaining the project  
- `.gitignore` to exclude unnecessary files  
- Git tags for releases  
- Documentation for tasks using markdown
- 
**Git** is a **version control system**—a tool that helps developers **track changes** in their code over time, **collaborate** with others, and **manage multiple versions** of a project efficiently.

Here’s a breakdown of what Git is and what it does:

---

### 🔧 **What is Git?**

Git is an **open-source distributed version control system**, originally created by **Linus Torvalds** (the creator of Linux) in **2005**. It allows you to manage your project's history and collaborate with others without overwriting each other's work.

---

### 📌 **Key Features of Git:**

1. **Distributed System:**
   - Every developer has a full copy of the repository, including the complete history of changes.
   - You can work offline and push changes when you're ready.

2. **Snapshot-based:**
   - Git takes **snapshots** of your files (not differences) every time you commit, which makes it fast and reliable.

3. **Branching and Merging:**
   - You can create branches to work on different features or fixes independently.
   - Merging integrates those changes back into the main branch (often called `main` or `master`).

4. **Efficient Collaboration:**
   - With platforms like GitHub, GitLab, or Bitbucket, multiple developers can work together and manage code changes via pull requests.

5. **Change Tracking:**
   - Git keeps track of every change, who made it, and when—helping you debug issues and revert to previous versions if needed.

---

### 💡 **Why Use Git?**

- Prevents loss of code
- Makes collaboration smoother
- Helps maintain a clean project history
- Supports working on multiple features simultaneously
- Essential in both small and large software projects

---
PuTTY is a free and open-source terminal emulator, serial console, and network file transfer application. It's most commonly used on Windows to connect to remote servers using SSH (Secure Shell), Telnet, rlogin, or serial connections.

**🔹 What PuTTY is Used For:**

SSH into remote servers (e.g., Linux/Unix machines)

Telnet sessions

Serial communication (for routers, embedded systems, etc.)

Transferring files using tools like PSCP or PSFTP (comes with PuTTY)

**🔐 Common Use Case:**
If you’re managing a cloud server (like AWS EC2 or DigitalOcean Droplet), you can use PuTTY to:

Load your .ppk key (PuTTY Private Key)

Connect securely via SSH to your server

Run command-line tools remotely

**📦 Components of PuTTY Suite:**
putty.exe – the main terminal application

pscp.exe – command-line secure file copy (like scp)

psftp.exe – SFTP client

puttygen.exe – generates SSH key pairs

pageant.exe – SSH authentication agent for PuTTY



`git init` is the command used to **create a new Git repository**.

---

### 📌 **What does `git init` do?**

When you run:

```
git init
```

in a folder, Git will:

- Create a hidden `.git` directory inside it.
- Set up all the necessary files and structure to start tracking versions of your code.
- Turn that folder into a **Git repository**, so you can start using Git commands like `git add`, `git commit`, etc.

---


### 🛠️ **Example:**

```bash
mkdir my-project
cd my-project
git init
```

Now, `my-project` is a Git repo. You can start adding files and tracking them with Git.

---

### ✅ After `git init`, you can:

- Add files: `git add filename`
- Save changes: `git commit -m "Initial commit"`
- Check status: `git status`

---



`git add` is the command used to **tell Git which changes you want to include in your next commit**.

---

### 📌 **What does `git add` do?**

It **stages** files—this means you're preparing them to be committed. The files are added to something called the **staging area**.

---

### 🛠️ **Example Usage:**

Let's say you changed a file called `index.html`.

To stage it, you'd run:

```
git add index.html
```

Now Git knows you want to include that change in your next commit.

---

### ✅ Common Variations:

- `git add filename` — Add a specific file  
- `git add .` — Add **all** changes in the current directory and below  
- `git add -A` — Add **all changes**, including file deletions  
- `git add folder/` — Add a whole folder

---

### 🔁 Git Workflow:

Here’s a basic Git flow to help you see where `git add` fits in:

1. You edit some files.
2. You run `git add filename` to stage them.
3. You run `git commit -m "message"` to save a snapshot of those staged changes.

---

Great question! 🌿

---

### 📌 **What is `git branch`?**

`git branch` is the Git command used to:

1. **Create**, **list**, or **delete** branches in your repository.
2. A **branch** in Git is like a separate line of development. It lets you work on features or fixes **without affecting** the main code (usually `main` or `master` branch).

---

### 🧠 **Think of it like this:**

- You're writing a story.
- You want to try a different ending without changing the original.
- You make a **branch**, write your changes there.
- If you like it, you can merge it back into the original!

---

### 🛠️ **Common `git branch` Commands:**

| Command | Description |
|--------|-------------|
| `git branch` | Show all branches in your repo |
| `git branch <name>` | Create a new branch |
| `git checkout <name>` | Switch to another branch |
| `git switch <name>` | (Modern way) Switch to another branch |
| `git checkout -b <name>` | Create and switch to a new branch |
| `git branch -d <name>` | Delete a branch |

---

### ✅ Example:

```bash
git branch            # Shows current branches
git branch feature-x  # Creates a new branch called "feature-x"
git switch feature-x  # Switches to that new branch
```


---


🔀 What is git merge?
git merge is the command that combines changes from one branch into another.

You usually use it when:

You've finished working on a feature in a separate branch

You want to bring those changes back into the main branch (like main or master)


Nice! Let’s break down **`.gitignore`** and **Git tags** — two super useful features that serve different purposes in a project.

---

## 📄 **What is `.gitignore`?**

`.gitignore` is a **special file** that tells Git **which files or folders to ignore**—i.e., **not track** or commit to the repository.

---

### 🔧 **Why use `.gitignore`?**

Some files shouldn't go into version control, like:

- Temporary files (`.log`, `.tmp`)
- Build artifacts (`/dist/`, `/build/`)
- OS/system files (`.DS_Store` on macOS)
- Secrets or API keys (like `.env`)

---

### 🛠️ **Example `.gitignore` file:**

```txt
# Ignore node_modules folder
node_modules/

# Ignore all .log files
*.log

# Ignore environment files
.env

# Ignore macOS system files
.DS_Store
```

Just place this file in the root of your repo and Git will skip tracking those listed files.

---

## 🏷️ **What are Git Tags?**

Tags in Git are used to **mark specific points in history**—usually for **releases** or important versions.

Think of tags like bookmarks or labels.

---

### 📌 **Why use tags?**

- To label a release (`v1.0.0`, `v2.1.5`)
- So others can easily check out or download that version
- Tags stay fixed, even if the code changes later

---

### 🛠️ **Common Tag Commands:**

```bash
git tag              # List all tags
git tag v1.0         # Create a lightweight tag
git tag -a v1.0 -m "Version 1.0"   # Annotated tag with a message
git show v1.0        # Show tag details
git push origin v1.0 # Push a tag to remote
git checkout v1.0    # Checkout a specific tagged version
```

---

### ✨ Difference Between Lightweight and Annotated Tags:

| Type          | Description |
|---------------|-------------|
| **Lightweight** | Simple pointer to a commit (no message or metadata) |
| **Annotated**  | Stored as a full object in Git with message, tagger name, and date |

-
## 📦 Steps to Follow

### 🔹 a. Initialize the Repo and Push to GitHub

```bash
mkdir devops-project
cd devops-project
git init
echo "# DevOps Project" > README.md
echo "node_modules/" > .gitignore
git add .
git commit -m "Initial commit with README and .gitignore"
git branch -M main
git remote add origin https://github.com/yourusername/devops-project.git
git push -u origin main
```

---

### 🔹 b. Create `dev`, `feature` Branches

```bash
git checkout -b dev
git push -u origin dev

git checkout -b feature/initial-setup
# make some changes
git commit -am "Add initial setup files"
git push -u origin feature/initial-setup
```

---

### 🔹 c. Use Pull Requests to Merge

- Open a pull request on GitHub:  
  `feature/initial-setup → dev`
- Review and merge via GitHub interface.
- Later, PR from `dev → main` for release.

---

### 🔹 d. Add a Proper `README.md`

Example content:

```markdown
# DevOps Project

## Overview
This project demonstrates Git best practices in a DevOps workflow.

## Branching Strategy
- `main`: production-ready code
- `dev`: integration branch for testing
- `feature/*`: new features and improvements

## How to Contribute
1. Clone repo
2. Create a feature branch
3. Commit your changes
4. Open a pull request
```

---

### 🔹 e. Use `.gitignore` and Tags

**.gitignore** example:

```
node_modules/
.env
*.log
.vscode/
```

**Create tags for versions:**

```bash
git checkout main
git pull
git tag -a v1.0 -m "Initial stable release"
git push origin v1.0
```

---

## 📝 Document All Tasks Using Markdown

``![WhatsApp Image 2025-04-11 at 12 06 38_508d052a](https://github.com/user-attachments/assets/b2592303-077b-46a8-a337-ef21a1d674d1) 

`![WhatsApp Image 2025-04-11 at 12 07 08_2a700515](https://github.com/user-attachments/assets/9664a120-05e9-414b-8fb2-6f69339c8f1b)
--
![WhatsApp Image 2025-04-11 at 12 07 08_2a9ef737](https://github.com/user-attachments/assets/55f93cdc-cc9b-499d-82a8-51a946a49e77)


![WhatsApp Image 2025-04-11 at 12 06 38_48accfb6](https://github.com/user-attachments/assets/be9b1850-9cff-4961-8689-9f17c7094eda) 


![WhatsApp Image 2025-04-11 at 12 12 43_5dbb966a](https://github.com/user-attachments/assets/7541260a-1731-4e27-92f8-ffc371eac425) 



![WhatsApp Image 2025-04-11 at 12 13 53_5995ea9d](https://github.com/user-attachments/assets/bee5c52a-688c-4694-b919-cd152350142c) 



![WhatsApp Image 2025-04-11 at 12 14 27_b970e64a](https://github.com/user-attachments/assets/052e7b13-38be-4511-9edf-d99edc88cdc8) 



![WhatsApp Image 2025-04-11 at 12 14 52_b22973f1](https://github.com/user-attachments/assets/d778003b-8996-4ac3-a895-ab9e48587af7) 



![WhatsApp Image 2025-04-11 at 12 15 28_33dc6715](https://github.com/user-attachments/assets/0f57f7d5-b155-4f85-874b-b271e5202e2e) 



![WhatsApp Image 2025-04-11 at 12 09 11_d0d72177](https://github.com/user-attachments/assets/03efe8e6-e34e-489b-8542-872175f3b653)



![WhatsApp Image 2025-04-11 at 12 09 11_f5f484b5](https://github.com/user-attachments/assets/1057071b-594f-4147-9af7-434b2914d641)









