---
name: model-reasoning
description: Choose an available AI model and reasoning level for a task or for authorized subtasks in Claude Code and Codex. Use for model selection, planning versus implementation, or a workflow that needs to balance quality, speed, and plan usage.
---

# Pick the model and reasoning level

Use Alex's starting settings below. Check the current session's model selector, configured agents, or available model list before picking. Use the names and effort values the host accepts. Prefer the closest available model for the job if a named one is missing.

| Model | Use it for | Start here |
| --- | --- | --- |
| Fable 5.2 | Architecture | High |
| Opus 5.5 | Coding | High |
| Sonnet 5.5 | Research + summaries | Medium |
| GPT-6.2 Astra | Hard decisions | Extra High |
| GPT-6.2 Sol | Frontend | High |
| GPT-6.1 Terra | Browser extraction | Medium |

Fable and Astra are the planning choices in their respective tools. Opus is the Claude coding workhorse. Sol also works well for general Codex implementation and English editing. Use Sonnet for bounded research and summaries, and use Terra for straightforward browser extraction when the needed browser tools are available.

## Route the job

1. Identify the deliverable, the irreversible decisions, the user's plan or budget if known, and a concrete check for the result. Handle a small task in one pass. For a larger job, separate the hard decision, the implementation, and any independent research or verification.
2. Assign a model and effort to each meaningful piece. Use the current provider and models the account exposes. Start with the table for substantive work. For mechanical edits or simple extraction, prefer a lighter available model at Medium or the lowest supported effort that meets the check.
3. If the user requested recommendations or a plan, show the task, model, effort and success check. For execution, use only the host's supported controls and authorized delegation. Pass both model and effort where they are configurable. If only named agent profiles are available, use an existing profile with matching settings. In a fixed-model session, tell the user which setting to select or continue with the current model when it is adequate.
4. Run the check. Escalate a hard blocker or a failed check with the relevant evidence and the specific decision. After resolving it, return routine work to the working model. Report the model and effort actually used separately from recommendations when the two differ.

## ChatGPT Plus ($20) in Codex

Use Codex signed in with your ChatGPT account. Begin with Standard speed and the models and efforts that appear for that account.

- Routine work: GPT-6.1 Terra on Medium for straightforward extraction when offered. Use GPT-6.2 Sol on Medium for clear edits or whenever Terra is missing and Sol is available.
- Main work: GPT-6.2 Sol on High for frontend changes, involved implementation and writing that needs care.
- Hard call: GPT-6.2 Astra on Extra High for a difficult plan or decision when that combination is offered and fits the allowance. Otherwise use Sol on High for a focused planning pass.
- When a named option is missing, use the closest model and effort already available. Keep paid credits and account changes under the user's control.

## Claude Code advisor

For a compatible Opus session, the user can select `/advisor fable` when Fable is available. Opus stays on the main job and can consult the advisor on a hard decision. The alias follows the available Fable family version. Fable 5.2 requires Claude Code v2.1.321 or later. Advisor calls use account allowance or credits. Let the user handle any account consent, then return to Opus if needed.

## Try it

> Use the model-reasoning skill. Plan my settings page redesign and docs FAQ. Pick an available model and reasoning level for each. Plan only.

Start with a planning pass only if the redesign has a real architectural decision. Route the interface work to an implementation model and the FAQ to a lighter model. Good checks are a settings page that works at phone width and FAQ answers traceable to the source docs.

[Codex settings and model access](https://help.openai.com/en/articles/20001275-chatgpt-work-and-codex) · [Codex subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents) · [Claude Code advisor](https://code.claude.com/docs/en/advisor)
