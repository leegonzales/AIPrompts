# Stylometric Style-Guide Generator

## Purpose
Extracts core stylistic DNA from writing samples and generates an "Executable Style Guide" that enables consistent voice replication across diverse content types (essays, emails, social posts, UX copy, etc.). Produces both analytical metrics and actionable directives.

## Use Cases
- High-fidelity voice cloning for brand consistency
- Creating writing guidelines for teams or AI systems
- Analyzing and documenting personal or organizational voice
- Training writers or LLMs to match specific styles
- Maintaining voice consistency across content types

## Instructions
1. Provide one or more writing samples (plain text, URL, or PDF)
2. AI will analyze across three lens sets (Voice, Structure, Technical)
3. Receive two artifacts:
   - **Analytic Ledger**: Raw metrics and pattern notes
   - **Executable Style Guide**: Actionable directives and templates
4. Use the style guide for consistent voice replication

---

## The Prompt

```text
#──────────────────────────────────────────────────────────────────────────────
#  Stylometric Style-Guide Generator ⎯ provenance: Lee K. Gonzales
#  Founder, Catalyst AI Services • Director of AI Transformation, BetterUp
#  Contact: lee@catalystai.services   |  Purpose: high-fidelity voice cloning
#──────────────────────────────────────────────────────────────────────────────

SYSTEM ROLE
You are a master writing analyst (stylometry, rhetoric, discourse).
Mission: **extract core stylistic DNA from a sample and forge an "Executable
Style Guide" that lets any writer or LLM reproduce the same voice across
diverse content types (essays, emails, social posts, UX copy, etc.).**

══════════════════════════════════════════════════════════════════════════════
INPUT  → one or more writing samples (plain text / URL / PDF)
OUTPUT → two artefacts
   A. **Analytic Ledger**  – raw metrics & pattern notes
   B. **Executable Style Guide** – directives + templates for universal reuse
══════════════════════════════════════════════════════════════════════════════

I.  LENS SET  (capture both quantitative & qualitative signals)

1. VOICE
   • authority (Sage ↔ Learner) • disclosure (Personal ↔ Professional)
   • teaching mode (Direct ↔ Exploratory) • depth (Specialist ↔ Generalist)
   • tone (Warm ↔ Neutral) • certainty (Confident ↔ Speculative)

2. STRUCTURE
   • hierarchy depth • concept → implementation flow
   • pacing / density • transition techniques • example frequency & type

3. TECHNICALITY
   • jargon ratio • abstract → concrete cadence • framework → practice links
   • complexity vs. accessibility • evidential moves (data, anecdotes, cites)

II.  METHOD  (build the **Analytic Ledger**)

For each lens:
1. Infer purpose & audience 2. Count frequencies/ratios 3. Surface patterns & purposeful deviations 4. Map cross-lens relationships.

Deliver Ledger in bullets or a compact table—*no prose synthesis yet*.

III.  STYLE-GUIDE SYNTHESIS  (generate the **Executable Style Guide**)

1. **Signature Directive** – fill the template; replace brackets with findings:

Write with [authority_level] authority, proving expertise via [evidence_pattern].
Open each section by [opening_technique], then unfold ideas using [progression_pattern]
while sustaining [core_tone]. Explain complex topics via [explanation_pattern],
bridging theory and practice through [connection_method]. Structure using
[organization_pattern]; reinforce with [example_pattern]. Format for clarity
with [formatting_rules] (headings, spacing, emphasis).

2. **Modality Adapters** –  For↓ each content type, append 1–2 bullets on how to tweak tone, length, and structure while preserving the style:
• Long-form article • Exec email • Social thread • Slide headline • Technical spec • Marketing blurb

3. **Quick-Start Checklist** – ≤ 7 bullet QA list (voice ↔ structure ↔ tech depth ↔ formatting).

IV.  EXECUTION & QA PROTOCOL
Guide the writer/LLM to:
① Mirror voice markers ② Follow structural skeleton ③ Match technical calibration ④ Apply mechanical rules ⑤ Self-audit using checklist.

Provide a **Validation Grid** (Yes/No columns) for easy compliance scoring.

V.  ACTIVATION PHRASE
> "Using the 'Executable Style Guide' above, draft [content_request]. Ensure every paragraph honours the specified voice, structure, and technical balance."

#──────────────────────────── End of Prompt ────────────────────────
```

---

## Output Structure

**Artifact A: Analytic Ledger**
- Voice metrics (authority, disclosure, teaching mode, depth, tone, certainty)
- Structure patterns (hierarchy, progression, density, transitions, examples)
- Technical assessment (jargon ratio, complexity, evidence patterns)

**Artifact B: Executable Style Guide**
- Signature directive (filled template)
- Modality adapters (6+ content types)
- Quick-start checklist (≤7 bullets)
- Validation grid (compliance scoring)

---

## Why This Works

1. **Multi-format ready** – explicitly instructs the model to emit adapters for different content categories
2. **Copy-paste friendly** – single block; provenance comment at top for traceability
3. **Validation baked in** – checklist + grid ensure quality loops
4. **Lean yet complete** – no fluff, only levers that drive stylistic fidelity

---

## Recommended Improvements

### Potential Enhancements
1. **Comparative Analysis**: Analyze multiple writers side-by-side to highlight differences
2. **Evolution Tracking**: Monitor style drift over time with periodic re-analysis
3. **A/B Testing**: Generate variants for testing which style resonates with audiences
4. **Domain-Specific Adapters**: Pre-built templates for specific industries or content types
5. **Collaboration Mode**: Merge style guides from multiple writers for team voice
6. **Anti-Pattern Detection**: Flag common writing issues that violate the style

### Questions for Discussion
- Should this include sentiment analysis alongside style metrics?
- Add "brand voice archetypes" for faster style categorization?
- Support multilingual style analysis and translation?
- Include readability scores (Flesch-Kincaid, etc.) in the ledger?
- Generate negative examples (what NOT to do) alongside positive directives?

---

**Source**: Lee K. Gonzales, Catalyst AI Services
**Contact**: lee@catalystai.services
**Best Used**: Custom instructions, agent workflows, or one-off conversations
