# Create 05-functional-requirements.md

Follow this instructions:

Check if file **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Functional requirements analysis**" below

### If file already exists:

- read the instructions from the section "**Functional requirements analysis**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
  - if not, ask additional questions to fulfill the rest of the file [doc/05-functional-requirements.md](/doc/05-functional-requirements.md)
  - if yes, ask the user if he wants to change the current requirements (write it out) or he wants to continue to the next phase

---

## Functional requirements analysis

### Role

You are an expert in designing websites, and your goal is to help the user to identify the functional requirements for the website based on previous documentation:

- the document **[doc/01-about-project.md](/doc/01-about-project.md)**
- the document **[doc/02-website-structure.md](/doc/02-website-structure.md)**
- the document **[doc/03-content-strategy.md](/doc/03-content-strategy.md)**
- the document **[doc/04-personas-and-user-journeys.md](/doc/04-personas-and-user-journeys.md)**

Read also the [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md) and use what is relevant for current task. Summarize for user what you already know based on this file relative to current task and ask if it is still valid and continue from here.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

- Start this interview with a big header "⚙️ Functional requirements analysis"

- Identify and analyze the functional requirements for the website based on the project's specific needs and constraints.

- Focus on **simple website functionality** as described in the README.md - this is for static content with minimal dynamic features.

- **IMPORTANT:** Consider the technical limitations mentioned in README.md:

  - No CMS (Content Management System) - but we will use AI agent to manage the content
  - No user registration or authentication
  - No payment processing
  - No advanced dynamic features

- **DO NOT ASK** minor or obvious questions like:
  - about page loading speed expectations (it is not important for simple website)
  - accessibility requirements (WCAG compliance level) (implement basic accessibility requirements)
  - about browser support requirements (just latest versions of major browsers)
  - mobile performance and responsive behavior (just basic responsive design)
  - URL structure for different languages (/en/, /sk/, etc. if more languages are needed)
  - about Content Management Workflow
    - since there's no CMS:
      - content will be updated through AI agent / updating files in the project
      - no content approval workflow if multiple authors
  - do not ask about GIT and backup and version control for content
  - about future scalability considerations (just basic scalability)

#### 1. Core Static Features Analysis

- Ask about essential static website features like navigation, responsive design, SEO optimization
- Identify content presentation requirements (text, images, videos, galleries)
- Ask about page transitions, loading states, and basic interactivity

#### 2. Basic Dynamic Features Analysis

Start with the basic dynamic features that are supported, for example:

- **Contact forms** - ask about form fields, validation, submission handling
- **Newsletter sign-up** - ask about email capture, integration requirements
- **Search functionality** - if needed for content discovery
- **Social media integration** - sharing buttons, social feeds
- **Analytics and tracking** - visitor analytics, conversion tracking

#### 3. Multilingual Support

- Ask if multilingual support is needed
- If yes, ask about:
  - Which languages are required
  - Content translation (content in local files and AI agent will translate it)
  - Language switcher placement and behavior

#### 4. Integration Requirements

Based on the current spec and ask for any third-party service integrations.

#### 5. Security and Privacy Requirements

- Ask about data protection requirements (GDPR compliance)
- Cookie policy implementation
- Form data handling and storage
- Privacy policy requirements

#### 6. Future Scalability Considerations

- Ask about potential future features that might be needed
- Identify any features that should be prepared for but not implemented initially

### Conversation Rules

1. Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2. After last question is answered, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

   - write the output to the file **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)**
   - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)
   - if needed, update the previous documentation in the files:
     - **[doc/01-about-project.md](/doc/01-about-project.md)**
     - **[doc/02-website-structure.md](/doc/02-website-structure.md)** - e.g. add new pages for required functionality
     - **[doc/03-content-strategy.md](/doc/03-content-strategy.md)** - e.g. add content elements for new features

3. **IMPORTANT:** - check the output in `05-functional-requirements.md` again, and every section which isn't the topic of the current phase (Functional requirements) must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place. The "Output template" is only an example and **the actual content and sections may vary** based on the project's specific needs.

4. **IMPORTANT:** for the new document `05-functional-requirements.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

5. Finish this phase/workflow.

### Output template:

# Functional Requirements

## Core Static Features

### Navigation & Structure

- **Responsive navigation:** Mobile-first design with hamburger menu for mobile devices
- **Breadcrumb navigation:** For multi-level pages (if applicable)
- **Footer navigation:** Secondary links and legal pages
- **404 error page:** Custom error page with navigation back to main content

### Content Presentation

- **Responsive design:** Mobile, tablet, and desktop optimization
- **Image optimization:** Automatic resizing and compression for different screen sizes
- **Video embedding:** Support for YouTube/Vimeo embeds
- **SEO optimization:** Meta tags, structured data, sitemap generation

## Basic Dynamic Features

### Forms

- **Contact form:** Name, email, message fields with validation
- **Form protection:** Turnstile integration to prevent spam
- **Form submission:** Email notifications via Resend service
- **Success/error states:** User feedback after form submission

### Newsletter & Communication

- **Email signup:** Newsletter subscription with email validation
- **Social media integration:** Sharing buttons for main content
- **Social media links:** Links to social profiles in footer

### Content Discovery

- **Search functionality:** <if needed> Basic content search
- **Content filtering:** <if needed> Category/tag-based filtering
- **Related content:** <if needed> Suggestions based on current page

## Multilingual Support <optional>

- **Languages:** <Primary language> (primary), <Additional languages>
- **URL structure:** File-based routing per locale (`/en/`, `/sk/`, etc.)
- **Language switcher:** Dropdown/toggle in header navigation
- **Content translation:** Separate content files per language

## Technical Integrations

### Analytics & Tracking

- **Cloudflare Web Analytics:** Basic visitor tracking and page views
- **Conversion tracking:** <if needed> Goal tracking for forms/newsletter

### Security & Privacy

- **Cookie consent:** Cloudflare Zaraz Consent Manager integration
- **GDPR compliance:** Privacy policy and data handling procedures
- **Form security:** Turnstile protection against spam and bots
- **HTTPS enforcement:** SSL certificate and secure connections

### Email Services

- **Transactional emails:** Resend integration for form submissions
- **Newsletter service:** <if needed> Integration with email service provider

## Content Management

### Content Updates

- **AI-driven updates:** Content management through AI agent
- **File based storage:** Content stored in project source code (JSON files or other files)
- **Version control:** Git-based content versioning

## Future Considerations <optional>

### Potential Enhancements

- **Advanced search:** Full-text search with filtering
- **User comments:** Comment system for blog posts
- **E-commerce basic:** Simple product showcase (no payments)
- **Advanced analytics:** More detailed user behavior tracking
