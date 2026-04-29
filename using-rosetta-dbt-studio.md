# Using Rosetta DBT Studio

## App Navigation

The app has a left sidebar that organizes its main features. Each section is designed for a different part of your dbt workflow.

### Projects

- View and manage your saved projects.
- Create a new project, import an existing one, or clone from Git.
- Open a project to switch to the project workspace.

### DBT Studio

This is the main working area for your selected project.

- The top header shows the active project and the database connection.
- The middle area displays project files and configuration.
- The right side may include panels for logs, command status, or contextual help.

### SQL Editor

Use the SQL Editor to write and run queries directly against your project connection.

- Browse project files in the left tree.
- Open SQL files or create a new query tab.
- Run queries using the query controls at the top.

### Notebooks

Notebooks let you explore your data with rich, interactive documents.

- Select a connection from the dropdown.
- Create notebook pages, add SQL blocks, and view results inline.
- Use notebooks for exploration, analysis, and collaboration.

### Object Explorer

Object Explorer provides a dashboard view of cloud and local data assets.

- See connected sources, recent items, and storage types.
- Access buckets, files, and schemas from supported cloud services.

### DataLake

DataLake is for managing tables, schemas, and catalogs from different backends.

- Create and browse DataLakes.
- Review recent queries and accessed tables.
- Use it when you need a central place for data lake metadata.

## Everyday Workflows

### Opening a Project

1. Go to **Projects**.
2. Select a project from the list.
3. Click the project card or action button to open it.

### Editing a dbt Model

1. Open the **DBT Studio** tab.
2. Use the file tree to find your model file, usually under `models/`.
3. Click the file to open it in the editor.
4. Edit the SQL and save changes.

### Running dbt

1. Open the active project.
2. Choose a dbt command from the UI.
3. Monitor progress in the command output or log panel.
4. When finished, inspect results for success or errors.

### Using Git

- The app includes Git integration for managing project changes.
- Use Git actions to commit, view changed files, and synchronize work.

## Tips for New Users

- Always start with a sample or existing project to understand the workflow.
- Use the **SQL Editor** to preview query results before running dbt models.
- If a connection is missing, create a new database connection in the DBT Studio tab.
- Keep your profiles and project settings updated when switching environments.
