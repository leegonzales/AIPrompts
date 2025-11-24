# AI Prompts Library

A curated collection of professional AI prompts for various use cases, from writing analysis to coaching and strategic thinking. These prompts are designed to work with modern LLMs like GPT-4, Claude, and similar models.

## Overview

This repository contains battle-tested prompts developed for real-world applications including:
- Stylometric analysis and writing replication
- Professional coaching and skill development
- Organizational analysis and strategic planning
- Daily briefings and intelligence gathering
- Research and fact-checking tools
- Learning and education systems
- Workflow optimization and productivity

## Repository Structure

```
.
├── prompts/
│   ├── writing-and-style/          # Writing analysis & style replication
│   ├── coaching-and-training/      # Educational & coaching prompts
│   ├── analysis-and-strategy/      # Business & org analysis
│   ├── workflow-and-productivity/  # Context transfer & process optimization
│   ├── daily-briefings/            # Daily intelligence & information prompts
│   ├── learning-and-education/     # Tutorial & skill-building prompts
│   └── research-and-analysis/      # Fact-checking & discovery tools
├── legacy/                         # Historical prompts & experiments
├── examples/                       # Usage examples & outputs
├── CONTRIBUTING.md                 # Contribution guidelines
├── LICENSE.md                      # MIT License
└── README.md                       # This file
```

## Prompt Categories

### Systems & Meta
- **co-strategist-operating-system.md** (Power: 10/10) - Foundational OS transforming Claude into co-strategist with archetypes, frameworks, and voice system

### Writing & Style
- **WritingAnalyzer.md** - Stylometric analysis for voice cloning
- **WritingStyleAnalyzer.md** - Style extraction and replication
- **DeepResearchEntityWritingAnalyzer.md** - Deep research-focused writing analysis
- **writing-style-analyzer-generator.md** (Power: 8/10) - Comprehensive voice analysis and reusable style directive generation
- **anti-cliche-writing-system.md** (Power: 8/10) - Detect and fix AI writing clichés across 5 categories

### Coaching & Training
- **ai-opportunity-coach-prompt.md** - AI opportunity discovery coaching
- **PROMPT-ALCHEMIST-TEACHER.md** - Prompt engineering training system
- **Prompt_Trainer.md** - Interactive prompt training sessions

### Analysis & Strategy
- **OrgSayVSDoGapAnalyzer.md** - Organizational alignment analysis
- **synthetic-workforce-inevitability-engine.md** - Business opportunity discovery in AI era
- **arbitrage-opportunity-analyst.md** (Power: 9/10) - Systematic arbitrage discovery across 8 asymmetry types with ethics-integrated 8-stage methodology
- **competitive-analysis-system.md** (Power: 10/10) - 6-framework competitive intelligence with OODA/Wardley/Rumelt/Christensen/Martin/Kagan
- **strategic-frameworks-interpreter.md** (Power: 9/10) - Apply OODA, Wardley, Cynefin, Dreyfus, and more to any situation

### Workflow & Productivity

#### Context Export Variants (Choose Based on Needs)

We provide three variants of context export prompts, each optimized for different scenarios:

| Variant | Best For | Length | Key Features |
|---------|----------|---------|--------------|
| **[Simple](prompts/workflow-and-productivity/context-continuity-export-simple.md)** | Quick handoffs, straightforward projects | ~500 words | 8 core sections, no setup, instant use |
| **[Comprehensive](prompts/workflow-and-productivity/context-continuity-export-comprehensive.md)** | Complex projects, team handoffs | ~1000 words | 10 sections including concepts, frameworks, onboarding note |
| **[Adaptive](prompts/workflow-and-productivity/context-continuity-export-adaptive.md)** | Variable complexity, sensitive contexts | 200-1000 words | Interactive mode selection, content filtering |

**When to use each:**
- **Simple**: Single user, clear scope, need context transfer now
- **Comprehensive**: Multi-session projects, team collaboration, high stakes
- **Adaptive**: Uncertain scope, mixed audiences, sensitive information

