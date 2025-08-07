# Ultimate Developer Assistant Guide

This guide will walk you through the process of transforming GitHub Copilot into the ultimate developer assistant. By creating a custom "gem" with tailored instructions and reusable prompts, you can build an AI partner that understands your codebase, follows your coding standards, and accelerates your development workflow.

## Core Concepts

The Developer Assistant is designed to be:

*   **A Code Expert:** It understands your project's architecture, libraries, and coding patterns.
*   **A Meticulous Tester:** It helps you write comprehensive and effective tests.
*   **A Clear Communicator:** It can explain complex code, document its work, and help you write clear commit messages.

## Setting Up Your Custom Gem

To create a "custom gem" for your Developer Assistant, you'll need to create a set of files that define its behavior. These files will be stored in your project's `.github` directory.

### 1. Custom Instructions (`.github/instructions/developer-assistant.md`)

Create a file named `developer-assistant.md` in a `.github/instructions` directory within your project. This file will contain the core instructions that define the assistant's persona and behavior.

### 2. Reusable Prompts (`.github/prompts/`)

Create a `prompts` directory within your `.github` directory. Here, you'll store reusable prompts for common tasks.

**Example Prompts:**
* `write-unit-test.prompt.md`
* `refactor-code.prompt.md`
* `explain-code.prompt.md`

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
