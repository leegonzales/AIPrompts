# Claimify - Factual Claim Extractor

## Purpose
Extracts, disambiguates, and structures factual claims from text for verification and fact-checking. Prepares content for red-teaming, source validation, or quality assurance without performing the actual fact-checking.

## Use Cases
- Preparing content for fact-checking teams
- Academic research verification
- Journalism and content quality assurance
- Detecting vague or unverifiable claims in writing
- Pre-publication review for factual accuracy

## Instructions
1. Paste this prompt followed by the text you want to analyze
2. AI will extract discrete, verifiable claims
3. Each claim gets structured metadata for verification
4. Use output to guide fact-checking work (not as fact-check itself)
5. Claims are disambiguated and split for clarity

---

## The Prompt

```text
You are a **claim extractor** preparing text for fact-checking.

Given the passage I provide, follow this protocol:

1. **Selection**
   - Identify sentences or fragments that contain **factual, verifiable information** (dates, quantities, causal claims, attributions, etc.).

2. **Disambiguation**
   - If a statement is ambiguous or conflates multiple ideas, split it into clearer sub-claims.
   - Note any claims that are too vague to verify as-is.

3. **Decomposition**
   - Break compound sentences into **discrete, standalone claims**, each of which could be individually checked against external sources.

4. **Evaluation-Ready Output**
   - Produce a numbered list of claims.
   - For each claim, include fields in a small JSON-ish format:

     - `claim`: the claim text.
     - `source_snippet`: minimal original text that supports it.
     - `ambiguity`: "low", "medium", or "high".
     - `check_type`: e.g., "statistical", "historical", "causal", "attribution", etc.

Output example format:

1. { "claim": "...", "source_snippet": "...", "ambiguity": "low", "check_type": "historical" }
2. { "claim": "...", ... }

Do **not** start fact-checking; only prepare the claims for later verification.
```

---

## Usage Example

**Input text:**
"The 2023 study by Stanford researchers found that AI models are 40% more accurate than humans at diagnosing rare diseases, which led to healthcare costs dropping by $2 billion last year."

**Expected output:**
```
1. { "claim": "A 2023 study was conducted by Stanford researchers on AI diagnostic accuracy", "source_snippet": "2023 study by Stanford researchers", "ambiguity": "low", "check_type": "attribution" }

2. { "claim": "AI models are 40% more accurate than humans at diagnosing rare diseases", "source_snippet": "AI models are 40% more accurate than humans at diagnosing rare diseases", "ambiguity": "medium", "check_type": "statistical" }

3. { "claim": "Healthcare costs dropped by $2 billion last year", "source_snippet": "healthcare costs dropping by $2 billion last year", "ambiguity": "high", "check_type": "statistical" }

4. { "claim": "The AI diagnostic accuracy caused healthcare cost reduction", "source_snippet": "which led to healthcare costs dropping", "ambiguity": "high", "check_type": "causal" }
```

---

## Customization Notes

**Check Types** (common categories):
- **Statistical**: Numerical claims, percentages, measurements
- **Historical**: Dates, events, timelines
- **Attribution**: Who said/did/discovered something
- **Causal**: X caused Y or X correlates with Y
- **Definitional**: What something is or means
- **Existence**: Something exists or occurred
- **Comparative**: X is more/less than Y

**Ambiguity Levels**:
- **Low**: Clear, specific, easily verifiable
- **Medium**: Needs context or clarification
- **High**: Vague, conflated, or missing key details

---

## Recommended Improvements

### Potential Enhancements
1. **Auto-Sourcing**: Suggest potential verification sources for each claim
2. **Priority Ranking**: Flag most important or impactful claims to check first
3. **Claim Clustering**: Group related claims to optimize verification work
4. **Red Flag Detection**: Highlight claims with common misinformation patterns
5. **Verification Templates**: Provide search queries or verification steps per claim
6. **Confidence Scoring**: Estimate how easily each claim can be verified
7. **Citation Linking**: Match claims to existing references if source document has citations

### Questions for Discussion
- Should this integrate with fact-checking databases (Snopes, PolitiFact, etc.)?
- Add support for claim dependency graphs (claim B depends on claim A)?
- Include "plausibility heuristics" to flag likely false claims?
- Support bulk processing for long documents or multiple sources?
- Add domain-specific modes (medical, legal, financial, political)?
- Generate automated fact-check prompts for each extracted claim?
- Track common sources of ambiguity to improve writing guidance?
