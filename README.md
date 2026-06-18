# token-breakdown


Always know where your tokens went.



After every response, appends a breakdown like:

---
📊 Token Breakdown
Plan [██░░░░░░░░] 20% · Code [██████░░░░] 60% · Review [██░░░░░░░░] 20%
Why: Most tokens went to writing the implementation — logic was straightforward.

Install

bash# Clone the repo
git clone https://github.com/TaeyangYeon/token-breakdown
cd token-breakdown

# Load into Claude Code
claude --plugin-dir .

Or install via plugin command

git clone https://github.com/TaeyangYeon/token-breakdown
claude --plugin-dir ./token-breakdown

cp -r ./token-breakdown ~/.claude/skills/token-breakdown

Phases

PhaseWhat it countsPlanThinking, architecture, clarifying questionsCodeActual code, configs, commands, file contentsReviewExplanations, caveats, alternatives, error notes

Why

Inspired by caveman and ponytail.
A single SKILL.md is all it takes.
