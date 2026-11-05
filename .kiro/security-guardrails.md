# Infrastructure Security Guardrails

## Core Syntax & Strategy
* **IaC Engine:** Maintain explicit, clean Terraform syntax.
* **Remediation Strategy:** When resolving Checkov failures, always append missing security attributes directly to the offending resource code blocks.

## Data Protection & Resilience
* **Backup Enforcement:** Always locate and review associated backup lifecycle configurations (e.g., `aws_efs_backup_policy`). Ensure the backup status is explicitly set to `ENABLED` to prevent data loss vulnerabilities.

## Strict Disallowances
* **Prohibited Layouts:** Never introduce wide-open network paths (e.g., `0.0.0.0/0`) or unencrypted data volumes to resolve a compilation issue.

