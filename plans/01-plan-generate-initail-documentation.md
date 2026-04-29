# Plan Generate Initial Documentation For DBT STUDIO

This plan defines a phased approach to scan the `dbt-studio` repository and generate end-user focused Markdown documentation inside `/Users/agondika/Documents/DBT STUDIO COMBINED/documentaiton-dbtstudio`.

## Goal

Create beginner-friendly documentation for new Rosetta DBT Studio users. The output will explain the Electron UI, main screens, user workflows, and core features without requiring developer-level knowledge.

## Phase 1 — User-first scope and discovery

1. Confirm the end-user documentation scope:
   - onboarding for new users launching the Electron app
   - Projects and workspace navigation
   - database connection setup in DBT Studio
   - SQL Editor usage
   - notebook workflow and data exploration
   - Object Explorer and cloud/source browsing
   - DataLake creation and management
   - Git integration and saving work
   - AI-assisted model generation and dbt command execution
2. Review existing UI labels and page names in the app:
   - Projects
   - DBT Studio
   - SQL Editor
   - Notebooks
   - Object Explorer
   - DataLake
   - Settings
3. Define the output structure for `/documentaiton-dbtstudio`:
   ```
   documentaiton-dbtstudio/
   ├── overview.md
   ├── getting-started.md
   ├── workspace-guide.md
   ├── screens/
   │   ├── projects.md
   │   ├── dbt-studio.md
   │   ├── sql-editor.md
   │   ├── notebooks.md
   │   ├── object-explorer.md
   │   └── datalake.md
   ├── features.md
   └── faq.md
   ```

## Phase 2 — Screen and workflow inventory

1. Scan the repo for UI components and screens used by end users:
   - `src/renderer/screens/`
   - `src/renderer/components/`
   - `src/renderer/layouts/`
   - `src/renderer/controllers/`
   - `src/renderer/hooks/`
2. Map code to user-facing screens and features:
   - Projects list and project actions
   - Project workspace / DBT Studio view
   - SQL Editor file tree and query tabs
   - Notebooks connection selection and page flow
   - Object Explorer dashboard and source browser
   - DataLake dashboard, create/manage flows, catalog view
   - Settings / connection config area
3. Identify user-facing workflows and feature triggers:
   - open/import/clone project
   - connect or switch database connections
   - create/edit/run SQL queries
   - generate dbt models and run dbt commands
   - view command status and logs
   - access AI assistants
   - browse cloud/data lake objects

## Phase 3 — User workflow documentation design

1. Define the primary user journeys:
   - first-time launch and project creation
   - opening an existing project
   - connecting to a database
   - running a dbt project
   - editing SQL and saving changes
   - exploring data with notebooks
   - browsing cloud storage and DataLakes
   - using Git and saving work
2. Design documentation pages for each journey:
   - step-by-step instructions
   - expected screen state and controls
   - common success and error outcomes
   - tips for new users
3. Determine the right level of detail:
   - focus on what users need to do in the UI
   - avoid developer build instructions except when needed for app setup
   - explain terms like "project", "connection", "model", "notebook", and "DataLake"

## Phase 4 — Generate screen-specific docs

1. Create docs for each major UI screen:
   - `Projects` — create/import/clone and switch projects
   - `DBT Studio` — manage dbt connection, project files, and commands
   - `SQL Editor` — open files, edit queries, run SQL, and inspect results
   - `Notebooks` — create notebooks, run SQL cells, and navigate notebook pages
   - `Object Explorer` — browse sources, buckets, and recent items
   - `DataLake` — create DataLakes and view metadata dashboards
2. Document key end-user features under `features.md`:
   - one-click dbt command execution
   - AI-assisted model generation and document creation
   - Git integration for project changes
   - built-in dbt docs generation
   - connection management and profile selection
3. Add practical examples and screenshots guidance:
   - sample project workflows
   - common menu/button labels
   - where to find logs and status details

## Phase 5 — Build the Markdown docs

1. Create the documentation files under `/documentaiton-dbtstudio` with a structure inspired by dbt Labs Studio IDE docs:
   - Use clear headings and subheadings for navigation
   - Include introductory sections with overviews and key benefits
   - Add prerequisites and setup instructions
   - Feature tables and detailed descriptions
   - Step-by-step getting started guides
   - FAQs and troubleshooting sections
   - Related docs and links
2. Content guidelines for each file:
   - **overview.md**: High-level introduction to Rosetta DBT Studio, what it solves, supported databases, data transformation journey. Include a brief video or image placeholder.
   - **getting-started.md**: Prerequisites (installing the app, basic requirements), first launch steps, creating/opening projects, initial database connection.
   - **workspace-guide.md**: Overview of the app interface, sidebar navigation, common workflows.
   - **screens/**: Each screen doc should have:
     - What the screen does
     - Key UI elements and controls
     - Step-by-step usage instructions
     - Screenshots or image placeholders (e.g., "![Screen layout](images/screen-name.png)")
     - Tips and common actions
   - **features.md**: Table of features with descriptions, similar to the dbt Labs example. Include AI assistance, dbt commands, Git integration, etc. Add expandable sections for detailed explanations.
   - **faq.md**: Common questions and answers, using collapsible sections if possible in Markdown.
3. Style and formatting:
   - Use Markdown tables for feature lists and comparisons.
   - Embed images and videos: Use `![alt text](path/to/image.png)` for images, and `<video>` tags or links for videos.
   - Use bold, italics, and code blocks for emphasis.
   - Include tips, notes, and warnings with callouts (e.g., `:::tip` or `> **Tip:**`).
   - Add expandable sections using HTML details/summary if needed: `<details><summary>Click to expand</summary>Content</details>`.
   - Cross-link between pages using relative links (e.g., `[Projects](screens/projects.md)`).
   - Use consistent terminology matching the app UI labels.
4. Incorporate multimedia for every feature:
   - Embed images and videos directly within the Markdown files using placeholders like `![Feature screenshot](path/to/image.png)` and `[Feature demo video](path/to/video.mp4)` or `<video src="path/to/video.mp4" controls></video>`.
   - For each major feature (e.g., database connection, SQL editing, AI assistance, dbt commands, Git integration, notebooks, object explorer, DataLake), include at least one image and one video link within the relevant documentation files.
   - Use placeholders initially: e.g., "![Database connection setup](images/database-connection.png)" and "[Database connection demo](videos/database-connection-demo.mp4)".
5. Ensure beginner-friendly tone:
   - Avoid technical jargon; explain terms.
   - Focus on user actions and outcomes.
   - Provide examples and real-world use cases.

## Phase 6 — Review and validate for new users

1. Review the generated docs from a beginner's perspective:
   - Can a new user open the app and start a project?
   - Are instructions clear and step-by-step?
   - Do images/videos enhance understanding?
   - Is the style engaging and similar to professional docs like dbt Labs?
2. Validate accuracy against the app UI and repository labels.
3. Refine wording, add cross-links, and build a small FAQ for common questions.
4. Test navigation: Ensure links work and structure is logical.

## Output expectations

- End-user focused Markdown documentation in `/Users/agondika/Documents/DBT STUDIO COMBINED/documentaiton-dbtstudio` styled like dbt Labs Studio IDE docs.
- Professional appearance with images and videos embedded within the Markdown files for every feature.
- Clear onboarding path for first-time Rosetta DBT Studio users.
- Screen-specific guides for Projects, DBT Studio, SQL Editor, Notebooks, Object Explorer, and DataLake.
- Feature-centric docs that help users understand app value and next actions.


