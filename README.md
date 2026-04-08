# Anastasiia Merchanskaia — Personal Website

A personal academic website built with **R Markdown** and hosted via **GitHub Pages**.

---

## 📁 File Structure

```
personal-website/
├── index.Rmd        # Home page
├── about.Rmd        # About Me page
├── projects.Rmd     # Projects page
├── styles.css       # All custom styles
├── header.html      # Shared HTML head (fonts, meta)
├── _site.yml        # Site configuration
├── docs/            # ← Generated output (served by GitHub Pages)
└── README.md
```

---

## 🚀 Setup Instructions

### 1. Open in RStudio
Open the folder as a project: `File → Open Project → select folder`

### 2. Install required packages
```r
install.packages("rmarkdown")
```

### 3. Build the site
In the RStudio console:
```r
rmarkdown::render_site()
```
This generates all HTML files into the `docs/` folder.

### 4. Push to GitHub
```bash
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/YOURREPO.git
git push -u origin main
```

### 5. Enable GitHub Pages
- Go to your repo on GitHub
- Click **Settings → Pages**
- Set Source to: **Deploy from branch → main → /docs**
- Click Save

Your site will be live at: `https://YOURUSERNAME.github.io/YOURREPO/`

---

## ✏️ Customizing

### Change your name / bio
Edit the text inside `about.Rmd` and `index.Rmd`.

### Add your photo
In `about.Rmd`, replace the `.photo-placeholder` div with:
```html
<img src="photo.jpg" alt="Anastasiia" style="width:100%; border-radius:4px;">
```
Then put `photo.jpg` in the same folder.

### Add a project card
Copy one of the `.project-card` blocks in `projects.Rmd` and fill in your details.

### Update social links
Search for `yourusername` in all `.Rmd` files and replace with your GitHub/LinkedIn handles.

### Rebuild after edits
```r
rmarkdown::render_site()
```
Then commit and push the `docs/` folder.
