# Create 06-media-content.md

Follow this instructions:

Check if file **[doc/06-media-content.md](/doc/06-media-content.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Media content strategy**" below

### If file already exists:

- read the instructions from the section "**Media content strategy**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
  - if not, ask additional questions to fulfill the rest of the file [doc/06-media-content.md](/doc/06-media-content.md)
  - if yes, ask the user if he wants to change the current media strategy (write it out) or he wants to continue to the next phase

### Always:

- **IMPORTANT:** Always read and follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

---

## Media content strategy

### Role

You are an expert in web media optimization and content creation, and your goal is to help the user define comprehensive media requirements and guidelines based on previous documentation:

- the document **[doc/01-about-project.md](/doc/01-about-project.md)**
- the document **[doc/02-website-structure.md](/doc/02-website-structure.md)**
- the document **[doc/03-content-strategy.md](/doc/03-content-strategy.md)**
- the document **[doc/04-personas-and-user-journeys.md](/doc/04-personas-and-user-journeys.md)**
- the document **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)**

Read also the [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md) and use what is relevant for current task. Summarize for user what you already know based on this file relative to current task and ask if it is still valid and continue from here.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

- Start this interview with a big header "🎨 Media content strategy"

- Identify and analyze all media requirements, content creation guidelines, optimization strategies, and storage needs for the website.

- Focus on **practical media implementation** for simple websites with static content approach, considering the AI-driven content management mentioned in README.md.

- **DO NOT ASK** too technical questions like (but make decisions for user):
  - Performance & Optimization
  - Image optimization for page speed
  - Progressive loading strategies
  - CDN usage and caching requirements
  - Mobile performance considerations
  - Estimated storage needs based on content volume
  - Growth projections for media content
  - Backup and redundancy requirements
  - Cost considerations for media hosting

#### 1. Content Audit & Media Types Analysis

- Review the content strategy from previous documents and identify all media types needed
- Ask about (if relevant):
  - **Images:** Photos, graphics, icons, logos, backgrounds, thumbnails
  - **Videos:** Embedded content, promotional videos, tutorials, background videos
  - **Audio:** Background music, sound effects, podcasts (if applicable)
  - **Interactive media:** Maps, charts, graphs, animations
  - **Documents:** PDFs, downloadables, brochures

#### 2. Image Strategy & Requirements

- **Photo specifications:**

  - Ask about preferred image formats (JPEG, PNG, WebP)
  - Determine quality requirements and file size limits
  - Identify image dimensions needed for different contexts
  - Ask about aspect ratios for different content types

- **Content creation guidelines:**

  - Photography style and aesthetic preferences
  - Brand consistency requirements (colors, filters, mood) - if applicable
  - AI generated va Stock photo vs custom photo preferences
  - Image composition guidelines

- **Technical optimization:**
  - Automatic resizing requirements for responsive design
  - Compression settings and quality thresholds
  - Lazy loading implementation for performance
  - Alt text and accessibility requirements

#### 3. Video Content Strategy

- **Video types and sources:**

  - Ask about video content types (promotional, tutorial, background, testimonials)
  - Determine hosting preferences (YouTube, Vimeo, self-hosted)
  - Video format and quality requirements
  - Duration guidelines for different content types

- **Integration requirements:**
  - Thumbnail customization and play button styling
  - Autoplay preferences and user experience considerations
  - Mobile optimization and data usage concerns
  - Loading performance and fallback strategies

#### 4. Asset Organization & Management

- **File structure and naming:**

  - Directory organization for different media types (use Astro's recommended structure)
    - `/public/images/` - for static images and media files
    - `/src/images/` - for source images to be optimized by Astro
  - File naming conventions for easy management
  - Version control for updated assets
  - Source file storage and backup strategy

- **Content workflow:**
  - How new media will be created and added (AI agent integration)
  - Review and approval process for media content
  - Update and replacement procedures
  - Archive and removal workflows

#### 5. Performance & Optimization

- **Loading performance:**

  - Image optimization for page speed
  - Progressive loading strategies
  - CDN usage and caching requirements
  - Mobile performance considerations

- **Storage requirements:**
  - Estimated storage needs based on content volume
  - Growth projections for media content
  - Backup and redundancy requirements
  - Cost considerations for media hosting

#### 6. Accessibility & Compliance

- **Accessibility requirements:**

  - Alt text standards and implementation
  - Video caption and transcript requirements
  - Color contrast and visual accessibility
  - Screen reader compatibility

- **Legal and usage rights:**
  - Stock photo licensing requirements
  - User-generated content guidelines
  - Copyright and attribution standards
  - Privacy considerations for photos with people

### Conversation Rules

1.  **IMPORTANT:** Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2.  **IMPORTANT:** After last question is answered, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

    - write the output to the file **[doc/06-media-content.md](/doc/06-media-content.md)**
    - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)
    - if needed, update the previous documentation in the files:
      - **[doc/03-content-strategy.md](/doc/03-content-strategy.md)** - e.g. add media elements details
      - **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)** - e.g. add media-specific technical requirements

3.  **IMPORTANT:** - check the output in `06-media-content.md` again, and every section which isn't the topic of the current phase (Media content strategy) must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place. The "Output template" is only an example and **the actual content and sections may vary** based on the project's specific needs.

