# Ultimate Workspace Personal Assistant Guide

This guide provides a comprehensive overview of how to transform GitHub Copilot into the ultimate personal assistant for your workspace. By combining custom instructions, reusable prompts, and a deep understanding of your tools, you can create an AI partner that streamlines your workflow and boosts productivity.

## Core Concepts

The Workspace Personal Assistant is designed to be:

*   **Context-Aware:** It understands your project's structure, key files, and communication patterns.
*   **Proactive:** It can anticipate your needs and suggest actions to help you stay organized.
*   **Integrated:** It works seamlessly with your existing tools, including Google Workspace, Slack, and project management software.

## Setting Up Your Custom Gem

To create a "custom gem" for your Workspace Personal Assistant, you'll need to create a set of files that define its behavior. These files will be stored in your project's `.github` directory.

### 1. Custom Instructions (`.github/copilot-instructions.md`)

Create a file named `copilot-instructions.md` in a `.github` directory within your project. This file will contain the core instructions that define the assistant's persona and behavior.

**Example `copilot-instructions.md`:**

```markdown
# Workspace Personal Assistant Instructions

You are a world-class personal assistant. Your primary goal is to help me stay organized, manage my tasks, and communicate effectively.

## Key Responsibilities:

*   **Summarize:** Provide concise summaries of emails, documents, and conversations.
*   **Draft:** Create professional and well-written drafts for emails, reports, and presentations.
*   **Organize:** Help me manage my to-do list, schedule meetings, and track deadlines.
*   **Find Information:** Quickly locate relevant information from my files and conversations.

## Communication Style:

*   Be clear, concise, and professional.
*   Use a friendly and helpful tone.
*   When in doubt, ask for clarification.

## Tool Integration:

*   You have access to my Google Workspace, Slack, and Jira.
*   Use the `@` command to reference files and people.
*   Use tools to create and modify files, schedule events, and update tasks.
```

### 2. Reusable Prompts (`.github/prompts/`)

Create a `prompts` directory within your `.github` directory. Here, you'll store reusable prompts for common tasks.

**Example Prompt: `summarize-document.prompt.md`**

```markdown
---
mode: agent
description: "Summarize the key points of a document."
---

Please read the attached document and provide a summary of the key takeaways. The summary should be no more than three bullet points.
```

**Example Prompt: `draft-email.prompt.md`**

```markdown
---
mode: agent
description: "Draft an email to a colleague."
---

Please draft an email to {colleague_name} about {topic}. The tone should be friendly and professional.
```

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
