# Ayushi Pareek — Portfolio

A minimal, production-ready portfolio site. Built in plain HTML and CSS, deployable on GitHub Pages in under five minutes.

## File structure

```
portfolio/
├── index.html          # Main page (hero, work, about, contact)
├── style.css           # All styles, shared across all pages
├── work/
│   ├── parseable.html  # Case study template
│   ├── deepsource.html # Case study template
│   └── appsmith.html   # Case study template
└── assets/             # Put your images here
    └── (your images)
```

---

## How to deploy on GitHub Pages

### Step 1: Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `yourusername.github.io` (replace with your actual GitHub username)
   - This gives you a clean URL: `https://yourusername.github.io`
   - Or name it anything else (e.g. `portfolio`) for a URL like `https://yourusername.github.io/portfolio`
4. Set visibility to **Public**
5. Click **Create repository**

### Step 2: Upload the files

**Option A — via browser (no coding required)**
1. Open your new repository on GitHub
2. Click **Add file** → **Upload files**
3. Drag all files and folders from this folder into the upload area
4. Click **Commit changes**

**Option B — via Git**
```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Choose **main** branch and **/ (root)** folder
4. Click **Save**
5. Your site will be live at `https://yourusername.github.io` in about 60 seconds

---

## Adding your images

1. Put all images in the `assets/` folder
2. In each HTML file, find the placeholder `<div>` elements that look like this:
   ```html
   <div class="work-card-image-placeholder" style="background: #f0ede8;"></div>
   ```
3. Replace them with an actual image tag:
   ```html
   <img src="../assets/parseable-cover.jpg" alt="Parseable product overview">
   ```
   (Use `assets/` instead of `../assets/` in `index.html`)

### Recommended image sizes
- **Work card thumbnails** (on homepage): 1200 × 675px (16:9)
- **Case study cover**: 1200 × 675px (16:9)
- **Case study body images**: any width, optimised to under 300kb each

Use [Squoosh](https://squoosh.app) to compress images before uploading.

---

## Customising the content

### Homepage hero copy
In `index.html`, find the hero section and update:
```html
<p class="hero-eyebrow">Senior product designer for developer tools</p>
<h1>I design for developers.<br><em>And I think like one.</em></h1>
<p class="hero-desc">I'm Ayushi, and I've spent five years...</p>
```

### Contact email
Search for `ayushipareek@gmail.com` and replace with your actual email.

### Social links
Search for the `social-links` section and replace `#` with your actual LinkedIn and Dribbble URLs.

### CV download
Place your ATS resume `.docx` file in the root folder and update the filename in `index.html`:
```html
<a href="your-resume-filename.docx">Download CV →</a>
```

### Case studies
Each case study page in `work/` has clearly marked placeholder sections with instructions. Replace the placeholder `<p>` text and `<div>` image placeholders with your actual content and images.

---

## Adding a custom domain (optional)

If you have a custom domain (e.g. `ayushipareek.com`):
1. Go to repository Settings → Pages → Custom domain
2. Enter your domain and click Save
3. At your domain registrar, add a CNAME record pointing to `yourusername.github.io`

GitHub's full guide: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
