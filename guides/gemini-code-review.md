# Gemini Code Review Guide

This guide explains how to use Gemini Code Assist to review your code in GitHub.

Gemini Code Assist is a powerful tool that can help you improve the quality of your code by providing automatic code reviews on your pull requests. It is a GitHub App that you need to install and configure in your repository.

For general guidance on how to write effective prompts, please refer to the [Prompting Best Practices](./prompting-best-practices.md) guide.

## How it Works

Gemini Code Assist uses a Gemini-powered agent to:

*   Automatically summarize pull requests.
*   Provide in-depth code reviews.
*   Answer your questions about the pull request.

## Installation

To install Gemini Code Assist, you need to:

1.  Go to the [Gemini Code Assist for GitHub app page](https://github.com/apps/gemini-code-assist).
2.  Click "Install" and select the organization and repositories where you want to use it.
3.  Follow the on-screen instructions to complete the setup.

## Usage

Once installed, Gemini Code Assist will automatically review new pull requests. It will add a comment to the pull request with its feedback.

You can also manually invoke Gemini Code Assist by adding comments to the pull request with the following commands:

*   `/gemini summary`: Posts a summary of the changes in the pull request.
*   `/gemini review`: Posts a code review of the changes in the pull request.
*   `/gemini help`: Shows an overview of the available commands.

## Example Code Review

Here is an example of how Gemini Code Assist might review a pull request.

**Original Code:**

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
```

**Gemini Code Assist Review:**

> This is a good implementation of the factorial function, but it is vulnerable to a stack overflow error for large values of `n` due to the recursive implementation. Consider rewriting this function iteratively to avoid this issue.
>
> Here is an example of an iterative implementation:
>
> ```python
> def factorial(n):
>     if n < 0:
>         raise ValueError("Factorial is not defined for negative numbers")
>     result = 1
>     for i in range(1, n + 1):
>         result *= i
>     return result
> ```

## Customization

You can customize the behavior of Gemini Code Assist by creating a `.github/gemini.yml` file in your repository. This file allows you to:

*   Define a custom style guide.
*   Configure the severity of the issues that Gemini reports.
*   And much more.

For more detailed information, please refer to the [official documentation](https://developers.google.com/gemini-code-assist/docs/review-github-code).
