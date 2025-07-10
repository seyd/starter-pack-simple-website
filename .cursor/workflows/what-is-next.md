# What's next?

This document traces the current phase and executes the corresponding workflow.

**Current phase:** none

> Here is the name/header of the current phase (next phase or currently in progress).
> If "none" is used, nothing was executed yet.

---

## Phases

### 0. Disclaimer

Disclaimer phase ensures the user understands this starter pack is designed for simple, static websites and explicitly does NOT include advanced features. This sets proper expectations and prevents users from going through the entire workflow only to discover the limitations don't match their requirements.

Workflow: [welcomne.md](/.cursor/workflows/welcome.md)

### 1. Initial discovery

Initial discovery is the focused kickoff phase where we capture the project’s core purpose, audience, value proposition, success metrics, and key constraints through a structured questionnaire. Its goal is to establish a shared strategic foundation before any site architecture or design work begins.

Workflow: [create-01-about-project.md](/.cursor/workflows/create-01-about-project.md)

### 2. Website structure design

Website structure design translates the discovery insights into a high-level content map—laying out the core pages for the main navigation and assigning auxiliary pages (e.g., terms and coditions, GDPR, privacy) to a footer (secondary menu) before any detailed layout or content work begins.

Workflow: [create-02-website-structure.md](/.cursor/workflows/create-02-website-structure.md)

### 3. Content strategy analysis

Content strategy analysis determines the content types, organization, and management approach for each page in the website structure, establishing what content is needed, how it's categorized, and how it will be maintained over time.

Workflow: [create-03-content-strategy.md](/.cursor/workflows/create-03-content-strategy.md)

### 4. Personas and user journeys

Personas and user journeys identifies the key user types (personas) who will visit the website and maps their specific needs, motivations, and interaction patterns. This ensures the site structure and content effectively serve different audiences before moving into detailed design and development.

Workflow: [create-04-personas-and-user-journeys.md](/.cursor/workflows/create-04-personas-and-user-journeys.md)

### 5. Individual change requests

Workflow: none

---

## Instructions for the agent

- start with a big header "What's the next step?".
- if current phase is `none`, start with the "**0. Disclaimer**"
- if current phase is not `none`, execute the phase mentioned as the current phase.
- when you start any phase, update the value of the `Current phase` in this document with the name (header) of that phase (with the number of the phase included)
- read and follow the instruction of the workflow file of the current phase
- when you finish the phase (workflow), update the value of the `Current phase` to the name of the following phase, and write a success message starting with the 🎉 emoji in **bold font** indicating that the phase has been successfully completed
- when the is no other phase left, just leave the value of the `Current phase` pointing to the last phase
- let the user know you have finnished the current phase and ask him if he wants to continue to the next one (or when it is the last phase, if he want to do this phase again)
  ```
  Please respond with:
  - ✅ "Yes" (or "Continue") - to continue the process
  - ❌ "No" (or "Stop") - to stop here
  ```
- if he don't want to continue, finish here like:
- if he want to continue, recommend him to open a new chat window with `Ctrl + N` and start with "**What's next?**"
