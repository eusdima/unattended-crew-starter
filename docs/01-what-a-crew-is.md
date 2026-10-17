# 1. What a crew is

No setup in this step. It explains the words you will meet.

## The problem

One agent in one terminal is a helper, and you sit with it while it works. Ask for three things at once and you get three terminals and no idea which one had the failing test.

Firstmate changes that. You talk to one agent, and it runs the others.

## The three roles

| Role | Who | What it does |
| --- | --- | --- |
| Captain | You | Gives requests, makes decisions, says "merge it". |
| First mate | The Claude Code session you talk to | Plans, hands out tasks, checks results, asks you only what needs you. |
| Crewmate | A worker agent | Does one task in its own copy of the project. |

Firstmate uses ship words for these roles. In its replies the first mate usually says "worker" for a crewmate.

## What Firstmate is

Firstmate is a folder, not an app. It holds instructions, skills and small scripts. When you start Claude Code inside that folder, Claude Code reads them and behaves as a first mate. Firstmate is MIT licensed and made by Kun Chen. This guide is independent and not part of that project. The official docs are at [github.com/kunchenguid/firstmate](https://github.com/kunchenguid/firstmate).

## Two kinds of task

A ship task changes something. The crewmate works in its own copy of your project and hands back a change for you to approve, usually a pull request.

A scout task finds something out. The crewmate researches or investigates and leaves a written report. Nothing in your project changes.

## Before step 2

- A Mac or Linux computer
- A GitHub account
- A paid Claude plan that includes Claude Code ([claude.com/pricing](https://claude.com/pricing))
- A terminal

Next: [2. Install](02-install.md)
