# Entry Points

## Primary CLI bootstrap
- `src/entrypoints/cli.tsx`
  - fast-path bootstrap
  - handles special flags before loading the full CLI
  - best starting point for distribution/packaging work

## Main runtime
- `src/main.tsx`
  - main application startup path
  - wires config, telemetry, tools, and session state

## Interactive launcher
- `src/replLauncher.tsx`
  - REPL / interactive session launcher

## Initialization surfaces
- `src/entrypoints/init.ts`
  - startup initialization and telemetry setup
- `src/entrypoints/sdk/*`
  - SDK-facing schema and control surfaces

## Maintenance note
`cli.tsx` is the best file to preserve as the external entrypoint. `main.tsx` is the heavy runtime path after bootstrap decisions are made.
