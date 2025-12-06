# Infrastructure Subagents

Infrastructure subagents are your DevOps and cloud computing experts, specializing in building, deploying, and maintaining modern infrastructure. These specialists handle everything from CI/CD pipelines to cloud architecture, from container orchestration to database administration. They ensure your applications run reliably, scale efficiently, and deploy seamlessly across any environment.

## <� When to Use Infrastructure Subagents

Use these subagents when you need to:
- **Design cloud architectures** for scalability and reliability
- **Implement CI/CD pipelines** for automated deployments
- **Orchestrate containers** with Kubernetes and Docker
- **Manage infrastructure as code** with modern tools
- **Optimize database performance** and administration
- **Set up monitoring and observability** systems
- **Respond to incidents** and ensure high availability
- **Secure infrastructure** and implement best practices

## Usage in Claude

Project-Specific Agents: Stored in the local project's root directory under .claude/agents/. These agents are only available within that specific project and take precedence over global agents

Global/User Agents: Stored in ~/.claude/agents/. These agents are available for all your projects and sessions. They have lower precedence than project-specific agents if names conflict.