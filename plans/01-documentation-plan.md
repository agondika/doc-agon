# Documentation Plan — Rosetta DBT Studio

This plan defines a phased approach to generate end-user focused Markdown documentation for Rosetta DBT Studio. The goal is to produce clear, beginner-friendly docs that help new users understand and use the app confidently.

## Goal

Create beginner-friendly documentation for new Rosetta DBT Studio users. The output explains the Electron desktop UI, main screens, user workflows, and core features — without requiring developer-level knowledge of dbt or SQL.

**Target audience:** Anyone new to Rosetta DBT Studio, including users who have never used dbt before.

---

## Structure


doc-agon/
├── plans/
│   └── 01-documentation-plan.md        ← 
├── images/                              ← screenshots 
├── videos/                              ← video link
│
├── overview.md                          ← what the app is and why it exists
├── installation-guide.md                ← how to download and install
├── getting-started.md                   ← first launch, projects, connections
├── ai-integration-guide.md              ← setting up your ai agent, and using it
│
├── screens/                             ← one doc per screen in the app
│   ├── projects.md                      ← Projects screen
│   ├── dbt-studio.md                    ← DBT Studio workspace
│   ├── sql-editor.md                    ← SQL Editor
│   ├── notebooks.md                     ← Notebooks
│   ├── connections.md                   ← Connections & Sources
│   ├── cloud-explorer.md                ← Cloud Explorer
│   └── datalake.md                      ← DataLake
│
├── features/                            ← one doc per major feature
│   ├── ai-assistant.md                  ← AI providers setup and usage
│   ├── git-integration.md               ← Git workflow inside the app
│   ├── dbt-commands.md                  ← Run, Test, Build, Compile etc
│   └── model-generation.md              ← Staging, Enhanced, Business layers
│
└── faq.md                               ← common questions and answers


---

## Documentation Status

| File | Status | Notes |
|------|--------|-------|
| overview.md | ✅ Done | |
| installation-guide.md | ✅ Done | |
| ai-integration-guide.md | ✅ Done| |
| getting-started.md | ✅ Done | |
| screens/projects.md | ❌ Not started | |
| screens/dbt-studio.md | ❌ Not started | |
| screens/sql-editor.md | ❌ Not started | |
| screens/notebooks.md | ❌ Not started | |
| screens/connections.md | ❌ Not started | |
| screens/cloud-explorer.md | ❌ Not started | |
| screens/datalake.md | ❌ Not started | |
| features/ai-assistant.md | ❌ Not started | |
| features/git-integration.md | ❌ Not started | |
| features/dbt-commands.md | ❌ Not started | |
| features/model-generation.md | ❌ Not started | |
| faq.md | ❌ Not started | |

---

## Phase 1 — Setup and Scope

1. Confirm documentation scope for end users:
   - Installation and first launch
   - Project creation, import, and cloning
   - Database connection setup
   - DBT Studio workspace navigation
   - SQL Editor usage
   - Notebooks workflow and data exploration
   - Object Explorer and cloud source browsing
   - DataLake creation and management
   - Git integration and saving work
   - AI-assisted model generation
   - dbt command execution

2. Confirm the app's main screens and UI labels:
   - Projects
   - DBT Studio
   - SQL Editor
   - Notebooks
   - Connections & Sources
   - Cloud Explorer
   - DataLake
   - Settings

3. Set up the folder structure in the repository:
   - Create `screens/` folder
   - Create `features/` folder
   - Create `images/` folder for screenshots
   - Create `videos/` folder for video references

---

## Phase 2 — Screen and Workflow Inventory

1. Map each screen to its user-facing purpose:
   - **Projects** — create, import, clone, and manage dbt projects
   - **DBT Studio** — main workspace for editing models and running dbt
   - **SQL Editor** — write and run SQL queries against your database
   - **Notebooks** — explore data interactively with SQL cells
   - **Connections & Sources** — manage database connections
   - **Cloud Explorer** — browse cloud storage buckets and files
   - **DataLake** — create and manage DataLake instances
   - **Settings** — configure app preferences, AI providers, dbt paths

2. Identify the primary user workflows:
   - First-time launch and project creation
   - Opening an existing project
   - Connecting to a database
   - Generating staging, enhanced, and business models
   - Running dbt commands from the UI
   - Writing and running SQL in the editor
   - Exploring data with Notebooks
   - Using AI to generate models and queries
   - Committing changes with Git
   - Browsing cloud storage and DataLakes

3. Note key UI elements per screen:
   - Buttons, dropdowns, and action menus
   - Sidebar navigation icons
   - Terminal panel at the bottom
   - File tree on the left
   - Tab bar across the top

