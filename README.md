# Model Reasoning

Pick a model and reasoning level for planning, implementation, and smaller tasks in Claude Code or Codex. The skill includes Alex’s starting settings from the Reasoning Reel and a ChatGPT Plus profile for Codex.

## Install

Choose the instructions for your app. These commands add the skill to your personal skills directory.

### Claude Code

~~~sh
mkdir -p ~/.claude/skills
git clone https://github.com/alexandreleciel/model-reasoning.git ~/.claude/skills/model-reasoning
~~~

Open a Claude Code session and type `/model-reasoning`.

### Codex

~~~sh
mkdir -p ~/.agents/skills
git clone https://github.com/alexandreleciel/model-reasoning.git ~/.agents/skills/model-reasoning
~~~

Open a Codex session and mention `$model-reasoning`.

You can also download [SKILL.md](SKILL.md) and put it in a folder named `model-reasoning` in the matching skills directory.

## Try it

> Use the model-reasoning skill. Plan my settings page redesign and docs FAQ. Pick an available model and reasoning level for each. Plan only.

The skill uses the models available in your account. When a session needs a manual model or effort selection, it tells you what to choose.

[Claude Code skills](https://code.claude.com/docs/en/skills) · [Codex skills](https://learn.chatgpt.com/docs/build-skills)
