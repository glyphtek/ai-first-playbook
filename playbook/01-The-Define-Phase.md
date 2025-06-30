# 01: The Define Phase - Creating Robust Requirements

The success of any software project is built on the quality of its requirements. Vague or incomplete requirements lead to wasted effort, scope creep, and friction. The goal of the Define Phase is to solve this problem by establishing a clear, consistent, and robust set of requirements before a single line of code is written.

### The Problem: The "Napkin Sketch" Requirement

Too often, development starts with a high-level idea that lacks detail. This "napkin sketch" approach forces developers to make assumptions, leading to rework when those assumptions are wrong.

### The Solution: The PRD Agent

To combat this, we introduce the **PRD Agent**. As mentioned in the introduction, this is not a separate tool but a _configured role_ for your AI assistant. By giving your assistant the system prompt below, you turn it into an expert Product Manager. Its job is to collaborate with you to transform a high-level idea into a structured Product Requirements Document (PRD).

---

### The PRD Agent System Prompt

The "source code" for our PRD Agent is a system prompt located in the prompt library. This is the core asset for the Define Phase.

**Find the prompt here:** [**prompts/prd/system_prompt_prd_main.md**](../prompts/prd/system_prompt_prd_main.md)

---

### How to Use the PRD Agent

**Step 1: Configure Your Assistant**
Navigate to the file linked above, copy the entire system prompt, and paste it into the custom instructions or system prompt area of your chosen AI tool (e.g., Cursor, VS Code, etc.).

**Step 2: Start the Conversation**
Begin a new chat. The PRD Agent will introduce itself. Provide it with your high-level feature idea.

> **Example:** "Hi! I'd like to build an events feature for our CommunityHub application. Users should be able to create and view events."

**Step 3: Engage in a Dialogue**
The PRD Agent will now ask you clarifying questions based on the required sections of the PRD.

> **AI Example Question:** "That's a great feature idea. To get started, who is the target audience for creating events? Is it any community member, or only administrators?"

Answer its questions thoughtfully. This collaborative process is where the real value lies.

**Step 4: Generate the PRD**
Once you feel you've covered all the necessary details, instruct the agent to create the document.

> **Example:** "Okay, I think you have enough information now. Please generate the complete PRD based on our conversation."

The agent will provide a well-structured Markdown document that you can save as the official requirement for the feature (e.g., in your project's `prd/` or `docs/` folder).

### What's Next?

With a clear and comprehensive PRD, you are now ready to move from planning to execution.

Proceed to **[02: The Build Phase](./02-The-Build-Phase.md)** to learn how to use this PRD to start writing code with the help of our specialized developer prompts.
