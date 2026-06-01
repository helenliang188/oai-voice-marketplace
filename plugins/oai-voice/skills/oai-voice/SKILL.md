---
name: oai-voice
description: Rewrite paragraphs, Slack posts, emails, docs, announcements, and leader communications so they are concise, conversational, evidence-led, and clear about the values behind key decisions. Use when the user asks to tighten, clarify, make more direct, make more human, sharpen, or improve writing while preserving the intended meaning.
---

# OAI Voice

## Overview

Use this skill to rewrite user-provided text so the reader understands the point quickly, trusts the claim because it is grounded in evidence, and can see the values behind important decisions.

For reusable style patterns and examples, read `references/style-patterns.md`.

## Rewrite Workflow

1. Identify the core message: what changed, what matters, and what the reader should understand or do next.
2. Preserve the user's intent and facts. Do not invent evidence, decisions, dates, metrics, approvals, or commitments.
3. Put the point first. Lead with the clearest conclusion, decision, ask, or update.
4. Make the language sound spoken. Prefer short sentences, common words, and natural transitions.
5. Use evidence to convince. Replace persuasion, hype, or reassurance with concrete proof, examples, numbers, observed behavior, or direct rationale.
6. Use values to explain key decisions. Name the actual principle behind the choice so readers can understand future tradeoffs.
7. Remove process-heavy framing unless the process itself matters to the reader.
8. Return the rewritten text first. Add a short note only when assumptions, missing context, or unresolved choices matter.

## Clarify Before Rewriting

Ask one to three focused questions when the draft cannot be sharpened responsibly. Do this when any of the following are unclear:

- The main point, decision, or ask.
- The intended audience and what they already know.
- The evidence that supports the claim.
- The value or principle behind a decision.
- The level of sensitivity, urgency, or formality.
- Whether a statement is confirmed fact, interpretation, or proposed language.

If the user wants momentum despite missing context, provide a draft with clear placeholders such as `[add evidence]` or `[name the decision principle]`.

## Style Rules

### Lead With the Point

- Start with the message, not the setup.
- Cut throat-clearing such as "I wanted to share," "as you may know," and "given everything going on."
- Use the first sentence to answer: "Why am I reading this?"
- Prefer one clear paragraph over a long buildup with a conclusion at the end.

### Write Like You Talk

- Use direct, human phrasing that would sound natural when read out loud.
- Prefer "we decided," "we learned," "we are changing," and "here is why" over abstract corporate phrasing.
- Keep warmth through clarity and specificity, not filler.
- Avoid jargon, inflated adjectives, and polished-but-empty language.

### Use Evidence to Convince

- Replace "we believe this is the right path" with the concrete reason it is the right path.
- Use numbers, customer or employee signals, observed patterns, research, or examples when available.
- Separate evidence from interpretation: "The data shows X, so we are doing Y."
- If evidence is missing, ask for it or mark the gap rather than overselling.

### Use Values to Explain Decisions

- Explain the principle behind the choice: speed, fairness, focus, accountability, transparency, customer impact, craft, resilience, or another user-supplied value.
- Connect the value to the tradeoff. Example: "We are choosing focus over breadth because spreading the team thinner would slow the work that matters most."
- Avoid hiding behind process. Process can support the decision, but it should not replace the reason.
- Make the decision logic reusable so readers understand how similar calls will be made later.

## Output Shape

Default to this structure:

```markdown
[rewritten paragraph]
```

When useful, add:

```markdown
[rewritten paragraph]

Notes:
- [assumption, missing evidence, or decision-value gap]
```

For larger rewrites, preserve the original format unless a cleaner structure is clearly better. Use headings, bullets, or numbered lists only when they help the reader scan.

## Guardrails

- Do not change the user's substantive meaning without saying so.
- Do not make unverified claims sound certain.
- Do not add confidentiality-sensitive details unless the user provided them and they are needed.
- Keep human review responsible for any downstream decision, especially for People, candidate, employee, performance, compensation, hiring, or promotion-related communications.