---

## Phase 3 — Content Design

1. Define what each doc needs:
   - **overview.md** — what the app is, what problem it solves, how it works, supported databases, data transformation journey
   - **installation-guide.md** — system requirements, download steps, first launch
   - **getting-started.md** — creating a project, connecting a database, loading the example project, navigating the interface
   - **screens/** — each screen gets: what it is, key UI elements, step-by-step instructions, screenshot placeholder, tips
   - **features/** — each feature gets: what it does, when to use it, how to use it, screenshot or video placeholder, common issues
   - **faq.md** — common questions based on things new users would ask

2. Define writing guidelines:
   - Write for someone who has never used dbt before
   - Avoid technical jargon — if a term is used, explain it
   - Focus on what the user sees and does, not how the code works
   - Use active voice — "Click the button" not "The button should be clicked"
   - Keep sentences short and clear
   - Use **bold** for UI element names
   - Use `code formatting` for file names, commands, and paths

3. Define formatting rules:
   - `#` for page title
   - `##` for main sections
   - `###` for subsections
   - Numbered lists for steps
   - Bullet points for options or features
   - Image placeholders: `![Description](../images/filename.png)`
   - Video placeholders: `> 📹 [Watch demo](../videos/filename.mp4)`
   - Tips: `> **Tip:** useful advice here`
   - Notes: `> **Note:** important thing to know`
   - Cross-links: `[Projects screen](screens/projects.md)`

---

## Phase 4 — Write Screen Docs

Write one `.md` file per screen inside the `screens/` folder.

Each screen doc follows this template:

```markdown
# Screen Name

## Overview
What this screen is and what you use it for.

## Key UI Elements
Description of the main buttons, panels, and controls.

## How to Use
Step-by-step instructions.

## Screenshot
![Screen name](../images/screen-name.png)

## Tips
Useful advice for new users.
```

Priority order:
1. `screens/projects.md` — first screen every user sees
2. `screens/dbt-studio.md` — main working screen
3. `screens/sql-editor.md` — frequently used
4. `screens/connections.md` — needed to connect a database
5. `screens/notebooks.md`
6. `screens/cloud-explorer.md`
7. `screens/datalake.md`

---

## Phase 5 — Write Feature Docs

Write one `.md` file per major feature inside the `features/` folder.

Each feature doc follows this template:

```markdown
# Feature Name

## What Is This?
Plain English explanation of what this feature does.

## When Would You Use It?
Real world context and use cases.

## How to Use It
Step-by-step instructions.

## Screenshot or Video
![Feature screenshot](../images/feature-name.png)
> 📹 [Watch demo](../videos/feature-name.mp4)

## Common Issues
Things that might go wrong and how to fix them.
```

Priority order:
1. `features/dbt-commands.md` — core functionality every user needs
2. `features/model-generation.md` — key value of the app
3. `features/ai-assistant.md` — popular feature, needs API key setup explained
4. `features/git-integration.md` — important for saving work

---

## Phase 6 — Write FAQ

Write `faq.md` last — after all other docs are done.

Base the questions on:
- Things that came up while writing other docs
- Common confusion points for new users
- Questions about installation, connections, AI setup, and dbt commands

Use collapsible sections for each question:

```markdown
<details>
<summary>How do I connect to my database?</summary>

Go to the Connections tab in the sidebar...

</details>
```

---

## Phase 7 — Review and Validate

1. Review every doc from a new user's perspective:
   - Can a new user install the app and start a project from just these docs?
   - Are all steps clear and complete?
   - Are all screenshot and video placeholders in place?
   - Do all cross-links between docs work?

2. Validate accuracy against the app UI:
   - Do button names match exactly what appears in the app?
   - Are all steps in the correct order?
   - Is any feature missing from the docs?

3. Final checks:
   - Consistent terminology throughout all files
   - No spelling or grammar errors
   - All relative links working
   - Status table in this plan updated to ✅ for all completed files

---

## Terminology Guide

Use these terms consistently across all documentation:

| Term | Definition |
|------|-----------|
| Project | A dbt project managed inside the app |
| Connection | A saved database connection |
| Model | A SQL transformation file (.sql) |
| Schema | The YAML file describing a model |
| Workspace | The main project editing area |
| DBT Studio tab | The main project screen |
| Run | Executing dbt models against the database |
| Source | Raw database tables before transformation |
| Staging | First transformation layer — cleaned data |
| Enhanced | Second transformation layer — joined data |
| Business | Final transformation layer — analysis-ready data |
| DataLake | A collection of tables managed by DuckLake |
| AI Provider | An AI service connected to power the AI features |


