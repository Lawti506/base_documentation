---
title: Projects
---

# 🏗️ Projects Overview

Welcome to my project portfolio! Each project includes detailed documentation
covering objectives, implementation, and results.

<hr class="section-divider">

## My Projects

<!-- ============================================================
     INSTRUCTIONS: Each project card has an image on the left.
     Replace YOUR_FILE_ID with your Google Drive image File ID.
     ============================================================ -->

<div class="project-card-horizontal" markdown>
<div class="project-card-image" style="background-image: url('https://drive.google.com/thumbnail?id=1lJF64u4UmLNtrHdB5WT4IilpH4-UBSXz&sz=w600');"></div>
<div class="project-card-content" markdown>

### 🔧 Project Template

<span class="status-badge in-progress">Template</span>

A starter template for documenting your project. Copy this to create new project entries.

**Tech Stack:** `Tool 1` · `Tool 2` · `Tool 3`

[:octicons-arrow-right-24: View Project Details](project-template.md)

</div>
</div>

<!-- ── Copy the block below for each new project ──────────── -->
<!--
<div class="project-card-horizontal" markdown>
<div class="project-card-image" style="background-image: url('https://drive.google.com/thumbnail?id=YOUR_FILE_ID&sz=w600');"></div>
<div class="project-card-content" markdown>

### 🚀 Your Project Name

<span class="status-badge completed">Completed</span>

Brief description of what this project does and why it matters.

**Tech Stack:** `Python` · `Arduino` · `3D Printing`

[:octicons-arrow-right-24: View Project Details](your-project.md)

</div>
</div>
-->

---

## ➕ How to Add New Projects

!!! info "Adding a New Project"

    1. **Copy** `project-template.md` and rename it  
       _(e.g., `smart-home-system.md`)_

    2. **Fill in** your project details using the template structure

    3. **Add a card** above by copying a project card block

    4. **Update** `mkdocs.yml` — add your new page:

        ```yaml
        nav:
          - Projects:
              - Overview: projects/index.md
              - "📋 Project Template": projects/project-template.md
              - Smart Home System: projects/smart-home-system.md  # ← add here
        ```

    5. **Run** `mkdocs serve` and check it out!
