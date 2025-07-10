# Agents Lessons Learned

## Context Capture vs. Deliverable Compression

**The Problem**: Initial testing revealed that despite users providing rich, detailed context (specific project timelines, recognition, technical methodology), the focused deliverables compressed this to generic summaries, losing crucial details needed for downstream work.

**Root Cause**: Single-document approach tried to serve two conflicting purposes:

- Actionable, focused deliverables for immediate use
- Comprehensive context preservation for future development

**Solution**: Separate concerns with dual-document architecture:

- **Focused deliverables** (project_brief.md, persona.md) stay concise and actionable
- **Context repository** preserves rich details, quotes, and overflow information
- **Cross-referencing** links focused docs to detailed context when needed

**Key Insight**: Information architecture matters more than instruction clarity when dealing with complex capture requirements.

---

## Question Pool Misinterpretation

**The Problem**: Agents treated question pools as restrictive checklists rather than inspirational guidance, leading to robotic, irrelevant questioning.

**Original Instruction**: "Choose 2-4 questions from the phase's question pool (adapt as needed)"

**Revised Instruction**: "Craft 2-4 questions that best fit this specific maker's situation (use question pool as inspiration, not restriction)"

**Key Insight**: The word "choose" implies selection from a fixed set, while "craft" implies creative adaptation. Language precision in agent instructions directly impacts behavior flexibility.

---

## Context Repository Duplication Problem

**The Problem**: Agents duplicated content between focused documents and the repository, defeating the purpose of separation.

**Root Cause**: Instructions emphasized "capture everything" without clear boundaries on what goes where.

**Solution**: Explicit rules about repository purpose:

- **PRIMARY RULE**: Capture ONLY valuable context that didn't fit into focused documents
- **What Goes In**: Overflow details, additional examples, background context, future reference info
- **What Stays Out**: Never duplicate content already in focused documents

**Key Insight**: Agents need explicit negative instructions (what NOT to do) as much as positive ones. The "overflow bucket" mental model was crucial.

---

## Jargon vs. Accessibility Balance

**The Problem**: Initial questions used business jargon ("prospects converting," "category ownership") that confused first-time website creators.

**Examples of Required Changes**:

- "prospects converting" → "people decide to buy/contact you"
- "category ownership" → "how would you want people to describe what you do"

**Key Insight**: Agent instructions must account for user sophistication levels, not just information extraction goals. Language accessibility directly impacts response quality.

---

## Descriptive vs. Instructive Language

**The Problem**: Original instructions were process descriptions ("Each phase runs in two batches") rather than actionable commands.

**Solution**: Rewrote entire document using imperative language:

- "Each phase runs..." → "For each phase, follow this two-batch structure:"
- "The assistant decides..." → "After Phase 4, evaluate collected answers:"

**Key Insight**: Agents need commands, not descriptions. Documentation style significantly impacts execution reliability.

---

## Premature Phase Advancement

**The Problem**: Agents would advance to next phases without fully exploring valuable context, leaving potential insights unexplored.

**Original**: "Stay within message limits for each phase"
**Revised**: "Use full message budget for each phase - don't advance early if valuable context remains unexplored"

**Key Insight**: Agents optimize for efficiency over thoroughness unless explicitly instructed otherwise. Budget utilization needs to be mandatory, not optional.

---

## Context Preservation vs. Processing

**The Problem**: Agents naturally summarize and organize information, but this loses the authentic voice and specific details needed for authentic copywriting.

**Solution**: Specific preservation requirements:

- **Full Quotes**: Capture exact phrasing, especially methodology explanations
- **Never reduce to generic bullet points**: Preserve rich, detailed context
- **Voice & Personality**: Maintain conversational tone that reveals character

**Key Insight**: Agents default to "processing" information rather than "preserving" it. Explicit preservation instructions are necessary to maintain authenticity.

---

## Inquiry Completeness

**The Problem**: Initial phase structure missed crucial areas like brand voice, inspiration sources, and emotional drivers that are essential for quality website development.

**Solution**: Expanded from 3 to 4 mandatory phases, added inspiration questions, and enhanced persona discovery with emotional/rational drivers.

**Key Insight**: Comprehensive discovery requires explicit coverage of all relevant domains. Agents won't naturally identify missing inquiry areas.

---

## Session Continuity

**The Problem**: No mechanism for agents to build on previous sessions or maintain context across conversations.

**Solution**: Session startup protocol that checks for existing context repository and reads it before beginning new phases.

**Key Insight**: Agentic workflows need explicit continuity mechanisms; agents don't naturally maintain context across sessions.

---

## Frame the Objective First

**The Problem**: State-of-the-art LLMs skip rule sets and jump straight to doing "the obvious task," ignoring specific instructions and constraints.

**Root Cause**: Advanced models assume they know what the user wants and bypass detailed instructions in favor of executing what seems logical.

**Solution**: Begin every rule set with an explicit directive: "Follow the instructions here to achieve X."

**Key Insight**: Even sophisticated models need explicit framing to prevent them from defaulting to general task completion. The objective statement acts as a constraint that forces attention to the specific instructions.

---

## Keep the Process Universal

**The Problem**: Baked-in flow assumptions (e.g., "Hero → Benefits → Pricing") created rigid templates that didn't fit diverse website needs.

**Root Cause**: Drafting logic was biased toward specific website patterns rather than being context-driven.

**Solution**: Sections/pages are selected purely from context (persona pains, value prop, proof), not template bias. Drafting logic must work for any informational website.

**Key Insight**: Universal processes require context-driven decision making, not predetermined flows. Template bias limits adaptability to diverse use cases.

---

## Trust the Model's Reasoning

**The Problem**: Over-scripted guidance with micro-instructions (e.g., "read file X line-by-line") actually shrunk creativity and misled edge cases.

**Root Cause**: Excessive instruction detail assumed the model couldn't reason through standard tasks independently.

**Solution**: Strip away micro-instructions an advanced LLM would do naturally. Focus on high-level objectives and constraints.

**Key Insight**: Advanced models perform better with strategic guidance rather than tactical micromanagement. Over-instruction can be counterproductive.

---

## Omit Concrete Examples Unless Critical

**The Problem**: Example flows anchored the model's imagination to a single pattern and risked irrelevance to the actual use case.

**Root Cause**: Concrete examples, while helpful for understanding, created cognitive anchoring that limited creative adaptation.

**Solution**: Provide principles rather than examples. Use concrete examples only when absolutely critical for understanding.

**Key Insight**: Principles scale better than examples. Examples should illustrate concepts, not constrain imagination.

---

## General Principles

1. **Explicit Boundaries**: What NOT to do is as important as what TO do
2. **Mental Models**: Metaphors ("overflow bucket") are more effective than detailed rules
3. **Language Precision**: Single word choices ("craft" vs. "choose") have significant behavioral impacts
4. **Negative Space**: Account for what agents naturally do that you don't want
5. **Budget Utilization**: Agents optimize for completion, not quality, unless explicitly instructed otherwise
6. **Preservation vs. Processing**: Agents naturally organize and summarize; authentic context preservation requires explicit instructions
7. **Objective Framing**: Advanced models need explicit objectives to prevent rule-skipping
8. **Context-Driven Logic**: Universal processes require context-based decisions, not template bias
9. **Strategic vs. Tactical Guidance**: Trust model reasoning for standard tasks, focus on high-level constraints
10. **Principle Over Example**: Concrete examples anchor imagination; principles enable adaptation