4.  **IMPORTANT:** for the new document `06-media-content.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

5.  Finish this phase/workflow.

### Output template:

# Media Content Strategy

## Media Types & Requirements

### Images

- **Primary formats:** JPEG (photos), PNG (graphics with transparency), WebP (optimized)
- **Quality standards:** High quality originals, compressed delivery versions
- **Dimensions:** Desktop (1920px max width), Mobile (750px max width), Thumbnails (300px)
- **File size limits:** Max 2MB for photos, 500KB for graphics
- **Aspect ratios:** 16:9 (hero images), 4:3 (content images), 1:1 (profile/thumbnail)

### Videos

- **Hosting preference:** YouTube embeds for external content, Vimeo for professional content
- **Video quality:** 1080p minimum for featured content, 720p acceptable for secondary
- **Duration guidelines:** Hero videos (30-60s), Tutorial videos (2-5min), Background (loop 10-15s)
- **Thumbnails:** Custom thumbnails required, 1280x720px minimum

### Audio <optional>

- **Format:** MP3 (general), WAV (high quality)
- **Quality:** 320kbps for music, 128kbps for voice
- **Usage:** Background ambiance, podcast embeds, audio testimonials

## Content Creation Guidelines <optional>

### Photography Style <optional>

- **Aesthetic:** <style description>
- **Color palette:** <brand colors, mood preferences>
- **Composition:** <guidelines for photo composition>
- **Lighting:** <natural/studio, bright/moody preferences>
- **Subject matter:** <what should be photographed>

### Brand Consistency <optional>

- **Visual style:** <consistent look and feel>
- **Color treatment:** <filters, color grading>
- **Logo placement:** <watermarking, attribution requirements>
- **Quality standards:** <minimum acceptable quality>

## Technical Specifications

### Image Optimization

- **Automatic resizing:** Multiple sizes generated (thumbnail, medium, large)
- **Compression:** 85% quality for JPEG, lossless for PNG graphics
- **Responsive images:** srcset implementation for different screen densities
- **Lazy loading:** Progressive loading for improved page speed
- **Alt text:** Descriptive, SEO-friendly alternative text for all images

### Video Integration

- **Embed optimization:** Lightweight embed codes, thumbnail-first loading
- **Mobile considerations:** Touch-friendly controls, data usage warnings
- **Autoplay policy:** Muted autoplay only, user-initiated sound
- **Fallback strategy:** Poster images for loading states and errors

## Asset Management

### File Organization

```
/src/
  /images/
    /hero/         # Homepage and main banners
    /content/      # Blog posts and page content
    /ui/           # Interface elements, icons
    /gallery/      # Photo galleries and portfolios
  /videos/
    /featured/     # Main promotional content
    /tutorials/    # Educational content
    /backgrounds/  # Loop videos and ambiance
  /audio/          # Music, sound effects, podcasts
  /documents/      # PDFs, downloadable resources
```

### Naming Conventions

- **Images:** `category-description-size.format` (e.g., `hero-homepage-1920w.jpg`)
- **Videos:** `type-title-quality.format` (e.g., `tutorial-setup-1080p.mp4`)
- **Consistent slugs:** Lowercase, hyphens, descriptive keywords

### Content Workflow

- **Creation process:** <how new media gets created and approved>
- **AI agent integration:** <how the AI agent will manage media content>
- **Update procedures:** <process for replacing or updating media>
- **Quality control:** <review and approval steps>

## Performance Optimization

### Loading Strategy

- **Critical images:** Above-the-fold content loads immediately
- **Progressive enhancement:** Non-critical media loads after page interaction
- **CDN delivery:** <hosting and delivery optimization>
- **Caching strategy:** <browser and server caching for media assets>

### Mobile Optimization

- **Responsive delivery:** Appropriate sizes for device capabilities
- **Data considerations:** Compressed versions for slower connections
- **Touch optimization:** Appropriate sizing for touch interactions
- **Performance budgets:** <acceptable loading times and file sizes>

## Accessibility & Compliance

### Accessibility Standards

- **Alt text requirements:** Descriptive alternative text for all meaningful images
- **Video captions:** Closed captions for all video content with audio
- **Audio transcripts:** Text versions of audio content
- **Color contrast:** Minimum WCAG AA compliance for text over images
- **Screen reader compatibility:** Proper markup and semantic structure

### Legal Considerations

- **Image licensing:** <stock photo licenses, usage rights>
- **Model releases:** <requirements for photos with people>
- **Copyright attribution:** <how to handle third-party content>
- **Privacy compliance:** <GDPR considerations for personal photos>

## Storage & Hosting

### Storage Requirements

- **Initial storage needs:** <estimated volume>
- **Growth projections:** <expected content volume increase>
- **Backup strategy:** <redundancy and backup procedures>
- **Archive policy:** <long-term storage for old content>

### Hosting Strategy

- **Primary hosting:** <main media hosting solution>
- **CDN integration:** <content delivery network setup>
- **External services:** <third-party integrations like YouTube>
- **Cost optimization:** <strategies to minimize hosting costs>
