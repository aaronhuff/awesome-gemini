# Ultimate Developer Assistant Guide

This guide will walk you through the process of transforming GitHub Copilot into the ultimate developer assistant. By creating a custom "gem" with tailored instructions and reusable prompts, you can build an AI partner that understands your codebase, follows your coding standards, and accelerates your development workflow.

## Core Concepts

The Developer Assistant is designed to be:

*   **A Code Expert:** It understands your project's architecture, libraries, and coding patterns.
*   **A Meticulous Tester:** It helps you write comprehensive and effective tests.
*   **A Clear Communicator:** It can explain complex code, document its work, and help you write clear commit messages.

## Setting Up Your Custom Gem

To create a "custom gem" for your Developer Assistant, you'll need to create a set of files that define its behavior. These files will be stored in your project's `.github` directory.

### 1. Custom Instructions (`.github/copilot-instructions.md`)

Create a file named `copilot-instructions.md` in a `.github` directory within your project. This file will contain the core instructions that define the assistant's persona and behavior.

**Example `copilot-instructions.md`:**

```markdown
# Developer Assistant Instructions

You are an expert software engineer. Your primary goal is to help me write high-quality, well-tested, and maintainable code.

## Key Responsibilities:

*   **Write Code:** Generate clean, efficient, and well-documented code that adheres to the project's coding standards.
*   **Write Tests:** Create comprehensive unit, integration, and end-to-end tests to ensure code quality.
*   **Refactor Code:** Identify opportunities to improve code structure, readability, and performance.
*   **Debug Code:** Help me identify and fix bugs in the codebase.
*   **Explain Code:** Provide clear and concise explanations of complex code sections.

## Technical Guidelines:

*   **Language:** The primary language for this project is {your_language}.
*   **Frameworks:** We use {your_frameworks}.
*   **Testing:** We use {your_testing_framework} for testing. All new code should be accompanied by tests.
*   **Style Guide:** Follow the {link_to_style_guide} for all code contributions.

## Tool Integration:

*   You have access to the entire codebase.
*   Use the `run_in_bash_session` tool to run tests, install dependencies, and execute scripts.
*   Use the `read_file` and `replace_with_git_merge_diff` tools to read and modify files.
```

### 2. Reusable Prompts (`.github/prompts/`)

Create a `prompts` directory within your `.github` directory. Here, you'll store reusable prompts for common tasks.

**Example Prompt: `write-unit-test.prompt.md`**

```markdown
---
mode: agent
description: "Write a unit test for a given function."
---

Please write a unit test for the following function:

{function_code}

The test should cover the following cases:
*   {case_1}
*   {case_2}
*   {case_3}
```

**Example Prompt: `refactor-code.prompt.md`**

```markdown
---
mode: agent
description: "Refactor a piece of code to improve its readability."
---

Please refactor the following code to improve its readability and maintainability. Explain the changes you made and why.

{code_to_refactor}
```

## Using Your Developer Assistant

Once you've set up your custom instructions and reusable prompts, you can start interacting with your assistant in Copilot Chat.

### Invoking Your Assistant:

*   **General Questions:** Simply ask your question in the chat window.
*   **Reusable Prompts:** Use the `/` command followed by the prompt's filename (e.g., `/write-unit-test`).

### Example Workflows:

*   **Generating a new feature:**
    *   In Copilot Chat, type: `I need to add a new feature that allows users to export their data as a CSV file. The data is stored in a PostgreSQL database. Please create a plan to implement this feature.`
*   **Writing a test for an existing function:**
    *   Copy the function code.
    *   In Copilot Chat, type: `/write-unit-test` and paste the function code.
*   **Refactoring a complex module:**
    *   In Copilot Chat, type: `/refactor-code` and provide the name of the module.

By following this guide, you can create a powerful and personalized Developer Assistant that will help you write better code, faster.
