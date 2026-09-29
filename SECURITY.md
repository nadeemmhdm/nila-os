# Security policy

Nila OS is experimental and not suitable for protecting sensitive workloads. No production security assurance is claimed.

## Report a vulnerability

Please use GitHub's private vulnerability reporting feature if enabled. Otherwise contact the repository maintainer privately before publishing exploit details. Do not post secrets or sensitive logs in public issues.

## Scope and practices

- No AI process should run as root.
- Privileged actions must pass through a separate authenticated permission gateway.
- Never send OS passwords via Telegram.
- Never commit API tokens, personal memory, encryption keys, backups or private VM images.
- Use strong unique credentials; change any default development credentials before enabling network access.
- Validate signed updates and recovery behavior before deployment.

Security features described in project plans are not necessarily implemented.
