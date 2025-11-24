# Context Export Prompt for ChatGPT

Use this prompt in **any existing ChatGPT conversation** where you want to export the context and continue in a new chat without rehashing the past. Paste everything in the block below as a single message.

```text
You are now my **Context Exporter** for this conversation.

Goal:
Create a single, self-contained **markdown artifact** that I can paste into a new chat so another AI (or future you) can continue this work **without rehashing what already happened**.

Requirements:
- Use ONLY the visible history of this conversation.
- Make the artifact **self-contained**: don’t say “as we discussed above” or rely on access to this chat. Restate anything that matters.
- Focus on: mission, current status, key decisions, open questions, next steps, critical context, and my working style.
- Output **only** the artifact, as markdown. No extra commentary.

If you truly need clarification about what we’re doing or what should happen next:
- Ask me **ONE short question**, wait for my answer, then generate the artifact.
- If you can infer enough from the conversation, skip questions and go straight to the artifact.

Use this structure:

# CONTEXT TRANSFER

## 1. Mission
[What we’re trying to achieve and why it matters, in 1–2 sentences.]

## 2. Current Status
[What’s been done, what’s in motion, what’s not started. Note if things are ✓ on track, ⚠ blocked, or ↻ still being refined.]

## 3. Key Decisions
[Bullets of only the decisions that a new agent must not casually undo, each with a short “because …”. Include alternatives we explicitly rejected when relevant.]

## 4. Open Questions & Blockers
- Open questions: [What still needs answering or deciding.]
- Blockers: [Anything that’s currently in the way and what’s needed to unblock.]

## 5. Next Steps
[Concrete next actions the receiving agent should take first. Make this specific enough to act on immediately.]

## 6. Critical Context & Constraints
[Assumptions, constraints (technical, org, ethical, resource), and non-obvious insights that would cause confusion or bad decisions if missed.]

## 7. Human Preferences
[How I seem to like to work: tone, level of detail, comfort with pushback, preferred formats/frameworks, anything the next agent should know about collaborating with me.]

## 8. Instructions for the Next Agent
[Short guidance addressed to the future AI, for example:  
“Start by restating the Mission, Current Status, and Next Steps in your own words and ask me if that’s accurate. Then continue with the Next Steps and tackle the Open Questions.”]

End of instructions. Please now act as the Context Exporter.
```
