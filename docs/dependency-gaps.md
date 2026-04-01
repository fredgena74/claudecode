# Dependency Gaps

This repository now has a reconstructed `package.json` with public npm dependencies pinned from registry metadata.

## Unresolved / internal packages
These packages are referenced by the source tree but are not available on the public npm registry:
- `@ant/claude-for-chrome-mcp`
- `@ant/computer-use-input`
- `@ant/computer-use-mcp`
- `@ant/computer-use-swift`
- `audio-capture.node`

## What this means
- Public dependencies are installable.
- The repo is still not a full open-source release artifact until the missing internal/native pieces are sourced or replaced.
- Feature flags may hide some of the unresolved paths, but the codebase still references them statically.

## Recommended next step
Decide whether the missing pieces should be:
1. vendored into the repo,
2. replaced with public equivalents, or
3. documented as internal-only feature gates.
