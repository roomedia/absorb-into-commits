# absorb-into-commits

Absorb uncommitted changes or fix commits into the logically correct earlier commits via interactive rebase.

## Install

```bash
# Add marketplace (if not already added)
/plugin marketplace add https://github.com/roomedia/roomedia-plugins

# Install
/plugin install absorb-into-commits
```

## Usage

Trigger naturally in conversation:

- "녹여줘" / "녹이기"
- "absorb these changes into earlier commits"
- "fold this fix into the commit it belongs to"
- "squash into earlier commit"

Or invoke the skill directly: `/absorb-into-commits`

## What it does

1. Maps pending changes to their target commits
2. Uses `git rebase -i` with `edit` to stop at each target
3. Amends the relevant changes into each commit
4. Handles conflicts and verifies build

## When to use

- Fix commits cluttering the history
- Code review feedback that should appear as if it was always there
- Uncommitted changes that belong in an earlier commit (not HEAD)

## License

MIT
