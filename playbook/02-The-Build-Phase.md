# 02: The Build Phase - From Requirements to Code

Welcome to the Build Phase. With a clear and detailed Product Requirements Document (PRD) from the Define Phase, we are now ready to write code. This chapter will walk you through the structured, interactive workflow for building software with an AI partner.

The goal here is not just speed, but also quality, consistency, and control.

### Your PRD is Your Map

The PRD you created in Phase 1 is the single source of truth for this phase. It provides the "map" for both you and your AI assistant, ensuring you are aligned on the goals and specifications of the feature you are building.

### The Core Workflow: The Confirmation Protocol

This is the most important concept in the entire playbook. To avoid the common pitfalls of AI-generated code (errors, hallucinations, unwanted complexity), we use a strict, turn-by-turn interactive workflow called the **Confirmation Protocol**.

This protocol ensures **you are always in control**. The AI is not allowed to act without your explicit approval.

The workflow is a simple, repeatable loop:

1.  **You give the AI a task** derived from the PRD (e.g., "Create the database table for events").
2.  **The AI proposes a `[PLAN]`**. It outlines the steps it will take and the files it will modify.
3.  **You approve or modify the plan**. This is the critical human validation step. You are the architect.
4.  **The AI executes the _first step_ of the plan** and presents a `[CODE_BLOCK]`.
5.  **You review and approve the code**.
6.  The AI proceeds to the next step of the plan, and the loop repeats until the task is complete.

Throughout this process, the AI will use specific labels for its output:

- `[PLAN]`: An outline of the steps it will take.
- `[CODE_BLOCK]`: A block of generated code, ready for you to review.
- `[SUGGESTION]`: An alternative approach or improvement it has identified.
- `[QUESTION]`: A request for clarification if the PRD is ambiguous.

### The Developer Prompt Library

To facilitate this workflow, the playbook includes a library of specialized system prompts that configure your AI assistant to act as an expert for a specific role.

- **[Backend Developer Prompt](../prompts/backend/system_prompt_backend_main.md):** Use this for building APIs, database schemas, and server-side logic.
- **[Frontend Developer Prompt](../prompts/frontend/system_prompt_frontend_main.md):** Use this for building UI components, managing state, and handling user interactions.
- **[Full-Stack Developer Prompt](../prompts/full-stack/system_prompt_fullstack_main.md):** Use this for features that require changes across the entire stack.

### Step-by-Step Walkthrough: Building the Events Feature

Let's continue with our "CommunityHub Events Feature" example.

**1. Choose Your Persona**
The first part of the feature requires a database table and an API. We will use the **Backend Developer Prompt**.

**2. Configure Your Assistant**
Navigate to the [Backend Prompt](../prompts/backend/system_prompt_backend_main.md), copy its content, and paste it into your AI tool's system prompt area.

**3. Provide Context**
Start a new chat and provide the AI with the full PRD you created in the Define Phase. This is essential context.

> **You:** "We are starting a new feature. Here is the complete PRD for it: [Paste the entire PRD markdown here]."

**4. Give the First Task**
Once the AI has the context, give it a granular task based on the PRD.

> **You:** "Excellent. Based on the PRD, let's start by creating the database schema for the 'Events' feature."

**5. Follow the Confirmation Protocol**
Now, you simply follow the interactive loop.

> **AI:** `[PLAN]`
>
> 1.  Create a new database migration file named `YYYYMMDDHHMMSS_create_events_table.js`.
> 2.  In this file, define the `events` table with the following columns based on the PRD: `id` (PK), `name` (string), `description` (text), `event_date` (datetime), `location` (string), and `organizer_id` (FK to users).
>
> Is this plan correct?

> **You:** "The plan looks good. Please proceed with step 1 and 2."

> **AI:** `[CODE_BLOCK]`
>
> ```javascript
> // contents of YYYYMMDDHHMMSS_create_events_table.js
> module.exports = {
>   up: async (queryInterface, Sequelize) => {
>     await queryInterface.createTable("events", {
>       // ... column definitions ...
>     });
>   },
>   down: async (queryInterface, Sequelize) => {
>     await queryInterface.dropTable("events");
>   },
> };
> ```
>
> Here is the code for the migration file. Shall I proceed with the next logical step, which is creating the API endpoint to list these events?

This loop continues—from database, to API, to business logic—until the backend portion of the PRD is fully implemented.

### What's Next?

By following this structured, interactive process, you can build features faster while maintaining high standards of quality and full control over the output. Once the code is written, the next step is to ensure it's correct and robust.

Proceed to **[03: The Validate Phase](./03-The-Validate-Phase.md)** to learn how to use AI to supercharge your code reviews and testing.
