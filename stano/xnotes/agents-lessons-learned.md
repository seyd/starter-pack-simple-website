# Agents Lessons Learned: Agentic Workflow Development

_Key insights from building discovery conversation workflows_

---

## 1. TECHNICAL SETUP & ENVIRONMENT

### **Lesson: Agents Can't Verify Their Own Configuration**

**What we learned**: Agents have no tools to check or modify their own operating environment (model type, thinking mode, etc.), but optimal performance depends on specific configurations.

**What we had to change**:

- Added explicit user verification step in session startup
- Required agents to explain why specific configurations matter
- Built in assumption that setup might be suboptimal and agent should adapt

**Key insight**: Don't assume optimal technical setup—design workflows that degrade gracefully and include user-driven verification steps.

---

## 2. CONVERSATION NATURALNESS

### **Lesson: Internal Process Language Leaks Into User Experience**

**What we learned**: Technical terms like "Batch A," "Batch B," "Part 1," "Part 2" were appearing in user-facing conversations, making interactions feel robotic and procedural.

**What we had to change**:

- Explicit instruction to never mention internal process terms to users
- Redesigned internal structure to be more natural ("questions" vs "batches")
- Added guideline to "keep conversation natural"

**Key insight**: Internal workflow terminology must be completely separated from user-facing language. Users should never feel like they're interacting with a process—it should feel like talking to a knowledgeable person.

---

## 3. INFORMATION FLOW & PHASE MANAGEMENT

### **Lesson: Users Don't Follow Phase Boundaries**

**What we learned**: In Phase 1, users naturally provide information meant for later phases (persona details, competitive insights, brand voice preferences), but our initial approach was too rigid to handle this gracefully.

**What we had to change**:

- Added "spillover handling" to capture early information in context repository
- Prevented pre-filling of later phase documents
- Designed context repository as "overflow bucket" for valuable but out-of-phase information

**Key insight**: Human conversation doesn't follow artificial boundaries. Design workflows that capture valuable information whenever it appears, not just when you're "supposed to" gather it.

---

## 4. FOLLOW-UP QUESTION STRATEGY

### **Lesson: Depth vs. Breadth Balance is Critical**

**What we learned**: Agents were naturally drilling deep into topics with multiple follow-up questions, making users feel like they were "doing work they hoped to avoid." This created fatigue and resistance.

**What we had to change**:

- Explicit "breadth over depth" guidance
- Instruction to accept brief answers and move to new ground
- Focus on "covering new areas" rather than "getting complete answers"
- Added warning against overwhelming users

**Key insight**: In discovery conversations, covering more ground is usually better than getting perfect detail on fewer topics. Users want to feel heard and understood, not interrogated.

---

## 5. CONTEXT REPOSITORY DESIGN

### **Lesson: Repository vs. Focused Documents Requires Clear Boundaries**

**What we learned**: Initial approach led to duplication between context repository and focused documents, creating confusion about what goes where.

**What we had to change**:

- Clear rule: repository only for valuable context that doesn't fit in focused documents
- "Never duplicate" principle
- Repository as "overflow bucket" concept
- Quality check question: "Is this already captured elsewhere?"

**Key insight**: In multi-document systems, each document needs a clear, non-overlapping purpose. Duplication creates maintenance burden and confusion about "source of truth."

---

## 6. USER CONTROL & AUTONOMY

### **Lesson: Users Need Explicit Control Mechanisms**

**What we learned**: Users felt rushed through phases and wanted ability to skip, extend, or redirect the conversation.

**What we had to change**:

- Added explicit control commands: **skip**, **next**, **done**, **finish**
- Required waiting for explicit confirmation before advancing phases
- Built in option to skip entire phases

**Key insight**: Agentic workflows must preserve user autonomy. Users should feel in control of the pace and direction, not swept along by the agent's process.

---

## 7. MESSAGE BUDGET MANAGEMENT

### **Lesson: Rigid Budget Allocation Can Waste Opportunities**

**What we learned**: Fixed message limits per phase sometimes meant advancing before valuable context was fully explored, while other phases finished early with budget unused.

**What we had to change**:

- Instruction to "use full message budget" before advancing
- Guidance to prioritize valuable unexplored context over strict adherence to limits
- Built in user control to advance early if desired

**Key insight**: Budget constraints should optimize for value extraction, not rigid adherence to arbitrary limits. Better to extract maximum value from willing participants than to rush through predetermined steps.

---

## 8. QUESTION CRAFTING & PERSONALIZATION

### **Lesson: Generic Question Pools Lead to Generic Conversations**

**What we learned**: Using question pools as checklists rather than inspiration led to impersonal, survey-like interactions.

**What we had to change**:

- Emphasized question pools as "inspiration, not requirements"
- Added instruction to "craft questions specifically for this maker's situation"
- Required using accumulated context to avoid redundancy and build on existing knowledge

**Key insight**: Every conversation should feel unique and personalized. Question pools should inspire creativity, not replace it.

---

## 9. COMPETITIVE LANDSCAPE ASSUMPTIONS

### **Lesson: "No Competition" Claims Need Special Handling**

**What we learned**: Many users initially claim they have "no competition," but this usually means they haven't thought about alternatives and substitutes.

**What we had to change**:

- Special nudge: "How do people solve the problem today, even imperfectly?"
- Reframing from "competitors" to "alternatives, work-arounds, substitutes"
- Persistent but gentle probing when users claim uniqueness

**Key insight**: Users often have blind spots about their competitive landscape. Gentle reframing helps them see alternatives they hadn't considered.

---

## 10. OVERALL WORKFLOW PHILOSOPHY

### **Meta-Lesson: Rigid Process vs. Natural Conversation**

**What we learned**: Our initial approach was too process-driven and not enough conversation-driven. Users could feel the "workflow" underneath the interaction.

**What we had to change**:

- Shifted from "executing a process" to "having a structured conversation"
- Removed visible process mechanics from user experience
- Prioritized natural flow over procedural completeness

**Key insight**: The best agentic workflows feel like expert human conversations that happen to be systematic, not like automated processes that happen to involve a human.

---

## DESIGN PRINCIPLES EMERGED

1. **Graceful Degradation**: Design for suboptimal conditions and environments
2. **Invisible Structure**: Users should benefit from structure without feeling constrained by it
3. **Context Capture**: Always capture valuable information when it appears, regardless of "phase"
4. **User Autonomy**: Preserve user control over pace, direction, and depth
5. **Natural Flow**: Prioritize conversation quality over process adherence
6. **Breadth Strategy**: Cover more ground rather than perfect any single area
7. **Value Extraction**: Use available time/budget to maximum advantage
8. **Personalization**: Every interaction should feel unique and contextual
