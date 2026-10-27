# shared

NuGet library `Genkan.Shared`: gateway-header auth, roles, entities, RabbitMQ topology/envelopes, health, hosting defaults, options used by more than one service.

Published to GitHub Packages (`https://nuget.pkg.github.com/genkan-software/index.json`).

## Release

```bash
git tag v1.0.0 && git push --tags
```

The workflow packs with the tag as version (`v1.2.0` -> `1.2.0`, `v1.3.0-rc.1` -> prerelease) and pushes it.
This repo is **not** part of the setup repo's "release every service" tag: release it yourself first, then bump the consumers
(Dependabot opens the PRs, see the service repos).

## Versioning

SemVer. A breaking change to `EventEnvelope`, `Topology`, `GatewayHeaders` or an entity = major bump.
Entity changes also need a new migration in `migrator`.
