## <center> Basic Git Commands </center>
-------------------------------------------------------------
Back to [Exercise - Try Out Git](./04_Exercise_Try%20Out%20Git.md)

-------------------------------------------------------------

Git works by remembering the changes to your files as if it's taking snapshots of your file system.

It will cover a few basic commands to start tracking files in the repo. Then, you'll save your first "snapshot" for Git to compare against.

### git status

The first and most commonly used Git command is `git status`. You've already used it once, in the preceding exercise, to see that you had initialized your Git repo properly.

`git status` displays the state of the working tree (and of the staging area—we'll talk more about the staging area soon). It lets you see which changes are currently being tracked by Git, so you can decide whether you want to ask Git to take another snapshot.

### git add

`git add` is the command you use to tell Git to start keeping track of changes in certain files.

The technical term is <i>staging</i> these changes. You'll use git add to stage changes to prepare for a commit. All changes in files that have been added but not yet committed are stored in the staging area.

### git commit

After you've staged some changes for commit, you can save your work to a snapshot by invoking the `git commit` command.

<i>Commit</i> is both a verb and a noun. It has essentially the same meaning as when you commit to a plan or commit a change to a database. As a verb, `committing changes means you put a copy (of the file, directory, or other "stuff") in the repository as a new version`. As a noun, a commit is the small chunk of data that gives the changes you committed a unique identity. The data that's saved in a commit includes the author's name and e-mail address, the date, comments about what you did (and why), an optional digital signature, and the unique identifier of the preceding commit.

### git log

The `git log` command allows you to see information about previous commits. Each commit has a message attached to it (a commit message), and the `git log` command prints information about the most recent commits, like their time stamp, the author, and a commit message. This command helps you keep track of what you've been doing and what changes have been saved.

### git help

You've already tried out the `git help` command, but it's worth reminding you about. Use this command to easily get information about all the commands you've learned so far, and more.

Remember, each command comes with its own help page, too. You can find these help pages by typing `git <command> --help`. For example, `git commit --help` brings up a page that tells you more about the `git commit` command and how to use it.



## <center>Personalized Scenario</center>

### How to Push Your Local Git Repository to GitHub

This guide explains how to connect your **local Git repository** to **GitHub** and push your commits successfully.

---

## Scenario
You have a local repository at:

```
C:\Users\Venu\OneDrive\Documents\GitHub_Self Study Material\GitHub Foundations Part-1
```

And when you ran:
```bash
git push origin main
```
you received this error:
```
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.
```

This means your local repository has **no remote connection** to GitHub yet.

---

## ✅ Step-by-Step Solution

### 1️⃣ Create a Repository on GitHub
1. Go to [https://github.com/new](https://github.com/new)
2. Enter a repository name (e.g. **GitHub-Foundations-Part-1**)
3. Choose **Public** or **Private**
4. Click **Create Repository**

You will get a repository URL like this:
```
https://github.com/<your-username>/GitHub-Foundations-Part-1.git
```

---

### 2️⃣ Link Your Local Repository to GitHub

Open PowerShell in your local project folder:

```bash
cd "C:\Users\Venu\OneDrive\Documents\GitHub_Self Study Material\GitHub Foundations Part-1"
```

Now link your GitHub repository (replace with your own username):

```bash
git remote add origin https://github.com/<your-username>/GitHub-Foundations-Part-1.git
```

Verify that the remote was added correctly:
```bash
git remote -v
```
Expected output:
```
origin  https://github.com/<your-username>/GitHub-Foundations-Part-1.git (fetch)
origin  https://github.com/<your-username>/GitHub-Foundations-Part-1.git (push)
```

---

### 3️⃣ Push Your Commits to GitHub

Now push your local branch to GitHub:
```bash
git push -u origin main
```

The `-u` flag sets the default upstream branch.  
From now on, you can simply use:
```bash
git push
```

---

### 4️⃣ Verify on GitHub

Visit your repository on GitHub in a browser — you should now see all your files and commit history 🎉

---

## ⚙️ Optional: Initialize a New Git Repo (if not yet initialized)
If you haven’t initialized Git before, run these first:
```bash
git init
git add .
git commit -m "Initial commit"
```
Then repeat steps 2–4 above.

---

## 🧠 Quick Reference

| Command | Purpose |
|----------|----------|
| `git init` | Initialize local Git repository |
| `git add .` | Stage all files for commit |
| `git commit -m "message"` | Commit your changes locally |
| `git remote add origin <URL>` | Connect to GitHub repository |
| `git push -u origin main` | Push to GitHub |

---

✅ **Tip:** If you want to use SSH instead of HTTPS, use:
```bash
git remote add origin git@github.com:<your-username>/GitHub-Foundations-Part-1.git
```

Then push:
```bash
git push -u origin main
```

---

### 🎯 Summary
- `git commit` only saves **locally**
- `git push` uploads to **GitHub**
- You must link your GitHub repo using `git remote add origin` before pushing



Next to []