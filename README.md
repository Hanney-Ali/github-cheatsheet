# github-cheatsheet
# 🧠 Git + GitHub Cheat Sheet for Web Projects

### 🛠️ Prerequisites

* ✅ Git installed → [https://git-scm.com/downloads](https://git-scm.com/downloads)
* ✅ GitHub account → [https://github.com](https://github.com)

---

## 📁 1. Set Up Your Project with Git

```bash
cd path/to/your/project-folder      # Move into your project directory
git init                            # Initialize Git repo
```

---

## 🔗 2. Connect to GitHub Repo

```bash
git remote add origin https://github.com/your-username/repo-name.git
git remote -v                       # Confirm connection
```

---

## 📦 3. Add, Commit & Push Code

```bash
git add .                           # Stage all files
git commit -m "Initial commit"      # Save with a message
git push -u origin master           # Push to GitHub (or use main)
```

If you’re using `main`:

```bash
git branch -M main
git push -u origin main
```

---

## ⚠️ Fix Common Errors

### Error: "origin does not appear to be a git repository"

✅ Solution:

```bash
git remote add origin <repo-url>
```

### Error: "RPC failed; curl 55 Send failure"

✅ Solution:

```bash
git config --global http.postBuffer 524288000
```

---

## 📸 4. Handle Large Images (4K or Media Files)

### Option A: Use Git LFS (for files under 100 MB)

```bash
git lfs install
git lfs track "*.png" "*.jpg"
git add .gitattributes
git add .
git commit -m "Track large files using Git LFS"
git push
```

🔗 [Git LFS Website](https://git-lfs.github.com)

### Option B: Use External Hosting

Upload images to a CDN (e.g., Imgur, Cloudinary) and reference them via URLs in HTML:

```html
<img src="https://cdn.com/your-hero.jpg" />
```

---

## 📜 5. Create a `README.md` (Auto-Displays on GitHub)

```bash
touch README.md
```

### Sample Content:

```markdown
# Avengers Website

A fan-built site featuring Marvel heroes and villains.

## 🚀 Live Site
[Click Here](https://yourusername.github.io/your-repo/)

## 📸 Screenshots
![Homepage](images/screenshot-home.png)
```

Commit it:

```bash
git add README.md
git commit -m "Add README"
git push
```

---

## 🌍 6. Host Your Site with GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → Scroll to **Pages**
3. Set Source:

   ```
   Branch: master/main → / (root)
   ```
4. Save → Get link like:

   ```
   https://yourusername.github.io/repo-name/
   ```

---

## 🔄 7. Regular Workflow for Updates

```bash
git add .
git commit -m "Describe update"
git push
```

---

## 🚩 8. Optional: Create `.gitignore`

Prevents uploading unnecessary files:

```bash
# .gitignore
node_modules/
*.log
.DS_Store
```

Add it:

```bash
git add .gitignore
git commit -m "Add .gitignore"
git push
```

---

## 🧪 9. Bonus Commands

```bash
git status            # See file changes
git log               # See commit history
git branch            # See current branch
git checkout -b new-feature   # Create new branch
```

---

## ✅ 10. Check Your GitHub Repo

Your project should now show:

* All your files
* A `README.md`
* Screenshots
* GitHub Pages live link

---

### 🏁 Summary Workflow

| Step            | Command                       |
| --------------- | ----------------------------- |
| Init            | `git init`                    |
| Link to GitHub  | `git remote add origin <url>` |
| Add Files       | `git add .`                   |
| Commit          | `git commit -m "message"`     |
| Push            | `git push -u origin main`     |
| Fix Large Files | `git lfs track "*.jpg"`       |
| Host Site       | GitHub Settings → Pages       |

---

📄 Save this file in your project folder for future reference!


 
