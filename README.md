# GRC Engineered — Personal Website

Personal website and blog for **Zeshan Ahmad**, GRC Specialist at Cisco Splunk.

Live at: `https://zeshan-ahmad.github.io` (replace with your GitHub username)

---

## 📁 Site Structure

```
/
├── index.html              ← Landing page (hero, about, experience, certs, blog previews, contact)
├── blog/
│   ├── index.html          ← Blog listing page
│   └── posts/
│       ├── iso-42001-practical-guide.html
│       ├── grc-automation-aws-ssm.html
│       └── cloud-risk-cspm-wiz.html
└── assets/
    └── css/
        ├── main.css         ← Landing page styles
        ├── blog.css         ← Blog listing styles
        └── post.css         ← Blog post styles
```

---

## 🚀 Deploying to GitHub Pages

### Step 1: Create the repository

- Go to [github.com](https://github.com) and create a **new repository**
- Name it exactly: `YOUR-USERNAME.github.io` (e.g. `zeshan-ahmad.github.io`)
- Set it to **Public**
- Do NOT initialize with README (you'll push your own files)

### Step 2: Push the site files

```bash
cd path/to/this/folder
git init
git add .
git commit -m "Initial site launch"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

- Go to your repository on GitHub
- Click **Settings** → **Pages** (in the left sidebar)
- Under **Source**, select `Deploy from a branch`
- Select branch: `main`, folder: `/ (root)`
- Click **Save**

Your site will be live at `https://YOUR-USERNAME.github.io` within 2–5 minutes.

---

## ✏️ Adding a New Blog Post

1. Copy any existing post from `blog/posts/` as a template
2. Update the `<title>`, `<meta name="description">`, category, headline, date, and content
3. Add a card linking to the new post in:
   - `blog/index.html` (in the `.posts-list` section)
   - `index.html` (in the `#blog` section — replace or add a card)
4. Commit and push — GitHub Pages auto-deploys

### Quick post template

```html
<!-- In blog/posts/your-new-post.html -->
<!-- Copy cloud-risk-cspm-wiz.html and update: -->
<!-- 1. <title> tag -->
<!-- 2. <meta name="description"> -->
<!-- 3. .post-cat text (category) -->
<!-- 4. .post-h-title (headline) -->
<!-- 5. .post-h-meta (author, date, reading time) -->
<!-- 6. .post-content (your article) -->
```

---

## 🎨 Customising

| What | Where |
|------|-------|
| Your name, tagline | `index.html` → `.hero-name`, `.hero-tagline` |
| Stats (years, certs) | `index.html` → `.hero-stats` |
| LinkedIn / GitHub URLs | `index.html` → `#contact` section |
| Email address | `index.html` → contact section `href="mailto:"` |
| Accent color | `assets/css/main.css` → `--accent: #2D5A4E` |
| Experience entries | `index.html` → `.timeline` section |
| Certifications | `index.html` → `.certs-grid` |

---

## 🌐 Adding a Custom Domain Later

1. Buy a domain (e.g. `zeshanahmad.com`)
2. In your domain registrar's DNS settings, add a CNAME record:
   - **Name**: `www`
   - **Value**: `YOUR-USERNAME.github.io`
3. In GitHub Pages settings, enter your custom domain
4. GitHub will auto-provision an SSL certificate

---

## 📝 Notes

- No build step required — this is pure HTML/CSS
- Fonts load from Google Fonts CDN
- Works perfectly on mobile
- Page speed: ~95+ Lighthouse score (no JavaScript frameworks, minimal dependencies)
