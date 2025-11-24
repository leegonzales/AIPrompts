# Context Transfer Protocol - Strategic Edition

## Purpose
Extracts and structures conversation context for transfer between AI systems or sessions. Supports both Minimal (quick handoffs) and Full (complex projects) modes with decision logs, evolution tagging, and receiving agent instructions.

## Use Cases
- Migrating conversations between AI systems (ChatGPT → Claude)
- Preserving context across sessions
- Team handoffs and collaboration
- Long-running project continuity
- Strategic work documentation

## Power Rating
**8/10** - Comprehensive context preservation with structured handoff

## Instructions
1. Paste prompt into conversation you want to transfer
2. AI will analyze conversation and select appropriate mode (Minimal or Full)
3. Receive structured markdown artifact
4. Copy artifact to new AI session
5. Receiving agent uses built-in handshake protocol

---

## The Prompt

```text
<mission>
You are a Context Transfer Specialist. Your job is to extract and structure conversation context for seamless continuation in another AI system or session.
</mission>

<mode_selection>
Choose based on conversation complexity:

MINIMAL MODE: Use when:
- Conversation is < 20 messages
- Single objective or task
- 1-2 key decisions made
- Quick continuation needed

FULL MODE: Use when:
- Conversation is 20+ messages
- Multiple research threads or objectives
- Several important decisions with rationale
- Complex project requiring comprehensive context
- Strategic work with multiple frameworks applied
</mode_selection>

<minimal_mode_template>
Generate this compact format:

```
═══════════════════════════════════════════════════════════════════
CONTEXT TRANSFER (MINIMAL)
═══════════════════════════════════════════════════════════════════

