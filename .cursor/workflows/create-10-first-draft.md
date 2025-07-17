# Create 10-first-draft.md

Follow this instructions:

Check if file **[doc/10-first-draft.md](/doc/10-first-draft.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Create a first draft**" below

### If file already exists:

- read the instructions from the section "**Create a first draft**" below
- check if Astro is already installed in the project
  - if not, complete the missing sections of the file [doc/10-first-draft.md](/doc/10-first-draft.md)
  - if yes, tell the user that Astro is already installed in the project and ask if he wants to change the current development setup or he wants to continue to the next phase

---

## Create a first draft

### Role

You are an expert in web development and technical architecture, and your goal is to create a first draft of the website based on the current documentation.

**IMPORTANT:** This workflow is autonomous and does not require any user input!

### Instructions

- Start this interview with a big header "🚧 First Draft of the Website"
  with description that in this phase we do not focus on the visual design, but on the functionality and content of the website.

- Read all the documentation/specification in the files:

  - [doc/01-about-project.md](/doc/01-about-project.md)
  - [doc/02-website-structure.md](/doc/02-website-structure.md)
  - [doc/03-content-strategy.md](/doc/03-content-strategy.md)
  - [doc/04-personas-and-user-journeys.md](/doc/04-personas-and-user-journeys.md)
  - [doc/05-functional-requirements.md](/doc/05-functional-requirements.md)
  - [doc/06-media-content.md](/doc/06-media-content.md)
  - [doc/07-textual-content.md](/doc/07-textual-content.md)
  - [doc/08-technical-specifications.md](/doc/08-technical-specifications.md)
  - [doc/09-development-setup.md](/doc/09-development-setup.md)
  - [doc/99-other-mixed-context.md](/doc/99-other-mixed-context.md)

- create a header based on the specification

- create a footer based on the specification

- create all the pages based on the specification

- **IMPORTANT:** do not create content not mentioned in the specification!

- do not create any visual design, but focus on the functionality and content of the website

  - use no borders or very soft color borders
  - use rounded corners
  - instead of nonexisting images use gray background placeholders

- create a separate components for all small content elements (e.g. hero section, contact map, copyright, newsletter signup, social media links, testimonials section, etc.) or for repeating content elements (e.g. blog post previews, service/product cards, etc.)

- use those components in the pages and other components (always follow the DRY principle)

- use react code for all the components and React islands (where it is relevant)

- in CSS use `@reference "tailwindcss";` when using the `@apply ...` command.

- mimimize tailwind style (in this phase), do not use colors, just black&white styles, almost like wireframes, focus is on the functionality and content of the website

- do not use emojis in the web site content

- do not run the project with `npm run dev` or `astro dev` command, just suggest the user to run the project with the command: `npm run dev` or ask if he wants to run it by the agent

- create complete dynamic functionality for all the pages and components

- when everything is done, ask the user if he wants to see the website in the browser,
  test the result and suggest the changes if needed

- recommend the user to commit this state of the project with the command:
  `git add . && git commit -m "+ First Draft of the Website completed successfully"`
  (and ask user if he wants your help with this command - to run it for him)

- Finish this phase/workflow.
