# Contributing

These guidelines apply to all repositories in the opntech organization. Repository-specific details (setup, commands, architecture) live in each repository's README.

## Workflow

- Never commit directly to the default branch (`staging` or `main`, depending on the repository).
- Branch off the default branch and open a pull request targeting it.
- Every change to production code goes through a pull request with review.
- CI must be green before merging; builds must be free of warnings and errors.

## Commits

Use Conventional Commits: `type: description` with types such as `feat:`, `fix:`, `chore:`, `refactor:`, `ci:`, `docs:`, `test:`. Keep the commit header at 100 characters or less; put additional detail in the commit body.

## Security & Coding Guideline

Binding for all contributions. Based on the [OWASP Secure Coding Practices Quick Reference Guide](https://owasp.org/www-project-secure-coding-practices-quick-reference-guide/).

1. Every change to production code is made via pull request with review.
2. CI must be green: SemGrep SAST/SCA with no open findings of severity High or above.
3. No secrets in code, configuration, or logs. Rotate exposed secrets immediately and report the incident internally.
4. Data access must always be tenant-bound (tenant separation).
5. No unmodified production data in development or test environments.
6. New dependencies: use a current version, no known CVEs of severity High or above, license checked.