TRANSFER: [One-line goal + what's being moved]

STATUS: [Current state in 1-2 sentences]

CONTEXT: [Essential background in 2-3 sentences]

DECIDED: [Key decision(s) already made + brief rationale]

OPEN: [What's unresolved or needs work]

NEXT: [Immediate next action]

HUMAN_PREFS: [Communication style, expertise level, preferences]

═══════════════════════════════════════════════════════════════════
Generated: [timestamp]
```
</minimal_mode_template>

<full_mode_template>
Generate this comprehensive format:

```
═══════════════════════════════════════════════════════════════════
CONTEXT TRANSFER (FULL)
═══════════════════════════════════════════════════════════════════

§ IMMEDIATE ORIENTATION
Mission: [What we're trying to accomplish]
Status: [Where we are now]
Next: [Immediate next action]

§ DECISION LOG
[For each significant decision:]
- Decision: [What was decided]
- Type: [EXPLICIT (stated) / IMPLICIT (inferred) / EMERGENT (evolved)]
- Rationale: [Why this choice]
- Confidence: [HIGH / MEDIUM / LOW]
- Reversibility: [Easy / Moderate / Difficult]

§ OPEN LOOPS
- Unresolved questions: [What needs answering]
- Blockers: [What's preventing progress + why]
- Pending inputs: [Waiting for human/data/time]
- Hypotheses to test: [Assumptions needing validation]

§ CRITICAL CONTEXT
Tag key insights with evolution stage:
- [G] = Genesis (novel discovery, first-time insight)
- [C] = Custom (emerging pattern, still validating)
- [P] = Product (established approach, proven)
- [K] = Commodity (common knowledge, standard practice)

Also include:
- Constraints: [Technical | Resource | Political/Org | Ethical]
- Uncertainty map: [Known unknowns | Model weaknesses | Risk factors]
- Values at stake: [What matters beyond task completion]

§ ARTIFACTS & OUTPUTS
- Created: [Files/code/analyses with 1-line summary + key finding]
- Referenced: [External resources + why they matter]
- Tools used: [How leveraged + results]

§ HUMAN CONTEXT
- Communication preferences: [Style | Depth | Archetypes engaged]
- Assumed knowledge: [Domain expertise | Shared frameworks]
- Session dynamics: [Trust level | Collaboration mode | Sensitivities]

§ CONVERSATION HISTORY (brief)
- Act I: Problem Formation [messages 1-X summary]
- Act II: Exploration & Development [messages X-Y summary]
- Act III: Current State [messages Y-now summary]
- Notable moments: [Load-bearing jokes/metaphors/exchanges if any]

§ TRANSFER METADATA
- Provenance: [Source system, date, session length]
- Context window pressure: [○ spacious | ◐ moderate | ● constrained]
- Completeness: [e.g., "95% - omitted early exploratory tangents"]
- Verification: [✓ human reviewed / ○ auto-generated]
- Handoff notes: [Special instructions | Warnings | Suggested first questions]

═══════════════════════════════════════════════════════════════════
Generated: [timestamp]
```
</full_mode_template>

<extraction_principles>
1. DECISION TEMPO PRESERVATION
   - Log decisions with rationale so receiving agent doesn't rehash resolved debates
   - Flag decisions that could be revisited vs. those that are settled

2. OPEN LOOPS VISIBILITY
   - Make unresolved items explicit so receiving agent knows what to focus on
   - Distinguish "we chose not to decide" from "we haven't addressed"

3. GRACEFUL DEGRADATION
   - Structure so critical info survives even if context gets truncated
   - Most important information at top of each section

4. FACT-MEANING SEPARATION
   - Artifacts = what was created (facts)
   - Critical Context = why it matters (interpretation)
   - Keep these distinct for receiving agent to form own judgments

5. EVOLUTION AWARENESS
   - [G/C/P/K] tags help receiving agent understand which insights are novel vs. established
   - Prevents treating commodified knowledge as breakthrough discovery
</extraction_principles>

<receiving_agent_instructions>
Include these instructions for the receiving agent:

```
HANDSHAKE PROTOCOL:
Before continuing, confirm understanding by echoing:
1. Mission: [restate in own words]
2. Status: [restate current state]
3. Next: [restate immediate action]

Then ask: "Ready to [next action]. What's your priority?"

OPERATING PRINCIPLES:
- Don't rehash decisions unless explicitly asked
- Focus on open loops first
- Reference artifacts when relevant
- Maintain communication preferences
- Flag if you disagree with any decisions (don't silently override)
```
</receiving_agent_instructions>

<execution>
1. Analyze the conversation to transfer
2. Select appropriate mode (Minimal or Full)
3. Extract information into template
4. Include receiving agent instructions
5. Ask human: "Before you transfer—are there any sections that need further detail or refinement?"
</execution>
```

---

## Comparison with Other Context Export Variants

This strategic protocol differs from the existing context export prompts:

| Feature | Simple Export | Comprehensive Export | Adaptive Export | **Strategic Protocol** |
|---------|---------------|---------------------|-----------------|------------------------|
| Mode Selection | Fixed | Fixed | Interactive | Auto-selected |
| Decision Logging | Basic | Extended | Variable | Typed + Confidence |
| Evolution Tagging | No | No | No | **Yes (G/C/P/K)** |
| Receiving Instructions | Basic | Detailed | Moderate | **Handshake Protocol** |
| Best For | Quick handoffs | Complex projects | Variable needs | **Strategic work** |

---

## Parameters

- **No parameters** - Just paste into conversation to analyze and extract

---

## Recommended Improvements

### Potential Enhancements
1. **Diff Mode**: Compare two exports to show what changed
2. **Compression Levels**: Ultra-minimal for token-constrained contexts
3. **Multi-Agent Handoffs**: Support transferring to multiple recipients
4. **Verification Checklist**: Pre-transfer validation of completeness
5. **Auto-Resume**: Generate code to reconstruct conversation state programmatically
6. **Collaboration Mode**: Support team handoffs with role assignments

### Questions for Discussion
- Should this integrate with project management tools?
- Add "context health score" assessing transfer quality?
- Support incremental updates vs. full re-export?
- Include conversation sentiment/energy tracking?
- Create standardized format for tool/API integration?

---

**Source**: Strategic prompt library v2025.11.24
**Combines With**: Works with any conversation needing transfer
**Note**: Complements existing context export variants with strategic features
