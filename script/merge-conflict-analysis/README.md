# Lockfile Merge Conflict Analysis

Scripts for testing git merge behavior with `actions.lock` files across
realistic development scenarios. Used to inform the lockfile format design
for [ADR 10032](https://github.com/github/c2c-actions/pull/10106).

## Usage

```bash
python3 lockfile_merge_test.py
```

No dependencies beyond Python 3.8+ and git. The script creates temporary
git repos, runs merge scenarios, and reports results. All temp files are
cleaned up automatically.

## What it tests

1. **Stress test** — 100 workflows with sequential names (worst case)
2. **Insertion position** — where new entries sort in the file
3. **Realistic names** — descriptive workflow names (typical repo)
4. **Per-workflow lockfiles** — comparison with one `.lock` per `.yml`
5. **Union merge strategy** — `.gitattributes merge=union` behavior
