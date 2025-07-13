# Create 08-technical-specifications.md

Follow this instructions:

Check if file **[doc/08-technical-specifications.md](/doc/08-technical-specifications.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Technical specifications design**" below

### If file already exists:

- read the instructions from the section "**Technical specifications design**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
  - if not, complete the missing sections of the file [doc/08-technical-specifications.md](/doc/08-technical-specifications.md)
  - if yes, ask the user if he wants to change the current technical specifications (write it out) or he wants to continue to the next phase

### Always:

- **IMPORTANT:** Always read and follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

---

## Technical specifications design

### Role

You are an expert in web development and technical architecture, and your goal is to design comprehensive technical specifications for the website based on all previous documentation:

- the document **[doc/01-about-project.md](/doc/01-about-project.md)**
- the document **[doc/02-website-structure.md](/doc/02-website-structure.md)**
- the document **[doc/03-content-strategy.md](/doc/03-content-strategy.md)**
- the document **[doc/04-personas-and-user-journeys.md](/doc/04-personas-and-user-journeys.md)**
- the document **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)**
- the document **[doc/06-media-content.md](/doc/06-media-content.md)**
- the document **[doc/07-textual-content.md](/doc/07-textual-content.md)**

Read also the [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md) and use what is relevant for current task. Summarize for user what you already know based on this file relative to current task and ask if it is still valid and continue from here.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

- Start this interview with a big header "🛠️ Technical specifications design"

- **AUTONOMOUS DESIGN APPROACH:** Unlike previous phases, you should **design the technical specifications autonomously** based on:

  - The established tech stack from README.md
  - Best practices for simple static websites
  - Requirements gathered in previous documentation phases
  - The constraints and features of this starter pack

- **LIMITED USER QUESTIONS:** Only ask the user about critical decisions that significantly impact the project:
  - Deployment preferences (if multiple viable options exist)
  - Third-party service preferences (when specific integrations are needed)
  - Performance vs. feature trade-offs (when there are meaningful choices)
  - Custom requirements that go beyond the standard starter pack scope

#### 1. Tech Stack Analysis & Decisions

Analyze all previous documentation and autonomously decide on:

- **Core framework configuration** (Astro 4 setup, routing, pages structure)
- **Styling**: Global CSS (common styles + reusables e.g. .btn-primary) + Tailwind CSS
- **Responsive**: Mobile-first approach (Tailwind CSS configuration, responsive breakpoints)
- **UI component strategy** (component architecture)
- **Build and deployment pipeline** (Cloudflare Pages setup, build optimization)
- **Performance optimization** (image optimization, code splitting, caching)

#### 2. Integration Requirements Design

Based on functional requirements, autonomously design:

- **Form handling** (Cloudflare Pages Functions + Turnstile implementation)
- **Email service** (Resend integration for contact forms and newsletters)
- **Analytics setup** (Cloudflare Web Analytics configuration)
- **SEO implementation** (Astro SEO + Sitemap generation)
- **Multilingual setup** (file-based routing if needed from requirements)

#### 3. Development Environment Setup

Design the complete development workflow:

- **Project structure** (folder organization, file naming conventions)
- **Development tools** (build scripts, dev server, debugging)
- **Content management** (JSON file structure for dynamic content)
- **Version control** (Git workflow, branch strategy)

#### 4. Performance & Optimization Strategy

Autonomously define:

- **Loading performance targets** (Core Web Vitals goals)
- **Image optimization pipeline** (responsive images, format selection)
- **Code optimization** (bundle size, tree shaking, compression)
- **Caching strategy** (browser cache, CDN, service worker if needed)

#### 5. Security & Compliance Implementation

Design security measures:

- **Form security** (Turnstile integration, validation)
- **Data protection** (GDPR compliance, cookie management)
- **Content security** (CSP headers, XSS protection)
- **Privacy implementation** (Zaraz Consent Manager if needed)

#### 6. Testing & Quality Assurance

Define testing approach:

- **Automated testing** (unit tests, integration tests if needed)
- **Performance testing** (Lighthouse CI, Core Web Vitals monitoring)
- **Cross-browser testing** (compatibility requirements)
- **Accessibility testing** (a11y compliance verification)

### Conversation Rules

1.  **IMPORTANT:** Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2.  **AUTONOMOUS APPROACH:** Design most technical decisions autonomously. Only ask users about:

    - Critical business decisions that impact functionality
    - Specific service preferences when multiple good options exist
    - Custom requirements beyond the standard starter pack scope

