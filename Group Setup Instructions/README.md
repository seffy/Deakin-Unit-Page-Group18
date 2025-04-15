
# SIT753 – Git Version Control (Sprint 1): (DRAFT)

This guide walks you through the entire Git Version Control Sprint 1 activity for SIT753, designed for team members new to Git, GitHub, and version control practices.

---

## 📘 1. Overview

Version Control helps developers collaborate effectively. In this sprint, you will work in a team of three to build a sample Deakin Unit Page using Git and GitHub, focusing on teamwork and version control rather than code complexity.

---

## 👥 2. Team Roles

Form a group of 3 and assign roles:
- **Team Leader (TL)** – Sets up the project, adds collaborators.
- **UI Designer (UI)** – Designs the user interface.
- **Front-End Developer (FD)** – Builds and styles front-end components.

---

## 🛠️ 3. Initial Setup

### a. GitHub Account
- Go to [GitHub](https://www.github.com/)
- Sign up or log in

### b. Install Git

⚠️ **BEFORE YOU PROCEED:** Please note that, since the group is using both **Windows** and **Apple Silicon Macs**, some instructions may not apply to Intel-based Macs. If you are using an Intel-based Mac, please verify the appropriate / recommended steps for Intel-based Macs online..
 
 
**🖥️ Windows**
1. Go to the official Git website:  
   [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. The download will start automatically.
3. Run the downloaded `.exe` file.
4. Follow the installation wizard:  
   - Click "Next" on most steps  
   - Choose your preferred editor (e.g., VS Code)  
   - Use default options unless you know what you’re doing
5. Open **Command Prompt** and type:
   ```bash
   git --version

You should see output like git version 2.x.x.


**🖥️ MACOS (Apple Silicon – M1/M2/M3)** 

⚠️ IMPORTANT: If you are using an Intel-based Macs, please verify the appropriate / recommended steps for Intel-based Macs online.

**Recommended steps for MACOS Apple Silicon – M1/M2/M3**
1. Install Homebrew (if not installed)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After installation, configure your shell:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

2. Install Git

```bash
brew install git
```

3. Confirm Installation

```bash
git --version
```

You should see output like `git version 2.x.x`.

**⚠️ Notes**

- Use **/opt/homebrew/** (not `/usr/local`) for Apple Silicon compatibility.
- Avoid running terminal in **Rosetta** unless absolutely necessary.
- Homebrew ensures you're using the ARM-native versions of packages.


### c. Configure Git
Replace with your details:
```bash
git config --global user.name "YOUR NAME"
git config --global user.email "YOUR EMAIL"
```

### d. Download GitHub Desktop (Optional but Highly Recommended)
1. Go to: [https://desktop.github.com/](https://desktop.github.com/)
2. Download GitHub Desktop
   - The site detects your OS automatically.
   - Click “Download for macOS” or “Download for Windows”.
3. Install the application**
   - **Windows**: Run the `.exe` file.
   - **macOS**: Open the `.dmg` file and drag it to the Applications folder.
4. Launch GitHub Desktop
   - Sign in with your GitHub account to get started.

### e. Download Visual Studio Code (VS Code)

1. Go to: [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Download VS Code
   - Choose your OS version (Windows, macOS Intel or Apple Silicon, or Linux).
   - Click the “Download” button.
3. Install VS Code
   - **Windows**: Run the `.exe` file.
   - **macOS**: Open the `.dmg` or `.zip` file and move it to Applications.
4. Launch VS Code

  ** Recommended Extensions:**
   - ESLint: For identifying and reporting on patterns in JavaScript.
   - Prettier: For code formatting.
   - GitHub Copilot: For AI-assisted code suggestions (if available).
   - Live Server: for real-time preview of HTML
---

## 🔗 4. Forking and Cloning the Repository

### TEAM LEADER Tasks: (DONE)
1. Go to: [https://github.com/seffy/Deakin-Unit-Page-Group18.git]
2. Click **Fork** (creates a copy in your GitHub account)
3. Go to **Settings > Collaborators**
4. Add UI and FD GitHub usernames

### All MEMBERS
1. Copy the HTTPS URL of the forked repo
2. In Terminal, navigate to your code folder
3. Run:
```bash
git clone https://github.com/seffy/Deakin-Unit-Page-Group18.git
```

4. Enter the folder:
```bash
cd Deakin-Unit-Page-Group18
open index.html
```

---

## 🎨 5. UI DESIGNER Tasks

### a. Create a new branch:
```bash
git checkout -b add-header
```

### b. Add Header and Logo
Insert this inside `<body>`:
```html
<div>
  <img src="logo.svg" alt="Deakin" width="200" height="210">
</div>
```

### c. Style it in `main.css`:
```css
div {
  background-color: darkcyan;
  text-align: right;
}
```

### d. Save and commit:
```bash
git add .
git commit -m "add header and logo"
git push -u origin add-header
```

---

## 💻 6. FRON-END DEVELOPER Tasks

### a. Create a new branch:
```bash
git checkout -b add-table
```

### b. Add Unit Details Table in `index.html`:
Add below the header:
```html
<h2>Unit details</h2>
<table>
  <tr><td>Year:</td><td>2023 unit information</td></tr>
  <tr><td>Enrolment modes:</td><td>Trimester 1...</td></tr>
  <tr><td>Credit point(s):</td><td>1</td></tr>
  <tr><td>Unit Chair:</td><td>Azadeh Ghari Neiat</td></tr>
</table>
```

### c. Style the table in `main.css`:
```css
th, td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}
tr:nth-child(odd) { background-color: #f2f2f2; }
```

### d. Save and commit:
```bash
git add .
git commit -m "add table"
git push -u origin add-table
```

---

## 🧑‍💼 7. Team Leader Content and Link

### a. Create a new branch:
```bash
git checkout -b add-unit-content
```

### b. Add paragraph and fee link to `index.html`:
```html
<h3>Content</h3>
<p>To be successful IT graduates...</p>
<a href="https://www.deakin.edu.au/students/enrolment-and-fees/fees">Current students</a>
```

### c. Save and commit:
```bash
git add .
git commit -m "add unit content and fee link"
git push -u origin add-unit-content
```

---

## 🔀 8. Merging Back to Main

### For Each Member:
1. Switch to `main` branch:
```bash
git checkout main
git pull
```

2. Merge your feature branch:
```bash
git merge <your-branch-name>
```

3. Push changes:
```bash
git push
```

---

## 🔁 9. Final Personal Edits

- **UI Designer**: Change header color to `blue` in CSS.
- **Front-End Developer**: Add a row for "Scheduled Learning Activities".
- **Team Leader**: Add a new section for "Hurdle Requirement".

---

## ✅ 10. Submission

Submit the following on OnTrack:
- Screenshot: GitHub > Insights > Contributors
- Screenshot: GitHub > Insights > Network
- Optional log file:
```bash
git log --pretty=format:"%h - %an - %ad - %s" --date=short > group_log.txt
```
- 
---



