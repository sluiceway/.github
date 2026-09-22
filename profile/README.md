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
- **It reads the tools you already use.** Pulumi, OpenTofu and Terraform, also behind Terragrunt or CDK for Terraform, Helm releases and Kubernetes manifests. One dashboard, whatever a stack is built with.

A sluiceway is a channel with a gate. Changes queue up behind the gate, and you decide what passes. The gate is called Penny.

### Status: beta

Sluiceway works end to end. It runs on a real repo with more than 50 stacks: every push updates the dashboard, a tick deploys that stack and nothing else, a Renovate update can be merged and deployed from the same box, and a scheduled scan reports drift. It is released as 0.x, so use `sluiceway/sluiceway@v0`, or pin a commit to review every update yourself. Expect rough edges, and tell us about every one you hit: the [onboarding log](https://docs.sluiceway.dev/onboarding-log/) is where they go.

Start at [sluiceway.dev](https://sluiceway.dev), or go straight to the [docs](https://docs.sluiceway.dev). The [decision records](https://docs.sluiceway.dev/why/) say why it works the way it does, and [what is not in v1](https://docs.sluiceway.dev/not-in-v1/) says what comes after.
