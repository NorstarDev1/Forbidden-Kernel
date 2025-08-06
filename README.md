# Obsidian Life OS: A Deep Dive

---

This document provides a comprehensive overview of the "Organize your Life with Obsidian" vault. It is intended to be a living document that serves as a guide for all members of SIVERSE LABS.

## Core Philosophy

This vault is designed to be a "second brain" or a "Life OS" (Operating System). It is a powerful system for managing knowledge, projects, tasks, and personal growth. It is built on the principles of **connected thinking**, **atomic notes**, and **progressive summarization**.

## Directory Structure

The vault is organized into a series of numbered directories, each with a specific purpose:

- [[`000 Inbox`]] : The landing zone for all new ideas, notes, and information. Items in the inbox should be processed regularly and moved to their appropriate location.
- [[`001 Templates`]] : Contains all the templates for creating new notes. This is the heart of the vault's content creation system.
- [[`002 Attachments`]] : The designated location for all file attachments, such as images, PDFs, and documents.
- [[`003 Archives`]] : For notes that are no longer active but that you want to keep for future reference.
- [[`004 Technic`]] : For notes related to technical topics.
- [[`005 Workflows`]] : For notes that describe various workflows.
- [[`006 Action`]] : The central hub for all actionable items. It contains subdirectories for:
    - [[1 Tasks]] : Individual tasks.
    - [[2 Projects]] : Larger initiatives that are composed of multiple tasks.
    - [[3 Goals]] : High-level objectives that projects and tasks are aligned with.
    - [[4 Values]] : The core principles that guide your goals and actions.
- [[`007 Kanban`]]: For Kanban boards, which can be used to visualize and manage workflows.
- [[`008 Events`]] : For managing events, appointments, and other time-based information.
- [[`009 Specs`]]: For project specifications and other detailed project documentation.
- [[`100 Zettelkasten`]] : The core of the knowledge management system. It is organized using the Zettelkasten method, which is a powerful way to build a network of interconnected ideas.
- [[`200 Watch List`]] : For tracking books, articles, and other media that you are actively creating or want to consume.
- [[`300 References`]] : For storing and organizing reference materials.
- [[`400 Business`]] : For notes related to business planning and success management.
- [[`500 Personal`]] : For personal notes, journaling, and self-reflection.
- [[`600 Periodic`]] : For daily, weekly, and monthly notes, which are great for tracking progress and building habits.
- [[`700 Lore Logs`]]: For in-character writings and story development.
- [[`800 SIVERSE LABS`]] : For notes related to SIVERSE LABS, including digital team members and project-specific documentation.

## Key Plugins

This vault is supercharged with a number of powerful plugins:

- **`Dataview`**: The engine of the vault's data organization. It allows you to query and display data from your notes using SQL-like queries, creating dynamic tables, lists, and dashboards that automatically update as your notes change.
- **`Templater`**: The heart of the vault's content creation system. It allows you to create dynamic templates with variables, functions, and scripts, automating the creation of complex, pre-populated notes.
- **`Tasks`**: A robust task management system that allows you to track tasks across your entire vault. You can add due dates, priorities, recurrence, and filters to create powerful, customized task views.
- **`QuickAdd`**: Streamlines the creation of new notes and content by providing a quick-capture interface. This is perfect for getting ideas down quickly without breaking your flow.
- **`Periodic Notes`**: Automates the creation of daily, weekly, and monthly notes, providing a consistent structure for journaling, planning, and reflection.
- **`CardBoard`**: Allows you to create and manage Kanban boards within Obsidian, providing a visual way to track projects and workflows. This is used for the `Project Kanban Board.md`.

## Core Workflows

### Creating New Notes

1.  Use the **`QuickAdd`** plugin to quickly create a new note from a template.
2.  Choose the appropriate template from the **`001 Templates`** directory.
3.  Fill in the relevant information in the note's YAML frontmatter and content. The `Templater` plugin will automatically fill in fields like the creation date.
4.  Link the new note to other relevant notes in the vault to build your web of knowledge.

### Managing Projects with Project Specs

1.  Create a new project spec file in the **`009 Specs`** directory using the `Proj_Spec_temp` template.
2.  Fill out the YAML frontmatter with the project's metadata, such as the `status`, `owner`, and `target_date`.
3.  Define the project's mission, objectives, and components in the body of the note.
4.  Add specific, actionable tasks to the "Active Tasks" table.
5.  Track the progress of all projects visually using the [[Project Kanban Board]]. This board automatically pulls tasks from all your project spec files.

## Key Files

- **[[Home]]**: The master dashboard that provides links to all the other important dashboards and periodic overviews.
- **[[006 Action/MCP Dashboard]]**: A comprehensive overview of your values, goals, and projects.
- **[[006 Action/2 Projects/Project Kanban Board.md|Project Kanban Board]]**: A Kanban board that visualizes the tasks from all of your project spec files.
- **[[001 Templates/0062 Projects/Proj_Spec_temp.md|Project Spec Template]]**: The template for creating new project specification files.

This vault is a powerful tool for organizing your life and work. By understanding its structure and workflows, you can unlock its full potential.