# 📚 First Year Engineering Drive @ UP

> Organised study materials for first year engineering students at the **University of Pretoria**.
> Maintained by [Swift Tuition](https://github.com/SwiftTuition).

---

## 📁 What's in here?

| Folder | Module | Description |
|--------|--------|-------------|
| `COS 132` | Computer Science 132 | Lecture slides, practicals, past papers |
| `EBN 111 + 122` | Engineering Mathematics 111 & 122 | Notes, tutorials, semester tests, class tests, exams |
| `FSK 116 + 176` | Physics 116 & 176 | Lecture slides, tutorial tests, semester tests, exams |
| `WTW 158` | Mathematics 158 | Notes, tutorials, semester tests, exams, lecture videos index |

> **Note:** Lecture videos (`.mp4` files) are **not** stored here — they're too large for GitHub. Everything else (PDFs, slides, practicals, assignments, etc.) is included.

---

## 🖥️ How to Download Everything to Your Computer

### Step 1 — Install Git (one time only)

Git is the tool that lets you download and sync this repo. You only need to do this once.

**Windows:**
1. Go to **[git-scm.com/download/win](https://git-scm.com/download/win)**
2. Download the installer and run it
3. Keep clicking **Next** — all default settings are fine
4. Click **Finish** when done

**Check it worked:**
Open **Command Prompt** (press `Win + R`, type `cmd`, press Enter) and type:
```
git --version
```
You should see something like `git version 2.x.x`. If you do, you're good!

> ❌ **Error: `'git' is not recognized as an internal or external command`**
> Git wasn't installed correctly or your computer needs a restart. Try restarting and running the command again. If it still fails, re-download and reinstall from the link above, and on the step that says *"Adjusting your PATH environment"*, make sure **"Git from the command line and also from 3rd-party software"** is selected.

---

### Step 2 — Pick a folder

Decide where on your computer you want the materials to live. For example:
```
C:\Users\YourName\Documents\UP Study Materials
```

You **don't** need to create the final folder yourself — Git will create it for you. Just navigate to the *parent* folder (e.g. `Documents`).

> ⚠️ **Avoid** putting it inside a OneDrive, Google Drive, or Dropbox sync folder. These cloud sync tools can conflict with Git and corrupt files.

---

### Step 3 — Open Command Prompt in your chosen location

1. Open **File Explorer** and go to the folder *inside which* you want the materials folder to appear (e.g. `Documents`)
2. Click the **address bar** at the top of File Explorer so it's highlighted
3. Type `cmd` and press **Enter**
4. A black Command Prompt window will open, already pointing at the right folder

---

### Step 4 — Clone (download) the repo

In the Command Prompt window, type this exactly and press Enter:

```
git clone https://github.com/SwiftTuition/First-Year-Engineering-Drive-UP.git
```

Git will create a folder called `First-Year-Engineering-Drive-UP` and download everything into it. This may take **5–15 minutes** depending on your internet speed — there are a lot of PDFs!

You'll see progress like:
```
Cloning into 'First-Year-Engineering-Drive-UP'...
remote: Counting objects: 3200, done.
Receiving objects: 100% (3200/3200), 4.40 GiB | 2.50 MiB/s, done.
```

When it finishes, open the folder in File Explorer — all the study materials will be inside.

---

**Common cloning errors:**

> ❌ **`fatal: repository not found`**
> Double-check you typed the URL correctly. Copy-paste it directly from this page to be safe.

> ❌ **`fatal: unable to access ... Could not resolve host`**
> You're not connected to the internet, or your firewall/network is blocking Git. Try on a different network (e.g. mobile hotspot) or check your internet connection.

> ❌ **The download seems stuck / nothing is happening**
> It's not stuck — it's downloading thousands of PDFs. Be patient. As long as you don't see an error message, it's working. Do not close the window.

> ❌ **`error: RPC failed; curl 18 transfer closed`**
> Your connection dropped mid-download. Just run the same `git clone` command again — Git will pick up where it left off... well actually it'll restart, but it'll work this time on a stable connection.

> ❌ **`fatal: destination path already exists`**
> You've already cloned it before. You don't need to clone again — just open the existing folder and follow the **Getting Updates** steps below.

---

## 🔄 Getting Updates

Whenever new materials are added or existing ones are improved, you can sync your copy in seconds.

### Step 1 — Open Command Prompt inside the repo folder

1. Open **File Explorer** and go into the `First-Year-Engineering-Drive-UP` folder
2. Click the address bar, type `cmd`, press **Enter**

### Step 2 — Pull the latest changes

```
git pull
```

That's it. Git downloads only what changed — not the whole thing again. You'll see either a list of updated files, or:
```
Already up to date.
```

> 💡 **Tip:** Make this a habit — run `git pull` at the start of every study session.

---

**Common pull errors:**

> ❌ **`fatal: not a git repository`**
> You're not inside the repo folder. Make sure you navigated *into* `First-Year-Engineering-Drive-UP` before opening cmd, not just into `Documents`.

> ❌ **`error: Your local changes to the following files would be overwritten by merge`**
> You've accidentally edited one of the files. To discard your local changes and force a clean update, run:
> ```
> git checkout -- .
> git pull
> ```
> ⚠️ This will discard any edits you've made locally. If you want to keep them, copy them somewhere else first.

> ❌ **`fatal: unable to access ... Could not resolve host`**
> No internet connection. Connect and try again.

> ❌ **`There is no tracking information for the current branch`**
> Run this instead:
> ```
> git pull origin main
> ```

---

## 💡 Suggesting Changes or Adding Materials

Found a past paper that's missing? Want to add your own notes? You can suggest changes through a **Pull Request (PR)**. Swift Tuition reviews every PR and decides whether to accept or decline it.

> ⚠️ **Do not push directly to the main branch.** Always follow the steps below so your suggestion goes through the review process. Direct pushes to main will be reverted.

---

### Step 1 — Make sure you're up to date first

```
git pull
```

Always start from the latest version.

---

### Step 2 — Create your own branch

A branch is your own safe workspace where you can make changes without affecting the main materials.

```
git checkout -b suggestion/YourName/short-description
```

Replace `YourName` and `short-description` with something meaningful. For example:
```
git checkout -b suggestion/Thabo/add-wtw158-2023-exam
git checkout -b suggestion/Lerato/fix-fsk116-semester-test-folder
git checkout -b suggestion/Pieter/add-ebn111-class-test-2024
```

The `suggestion/` prefix is **required** — it identifies your PR as a community contribution for review.

> ❌ **`fatal: A branch named '...' already exists`**
> You already created this branch before. Either switch to it with `git checkout suggestion/YourName/description`, or pick a slightly different name.

---

### Step 3 — Add your files

Copy the files you want to contribute into the correct subfolder (e.g. `WTW 158/Exams/`), then stage them:

```
git add .
```

Then commit with a clear, descriptive message:

```
git commit -m "Add WTW 158 2023 main exam paper and memo"
```

> 💡 **Good commit messages:** say *what* you added and *which module* it's for.
> - ✅ `Add FSK 116 semester test 1 2024 memo`
> - ✅ `Add EBN 122 class test 2 2023 with solutions`
> - ❌ `added stuff`
> - ❌ `files`

> ❌ **`nothing to commit, working tree clean`**
> Git doesn't see your new files. Make sure you actually copied them into the repo folder (inside `First-Year-Engineering-Drive-UP`), then run `git add .` again.

---

### Step 4 — Push your branch

```
git push origin suggestion/YourName/short-description
```

> ❌ **`error: src refspec does not match any`**
> Your branch name in the push command doesn't match what you created. Run `git branch` to see your branch name, then copy it exactly.

> ❌ **`remote: Permission to ... denied`**
> You're not authenticated. Run:
> ```
> git config --global credential.helper manager
> ```
> Then try the push again — a login window should pop up. Sign in with your GitHub account.

---

### Step 5 — Open a Pull Request on GitHub

1. Go to **[github.com/SwiftTuition/First-Year-Engineering-Drive-UP](https://github.com/SwiftTuition/First-Year-Engineering-Drive-UP)**
2. You'll see a yellow banner saying your branch was recently pushed — click **"Compare & pull request"**
3. Write a short description of what you're adding and why
4. Click **"Create pull request"**

Swift Tuition will review it. If accepted ✅ — your files get merged in. If declined ❌ — you'll see a note explaining why. No hard feelings!

---

## ⚡ Quick Reference

| What you want to do | Command |
|---------------------|---------|
| Download the repo (first time only) | `git clone https://github.com/SwiftTuition/First-Year-Engineering-Drive-UP.git` |
| Get the latest updates | `git pull` |
| Create a suggestion branch | `git checkout -b suggestion/YourName/description` |
| Stage all your new files | `git add .` |
| Commit your changes | `git commit -m "Your message here"` |
| Push your branch | `git push origin suggestion/YourName/description` |
| See what branch you're on | `git branch` |
| Switch back to main branch | `git checkout main` |
| Discard local changes (careful!) | `git checkout -- .` |

---

## 📬 Questions?

Reach out to **Swift Tuition** via GitHub or at **admin@swifttuition.co.za**.

> All PRs using the `suggestion/` prefix are reviewed. Anything pushed directly to `main` without a PR will be reverted.
