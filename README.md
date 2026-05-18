# Derrick Jesse Mokaya — Portfolio

Personal portfolio and blog built with [Jekyll Chirpy Theme](https://github.com/cotes2046/jekyll-theme-chirpy) and hosted on GitHub Pages.

## 🚀 Live Site

> https://derrickmokaya.github.io  *(update after deployment)*

---

## 📁 File Structure

```
portfolio/
├── _config.yml          # Site-wide settings — update this first
├── _tabs/
│   ├── about.md         # CV / About page
│   ├── projects.md      # Projects showcase
│   └── contact.md       # Contact page
├── _posts/
│   ├── 2025-11-01-welcome.md
│   └── 2025-10-15-nssf-reconciliation.md
├── assets/
│   ├── img/
│   │   └── avatar.jpg   # Your profile photo
│   └── files/
│       └── Derrick_Jesse_Mokaya_CV.pdf  # Upload your CV here
├── Gemfile
└── README.md
```

---

## ⚙️ Setup Instructions

### 1. Fork the Chirpy Starter

Go to: https://github.com/cotes2046/chirpy-starter  
Click **"Use this template"** → **"Create a new repository"**  
Name it: `YOUR_GITHUB_USERNAME.github.io`

### 2. Clone Your New Repo

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
cd YOUR_USERNAME.github.io
```

### 3. Copy These Files Into Your Repo

Replace or add all files from this package into your cloned repo folder.

### 4. Update `_config.yml`

Open `_config.yml` and update:

```yaml
url: "https://YOUR_USERNAME.github.io"
github:
  username: YOUR_USERNAME
social:
  email: your.email@gmail.com
  links:
    - https://www.linkedin.com/in/YOUR_LINKEDIN
```

### 5. Add Your CV PDF

Create the folder `assets/files/` and drop in:
- `Derrick_Jesse_Mokaya_CV.pdf`

### 6. Commit and Push

```bash
git add .
git commit -m "Initial portfolio setup"
git push origin main
```

### 7. Enable GitHub Pages

Go to your repo → **Settings** → **Pages**  
Source: **GitHub Actions** (Chirpy uses the built-in Jekyll workflow)

Your site will be live at `https://YOUR_USERNAME.github.io` within 2–5 minutes.

---

## ✏️ Adding New Blog Posts

Create a new file in `_posts/` following the naming convention:

```
YYYY-MM-DD-post-title.md
```

Example: `_posts/2025-12-01-my-power-bi-project.md`

Front matter template:

```yaml
---
title: "Your Post Title"
date: 2025-12-01 09:00:00 +0300
categories: [Projects, Data Analytics]
tags: [power-bi, sql, excel]
---

Your content here in Markdown.
```

---

## 🎨 Customisation Tips

- **Dark mode:** Change `theme_mode: light` to `theme_mode: dark` in `_config.yml`
- **Avatar:** Replace `assets/img/avatar.jpg` with your photo (keep the same filename)
- **Sidebar links:** Add social links under `social.links` in `_config.yml`
- **Favicon:** Add favicon files to `assets/img/favicons/` (use https://realfavicongenerator.net)

---

## 📦 Local Development (Optional)

```bash
# Install Ruby + Bundler first, then:
bundle install
bundle exec jekyll serve
# Visit http://localhost:4000
```

---

Built with ❤️ using [Chirpy](https://github.com/cotes2046/jekyll-theme-chirpy)
