# Create 09-development-setup.md

Follow this instructions:

Check if file **[doc/09-development-setup.md](/doc/09-development-setup.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Development setup**" below

### If file already exists:

- read the instructions from the section "**Development setup**" below
- check if Astro is already installed in the project
  - if not, complete the missing sections of the file [doc/09-development-setup.md](/doc/09-development-setup.md)
  - if yes, tell the user that Astro is already installed in the project and ask if he wants to change the current development setup or he wants to continue to the next phase

---

## Development setup

### Role

You are an expert in web development and technical architecture, and your goal is to install base Astro project with all necessary dependencies and configurations.

**IMPORTANT:** This workflow is autonomous and does not require any user input!

### Instructions

- Start this interview with a big header "⚙️ Development setup"

- Install Astro 4.x in the project with the command:
  `npm create astro@latest astro -- --template framework-react --no-git --no-install --yes`

  This would install a new Astro project into a folder `astro`.

  - `--template framework-react` - Use React as the framework
  - `--no-install` - Skip npm install after scaffolding
  - `--no-git` - Don't initialize a Git repository
  - `--yes` - Skip all prompts and accept defaults automatically

- Then add to the file `/astro/.gitignore` (append at the end of the file) content of the file [.gitignore](/.gitignore)

- Then add to the file `/.cursorignore` this content:

  ```
  # dependencies
  node_modules/
  ```

- Then copy to the file `/astro/README.md` content of the file [README.md](/.gitignore) (replace the original content)

- Then move the content of the folder `/astro/` to the root folder of the project and delete the folder `/astro/`

- Install the dependencies with the command: `npm i`

- Install the Tailwind CSS with the command: `npm install tailwindcss @tailwindcss/vite`

- Update the file `/tsconfig.json`: change the line:
  `"extends": "astro/tsconfigs/strict",`
  to new value:
  `"extends": "./node_modules/astro/tsconfigs/strict.json",`

- Create a new file (if doesn't exist yet) `/src/styles/global.css`

- Update content of the file `/src/styles/global.css` with this content:

  ```
  @import "tailwindcss";

  html,
  body {
    margin: 0;
    padding: 0;
    min-height: 100vh;
  }
  ```

- Update the file `/astro.config.mjs` with this content:

  - add the import of the Tailwind CSS: `import tailwindcss from "@tailwindcss/vite";`
  - add the plugin to the Vite configuration: `vite: { plugins: [tailwindcss()] },`
    with the comment above: "// Enable Tailwind CSS to support Tailwind CSS classes."

- Remove example component from the file `/src/components/` (e.g. "Counter")
  and remove it completely from the project (e.g. from the `/src/pages/index.astro`).

- Create a new file `/src/layouts/MainLayout.astro` with reusable layout for all the pages and:

  - add style to this file: `import '../styles/global.css';`
  - implement this layout to the `/src/pages/index.astro` file

- Create a new components "Header" and "Footer" (empty for now) and add them to the file `/src/layouts/MainLayout.astro`

- Write a log about this installation in the file `/doc/09-development-setup.md`

- Do not offer to test the project now (e.g. `npm run dev`).

- Print the success message: "✅ Development setup completed successfully"
  and recommend the user to commit this state of the project with the command:
  `git add . && git commit -m "✅ Development setup completed successfully"`
  (and ask user if he wants your help with this command - to run it for him)

- Finish this phase/workflow.
