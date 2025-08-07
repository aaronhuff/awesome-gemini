# Ultimate Workspace Personal Assistant Guide

This guide provides a comprehensive overview of how to transform GitHub Copilot into the ultimate personal assistant for your workspace. By combining custom instructions, reusable prompts, and a deep understanding of your tools, you can create an AI partner that streamlines your workflow and boosts productivity.

## Core Concepts

The Workspace Personal Assistant is designed to be:

*   **Context-Aware:** It understands your project's structure, key files, and communication patterns.
*   **Proactive:** It can anticipate your needs and suggest actions to help you stay organized.
*   **Integrated:** It works seamlessly with your existing tools, including Google Workspace, Slack, and project management software.

## Setting Up Your Custom Gem

To create a "custom gem" for your Workspace Personal Assistant, you'll need to create a set of files that define its behavior. These files will be stored in your project's `.github` directory.

### 1. Custom Instructions (`.github/instructions/google-workspace-assistant.md`)

Create a file named `google-workspace-assistant.md` in a `.github/instructions` directory within your project. This file will contain the core instructions that define the assistant's persona and behavior.

### 2. Reusable Prompts (`.github/prompts/`)

Create a `prompts` directory within your `.github` directory. Here, you'll store reusable prompts for common tasks.

**Example Prompts:**
* `summarize-document.prompt.md`
* `draft-email.prompt.md`
* `create-todo-list.prompt.md`

## Using Your Workspace Personal Assistant

Once you've set up your custom instructions and reusable prompts, you can start interacting with your assistant in Copilot Chat.

### Invoking Your Assistant:

*   **General Questions:** Simply ask your question in the chat window.
*   **Reusable Prompts:** Use the `/` command followed by the prompt's filename (e.g., `/summarize-document`).

### Example Workflows:

*   **Summarizing a long email thread:**
    *   Open the email thread.
    *   In Copilot Chat, type: `/summarize-document`
*   **Drafting a project update:**
    *   In Copilot Chat, type: `Draft a project update for the team. We've completed the design phase and are moving on to development. The key deadline is next Friday.`
*   **Creating a to-do list:**
    *   In Copilot Chat, type: `Create a to-do list for the rest of the day. I need to finish the Q3 report, prepare for my 1:1 with my manager, and respond to all unread emails.`

By following this guide, you can create a powerful and personalized Workspace Personal Assistant that will help you work smarter, not harder.
