# 3. Add one project

Pick a GitHub repository you own and do not mind experimenting on. A personal site works well. If you have none, push [`examples/minimal-project/`](../examples/minimal-project/) to a new repository of your own.

## Tell the first mate

In the first mate's chat, ask in plain English. "Ahoy" is optional.

```text
You: ahoy, add my project github.com/you/your-site
First mate: I'll clone it as your-site. ... Go ahead?
You: yes
```

This is an example. The wording will differ, but the first mate confirms the same things before it clones: where the project lives, what to call it, how its changes ship and who approves merges.

## How changes ship

Firstmate calls this the delivery mode. You choose it per project and can change it later by asking.

- `direct-PR`: a crewmate pushes a branch and opens a pull request. You read it on GitHub and tell the first mate to merge. Start here.
- `no-mistakes`: the same, but a review and test pipeline runs before the pull request opens.
- `local-only`: nothing is pushed. The crewmate leaves a finished branch on your computer and the first mate merges it locally after you approve.

For a GitHub project the default mixes the first two. Ask for `direct-PR` for your first task, since it has fewer parts.

## What the first mate will not do

The first mate reads your project but does not edit it, apart from a few guarded steps you approve. Changes come from crewmates working in their own copies. A setting called `yolo` lets the first mate merge passing work without asking. It is off unless you turn it on, and you should leave it off.

Previous: [2. Install](02-install.md) · Next: [4. First task](04-first-task.md)
