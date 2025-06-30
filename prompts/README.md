# How to Use These System Prompts

The system prompts in this directory are the engine of the AI-First Playbook. They are designed to be used in development environments that support custom system prompts or instructions for an AI assistant.

### Step-by-Step Instructions

1.  **Navigate:** Choose the prompt that matches your context (e.g., `backend/` or `full-stack/`).
2.  **Select:** Open the relevant prompt file, for example, `system_prompt_backend_main.md`.
3.  **Copy:** Select and copy the entire Markdown content of the file.
4.  **Paste:** Paste the copied text into the designated "System Prompt," "Custom Instructions," or equivalent configuration area of your AI-powered tool.

**This methodology is confirmed to work well with:**

- AI-native editors like **Cursor or Windsurf**.
- Standard editors with AI extensions like **VS Code + Copilot Chat**.
- AI command-line interfaces (CLIs) like **Codex, Gemini-CLI, and Claude Code**.

---

### ⚠️ Important: Human-in-the-Loop Requirement

These prompts are **intentionally NOT designed** for use in fully autonomous, "fire-and-forget" agentic AI workflows.

The entire methodology of this playbook is built on the **Confirmation Protocol**, which requires a human developer to be an active participant in the workflow. The AI is instructed to `[PLAN]`, propose `[CODE_BLOCK]`s, and then **wait for your explicit command** before proceeding.

Attempting to run these prompts in an automated loop that bypasses human approval will fail and violates the core principles of this project. This is a methodology for **augmenting and accelerating human developers, not replacing them.**
