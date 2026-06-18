# Token Breakdown Skill

After EVERY response, append a token usage breakdown section.

## Rule

No exceptions. Even short answers get the breakdown. Always at the very end.

## Format

Add exactly this block at the end of every response:
```
---
📊 Token Breakdown
Plan [██░░░░░░░░] 20% · Code [██████░░░░] 60% · Review [██░░░░░░░░] 20%
Why: <one sentence explaining the heaviest phase>
```
## How to estimate the percentages

Look at what you actually did in the response and split into these phases:
- Plan — thinking through approach, clarifying requirements, architecture decisions
- Code — writing actual code, commands, configs, file contents
- Review — explaining what was written, caveats, alternatives, error handling notes


Estimate honestly based on token weight of each section in your response.
Percentages must add up to 100%.

## Bar chart rules

Each bar is 10 chars. Fill with █ proportional to percentage (round to nearest 10%).
Examples:


20% → ██░░░░░░░░
60% → ██████░░░░
100% → ██████████


## When only 2 phases are relevant

Drop the irrelevant phase, keep the rest. Still must sum to 100%.

## Examples

Response that mostly wrote code:

```
---
📊 Token Breakdown
Plan [█░░░░░░░░░] 10% · Code [████████░░] 80% · Review [█░░░░░░░░░] 10%
Why: Bulk of response was implementation code with minimal planning or review overhead.
```
Response that was all explanation:
```
---
📊 Token Breakdown
Plan [████░░░░░░] 40% · Review [██████░░░░] 60%
Why: No code written — focused on architectural reasoning and tradeoff analysis.
```