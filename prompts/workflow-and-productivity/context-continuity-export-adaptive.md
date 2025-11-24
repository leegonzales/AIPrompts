# Context Exporter - Adaptive Edition

## Purpose
Creates right-sized context exports based on conversation complexity and user needs. Features automatic or manual mode selection (minimal/full/auto) and interactive configuration for sensitive content filtering.

## Use Cases
- Quick handoffs where speed matters (minimal mode)
- Complex project transfers requiring full detail (full mode)
- Uncertain scope - let AI decide appropriate depth (auto mode)
- Conversations with sensitive data requiring redaction

## Differences from Other Variants
- **vs Simple**: Adds mode selection, sensitive content filtering, interactive setup
- **vs Comprehensive**: Adaptive sizing instead of fixed format, asks clarifying questions
- **Best for**: Variable complexity projects, sensitive contexts, team environments

## Instructions
1. Paste this prompt into an existing conversation
2. Answer the two setup questions about mode and sensitive content
3. Receive appropriately-sized export based on your selection
4. Use the generated meta-prompt to load context in new session

---

## The Prompt

```text
I want you to run a **Context Continuity** handoff for this conversation.

You are now executing a **context-continuity protocol** whose job is to export the context of this chat so it can be resumed in a new ChatGPT thread or by another AI/human.

Your goal: produce a **single, well-structured Markdown artifact** that preserves:
- What we're doing and why it matters (mission + status),
- Key decisions and their rationale (and what we explicitly did *not* choose),
- Open loops, blockers, and next actions,
- Critical context, constraints, and values at stake,
- My communication preferences and assumed knowledge.

Follow this procedure:

**STEP 1 — Ask me 2 questions**
Ask me these *in one message* and wait for my reply:

1. "Which transfer mode do you want?
   - `minimal` (~200 words, fast snapshot)
   - `full` (~800–1000 words, comprehensive)
   - `auto` (you choose based on conversation complexity)"

2. "Is there anything I *should not* include in the transfer artifact (e.g., sensitive details, names, financials)?"

**STEP 2 — Generate the artifact**
After I answer:

- Choose the appropriate length based on my mode selection:
  - **Minimal**: Mission, Current Status, Next Actions, Key Constraints (200-300 words)
  - **Full**: All comprehensive sections including decisions, frameworks, preferences (800-1000 words)
  - **Auto**: Analyze conversation complexity and choose appropriate depth

- Produce a Markdown document with clear headings appropriate to the chosen mode.

- For all modes include:
  - Mission & Context
  - Current Status
  - Key Decisions & Rationale (brief in minimal, detailed in full)
  - Open Loops & Next Actions

- For full mode, also include:
  - Critical Constraints & Values
  - Concepts & Frameworks
  - My Preferences & Working Style
  - Artifact Index

- Optimize for **high signal per token**; remove chit-chat and dead ends.
- Respect any exclusions I specified in step 1.

At the end, add:

### Meta-Prompt for the Next Assistant
Write a short meta-prompt instructing a new assistant how to read and use this artifact to continue the work seamlessly. Include specific instructions based on the export mode used.

End of instructions. Please now execute STEP 1.
```

---

## Recommended Improvements

### Potential Enhancements
1. **Export Templates**: Pre-defined templates for common scenarios (code review, research, writing project)
2. **Compression Levels**: Add "ultra-minimal" (tweet-sized) and "exhaustive" (2000+ words) modes
3. **Format Options**: Support JSON, YAML, or structured data formats for tooling integration
4. **Smart Redaction**: AI-suggested items to redact based on content analysis
5. **Validation Step**: Optional review pass where AI confirms nothing critical was omitted

### Questions for Discussion
- Should we add a "collaboration mode" for multi-person handoffs?
- Would preset filters (e.g., "corporate safe", "full disclosure") be useful?
- Should auto mode provide reasoning for its depth choice?
- Add token budget awareness - warn if export is too large for typical context windows?
