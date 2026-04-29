# Getting Started with Rosetta DBT Studio

## Welcome

Rosetta DBT Studio is a desktop app for working with dbt projects, generating models, and running SQL transformations without using the terminal.

## Opening the App

1. Launch Rosetta DBT Studio from your Applications folder.
2. The app opens to the **Projects** screen.
3. If this is your first time, choose one of:
   - **Clone** an existing dbt project
   - **Import** a local project
   - **New** to create a new project from scratch

## Create or Open a Project

- **New**: sets up a starter dbt project and sample profile files.
- **Import**: opens an existing project folder on your computer.
- **Clone**: downloads a project from a Git repository.

After opening a project, you will see the project name and path in the top header.

## Connect to a Database

1. Open the **DBT Studio** tab.
2. Locate the connection selector at the top.
3. Choose or create a new database connection.
4. Use the connection panel to enter host, database, schema, and authentication details.

## Explore the App Interface

The left sidebar includes the main areas of the app:

- **Projects** — manage your dbt projects
- **DBT Studio** — project workspace and active dbt connection
- **SQL Editor** — write and run SQL queries
- **Notebooks** — create and explore notebooks connected to your data
- **Object Explorer** — browse data sources and cloud storage
- **DataLake** — manage DataLake connections and metadata
- **Settings** — configure app preferences

## Run dbt Commands

Inside a project, you can run dbt commands from the UI without using a terminal.

- Look for command buttons or the command bar in the active project workspace.
- Run standard commands like:
  - `dbt run`
  - `dbt test`
  - `dbt compile`
  - `dbt docs generate`

## Save and Close

- Save any open files inside the editor using the save button in the tab bar.
- Close projects by switching back to the **Projects** tab and selecting a different project or closing the app.
