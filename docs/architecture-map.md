# Architecture Map

This document captures a working map of the imported Claude Code CLI source tree.
It is based on source inspection and should be treated as maintenance notes, not as a formal product spec.

## 1. Product shape
The codebase appears to have two layers:
- a public-facing CLI surface
- internal capability layers that are selectively enabled or composed

## 2. Core engineering areas
### Token management and context control
Likely centered around:
- `src/query.ts`
- `src/cost-tracker.ts`
- `src/services/compact/*`
- `src/utils/tokenBudget.ts`
- `src/utils/tokenEstimation.ts`

### Memory and knowledge management
Likely centered around:
- `src/services/SessionMemory/*`
- `src/memdir/*`
- `src/services/extractMemories/*`
- `src/services/autoDream/*`

### Multi-agent orchestration
Likely centered around:
- `src/tools/AgentTool/*`
- `src/services/swarm/*`
- `src/utils/concurrentSessions.ts`
- `src/utils/standaloneAgent.ts`

### Security and permissioning
Likely centered around:
- `src/utils/permissions/*`
- `src/tools/BashTool/*`
- `src/tools/FileWriteTool/*`
- `src/services/teamMemorySync/*`
- `src/utils/secureStorage/*`

### UI / terminal system
Likely centered around:
- `src/components/*`
- `src/ink/*`
- `src/components/PromptInput/*`
- `src/components/messages/*`

### Platform / ecosystem layer
Likely centered around:
- `src/services/mcp/*`
- `src/utils/plugins/*`
- `src/commands/install-github-app/*`
- `src/commands/install-slack-app/*`

## 3. Working taxonomy
A practical maintenance taxonomy for this repo:
1. CLI entrypoints and commands
2. Tool execution and safety
3. Session and memory systems
4. UI and interactive state
5. Services / integrations
6. Utilities and shared infrastructure

## 4. Maintenance implications
- Changes to token handling should be reviewed for performance regressions.
- Security-related code should be treated as high-risk and validated carefully.
- Memory and agent orchestration code should be tested against session recovery and cross-session behavior.
- UI changes should remain compatible with terminal and component renderers.
