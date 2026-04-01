# Maintenance Roadmap

## Immediate priorities
- Add a real `package.json` / workspace manifest if this tree is meant to be built and tested independently.
- Decide on licensing before broad redistribution.
- Identify the actual build/test entrypoints.
- Add a minimal CI workflow once the toolchain is known.

## Short-term priorities
- Create a file inventory by subsystem.
- Add a top-level architecture diagram or module map.
- Document the maintenance process for issues, releases, and version tags.
- Separate verified facts from analysis notes.

## Medium-term priorities
- Add smoke tests for the CLI startup path.
- Add tests around token handling / compaction / permissions.
- Validate plugin / MCP integration boundaries.
- Reduce the “imported snapshot” feeling by adding reproducible setup instructions.

## Suggested issue backlog
1. Reconstruct package manifest
2. Add build and test commands
3. Add CI baseline
4. Add architecture overview
5. Add release checklist
6. Add license decision note
