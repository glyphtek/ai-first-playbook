# Example Project: CommunityHub

## Project Purpose

This "CommunityHub" project is the official case study and reference implementation for the **[AI-First Playbook](https://github.com/glyphtek/ai-first-playbook)**.

Its entire lifecycle—from requirements to code to validation—is driven by the methodologies and AI agents defined in the playbook. It serves as a practical, real-world demonstration of the playbook in action.

---

### **Status: Project Brief**

This document serves as the official **Project Brief**. It is the initial, high-level input for the PRD Agent to begin the **Define Phase** of the AI-First Playbook workflow.

---

### Project Overview

CommunityHub is a universal, template platform for building community management applications. It's designed to provide core features that any group, club, or organization would need, such as member management, event scheduling, and announcements.

### Core Features

- **User & Authentication:**
  - User Registration (email/password)
  - User Login / Logout
  - User Profile Management (view and edit own profile)
- **Community & Member Management:**
  - Member Directory (searchable list of public profiles)
  - Role-Based Access Control (Admin, Moderator, Member)
- **Content & Engagement:**
  - Announcements (Admins/Mods can create, all can view/comment)
  - Resource Sharing (ability to post links or upload documents to a shared library)
- **Event Management:**
  - Event Creation (with title, description, date/time, location)
  - Event Calendar/List View
  - RSVP System (ability to mark attendance)

### Proposed Tech Stack

- **Runtime:** Bun
- **Backend:** ElysiaJS with TypeScript
- **Frontend:** React (Vite) with TypeScript
- **Database:** PostgreSQL (managed with Docker)
- **Testing:** Vitest, Playwright for E2E

### Prerequisites

- Bun (v1.0 or higher)
- Docker & Docker Compose
- Git

### Getting Started (Placeholder)

#### Installation & Setup

1.  Clone the repository.
2.  Install all dependencies: `bun install`
3.  Set up environment variables by copying `.env.example` to `.env`.
4.  Start the database: `docker-compose up -d`

#### Running the Application

- **To run the backend & frontend concurrently:** `bun dev`

### How This Demonstrates the Playbook

This project will be built following these steps from the AI-First Playbook:

1.  **Define Phase:** The requirements for this project will be generated from this brief using the **PRD Agent**. The final document will be saved in the `/prd` directory.
2.  **Build Phase:** The source code will be generated using the **Backend** and **Frontend Developer Agents**, following the interactive **Confirmation Protocol**.
3.  **Validate Phase:** All code will be reviewed using the **Code Reviewer Agent**, and tests will be generated with assistance from the developer agents.
