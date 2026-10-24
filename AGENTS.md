# AGENTS.md

Ansible role that installs and configures Apache 2.4 on Debian (bookworm, trixie).

## Layout

- `defaults/main.yml`: all role variables with defaults; the README points here
- `tasks/`: `main.yml` (install, modules, config) and `vhost.yml` (virtual host handling)
- `handlers/main.yml`: Apache reload/restart handlers
- `templates/apache2/`, `files/apache2/`: Apache config templates and static module/conf files
- `meta/main.yml`, `requirements.yml`: Galaxy metadata and collection dependencies
- `molecule/default/`: integration test (Docker, Debian 13)

## Checks

- `ansible-lint` must pass with the default configuration (no `.ansible-lint`)
- `molecule test` runs the role in a container; CI runs it on Debian 12 and 13
- `ansible-lint` creates `.ansible/`; it is git ignored, never commit it

## Conventions

- Use fully qualified module names, quoted octal `mode` values and `true`/`false` booleans
- Give every task a `name`
- New or changed role variables need an entry in `defaults/main.yml` and the README
- Pin GitHub Actions to commit SHAs with a `# vX.Y.Z` comment; Dependabot keeps them current

## Commits and PRs

- Write in English, use conventional commit titles (`feat:`, `fix:`, `chore:`, `ci:`; `!` for breaking changes)
- The PR title sets the release-drafter label (`enhancement`, `bug`, `chore`, `breaking`); a breaking change bumps the major version
- Open PRs as draft and fill in `.github/pull_request_template.md`: what changed and why, plus a breaking changes section if needed
- Do not list changed files or claim test results in the description; CI covers that
