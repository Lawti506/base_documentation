# 📖 MkDocs Documentation Site — Student Template

A beautiful, ready-to-use documentation website template built with
[MkDocs](https://www.mkdocs.org/) and the
[Material](https://squidfunk.github.io/mkdocs-material/) theme.

Perfect for students to document their learning, projects, and portfolio.

---

## ✨ Features

- 🎨 **Modern Design** — Material theme with dark/light mode toggle
- 📑 **4-Tab Navigation** — Home, About Me, Documentation, Projects
- 📝 **Markdown-Based** — Write content in simple Markdown files
- 🖼️ **Google Drive Images** — Embed images directly from Google Drive
- 📱 **Responsive** — Looks great on desktop and mobile
- 🔍 **Built-in Search** — Full-text search across all pages
- 🚀 **Easy Deployment** — Deploy to GitHub Pages in minutes
- 📋 **Templates Included** — Ready-made templates for docs and projects

---

## 🚀 Quick Start

### Prerequisites

- **Python 3.8+** installed ([download](https://www.python.org/downloads/))
- **pip** (comes with Python)
- **Git** ([download](https://git-scm.com/downloads))

### Installation

```bash
# 1. Clone this repository (or use GitHub Codespaces — see below)
git clone https://github.com/yourusername/yourrepo.git
cd yourrepo

# 2. Install MkDocs and the Material theme
pip install -r requirements.txt

# 3. Start the local development server
mkdocs serve

# 4. Open your browser to:
#    http://127.0.0.1:8000
```

---

## 📂 Project Structure

```
.
├── mkdocs.yml                    # ⚙️  Site configuration
├── README.md                     # 📖 This file
└── docs/
    ├── index.md                  # 🏠 Home page
    ├── about/
    │   └── index.md              # 🧑‍💻 About Me page
    ├── documentation/
    │   ├── index.md              # 📚 Documentation overview
    │   ├── getting-started.md    # 🚀 Feature reference guide
    │   └── template.md           # 📝 Blank doc template
    ├── projects/
    │   ├── index.md              # 🏗️ Projects overview
    │   └── project-template.md   # 📋 Project doc template
    ├── stylesheets/
    │   └── extra.css             # 🎨 Custom styles
    └── overrides/                # 🔧 Theme overrides (advanced)
```

---

## ✏️ How to Customize

### 1. Edit Your Info

| File | What to Change |
|------|---------------|
| `mkdocs.yml` | Site name, URL, social links |
| `docs/index.md` | Home page welcome message |
| `docs/about/index.md` | Your name, bio, skills, photo |

### 2. Add New Documentation

```bash
# Copy the template
cp docs/documentation/template.md docs/documentation/my-topic.md

# Edit the new file
# Then add it to mkdocs.yml:
```

```yaml
nav:
  - Documentation:
      - Overview: documentation/index.md
      - Getting Started Guide: documentation/getting-started.md
      - My New Topic: documentation/my-topic.md   # ← add this line
```

### 3. Add New Projects

```bash
# Copy the project template
cp docs/projects/project-template.md docs/projects/my-project.md

# Edit the new file
# Then add it to mkdocs.yml:
```

```yaml
nav:
  - Projects:
      - Overview: projects/index.md
      - My Project: projects/my-project.md   # ← add this line
```

---

## 🖼️ Embedding Google Drive Images

1. **Upload** your image to Google Drive
2. **Right-click** → Share → change to **"Anyone with the link"**
3. **Copy** the share link:
   ```
   https://drive.google.com/file/d/ABC123XYZ/view?usp=sharing
   ```
4. **Extract** the File ID: `ABC123XYZ`
5. **Use in Markdown**:
   ```markdown
   ![My Image](https://drive.google.com/thumbnail?id=ABC123XYZ&sz=w800)
   ```

### Size Options

| Size | Parameter | Best For |
|------|-----------|----------|
| Small | `sz=w400` | Thumbnails, icons |
| Medium | `sz=w800` | In-line images |
| Large | `sz=w1200` | Full-width images |

---

## 💻 Edit Online with GitHub Codespaces (Recommended for Students)

No local setup needed! Just open the repo in a browser:

1. Go to the GitHub repository page
2. Click **Code → Codespaces → New codespace**
3. Wait ~1–2 minutes for the container to build
4. The **live preview** opens automatically at port `8000`
5. Edit any `.md` file in `docs/` — the preview updates instantly

---

## 🌐 Deploy to GitHub Pages

### Automatic Deployment (GitHub Actions)

This repo includes a pre-configured workflow at `.github/workflows/deploy.yml`.

**One-time setup:**
1. Push your code to GitHub
2. Go to **Settings → Pages**
3. Set **Source** to: `Deploy from a branch` → branch `gh-pages` → folder `/ (root)`
4. Click **Save**

From then on, every push to `main` automatically rebuilds and redeploys the site.

Your site will be live at:
```
https://yourusername.github.io/yourrepo/
```

### Manual Deployment

```bash
# One-command deployment from your local machine
mkdocs gh-deploy
```

---

## 🎨 Customization Tips

### Change Colors

Edit `mkdocs.yml` — change `primary` and `accent`:

```yaml
palette:
  - scheme: default
    primary: deep purple    # try: indigo, teal, blue, green, red
    accent: amber           # try: teal, pink, orange, cyan
```

### Change Font

```yaml
font:
  text: Outfit              # try: Inter, Poppins, Nunito
  code: Fira Code           # try: JetBrains Mono, Source Code Pro
```

### Add More Social Links

```yaml
extra:
  social:
    - icon: fontawesome/brands/twitter
      link: https://twitter.com/yourusername
    - icon: fontawesome/brands/instagram
      link: https://instagram.com/yourusername
```

---

## 📚 Resources

- [MkDocs Documentation](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Mermaid Diagrams](https://mermaid.js.org/)

---

## 📄 License

This template is open source. Feel free to use, modify, and share!
