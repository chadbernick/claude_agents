## Claude Code Agents

This repository serves as the definitive collection of Claude Code subagents - specialized AI agents designed for specific development or strategic tasks. 

## Usage in Claude

Project-Specific Agents: Stored in the local project's root directory under .claude/agents/. These agents are only available within that specific project and take precedence over global agents

Global/User Agents: Stored in ~/.claude/agents/. These agents are available for all your projects and sessions. They have lower precedence than project-specific agents if names conflict.