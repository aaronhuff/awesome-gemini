# Prompting Best Practices

This guide provides a set of best practices for designing effective prompts that elicit accurate and high-quality responses from large language models like Gemini. These strategies are based on the official [Google AI for Developers Prompting Strategies Guide](https://ai.google.dev/gemini-api/docs/prompting-strategies).

## 1. Be Clear and Specific

The most important principle of prompt design is to be clear and specific in your instructions. The model is not a mind reader, so you need to provide it with all the necessary information to understand your request.

*   **Good:** "Summarize the following text in three bullet points."
*   **Less Good:** "Summarize this."

### Constraints

Clearly define what the model should and should not do.

**Example:**

> Summarize the following article, but do not include any information about the author's personal life.

### Response Format

Specify the desired format for the output. This could be a list, a JSON object, a table, or any other format.

**Example:**

> Extract the names of all the people mentioned in the following text and return them as a JSON array.

## 2. Provide Examples (Few-Shot Prompting)

One of the most effective ways to guide the model's response is to provide it with examples of the desired output. This is known as "few-shot prompting."

A prompt with no examples is called a "zero-shot prompt." While these can be effective for simple tasks, few-shot prompts are generally more reliable for complex requests.

**Example (Zero-Shot):**

> Classify the following sentiment as positive, negative, or neutral: "I'm not sure if I like the new design."

**Example (Few-Shot):**

> **Input:** "I love the new design!"
> **Output:** Positive
>
> **Input:** "The new design is terrible."
> **Output:** Negative
>
> **Input:** "I'm not sure if I like the new design."
> **Output:**

By providing examples, you can guide the model to produce the output in the format and style you want.

## 3. Provide Context

Give the model the necessary context to understand your request. This could be a document, a set of instructions, or any other relevant information.

**Example:**

> **Context:** [Paste a long article about the history of the internet]
>
> **Question:** According to the provided article, who are the key figures in the development of the internet?

By providing the article as context, you ensure that the model's answer is based on the information you've provided, rather than its general knowledge.

## 4. Break Down Complex Tasks

For complex tasks, it's often best to break them down into smaller, more manageable steps. You can do this by chaining prompts together, where the output of one prompt becomes the input for the next.

**Example:**

1.  **Prompt 1:** "Generate a list of ideas for a blog post about the benefits of exercise."
2.  **Prompt 2:** "Take the first idea from the list and write an outline for a blog post."
3.  **Prompt 3:** "Write a full blog post based on the provided outline."

## 5. Use Prefixes

Prefixes can be used to signal different parts of the prompt to the model.

*   **Input Prefix:** Use prefixes to label different parts of your input.
*   **Output Prefix:** Use a prefix to indicate the expected format of the output.

**Example:**

> **English:** "Hello"
> **French:** "Bonjour"
>
> **English:** "Goodbye"
> **French:**

This signals to the model that you are asking for a translation from English to French.

## 6. Iterate on Your Prompts

Prompt design is often an iterative process. If you're not getting the results you want, try rephrasing your prompt, adding more examples, or providing more context.

## 7. What to Avoid

*   **Avoid ambiguity:** Be as clear and specific as possible.
*   **Don't assume knowledge:** Provide all the necessary context.
*   **Don't rely on the model for factual accuracy:** Always verify the model's responses, especially for important information.
*   **Avoid overly complex prompts:** Break down complex tasks into smaller steps.

## Further Reading

For more in-depth examples and hands-on tutorials, please see the [Gemini API Cookbook](https://github.com/google-gemini/cookbook).
