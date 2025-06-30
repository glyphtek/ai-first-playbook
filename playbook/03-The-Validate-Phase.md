# 03: The Validate Phase - Ensuring Code Quality with AI

You have successfully used the Build Phase workflow to generate code that meets the requirements of your PRD. Now, how do you ensure that code is robust, secure, and maintainable? The Validate Phase is split into two key activities: a formal code review using a specialized agent, and an interactive process for generating tests.

### Part 1: Formal Code Review with the Reviewer Agent

To ensure an objective, thorough, and consistent review process, we use a dedicated **Code Reviewer Agent**. This agent is configured with a specific system prompt that makes it an expert in code quality, security, and best practices.

**The "Code Reviewer" System Prompt:**
The prompt for this agent is located in the prompt library.

- **Find the prompt here:** [**../prompts/review/system_prompt_code_reviewer.md**](../prompts/review/system_prompt_code_reviewer.md)

**The Formal Review Workflow:**

1.  **Configure the Agent:** In a new chat session or tool, load the "Code Reviewer Agent" system prompt.
2.  **Provide Context:** Give the agent the PRD for the feature and the code you want it to review.
3.  **Receive the Report:** The agent will automatically analyze the code and provide a structured report covering security, best practices, readability, and actionable suggestions. This report can be attached to a pull request to guide human reviewers.

### Part 2: AI-Powered Test Generation

While the Code Reviewer Agent analyzes quality, you can use your primary **Developer Agent** (Backend, Frontend, etc.) to accelerate the creation of tests.

**The "Test Engineer" Workflow:**

1.  **Provide Context:** In your ongoing development chat, give your AI assistant the specific function or component you want to test.
2.  **Request Specific Tests:** Be explicit about what you need. This process is interactive, just like the Build Phase.

> **Example Prompts:**
>
> - "Write a complete suite of unit tests for this function using **Vitest**. Please include tests for the primary success case, at least one error case, and one edge case (e.g., handling null or empty input)."
> - "Generate a Storybook story for this React component."
> - "Propose a `[PLAN]` for an E2E test script using Playwright for the user flow described in the PRD."

### Human Is the Final Checkpoint

Remember the core principle: **Human-in-the-Loop Validation**. The AI's output—whether it's a code review report or a generated test—is a high-quality draft, not a final product. You must read, understand, and approve every change. The AI accelerates the process, but you are the ultimate guarantor of quality.

### What's Next?

With code that is both built and formally validated, the final step is to integrate these workflows into your team's broader processes.

Proceed to **[04: The Accelerate Phase](./04-The-Accelerate-Phase.md)** to learn about CI/CD integration and DevOps.
