# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) rules of the apps deployed on my VPS (Kamal 2 and Cloudflare Workers), used by the Mend-hosted Renovate app.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>rael06/renovate-config"]
}
```

In short (`default.json`): runs before 7 am on Mondays (Europe/Paris), versions at least 3 days old, majors wait for an approval in the Dependency Dashboard issue, non-major npm updates grouped in one weekly pull request merged by hand (merging deploys), GitHub Actions and pinned tools (Kamal, Wrangler, Trivy, accessory images) merged automatically once the checks pass, `kamal-proxy` never automatically.

This repository is public because the Mend app does not let a public repository extend a preset kept in a private one. It holds rules only, no secret.
