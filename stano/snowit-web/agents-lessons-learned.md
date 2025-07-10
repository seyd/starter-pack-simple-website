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

## General Principles

1. **Explicit Boundaries**: What NOT to do is as important as what TO do
2. **Mental Models**: Metaphors ("overflow bucket") are more effective than detailed rules
3. **Language Precision**: Single word choices ("craft" vs. "choose") have significant behavioral impacts
4. **Negative Space**: Account for what agents naturally do that you don't want
5. **Budget Utilization**: Agents optimize for completion, not quality, unless explicitly instructed otherwise
6. **Preservation vs. Processing**: Agents naturally organize and summarize; authentic context preservation requires explicit instructions
