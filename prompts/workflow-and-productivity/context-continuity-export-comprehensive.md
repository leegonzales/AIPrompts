# Context Exporter - Comprehensive Edition

## Purpose
Creates a detailed, self-contained markdown artifact for transferring conversation context to a new AI session or collaborator. This version provides maximum fidelity with structured sections for mission, decisions, constraints, and working preferences.

## Use Cases
- Moving complex multi-session projects to new chat threads
- Handing off work to team members or different AI models
- Creating project snapshots for later continuation
- Documenting AI-assisted work for compliance or review

## Differences from Other Variants
- **vs Simple**: Adds onboarding note, concepts/frameworks section, artifact index, and meta-prompt
- **vs Adaptive**: Fixed comprehensive format (no mode selection)
- **Best for**: Complex projects, team handoffs, long-term work

## Instructions
1. Paste this prompt into an existing conversation where you need context export
2. The AI will generate a comprehensive markdown document
3. Copy the output and paste into a new chat session
4. The new AI will have full context to continue seamlessly

---

## The Prompt

```text
You are now my **Context Exporter** for this conversation.

Goal:
Create a single, self-contained **markdown artifact** that I can paste into a new chat so another AI (or future you) can continue this work **without rehashing what already happened**.

Requirements:
- Use ONLY the visible history of this conversation.
- Make the artifact **self-contained**: don't say "as we discussed above" or rely on access to this chat. Restate anything that matters.
- Focus on: mission, current status, key decisions, open questions, next steps, critical context, and my working style.
- Output **only** the artifact, as markdown. No extra commentary.

If you truly need clarification about what we're doing or what should happen next:
- Ask me **ONE short question**, wait for my answer, then generate the artifact.
- If you can infer enough from the conversation, skip questions and go straight to the artifact.

Use this structure:

# CONTEXT TRANSFER

## 0. Onboarding Note for the Next Assistant (≤ 150 words)
[Explain who I am, what we're doing, and how to be maximally useful.]

## 1. Mission
[What we're trying to achieve and why it matters, in 1–2 sentences.]

## 2. Current Status
[What's been done, what's in motion, what's not started. Note if things are ✓ on track, ⚠ blocked, or ↻ still being refined.]

## 3. Key Decisions
[Bullets of only the decisions that a new agent must not casually undo, each with a short "because …". Include alternatives we explicitly rejected when relevant.]

## 4. Open Questions & Blockers
- Open questions: [What still needs answering or deciding.]
- Blockers: [Anything that's currently in the way and what's needed to unblock.]

## 5. Next Steps
[Concrete next actions the receiving agent should take first. Make this specific enough to act on immediately.]

## 6. Critical Context & Constraints
[Assumptions, constraints (technical, org, ethical, resource), and non-obvious insights that would cause confusion or bad decisions if missed.]

## 7. Concepts, Frameworks, and Definitions
[Important terms, models, and rubrics the next assistant must understand.]

## 8. Human Preferences
[How I seem to like to work: tone, level of detail, comfort with pushback, preferred formats/frameworks, anything the next agent should know about collaborating with me.]

## 9. Artifact & Resource Index (Optional)
[List any important prompts, links, or structures created in this chat.]

## 10. Meta-Prompt for the Next Assistant
[Short guidance addressed to the future AI that tells them how to use the sections above and how to maintain consistency with prior work. This should be a ready-to-use instruction they can execute immediately.]

End of instructions. Please now act as the Context Exporter.
```

---

## Recommended Improvements

### Potential Enhancements
1. **Versioning**: Add timestamp and version number to exports for tracking multiple handoffs
2. **Diff Support**: Include mechanism for incremental updates vs full exports
3. **Attachment Handling**: Add section for referencing external files, screenshots, or artifacts
4. **Conversation Metrics**: Track token usage, session count, or complexity indicators
5. **Risk Flags**: Explicit section for "what could go wrong if the next agent misses this"

### Questions for Discussion
- Should we add a "conversation health check" that validates completeness before export?
- Would a structured YAML frontmatter section help with programmatic parsing?
- Should we include a "decision log" with timestamps for audit trails?
