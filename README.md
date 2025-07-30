# devenv-ai-agents

A collection of specialized AI agents like [Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) using https://devenv.sh


## Available Agents

- **nix-specialist**: Expert nix and nixos review specialist that checks for quality and best practices (runs proactively)
## Usage

To use these Claude code agents in your devenv.sh project, import this repository in your `devenv.yaml`:

```yaml title="devenv.yaml"
inputs:
  dz0ny-claude-agents:
    url: github:dz0ny/devenv-ai-agents
    flake: false
imports:
  - dz0ny-claude-agents
```

## Learn More

- [Claude Code Integration](https://devenv.sh/integrations/claude-code/)
- [Composing using imports](https://devenv.sh/composing-using-imports/)
- [devenv.sh documentation](https://devenv.sh)