3.  **IMPORTANT:** After autonomous design is complete, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

    - write the output to the file **[doc/08-technical-specifications.md](/doc/08-technical-specifications.md)**
    - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)
    - if needed, update the previous documentation in the files to ensure consistency with technical decisions

4.  **IMPORTANT:** - check the output in `08-technical-specifications.md` again, and every section which isn't the topic of the current phase (Technical specifications) must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place. The "Output template" is only an example and **the actual content and sections may vary** based on the project's specific needs.

5.  **IMPORTANT:** for the new document `08-technical-specifications.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

6.  Finish this phase/workflow.

### Output template:

# Technical Specifications

## Core Technology Stack

### Frontend Framework

- **Framework:** Astro 4.x (Static Site Generator)
- **Styling**: Global CSS (common styles + reusables e.g. .btn-primary) + Tailwind CSS
- **Responsive**: Mobile-first approach (Tailwind CSS configuration, responsive breakpoints)
- **UI component strategy** (component architecture)
- **Build target:** Static HTML with minimal JavaScript

### Development Environment

- **IDE:** Cursor (AI-powered development)
- **Package Manager:** npm
- **Node.js version:** LTS (specify version)
- **Build tool:** Astro's native build system

## Architecture Decisions

### Project Structure

```
/
├── public/                 # Static assets copied verbatim to /dist
│   ├── robots.txt
│   ├── favicon.svg
│   └── images/            # Static images and media files
├── src/
│   ├── pages/             # Route-generating files (.astro, .md, .ts) - required
│   │   ├── index.astro
│   │   ├── about.astro
│   │   └── blog/[slug].astro
│   ├── layouts/           # Shared shells (headers, footers, meta)
│   ├── components/        # Re-usable UI pieces (.astro / *.jsx etc.)
│   ├── content/           # Markdown & data loaded via collections
│   │   └── blog/*.md
│   ├── actions/           # Server-only logic exposed to the client
│   │   ├── index.ts       # export const server = { … }
│   │   └── forms.ts       # Contact forms and email handling
│   ├── styles/            # Global CSS, Sass, Tailwind entry points
│   ├── images/            # Source images to be optimized by Astro
│   ├── lib/               # Utilities, types, fetchers
│   └── tests/             # (optional) Unit/integration tests (Vitest, Playwright, etc.)
├── doc/                   # Project documentation
├── astro.config.mjs       # Framework config (integrations, paths)
├── content.config.ts      # Zod schemas for `src/content/**`
├── tsconfig.json          # TS settings & path aliases
├── package.json           # Scripts & dependencies
└── .env*                  # Secrets that never go in git
```

### Content Management Strategy

- **Static content:** Markdown files with frontmatter in `src/content/`
- **Dynamic content:** Content collections using Astro's content system
- **Content schema:** Zod schemas defined in `content.config.ts`
- **Content updates:** AI agent-driven through Git workflow
- **Multilingual content:** <if applicable> File-based routing with locale folders

### Component Architecture

- **Static components:** Astro components (.astro)
- **Interactive components:** React islands for dynamic functionality
- **Styling approach:** Tailwind classes with component variants
- **Accessibility:** WCAG 2.1 AA compliance built-in

## Infrastructure & Hosting

### Hosting Platform

- **Primary hosting:** Cloudflare Pages
- **CDN:** Cloudflare global network (if is needed, most of the time it is not needed for small pages)
- **DNS:** Cloudflare DNS management (if needed, sometimes is Cloudflare Pages enough)
- **SSL:** Automatic HTTPS with Cloudflare certificates

### Deployment Strategy

- **Deployment trigger:** Git push to main branch
- **Build command:** `npm run build` or `pnpm build`
- **Output directory:** `dist/`
- **Environment variables:** Managed through Cloudflare dashboard

### Performance Optimization

- **Image optimization:** Astro's built-in image service
- **Code splitting:** Automatic by Astro build process
- **Caching strategy:** Cloudflare edge caching with custom rules
- **Compression:** Brotli and Gzip compression enabled

## Dynamic Features Implementation

### Forms & Communication

- **Contact forms:** Cloudflare Pages Functions with Turnstile protection
- **Email service:** Resend API (EU region) for transactional emails
- **Form validation:** Client-side validation + server-side sanitization
- **Success handling:** Inline success messages and email confirmations

### Analytics & Tracking

- **Web analytics:** Cloudflare Web Analytics (privacy-focused)
- **Performance monitoring:** Core Web Vitals tracking
- **Error tracking:** <if needed> Specify error monitoring service
- **Goal tracking:** Custom events for form submissions and key actions

### SEO Implementation

- **Meta tags:** Dynamic SEO component with Open Graph
- **Sitemap:** Auto-generated XML sitemap
- **Schema markup:** Structured data for relevant content types
- **Robots.txt:** Configured for optimal crawling

## Security & Privacy

### Security Measures

- **Form protection:** Cloudflare Turnstile for spam prevention
- **Content Security Policy:** Strict CSP headers configuration
- **XSS protection:** Input sanitization and output encoding
- **HTTPS enforcement:** Redirect all HTTP to HTTPS

### Privacy Compliance

- **Cookie management:** <if needed> Zaraz Consent Manager integration
- **GDPR compliance:** Privacy policy implementation and data handling
- **Analytics privacy:** Privacy-focused analytics without personal data collection
- **Form data handling:** Secure processing and optional data retention

## Development Workflow

### Local Development

- **Dev server:** `npm run dev` with hot reload
- **Port:** Default 4321 (Astro default)
- **Environment:** Local development with environment variables
- **Testing:** <specify testing approach>

### Version Control

- **Repository:** Git with main branch deployment
- **Branching strategy:** Feature branches with PR workflow
- **Commit conventions:** Conventional commits for automated changelog
- **CI/CD:** Automatic deployment on main branch push

### Content Updates

- **Content workflow:** AI agent manages content through Git
- **Review process:** <specify if needed> Content review before deployment
- **Backup strategy:** Git history as content backup
- **Rollback procedure:** Git revert for quick rollbacks

## Performance Targets

### Core Web Vitals Goals

- **Largest Contentful Paint (LCP):** < 2.5 seconds
- **First Input Delay (FID):** < 100 milliseconds
- **Cumulative Layout Shift (CLS):** < 0.1
- **Time to First Byte (TTFB):** < 800 milliseconds

### Optimization Strategy

- **Image optimization:** WebP format with fallbacks, responsive sizing
- **JavaScript optimization:** Minimal JS bundle, tree shaking enabled
- **CSS optimization:** Tailwind CSS purging, critical CSS inlining
- **Resource hints:** Preload critical resources, prefetch key pages

## Testing & Quality Assurance

### Automated Testing

- **Build validation:** Automated build testing on deployment
- **Link checking:** Automated broken link detection
- **Performance testing:** Lighthouse CI integration
- **Accessibility testing:** <if needed> Automated a11y testing

### Browser Support

- **Modern browsers:** Latest 2 versions of Chrome, Firefox, Safari, Edge
- **Mobile support:** iOS Safari, Chrome Android
- **Legacy support:** <specify if needed> IE11 or specific requirements
- **Progressive enhancement:** Core functionality works without JavaScript

## Monitoring & Maintenance

### Performance Monitoring

- **Core Web Vitals:** Continuous monitoring via Cloudflare Analytics
- **Uptime monitoring:** <if needed> External uptime monitoring service
- **Performance budgets:** Asset size limits and performance thresholds
- **Alert system:** Notifications for performance degradation

### Maintenance Schedule

- **Security updates:** Monthly dependency updates
- **Content review:** <specify frequency> Regular content freshness review
- **Performance audit:** Quarterly performance optimization review
- **Backup verification:** <specify frequency> Regular backup integrity checks

## Third-Party Integrations

### Required Services

- **Email delivery:** Resend API for transactional emails
- **Form protection:** Cloudflare Turnstile for spam prevention
- **Analytics:** Cloudflare Web Analytics for visitor insights
- **Hosting:** Cloudflare Pages for static site hosting

### Optional Services <if applicable>

- **Newsletter:** <if needed> Email service provider integration
- **Social media:** <if needed> Social platform integrations
- **Maps:** <if needed> Google Maps or alternative mapping service
- **Search:** <if needed> Client-side search implementation

## Scalability Considerations

### Traffic Handling

- **Expected traffic:** <estimate based on requirements>
- **Scaling strategy:** Cloudflare's global CDN automatically handles traffic spikes
- **Resource limits:** Cloudflare Pages limits and upgrade paths
- **Performance degradation:** Graceful degradation strategies

### Content Scaling

- **Content volume:** <estimate based on content strategy>
- **Media storage:** Cloudflare R2 or similar for large media files
- **Database needs:** <if needed> Workers KV or Neon Postgres for dynamic data
- **Search scaling:** <if needed> Client-side search or external search service
