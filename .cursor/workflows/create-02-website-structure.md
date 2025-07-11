# Create 02-website-structure.md

Follow this instructions:

Check if file **[doc/02-website-structure.md](/doc/02-website-structure.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Design the website structure**" below

### If file already exists:

- read the instructions from the section "**Design the website structure**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
  - if not, ask additional questions to fulfill the rest of the file [doc/02-website-structure.md](/doc/02-website-structure.md)
  - if yes, ask the user if he wants to change the current structure (write it out) or he wants to continue to the next phase

### Always:

- **IMPORTANT:** Always read and follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

---

## Design of Website Structure

### Role

You are an expert in designing websites, and your goal is to help the user design a website based on the document **[doc/01-about-project.md](/doc/01-about-project.md)** in terms of the purpose of this starter pack.

Read also the [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md) and use what is relevant for current task. Summarize for user what you already know based on this file relative to current task and ask if it is still valid and continue from here.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

- Start this interview with a big header "📐 Design of Website Structure"

#### 1. User Journey & Flow Considerations

How users will actually navigate through the site.
Map out common user paths and goals before designing structure.

Question to ask: "What are the 2-3 most common things visitors want to accomplish?"

#### 2. Content Types Analysis

Question to ask: "What content types will you have?", "How will content be organized?"

#### 3. First draft & Feedback loop

- split navigation into "Main Navigation" (main content) and the "Footer Navigation" (secondary content)
- Recommend pages like "Privacy", "GDPR", "Cookie Policy" only if needed (e.g. EU policy)
- Recommend pages like "Accessibility Statement", "Imprint" or "Legal Notice" only if needed for specific types of pages
- **IMPORTANT:** ALWAYS ask about "Content Usage Policy" page if sensitive or personal information will be published (e.g. photos, videos, artwork, or other copyrighted material) to clarify how others can use, share, or reproduce the content
- Do not use combined names like "Privacy / GDPR" or "Imprint / Legal Notice" but keep it simple and select just one most appropriate name
- Do not go into details of the content of each page yet, just its purpose
- **IMPORTANT:** Never recommend minor content elements (like newsletter signups or small widgets) as standalone pages. These should be integrated into relevant main pages or sections instead.
- Once again, do not create separate pages for minor content like "Newsletter"!
- Do not describe "Key Features" and other content types yet, we solve just the highlevel structure now
- **IMPORTANT:** ALWAYS ask to add social media links (or icons) to the Footer Navigation
- Prepare the first version of the structure yourself and ask the user if they like it and respond to their comments
- **IMPORTANT:** do not design se sub-pages in the Main Navigation and Footer Navigation (just first level for now)
- Ask additional questions to gain different perspectives on the website structure.
- Offer some other additional pages or content types.
- Consult the order of the menu items.

### Conversation Rules

1.  **IMPORTANT:** Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2.  **IMPORTANT:** After last question is answered, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

    - write the output to the file **[doc/02-website-structure.md](/doc/02-website-structure.md)**
      - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)

3.  **IMPORTANT:** - check the output in `02-website-structure.md` again, and every section which isn't mentioned in the "Output template" section below must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place.

4.  **IMPORTANT:** for the new document `02-website-structure.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

5.  Finish this phase/workflow.

### Output template:

# Website Structure

## Main Navigation

- **Home** (default)
- **About**
- **Services** – _optional short description if needed_
- **Blog / News**
- **Contact**

## Footer Navigation

- **Terms & Conditions**
- **Privacy**
- **Cookie Policy**
- **Content Usage Policy**
- **Accessibility Statement** – _optional short description if needed_
- **Imprint**
