# Git Commands: Connect & Commit Your Chapter 1 Notes

A quick reference for using the terminal to connect your local repository to GitHub and commit your `.txt` notes file on Chapter 1 (*The Machine Learning Landscape*).

---

## 1. One-Time Setup

### Configure your identity
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### Clone the repo to your computer (if you haven't already)
```bash
git clone https://github.com/TheOohWee/handson-ml3.git
cd handson-ml3
```

### Connect your local repo to GitHub (if you cloned manually or forked)
```bash
# Check whether a remote is already set
git remote -v

# If no remote exists, add one
git remote add origin https://github.com/TheOohWee/handson-ml3.git

# Verify the remote was added
git remote -v
```

---

## 2. Commit Your txt Notes File

Once your `chapter_01_notes.txt` file is ready on your computer:

```bash
# 1. Copy your txt file into the repo folder (replace the path with where your file actually is)
cp /path/to/your/chapter_01_notes.txt /path/to/handson-ml3/chapter_01_notes.txt

# 2. Go into the repo folder
cd /path/to/handson-ml3

# 3. Check that git sees the new file
git status

# 4. Stage the file
git add chapter_01_notes.txt

# 5. Commit it with a message
git commit -m "Add Chapter 1 notes"

# 6. Push to GitHub
git push origin main
```

> **Tip:** If your default branch is named `master` instead of `main`, use `git push origin master`.

---

## 3. Useful Status Commands

```bash
git status          # see which files have changed
git diff            # see line-by-line changes before staging
git log --oneline   # view your commit history
```
