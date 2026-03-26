# Debate System

A multi-agent debate system where AI agents argue opposing sides of any decision,
scored by a Judge agent. Built to surface better reasoning than single-prompt LLMs.

## Agents
- **Advocate** — argues strongly in favor of the proposition
- **Skeptic** — challenges assumptions and demands evidence
- **Devil's Advocate** — finds worst-case scenarios and failure modes
- **Judge** — scores all agents and delivers a structured verdict

## Setup

1. Clone the repo and create a virtual environment:
```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
   pip install -r requirements.txt
```

3. Add your Anthropic API key to `.env`:
```
   ANTHROPIC_API_KEY=sk-ant-your-key-here
```

## Usage
```bash
python main.py "Was investing in WeWork at a $47B valuation in 2019 a good decision?"
```

Debate transcripts are saved automatically to `outputs/`.

## Benchmark

| Domain | Decisions tested | Judge accuracy |
|--------|-----------------|----------------|
| Startup investments | — | — |

*Accuracy = judge verdict matched real-world outcome*

## Roadmap
- [ ] 3-round debate engine (CLI)
- [ ] Scoring rubric + benchmark dataset
- [ ] Web UI with streaming responses
- [ ] Custom persona support
