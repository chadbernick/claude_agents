# Developer Experience Subagents

Developer Experience subagents are your productivity multipliers, focusing on making development faster, easier, and more enjoyable. These specialists handle everything from code refactoring to documentation, from build optimization to Git workflows. They remove friction from the development process, automate repetitive tasks, and help teams work more efficiently with better tools and practices.

## <� When to Use Developer Experience Subagents

Use these subagents when you need to:
- **Refactor legacy code** for better maintainability
- **Optimize build systems** for faster development
- **Create developer tools** and CLI applications
- **Write technical documentation** that developers love
- **Manage dependencies** and package updates
- **Streamline Git workflows** and branching strategies
- **Modernize codebases** with latest practices
- **Improve developer productivity** across teams

## Usage in Claude

Project-Specific Agents: Stored in the local project's root directory under .claude/agents/. These agents are only available within that specific project and take precedence over global agents

Global/User Agents: Stored in ~/.claude/agents/. These agents are available for all your projects and sessions. They have lower precedence than project-specific agents if names conflict.