# 🚀 How to Deploy Your Site on GitHub Pages

This guide walks you through publishing your MkDocs documentation site on the internet using **GitHub** — for free. Follow every step in order.

---

## What You Will Need

| Requirement | Where to get it |
|---|---|
| A GitHub account | [github.com/signup](https://github.com/signup) |
| This repository | Your teacher will share the GitHub repo link |

No Python or software installation is needed if you use **Codespaces**.

---

## Step 1 — Fork or Copy the Repository

Your teacher will give you one of these options:

=== "Option A — You already have the repo"

    Your teacher has already added you as a collaborator.  
    Skip to **Step 2**.

=== "Option B — Fork it yourself"

    1. Open the GitHub repo link your teacher shared
    2. Click the **Fork** button (top-right corner)
    3. Keep the default settings and click **Create fork**
    4. You now have your own copy — continue to Step 2

---

## Step 2 — Enable GitHub Pages

!!! warning "Do this ONCE before your first deployment"

1. Open your repository on GitHub
2. Click **Settings** (the cog icon in the top menu)
3. In the left sidebar, click **Pages**
4. Under **Source**, choose:
   - **Deploy from a branch**
   - Branch: `gh-pages`
   - Folder: `/ (root)`
5. Click **Save**

!!! note
    The `gh-pages` branch is created automatically when the first deployment runs.  
    If you don't see it yet, complete Step 4 first, then come back and set this.

---

## Step 3 — Edit Your Site

You have two ways to edit your site. **Codespaces is strongly recommended.**

=== "🌐 Codespaces (No installation — works in your browser)"

    1. Open your repository on GitHub
    2. Click the green **Code** button
    3. Click the **Codespaces** tab
    4. Click **New codespace**

        ![Codespaces button location](https://docs.github.com/assets/cb-169695/mw-1440/images/help/codespaces/new-codespace-button.webp)

    5. Wait **1–2 minutes** for the environment to build
    6. A **live preview** of your site opens automatically in the browser panel

    **To edit a page:**

    1. In the file explorer on the left, open the `docs/` folder
    2. Click any `.md` file (e.g. `docs/about/index.md`)
    3. Make your changes — the live preview updates instantly!

=== "💻 Local Machine (requires Python installed)"

    ```bash
    # 1. Clone your repository
    git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
    cd YOUR-REPO

    # 2. Install dependencies
    pip install -r requirements.txt

    # 3. Start the live preview
    mkdocs serve

    # 4. Open in your browser:
    #    http://127.0.0.1:8000
    ```

---

## Step 4 — Save and Publish Your Changes

Every time you save and push your changes to GitHub, the site rebuilds automatically.

=== "In Codespaces"

    1. Press `Ctrl+S` (or `Cmd+S` on Mac) to save your file
    2. Click the **Source Control** icon in the left sidebar (it looks like a branch)
    3. In the **Message** box, type a short description of your change  
       Example: `Update my About Me page`
    4. Click the **✔ Commit** button (tick/checkmark)
    5. Click **Sync Changes** (or **Push**)

    !!! tip
        You can also use the terminal inside Codespaces:
        ```bash
        git add .
        git commit -m "Your message here"
        git push
        ```

=== "On your local machine"

    ```bash
    git add .
    git commit -m "Your message here"
    git push
    ```

---

## Step 5 — Watch the Deployment Run

1. Go to your repository on GitHub
2. Click the **Actions** tab
3. You will see a workflow called **Deploy MkDocs to GitHub Pages** running
4. Click on it to watch the progress
5. When it shows a **green tick ✅**, your site is live!

!!! note "How long does it take?"
    Usually **1–3 minutes** from when you push your changes.

---

## Step 6 — Visit Your Live Website

Your site URL follows this pattern:

```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```

**Example:** if your GitHub username is `ahmed` and the repo is `my-docs`:
```
https://ahmed.github.io/my-docs/
```

You can find the exact URL in **Settings → Pages** (it appears at the top once the site is live).

---

## 📝 What to Edit

| File | What it controls |
|------|-----------------|
| `mkdocs.yml` | Site name, your GitHub URL, social links |
| `docs/index.md` | Home page welcome message |
| `docs/about/index.md` | Your name, bio, skills, photo |
| `docs/documentation/` | Your notes and guides |
| `docs/projects/` | Your project writeups |

### Changing Your Site Name

Open `mkdocs.yml` and update the top lines:

```yaml
site_name: Ahmed's Documentation    # ← Your name/project
site_url: https://ahmed.github.io/my-docs/
site_author: Ahmed Al-Rashid

repo_url: https://github.com/ahmed/my-docs
repo_name: ahmed/my-docs
```

### Adding a New Page

1. Create a new `.md` file inside `docs/documentation/`
2. Add it to `mkdocs.yml` under the `nav:` section:

```yaml
nav:
  - Documentation:
      - Overview: documentation/index.md
      - My New Topic: documentation/my-new-topic.md   # ← add this
```

---

## ❓ Troubleshooting

| Problem | Solution |
|---------|----------|
| Actions tab shows a red ❌ | Click the failed run → read the error log → check your `mkdocs.yml` for typos |
| Site URL shows 404 | Go to **Settings → Pages** and confirm source is set to `gh-pages` branch |
| Changes not showing | Wait 2–3 minutes and refresh. If still not updated, check the Actions tab |
| Codespace preview not opening | In the terminal, run `mkdocs serve --dev-addr=0.0.0.0:8000` manually |

---

!!! success "You're done!"
    Your site is now live on the internet and updates automatically every time you push a change. 🎉
