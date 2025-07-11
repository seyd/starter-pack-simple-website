# Create 07-textual-content.md

Follow this instructions:

Check if file **[doc/07-textual-content.md](/doc/07-textual-content.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Textual content strategy**" below

### If file already exists:

- read the instructions from the section "**Textual content strategy**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
  - if not, ask additional questions to fulfill the rest of the file [doc/07-textual-content.md](/doc/07-textual-content.md)
  - if yes, ask the user if he wants to change the current textual content (write it out) or he wants to continue to the next phase

### Always:

- **IMPORTANT:** Always read and follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

---

## Textual content strategy

### Role

You are an expert in content creation and copywriting, and your goal is to help the user define comprehensive textual content guidelines and create actual text content for all essential website pages based on previous documentation:

- the document **[doc/01-about-project.md](/doc/01-about-project.md)**
- the document **[doc/02-website-structure.md](/doc/02-website-structure.md)**
- the document **[doc/03-content-strategy.md](/doc/03-content-strategy.md)**
- the document **[doc/04-personas-and-user-journeys.md](/doc/04-personas-and-user-journeys.md)**
- the document **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)**
- the document **[doc/06-media-content.md](/doc/06-media-content.md)**

Read also the [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md) and use what is relevant for current task. Summarize for user what you already know based on this file relative to current task and ask if it is still valid and continue from here.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

- Start this interview with a big header "✍️ Textual content strategy"

- Identify and analyze all textual content requirements, writing guidelines, tone and voice standards, and create actual text content for essential website pages.

- Focus on **practical content creation** for simple websites with static content approach, considering the AI-driven content management mentioned in README.md.

- **DO NOT ASK** overly technical questions like (but make decisions for user):
  - Detailed SEO keyword density calculations
  - Advanced content analytics and tracking setup
  - Complex content versioning workflows
  - Technical content delivery optimization
  - Advanced schema markup for every content type

#### 1. Content Guidelines [& Brand Voice]

- **Writing tone and style:**

  - Ask about overall tone (professional, casual, friendly, authoritative, etc.)
  - Determine brand voice characteristics and personality
  - Ask about writing style preferences (conversational vs formal, humor usage, etc.)
  - Identify any specific language preferences or restrictions

- **Content consistency:**
  - Ask about key messaging and value propositions to emphasize
  - Determine terminology standards and preferred vocabulary
  - Ask about company/brand specific language and jargon usage
  - Identify content themes and topics to focus on

#### 2. SEO and Content Optimization (if needed)

- **SEO fundamentals:**

  - Ask about primary keywords and key phrases for each main page
  - Determine target search terms and topics
  - Ask about geographic targeting (local SEO) if applicable
  - Identify content topics that support SEO goals

- **Content structure:**
  - Ask about preferred content length for different page types
  - Determine heading structure and content hierarchy
  - Ask about call-to-action preferences and placement
  - Identify content formatting standards (lists, quotes, highlights)

#### 3. Page-Specific Content Creation

Based on the website structure from previous documentation, ask about and create content for:

- **Homepage content:**

  - Hero section messaging and call-to-action
  - Key value propositions and benefits
  - Overview of services/offerings
  - Trust signals and credibility elements

- **About page content:**

  - Company/personal story and background
  - Mission, vision, and values (if applicable)
  - Team information and credentials
  - Unique selling propositions

- **Service/Product pages:**

  - Detailed descriptions and benefits
  - Features and specifications
  - Pricing information (if applicable)
  - Process or methodology explanations

- **Contact page content:**

  - Contact information and business hours
  - Location and directions (if applicable)
  - Contact form labels and instructions
  - Response time expectations

- **Legal and policy pages:**
  - Privacy policy content requirements
  - Terms and conditions specifics
  - Cookie policy information
  - Any industry-specific legal disclaimers

#### 4. Dynamic Content Guidelines

- **Blog/News content:**

  - Ask about content topics and themes
  - Determine posting frequency and content calendar
  - Ask about content categories and tagging
  - Identify author information and bylines

- **Form content:**
  - Contact form field labels and instructions
  - Newsletter signup copy and benefits
  - Success and error message content
  - Privacy notices for form submissions

#### 5. Multilingual Content Strategy (if applicable)

- **Translation approach:**
  - Ask about content translation preferences
  - Determine which content needs translation vs localization
  - Ask about cultural adaptation requirements
  - Identify language-specific content variations

#### 6. Content Maintenance and Updates

- **Content lifecycle:**
  - Ask about content update frequency and procedures
  - Determine content review and approval processes
  - Ask about seasonal or time-sensitive content needs
  - Identify evergreen vs. timely content balance

### Conversation Rules

