# Orchestration Subagents

Orchestration subagents are your conductors and coordinators, managing complex multi-agent workflows and optimizing AI system performance. These specialists excel at the meta-level - orchestrating other agents, managing context, distributing tasks, and ensuring smooth collaboration between multiple AI systems. They turn chaos into symphony, making complex AI systems work harmoniously together.

## <� When to Use Orchestration Subagents

Use these subagents when you need to:
- **Coordinate multiple agents** for complex tasks
- **Optimize context usage** across conversations
- **Distribute tasks** efficiently among specialists
- **Handle errors** gracefully in multi-agent systems
- **Synthesize knowledge** from various sources
- **Monitor performance** of AI workflows
- **Design complex workflows** with multiple steps
- **Scale AI operations** across teams

## Usage in Claude

Project-Specific Agents: Stored in the local project's root directory under .claude/agents/. These agents are only available within that specific project and take precedence over global agents

Global/User Agents: Stored in ~/.claude/agents/. These agents are available for all your projects and sessions. They have lower precedence than project-specific agents if names conflict.