# actions-test-fixtures

Test fixtures for actions dependency tooling. These are minimal action stubs
used by integration tests. Not intended for production use.

## Actions

- `simple-node/` -- leaf node action, no transitive dependencies
- `simple-composite/` -- composite action that uses `simple-node` + `actions/checkout@v4`
- `nested-composite/` -- composite that uses `simple-composite` (recursion depth 2)
