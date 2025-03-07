# Getting Started with Git – A Step-by-Step Walkthrough

Git is a powerful version control system, and setting it up is straightforward. This guide will walk you through **installing Git, configuring it, creating repositories, making commits, and pushing changes to GitHub.**

---

## 1. Install Git

### Windows
- Download Git from the official site: [Git for Windows](https://git-scm.com/downloads)
- Run the installer and select **“Use Git from the Windows Command Prompt”** when prompted.
- Keep the other default settings.

### macOS
- Run this command in the **Terminal**:
  ```sh
  brew install git
  ```
  If you don’t have Homebrew, install it first with:
  ```sh
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

### Linux
- Run the following command:
  ```sh
  sudo apt install git  # Debian/Ubuntu
  sudo dnf install git  # Fedora
  sudo pacman -S git    # Arch
  ```

---

## 2. Configure Git

After installing Git, configure it with your name and email:

```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

To check your configuration:
```sh
git config --list
```

---

## 3. Initialize a New Git Repository

Navigate to your project folder and initialize Git:

```sh
cd /path/to/your/project
git init
```

This creates a `.git` folder, which tracks all changes.

---

## 4. Add and Commit Files

Create a new file:
```sh
echo "Hello, Git!" > hello.txt
```

Add it to the staging area:
```sh
git add hello.txt
```

Commit the file:
```sh
git commit -m "Initial commit"
```

---

## 5. Connect to GitHub (or another remote repository)

### Create a Repository on GitHub
1. Go to [GitHub](https://github.com/)
2. Click **New Repository** → Enter a name → Click **Create Repository**.
3. Copy the repository URL (e.g., `https://github.com/yourusername/repository.git`).

### Link Your Local Repository
Run this command to connect your local repository to GitHub:
```sh
git remote add origin https://github.com/yourusername/repository.git
```

Verify the remote:
```sh
git remote -v
```

---

## 6. Push Your Code to GitHub

Upload your code to GitHub:
```sh
git push -u origin main
```

If your branch is named `master` instead of `main`, use:
```sh
git push -u origin master
```

---

## 7. Pull Changes from GitHub

If you work on multiple computers or collaborate with others, always fetch the latest changes:
```sh
git pull origin main
```

---

## 8. Create and Work with Branches

Creating a new branch:
```sh
git branch feature-branch
```

Switch to the new branch:
```sh
git switch feature-branch
```
or
```sh
git checkout feature-branch
```

Make changes, add, commit, and push:
```sh
git add .
git commit -m "Added a new feature"
git push origin feature-branch
```

---

## 9. Merge Branches

After finishing your feature, switch back to `main`:
```sh
git switch main
```

Merge the feature branch:
```sh
git merge feature-branch
```

Delete the merged branch:
```sh
git branch -d feature-branch
```

---

## 10. Cloning an Existing Repository

To download a repository from GitHub:
```sh
git clone https://github.com/yourusername/repository.git
```

---

## Next Steps

Now that you're comfortable with Git basics, explore:
- **GitHub Issues & Pull Requests** for collaboration.
- **.gitignore** files to exclude unnecessary files.
- **Rebasing & Cherry-picking** for advanced version control.

Would you like help with Git workflows like **forking, rebasing, or handling merge conflicts**? 🚀
