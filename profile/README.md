<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sluiceway/sluiceway/05403b5ab026c6a7c98837bd6dc08881dbbd0273/assets/mascot/in-sync-dark.svg">
    <img alt="Sluiceway: Penny, the sluice gate, asleep because everything is in sync" src="https://raw.githubusercontent.com/sluiceway/sluiceway/05403b5ab026c6a7c98837bd6dc08881dbbd0273/assets/mascot/in-sync-light.svg" width="440">
  </picture>
</p>

## A deploy dashboard that lives in a GitHub issue

After a merge, Sluiceway previews every infrastructure stack in your repo and keeps one issue up to date: which stacks have changes waiting, and what those changes are. You tick a stack's box, and a GitHub Actions run deploys exactly that stack.

- **It is a GitHub Action and nothing else.** No server, no database, no hosted part.
- **It never holds your credentials.** Previews and deploys run in your own runners, with your own secrets.
- **The issue is a view, never the source of truth.** Before every deploy the stack is previewed again, and nothing happens unless the fresh preview still matches what you ticked.
- **Pulumi first.** The core is tool-neutral, so OpenTofu and Terraform can follow.

A sluiceway is a channel with a gate. Changes queue up behind the gate, and you decide what passes. The gate is called Penny.

### Status

Sluiceway is being built in the open and is not usable yet. The plan, the decisions and the progress are all in [sluiceway/sluiceway](https://github.com/sluiceway/sluiceway): start with the [README](https://github.com/sluiceway/sluiceway#readme), the [build plan](https://github.com/sluiceway/sluiceway/blob/main/docs/build-plan.md) and the [decision records](https://github.com/sluiceway/sluiceway/tree/main/docs/adr). Watch the repo's releases to hear when the first version lands.
