# 4. Run one worker on one task

Ask for something small and real that you can check in a minute: a broken link, a typo, a missing alt text. [examples/first-task-brief.md](../examples/first-task-brief.md) shows what to include.

```text
You: fix the broken link in the footer of your-site
First mate: On it. A worker is on it in its own window.
First mate, a few minutes later: Pull request ready for review: github.com/you/your-site/pull/1. Merge it?
You: merge it
```

Again, the wording will differ. The shape holds: one request, a finished change back, and nothing merged until you say so.

## Watch it, if you want to

Each crewmate runs in a tmux window. If you started the first mate outside tmux, Firstmate keeps the crew in a detached session named `firstmate`. In a second terminal:

```sh
tmux attach -t firstmate
```

Press `Ctrl-b`, then `d`, to leave without stopping anything. You do not have to watch.

## Check before you merge

Open the pull request and read it. If something is wrong, say so in plain English and the first mate passes it back to the crewmate. When it looks right, say `merge it`.

## Why workers do not ask before each command

By default Firstmate starts Claude Code workers with permission prompts switched off. What keeps that safe is the isolation: each worker is in its own copy of your project, and nothing reaches your real code until you approve the merge.

If you would rather have Claude Code check each action, switch workers to auto mode. In the `firstmate` folder:

```sh
mkdir -p config && echo auto > config/claude-permission-mode
```

Workers started after that use auto mode. The setting is documented in Firstmate's [configuration docs](https://github.com/kunchenguid/firstmate/blob/main/docs/configuration.md#claude-permission-mode-configclaude-permission-mode).

## Two rules for every unattended run

1. Keep approvals on. The crew prepares; you say yes to anything public, paid or permanent.
2. Never give an agent your card. Do not paste a card number, bank login or payment API key anywhere an agent can read it. Buy things yourself.

## You are done when

- Claude Code and Firstmate start without errors
- Your first mate knows one of your projects
- A crewmate finished one task and you approved it

Previous: [3. Add one project](03-add-one-project.md) · Back to the [README](../README.md)