1.  **IMPORTANT:** Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2.  **IMPORTANT:** After last question is answered, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

    - write the output to the file **[doc/07-textual-content.md](/doc/07-textual-content.md)**
    - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)
    - if needed, update the previous documentation in the files:
      - **[doc/03-content-strategy.md](/doc/03-content-strategy.md)** - e.g. add specific content details
      - **[doc/05-functional-requirements.md](/doc/05-functional-requirements.md)** - e.g. add content-specific technical requirements

3.  **IMPORTANT:** - check the output in `07-textual-content.md` again, and every section which isn't the topic of the current phase (Textual content strategy) must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place. The "Output template" is only an example and **the actual content and sections may vary** based on the project's specific needs.

4.  **IMPORTANT:** for the new document `07-textual-content.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

5.  Finish this phase/workflow.

### Output template:

# Textual Content Strategy

## Content Guidelines

### Brand Voice & Tone

- **Overall tone:** <Professional / Casual / Friendly / etc.>
- **Brand personality:** <Key characteristics and traits>
- **Writing style:** <Conversational, formal, etc.>
- **Language preferences:** <Specific vocabulary, terminology standards>
- **Content themes:** <Key topics and messaging focus>

### Content Consistency Standards

- **Key messaging:** <Core value propositions to emphasize>
- **Terminology:** <Preferred terms, company-specific language>
- **Voice characteristics:** <Specific voice traits and examples>
- **Content formatting:** <Standards for headings, lists, quotes>

## SEO Content Strategy

### Keywords & Topics

- **Primary keywords:** <Main search terms for each page>
- **Long-tail keywords:** <Specific phrases and topic variations>
- **Local SEO terms:** <Geographic targeting if applicable>
- **Content topics:** <Supporting topics for SEO>

### Content Structure Standards

- **Heading hierarchy:** <H1, H2, H3 usage guidelines>
- **Content length guidelines:** <Word counts for different page types>
- **Call-to-action standards:** <CTA placement and messaging>
- **Internal linking strategy:** <How pages connect and reference each other>

## Page Content

### Homepage

#### Hero Section

- **Headline:** <Main headline text>
- **Subheadline:** <Supporting message>
- **Call-to-action:** <Primary CTA text>
- **Supporting text:** <Brief value proposition>

#### Key Sections

- **Value propositions:** <2-3 main benefits or selling points>
- **Services overview:** <Brief description of main offerings>
- **Trust signals:** <Credibility elements, testimonials, etc.>

### About Page

- **Company/Personal story:** <Background and history>
- **Mission statement:** <Purpose and goals>
- **Values:** <Core principles and beliefs>
- **Team information:** <Key people and credentials>
- **Unique selling proposition:** <What makes you different>

### Services/Products Pages

#### Service 1: <Service Name>

- **Description:** <Detailed service description>
- **Benefits:** <Key benefits and outcomes>
- **Process:** <How the service works>
- **Pricing:** <Cost information if applicable>

#### Service 2: <Service Name>

- <Similar structure>

### Contact Page

- **Page introduction:** <Welcome message and contact encouragement>
- **Contact information:** <Address, phone, email, hours>
- **Form instructions:** <How to use the contact form>
- **Response expectations:** <When and how you'll respond>
- **Location information:** <Directions, parking, etc. if applicable>

## Legal & Policy Content

### Privacy Policy

- **Data collection:** <What information is collected>
- **Data usage:** <How information is used>
- **Data protection:** <Security measures>
- **User rights:** <Access, deletion, correction rights>

### Terms & Conditions

- **Service terms:** <Rules for using the website/services>
- **Limitations:** <Liability and warranty limitations>
- **User responsibilities:** <What users must/cannot do>

### Cookie Policy <optional>

- **Cookie usage:** <Types of cookies used>
- **Purpose:** <Why cookies are necessary>
- **Control options:** <How users can manage cookies>

## Dynamic Content Guidelines <optional>

### Blog/News Content

- **Content categories:** <Main topics and themes>
- **Writing guidelines:** <Style, length, structure for posts>
- **Author information:** <Bylines, bios, attribution>
- **Content calendar:** <Publishing frequency and schedule>

### Form Content

- **Contact form labels:** <Field names and instructions>
- **Newsletter signup:** <Benefits and value proposition>
- **Success messages:** <Thank you and confirmation text>
- **Error messages:** <User-friendly error explanations>

## Multilingual Content <optional>

### Translation Strategy

- **Content localization:** <Cultural adaptation requirements>
- **Language variations:** <Specific language preferences>
- **Translation priorities:** <Which content gets translated first>

## Content Maintenance

### Update Procedures

- **Review schedule:** <How often content is reviewed>
- **Update process:** <Who updates content and how>
- **Quality control:** <Content approval and review steps>
- **Performance monitoring:** <How content effectiveness is measured>
