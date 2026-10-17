# Unattended Crew starter

A short guide to running your first AI crew with [Firstmate](https://github.com/kunchenguid/firstmate) on Claude Code. It ends with one project added, one worker dispatched and one task reviewed and merged by you.

> This is an independent guide. It is not affiliated with or endorsed by Kun Chen, the Firstmate project or Anthropic. Firstmate's own repository, [kunchenguid/firstmate](https://github.com/kunchenguid/firstmate), is the official source for how it works. If this guide and that repository disagree, the repository wins.

## What a crew is

A crew is a set of AI agents that work for you while you talk to only one of them. You are the captain. You give requests to the first mate, a single Claude Code session, and it hands each task to a crewmate: a worker agent with its own copy of your project, so workers never step on each other. The first mate checks the results and comes back to you only for decisions, and nothing reaches your real code until you say "merge it".

Firstmate is the open-source folder of instructions and scripts that turns a Claude Code session into a first mate. It is MIT licensed and made by Kun Chen.

## What you need

- A Mac or a Linux computer.
- A terminal you are comfortable pasting commands into. You do not need to write code.
- A GitHub account.
- A paid Claude plan that includes Claude Code. See [claude.com/pricing](https://claude.com/pricing) for the current plans. The free plan does not include Claude Code.
- A GitHub repository you own and can experiment on, such as a personal site. Avoid anything with customers on it for your first run.

## The four steps

Each step has a short page in [`docs/`](docs/). The commands below are the whole path.

### 1. Understand the roles

Read [docs/01-what-a-crew-is.md](docs/01-what-a-crew-is.md). It takes two minutes and has no commands.

### 2. Install Claude Code and Firstmate

Full page: [docs/02-install.md](docs/02-install.md).

```sh
curl -fsSL https://claude.ai/install.sh | bash
```

Open a new terminal, then check it:

```sh
claude --version
```

Install `git` and the GitHub CLI (`gh`) with your package manager, then sign in:

```sh
gh auth login
```

Clone Firstmate and start your first mate from inside the folder:

```sh
git clone https://github.com/kunchenguid/firstmate
cd firstmate
claude
```

On first start the first mate checks its tools and asks before it installs anything. Read the list and approve it.

### 3. Add one project

Full page: [docs/03-add-one-project.md](docs/03-add-one-project.md). In the first mate's chat, type a plain request:

```text
ahoy, add my project github.com/you/your-site
```

It will confirm where the project lives and how changes should ship. For a first project, `direct-PR` is the simplest choice: a worker opens a pull request and you merge it yourself.

### 4. Dispatch one worker on one task

Full page: [docs/04-first-task.md](docs/04-first-task.md). Pick something small that you can check in a minute:

```text
fix the broken link in the footer of your-site
```

A worker takes the task in its own copy of the project. A few minutes later the first mate reports a pull request. Read it on GitHub. If it looks right, say `merge it`. [examples/first-task-brief.md](examples/first-task-brief.md) shows what a good request contains, and [examples/minimal-project/](examples/minimal-project/) is a tiny site you can push to GitHub and practise on.

## Two rules for unattended runs

1. Keep approvals on. The crew prepares; you say yes to anything public, paid or permanent.
2. Never give an agent your card. Buy things yourself, after the crew has done the research.

## What to try next

- Ask for a scout task: "look into why the contact form is slow and write up what you find". A scout leaves a report and changes nothing.
- Run two small tasks at once on the same project and watch the workers in `tmux attach -t firstmate`.
- Switch a project to the `no-mistakes` mode, which runs a review and test pipeline before a pull request opens.
- Read Firstmate's [configuration docs](https://github.com/kunchenguid/firstmate/blob/main/docs/configuration.md) to see what you can tune.

## Keep going

- The free course walks through these four steps in more detail: [unattendedcrew.com](https://unattendedcrew.com)
- The full Unattended Crew course goes on to running a crew day to day. It is on the same site.

## Licence

This guide is released under the [MIT licence](LICENSE), copyright 2026 Eustațiu Digital Studio. Firstmate has its own MIT licence, copyright Kun Chen.