All variants create self-contained markdown artifacts for seamless conversation handoffs between AI sessions.

**Strategic Edition:**
- **context-transfer-protocol-strategic.md** (Power: 8/10) - Advanced context transfer with decision logs, evolution tagging (G/C/P/K), and receiving agent handshake protocol

### Daily Briefings
- **executive-brief-daily.md** - Industry headlines, market updates, leadership insights
- **weather-intelligence-immersive.md** - Time-aware, vivid weather forecasting

### Learning & Education
- **algorithms-tutor-daily.md** - Daily CS fundamentals with progressive Q&A
- **prompt-alchemist-trainer-v3.md** (Power: 9/10) - Gamified prompt engineering mastery system with 5 levels, XP progression, 8 personas
- **workshop-architect-framework.md** (Power: 8/10) - Design transformational learning experiences with psychological safety and Dreyfus progression

### Research & Analysis
- **claimify-fact-checker.md** - Extract and structure factual claims for verification
- **openai-pdf-hunter.md** - Discover new OpenAI system cards and technical docs
- **company-intelligence-analyst.md** (Power: 9/10) - Decision-grade company research with evidence hierarchy and confidence taxonomy
- **strategic-research-orchestrator.md** (Power: 9/10) - Time-bounded research with quality gates and practitioner focus

## How to Use

1. **Browse the categories** in the `prompts/` directory to find relevant prompts
2. **Read the prompt header** (Purpose, Use Cases, Instructions) to understand what it does
3. **Copy the prompt** from "The Prompt" section
4. **Customize** based on "Customization Notes" if needed
5. **Paste** into your LLM of choice (ChatGPT, Claude, etc.)
6. **Review** the "Recommended Improvements" section for potential enhancements

### Best Practices

- Read the full prompt file before using to understand its structure and purpose
- Many prompts include system role definitions - paste these at the start of a new conversation
- Some prompts use state management or memory systems - follow the internal instructions carefully
- Experiment with parameters and adapt prompts to your specific needs
- Check "Differences from Other Variants" sections when multiple versions exist

## Prompt Structure

Each prompt file follows a consistent format:

```markdown
# Prompt Name

## Purpose
[What this prompt does]

## Use Cases
[When and why to use it]

## Instructions
[How to use it]

---

## The Prompt
[The actual prompt to copy/paste]

---

## Recommended Improvements
[Potential enhancements and discussion questions]
```

## Contributing

Contributions are welcome! If you have prompts that have proven valuable in your work:

1. Fork this repository
2. Add your prompt to the appropriate category (or propose a new one)
3. Follow the standard prompt structure (see CONTRIBUTING.md)
4. Include "Recommended Improvements" section
5. Submit a pull request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## Quality Standards

All prompts in this repository should:
- Be production-tested (actually used in real work)
- Include clear instructions or system role definitions
- Be well-documented with purpose and use cases
- Follow the consistent markdown format
- Include "Recommended Improvements" section
- Avoid hardcoded personal information

## Legacy Content

The `legacy/` directory contains historical prompts from earlier ChatGPT experiments. These are preserved for reference but may not work well with modern models.

## License

This repository is licensed under the MIT License. See [LICENSE.md](LICENSE.md) for details.

You are free to use, modify, and distribute these prompts. Attribution is appreciated but not required.

## Author

**Lee K Gonzales**
- Founder, Catalyst AI Services
- Director of AI Transformation, BetterUp
- Contact: lee@catalystai.services

## Acknowledgments

These prompts represent years of experimentation and real-world application across various domains. Special thanks to the AI research community for inspiration and feedback.

## Further Reading

- [Prompt Engineering Guide](https://www.promptingguide.ai/)
- [OpenAI Best Practices](https://platform.openai.com/docs/guides/prompt-engineering)
- [Anthropic's Claude Prompt Design](https://docs.anthropic.com/claude/docs/introduction-to-prompt-design)

---

Last updated: November 2025
