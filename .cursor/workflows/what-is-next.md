# What's next?

This document traces the current phase and executes the corresponding workflow.

**Current phase:** none

> Here is the name/header of the current phase (next phase or currently in progress).
> If "none" is used, nothing was executed yet.

---

## Phases

### 0. Disclaimer

Disclaimer phase ensures the user understands this starter pack is designed for simple, static websites and explicitly does NOT include advanced features. This sets proper expectations and prevents users from going through the entire workflow only to discover the limitations don't match their requirements.

Workflow: [welcome.md](/.cursor/workflows/welcome.md)

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

### 5. Functional requirements analysis

Functional requirements analysis identifies the features needed for the website based on the project's specific needs and constraints.

Workflow: [create-05-functional-requirements.md](/.cursor/workflows/create-05-functional-requirements.md)

### 6. Media content analysis

Media content analysis defines comprehensive media requirements including image specifications, video integration strategies, and asset organization systems. This phase establishes optimization standards and accessibility compliance.

Workflow: [create-06-media-content.md](/.cursor/workflows/create-06-media-content.md)

### 7. Textual content analysis

Textual content analysis establishes content guidelines including brand voice, tone standards, etc., then creates actual written content for all essential website pages. This phase transforms previous strategic insights into practical, ready-to-use text that aligns with user personas and business goals.

Workflow: [create-07-textual-content.md](/.cursor/workflows/create-07-textual-content.md)

### 8. Technical specifications

Technical specifications define the technical requirements for the website, including the tech stack, hosting platform, deployment strategy, and maintenance schedule.

Workflow: [create-08-technical-specifications.md](/.cursor/workflows/create-08-technical-specifications.md)

### 9. Development setup

Development setup is the phase where we install the necessary tools and dependencies to start the development of the website.

Workflow: [create-09-development-setup.md](/.cursor/workflows/create-09-development-setup.md)

### 10. First draft of the website

First draft of the website is the phase where we create a first draft of the website based on the current documentation.

Workflow: [create-10-first-draft.md](/.cursor/workflows/create-10-first-draft.md)

### 11. Individual change requests

Workflow: none

---

## Instructions for the agent

- start with a big header "What's the next step?".
- if current phase is `none`, start with the "**0. Disclaimer**"
- if current phase is not `none`, execute the phase mentioned as the current phase.
- when you start any phase, update the value of the `Current phase` in this document with the name (header) of that phase (with the number of the phase included)
- read and follow the instruction of the workflow file of the current phase
- **IMPORTANT**: always follow the workflow [update-tasks.md](/.cursor/workflows/update-tasks.md)
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
