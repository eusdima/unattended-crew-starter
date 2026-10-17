# 2. Install Claude Code and Firstmate

Paste these one at a time and wait for each to finish.

## Install Claude Code

Anthropic's installer for macOS and Linux:

```sh
curl -fsSL https://claude.ai/install.sh | bash
```

Open a new terminal window and check:

```sh
claude --version
```

You should see a version number. If the shell cannot find `claude`, open another fresh terminal. Anthropic's [setup page](https://code.claude.com/docs/en/setup) covers other cases.

## Install git and the GitHub CLI

Many machines already have git. On a Mac with Homebrew:

```sh
brew install git gh
```

On Linux, install the `git` and `gh` packages with your package manager.

## Sign in to GitHub

```sh
gh auth login
```

The default answers are fine.

## Get Firstmate

```sh
git clone https://github.com/kunchenguid/firstmate
cd firstmate
```

This folder is your first mate's home. Start it from here every time.

## Start your first mate

```sh
claude
```

Claude Code asks you to sign in with your Claude account and asks whether you trust the folder. Say yes to both.

Then the first mate checks its tools. Firstmate's own bootstrap script knows these: `tmux`, `treehouse`, `no-mistakes`, `node`, and the helpers `gh-axi`, `chrome-devtools-axi`, `tasks-axi` and `quota-axi`. If any are missing, the first mate lists each one with its install command and waits. Read the list, then say yes. If it asks you to sign in to GitHub again, type `! gh auth login` in the chat to run it in the same window.

When the tools are in place, the first mate waits for your first request. Leave it running.

Firstmate's [Quick Start](https://github.com/kunchenguid/firstmate#quick-start) is the official version of this page.

Previous: [1. What a crew is](01-what-a-crew-is.md) · Next: [3. Add one project](03-add-one-project.md)
