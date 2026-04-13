# Agent Instructions

## Git / Fork / PR Protocol

### ALWAYS use forks for PRs

When contributing to a repository where you do not have direct push access:

1. **Fork the repository** using the GitHub API (`gh repo fork`)
2. **Clone your fork** to your working directory
3. **Create a feature branch** in your fork
4. **Make and commit changes** to your fork
5. **Push to your fork** (not the upstream)
6. **Create a PR** via GitHub API targeting the upstream repository

### NEVER push directly to upstream repositories

- If you receive a "permission denied" error on push, do NOT attempt to force push or use different credentials
- Always fall back to the fork workflow instead

### Repository access notes

- **areopagus-bot** has admin access to `areopagus-bot/*` repos — push directly is OK there
- **areopagus-bot** has pull-only access to `project-areopagus/*` repos — MUST use fork workflow

## GitHub Credentials

### Credential Whitelist

Only use the following GitHub credentials:

| User | Email | Key |
|------|-------|-----|
| `areopagus-bot` | `areopagus-bot@proton.me` | SSH key: `~/.ssh/gh-bot-areopagus` |

### Using SSH Keys

- Load the appropriate key into the SSH agent: `ssh-add ~/.ssh/gh-bot-areopagus`
- For `areopagus-bot` owned repos, use `git@github.com:areopagus-bot/repo.git`
- For forks, push to `git@github.com:areopagus-bot/fork.git`
