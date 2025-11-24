# OpenAI PDF Hunter - System Card Discovery

## Purpose
Systematically discovers and summarizes new OpenAI PDFs (system cards, whitepapers, technical documentation) by scanning their CDN across date ranges. Helps researchers and practitioners stay current with OpenAI releases.

## Use Cases
- Tracking new OpenAI model releases and system cards
- Research literature review
- Monitoring AI safety and policy documentation
- Discovering technical architecture details
- Staying current with OpenAI's public research

## Instructions
1. Specify how many days back to search (N days)
2. AI will search OpenAI's CDN day-by-day
3. For each PDF found: title, URL, summary, and key details
4. Final roll-up summary of most important documents
5. Useful for weekly or monthly research updates

---

## The Prompt

```text
You are a research assistant scanning for new OpenAI PDFs hosted on their CDN.

Task:
For each of the **last N days** (I'll specify N), perform a search using a query like:

`site:cdn.openai.com/ filetype:pdf after:[YYYY-MM-DD] before:[YYYY-MM-DD+1]`

For each day:
1. List any PDFs found (title or filename + short description).
2. Note the URL and publication or modification date if available.
3. Summarize each document in 2–4 bullets:
   - Purpose or topic.
   - Key methods or architecture details (if technical).
   - Any noteworthy safety, policy, or capability notes.
4. At the end, give me a **roll-up summary**:
   - The 3–5 most important documents across all days.
   - One paragraph on why they matter for practitioners.

Format:
- Use a heading per day.
- Under each, list documents as bullets.
- Keep summaries concise; aim for high signal per word.
```

---

## Usage Example

**Input:**
"Search the last 7 days for new OpenAI PDFs"

**Expected output format:**
```
## 2025-11-18
- **GPT-4.5 System Card** (cdn.openai.com/.../gpt-4.5-system-card.pdf)
  - Purpose: Safety evaluation and capability assessment for GPT-4.5
  - Key methods: Red teaming, adversarial testing, bias measurement
  - Safety notes: Improved refusal rates for harmful content, reduced hallucinations
  - Notable: First model to pass comprehensive medical licensing exam

## 2025-11-19
[No PDFs found]

## 2025-11-20
- **Whisper v3 Technical Report** (cdn.openai.com/.../whisper-v3-technical.pdf)
  ...

## Roll-up Summary
Most important documents:
1. GPT-4.5 System Card - Major model release
2. Whisper v3 Technical Report - Speech recognition breakthrough
3. [...]

Why they matter:
These releases signal OpenAI's continued focus on safety-first deployment...
```

---

## Customization Notes

**Search Scope Options**:
- Default: Last N days
- Alternative: Specific date range
- Variant: Search by keyword (e.g., "safety", "GPT-4", "DALL-E")

**Document Categories**:
- System cards (model releases)
- Technical reports and papers
- Safety and policy documents
- API documentation
- Research methodology papers

**Summary Depth**:
- Minimal: Title, date, 1-line description
- Standard: 2-4 bullet summary (as shown)
- Detailed: Full abstract, key findings, methodology notes

---

## Recommended Improvements

### Potential Enhancements
1. **Multi-Source**: Extend to Anthropic, Google DeepMind, Meta AI, etc.
2. **Automated Alerts**: Set up recurring searches with email/Slack notifications
3. **Comparison Mode**: Compare new system cards to previous versions
4. **Citation Export**: Generate BibTeX or other citation formats
5. **Trend Analysis**: Track patterns across releases (safety focus, capability areas)
6. **Full-Text Extraction**: Download and analyze complete PDF contents
7. **Topic Clustering**: Group documents by theme (safety, capabilities, efficiency)

### Questions for Discussion
- Should this include GitHub releases and model card updates?
- Add "significance scoring" to rank documents by importance?
- Include community reactions or social media sentiment?
- Support RSS/Atom feed generation for automated monitoring?
- Add diff mode showing changes between document versions?
- Integrate with academic paper databases (arXiv, Papers with Code)?
- Create digest modes (daily, weekly, monthly) with different depth?
