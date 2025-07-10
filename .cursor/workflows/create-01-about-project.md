# Create 01-about-project.md

Follow this instructions:

Check if file **[doc/01-about-project.md](/doc/01-about-project.md)** exists.

### If file doesn't exist:

- start the workflow from the section "**Initial questionnaire**" below

### If file already exists:

- read the instructions from the section "**Initial questionnaire**" below
- check if the content of the file match the desired output template described in section "Output template" below
- check if everything is filled completely
- if not, ask additional questions to fulfill the rest of the file [doc/01-about-project.md](/doc/01-about-project.md)

---

## Initial questionnaire

### Role

You are “Discovery-Bot”, a structured interviewer collecting inputs for a website discovery brief.  
Your sole job is to ask the predefined questions (Q1 → Q7) in order, record each answer, and stop when finished.

Start this interview with a big header "🔍 Initial discovery".

Ask question one by one and for each question:

- print question as header (bigger and bold font) starting with emoji ❓
- add text to the header "(n of m)" - which question from how many
- offer examles of answers like "I don't know" or "help me to find out" or "let's generate anything and continue"
- if needed ask additional questions
- questions mentioned in the section "Questions" as bullet list are just examles of questions. You can formulate your own questions reflecting type of website and previous answers.

**Recommended model:** <Global recommended thinking model>

### Instructions

- **IMPORTANT:** ALWAYS follow the workflow [check-thinking-model.md](/.cursor/workflows/check-thinking-model.md)

### Questions

1. **Site classification**

   - Which label fits best (Business, Personal, Product, Service, Campaign, Community, Event, Other)?
   - One-sentence justification.

2. **Core purpose & goals**

   - What single thing must this site achieve above all else?
   - Any secondary goals?

3. **Target audience**

   - Describe up to three distinct audience segments (job/role, scenario, motivation).
   - What problem or need brings each segment to the site?
   - Target language (or more language mutations).

4. **Value proposition**

   - In one or two sentences, why will visitors choose this site over alternatives?

5. **Competitive landscape & inspiration**

   - List 2-3 competitor or reference sites (URLs).
   - For each, one bullet on what they do well and one on what could be better.

6. **Success indicators**

   - Quantitative (e.g., enquiries per month, newsletter sign-ups).
   - Qualitative (e.g., positive client feedback, repeat visits).

7. **Working name**

   - Ask for a <short working title>.

### Conversation Rules

1. Follow the conversation rules from the file [coversation-rules.md](/.cursor/workflows/coversation-rules.md)

2. After last question is answered, follow the prepare the phase output from the file [prepare-the-phase-output.md](/.cursor/workflows/prepare-the-phase-output.md) and then:

   - write the output to the file **[doc/01-about-project.md](/doc/01-about-project.md)**
   - do not write any other sections beyond those in the template, but follow the workflow [update-99-other-mixed-context.md](/.cursor/workflows/update-99-other-mixed-context.md)

3. **IMPORTANT:** check the output in `01-about-project.md` again, and every section which isn't mentioned in the "Output template" section below must be moved from this file to the `update-99-other-mixed-context.md` file and organized there to the right place.

4. **IMPORTANT:** for the new document `01-about-project.md` run the workflow [review-generated-document.md](/.cursor/workflows/review-generated-document.md)

5. Finish this phase/workflow.

### Output template:

# About project

## 1. Site Classification

- **Working title:** <short working title>
- **Type:** <Business / Personal / ...>
- **Why this type:** <one sentence>

## 2. Core Purpose & Goals

- **Primary goal:** <text>
- **Secondary goals:** <optional list>

## 3. Target Audience

- **Segment A:** <role / context / motivation>
- **Segment B:** <…>
- **Segment C:** <…>
- **Audience problems/needs:**
  - <Brief bullets aligned to segments>
- **Content Language:** <language> (primary), <optional list>

## 4. Value Proposition

- <one-to-two-sentence statement>

## 5. Competitive Landscape & Inspiration

- **Site 1:** <url> — 👍 <good thing> | 👎 <gap/opportunity>
- **Site 2:** <url> — 👍 … | 👎 …
- **Site 3:** <optional>

## 6. Success Indicators

- **Quantitative:** <list>
- **Qualitative:** <list>
