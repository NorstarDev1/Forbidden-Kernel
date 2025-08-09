# Project Management Guide

This guide outlines the standardized project management system implemented within this Obsidian vault, leveraging Dataview and Templater for dynamic and collaborative project tracking.

---

## 📊 Project Dashboards

Project dashboards provide a unified view of each project, integrating project specifications, tasks, goals, and team information. They are designed to be a "resurrection packet" for quick onboarding and context retrieval.

### How to Create a New Project Dashboard:

1.  **Open the Templater Plugin:** In Obsidian, use the command palette (`Ctrl/Cmd + P`) and search for "Templater: Open Insert Template modal".
2.  **Select `Dashboard_Template`:** Choose `Dashboard_Template.md` from the list of available templates.
3.  **Name Your Dashboard:** When prompted, name your new note in the format `[Project Name] Project Dashboard` (e.g., `My_New_Project Project Dashboard`). This naming convention is crucial for Dataview queries to function correctly.
4.  **Create Project Specification:** Create a corresponding project specification note in `062_Projects/000_[Project_Name]/[Project_Name]_Project_Spec.md` (e.g., `062_Projects/000_My_New_Project/My_New_Project_Project_Spec.md`). This note should include the following YAML frontmatter:

    ```yaml
    tags: [project-spec]
    project: My_New_Project # Use the exact project name from your dashboard title
    status: In Progress # e.g., Planning, In Progress, Completed, On Hold
    start_date: YYYY-MM-DD
    end_date: YYYY-MM-DD
    team_lead: [[Your Name]] # Link to your profile note
    team_members:
      - [[Team Member 1]] # Link to their profile note
      - [[Team Member 2]]
    ```

    *Ensure the `project` field matches the project name used in your dashboard title.*

### Dashboard Sections Explained:

*   **Project Overview:** Displays key metadata from the project specification.
*   **Team:** Lists team members with links to their profile notes (requires profile notes in `810_Digital_Team_Members` or `820_Human_Team_Members`).
*   **Project Vision/Mission, Requirements/User Stories, Design/Architecture, Development Progress, Testing Status, Deployment/Release, Communication Log:** These sections dynamically pull notes tagged with `#vision`, `#requirements`, `#design`, `#development`, `#testing`, `#release`, and `#communication` respectively, from within the project's directory (`062_Projects/000_[Project_Name]`).
*   **Immediate Next Steps (Resurrection Packet):** A manually curated list of high-priority actions for quick context and onboarding.
*   **Project Files:** Lists all Markdown files within the project's directory.
*   **Open Tasks:** Displays uncompleted tasks from notes within the project's directory.
*   **Recent Notes:** Shows recently modified notes within the project's directory.
*   **Quick Links:** Provides direct links to important project files.

---

## 👥 Team Member Profiles

Team member profiles are stored in `810_Digital_Team_Members` and `820_Human_Team_Members`. Ensure these notes have a consistent naming convention (e.g., `[Name]_Filled_Profile.md`) and include relevant metadata for Dataview queries.

---

## 🌐 Dashboard of Dashboards

The central `000_Dashboard_of_Dashboards.md` note automatically lists all project dashboards (notes tagged with `#dashboard`). This provides a single entry point to all active projects.

---

*This guide is part of the SIVERSE LABS knowledge management system. For questions or improvements, contact Norstar or Aura.*