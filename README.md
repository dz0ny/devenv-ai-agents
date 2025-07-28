# devenv-claude-agents

A collection of specialized Claude code agents using https://devenv.sh


## Available Agents

- **code-reviewer**: Expert code review specialist that checks for quality, security, and best practices (runs proactively)
- **architecture-designer**: System architecture and API design specialist for planning new features or refactoring
- **documentation-writer**: Technical documentation expert for maintaining docs, API specs, and changelogs
- **devops-specialist**: CI/CD and infrastructure automation expert for deployment and DevOps improvements
- **fullstack-developer**: Full-stack implementation specialist for features across the entire stack
- **quality-assurance**: Quality assurance and compliance expert for testing and regulatory verification

## Usage

To use these Claude code agents in your devenv.sh project, import this repository in your `devenv.yaml`:

```yaml title="devenv.yaml"
inputs:
  devenv-ai-agents:
    url: github:cachix/devenv-ai-agents
    flake: false
imports:
  - devenv-ai-agents
```

## Extending agents

If you'd like to expand agent prompt:


```nix
{ pkgs, lib, ... }: {
  claude.code.agents = {
    code-reviewer.prompt = ''
      NEVER say "You're right"!
    '';
  };
}
```

If you'd like to override the whole prompt:

```nix
{ pkgs, lib, ... }: {
  claude.code.agents = {
    code-reviewer.prompt = lib.mkForce ''
      Do a basic code review.
    '';
  };
}
```

## Learn More

- [Claude Code Integration](https://devenv.sh/integrations/claude-code/)
- [Composing using imports](https://devenv.sh/composing-using-imports/)
- [devenv.sh documentation](https://devenv.sh)
