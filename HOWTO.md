# How to publish this portfolio to GitHub

## Option A — 100% in the browser (no Git installed)
1. Go to https://github.com/new
2. **Repository name:** `Uptrail-Data-Analyst-Portfolio`
3. Choose **Public** (recommended for sharing) → **Create repository**.
4. Click **“uploading an existing file”** (or **Add file → Upload files**).
5. Drag-drop the contents of the zip you downloaded (all folders/files), then **Commit changes**.
6. After it uploads, add your PDFs:
   - Drop each project PDF into its matching `projects/project-X` folder.
   - Drop your certificates into `certificates/`.
7. Edit the **README.md** in GitHub to replace placeholders and confirm the PDF links work.

## Option B — GitHub Desktop (easy on Windows/macOS)
1. Install **GitHub Desktop** from https://desktop.github.com/
2. Click **File → New repository**:
   - Name: `Uptrail-Data-Analyst-Portfolio`
   - Local path: choose a folder on your machine
   - Initialize with README (unchecked is fine)
3. After it creates the local repo, open the folder and **copy all files** from the zip into it.
4. Back in GitHub Desktop:
   - You’ll see changes → **Commit to main**, then **Publish repository** (Public).
5. Add your PDFs into the right folders, commit again, **Push origin**.

## Option C — Command line (Git) on Windows PowerShell
```powershell
# 1) Configure Git (one-time)
git config --global user.name "Rory Scott"
git config --global user.email "you@example.com"

# 2) Create a new repo locally
mkdir Uptrail-Data-Analyst-Portfolio
cd Uptrail-Data-Analyst-Portfolio
# Copy the extracted contents of the zip into this folder

git init
git add .
git commit -m "Initial portfolio with structure, README, and license"

# 3) Create the repo on GitHub (do this in the browser first) and copy its URL, e.g.:
# https://github.com/<your-username>/Uptrail-Data-Analyst-Portfolio.git

git branch -M main
git remote add origin https://github.com/<your-username>/Uptrail-Data-Analyst-Portfolio.git
git push -u origin main
```

### Adding your PDFs later
```powershell
# Example: add your first project PDF and push
git add projects/project-1/project-1-report.pdf
git commit -m "Add project 1 PDF"
git push
```
