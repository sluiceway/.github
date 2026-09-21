<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sluiceway/sluiceway/6eb8d045673dbd32fe37d71ea941d59e1cb04675/assets/mascot/in-sync-dark.svg">
    <img alt="Sluiceway: Penny, the sluice gate, asleep on the quay because everything is in sync" src="https://raw.githubusercontent.com/sluiceway/sluiceway/6eb8d045673dbd32fe37d71ea941d59e1cb04675/assets/mascot/in-sync-light.svg" width="880">
  </picture>
</p>

## A deploy dashboard that lives in a GitHub issue

After a merge, Sluiceway previews every infrastructure stack in your repo and keeps one issue up to date: which stacks have changes waiting, and what those changes are. You tick a stack's box, and a GitHub Actions run deploys exactly that stack.

- **It is a GitHub Action and nothing else.** No server, no database, no hosted part.
- **It never holds your credentials.** Previews and deploys run in your own runners, with your own secrets.
- **The issue is a view, never the source of truth.** Before every deploy the stack is previewed again, and nothing happens unless the fresh preview still matches what you ticked.
- **Pulumi first.** The core is tool-neutral, so OpenTofu and Terraform can follow.

A sluiceway is a channel with a gate. Changes queue up behind the gate, and you decide what passes. The gate is called Penny.

### Status: beta

Sluiceway works end to end. It runs on a real repo with 51 stacks: every push updates the dashboard, and a tick deploys that stack and nothing else. There is no tagged release yet, so for now you pin a commit. Expect rough edges, and tell us about every one you hit: the [onboarding log](https://github.com/sluiceway/sluiceway/blob/main/docs/onboarding-log.md) is where they go.

Start with the [README](https://github.com/sluiceway/sluiceway#readme). The [decision records](https://github.com/sluiceway/sluiceway/tree/main/docs/adr) say why it works the way it does, and [what is not in v1](https://github.com/sluiceway/sluiceway/blob/main/docs/later.md) says what comes after.
