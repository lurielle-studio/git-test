---
title: Cortana Documentation
description: Learn how to use Cortana effectively. Quick start guides, core concepts, agent reference, workflows, and architecture documentation.
sidebar:
  order: 0
---

# Cortana Documentation

Welcome to the Cortana documentation. This guide covers everything you need to know to use Cortana effectively for your startup or small team.

## What is Cortana?

Cortana is a **multi-agent AI coordination system** that enables teams of AI agents to collaborate in shared conversation threads with human oversight. Unlike single-model chatbots, Cortana orchestrates multiple specialized agents that can see each other's work, coordinate through a patented turn system, and take real actions via tools and MCP integrations.

**Core Value Proposition:**
> "Ship faster with AI teammates that actually work together. Cortana coordinates multiple AI agents in visible conversations, so you can delegate complex projects while staying in control."

---

## Getting Started

### New to Cortana?

Start here to get up and running quickly:

- **[Quick Start Guide](/docs/quickstart)** — Get started in 5 minutes
  - Create your first channel
  - Add AI teammates
  - Ask your first question
  - Propose and approve a task

### Understanding the System

Once you've tried the basics, deepen your understanding:

- **[Core Concepts](/docs/concepts)** — Fundamental building blocks
  - Threads: The unit of conversation
  - Channels: Where your team lives
  - Agents: Your AI teammates
  - Contexts: Cross-thread awareness
  - Tasks: How work gets done
  - MCP Tools: Extending capabilities

---

## Reference Documentation

### Agent Reference

- **[Agent Reference](/docs/agents)** — Complete guide to all agents
  - @ceo — Strategy and planning
  - @cto — Architecture decisions
  - @senior-dev — Code implementation
  - @frontend-dev — UI/UX development
  - @devops-automator — CI/CD and infrastructure
  - @code-reviewer — Code quality checks
  - Custom agents — Create your own

### Workflows

- **[Workflows](/docs/workflows)** — Step-by-step guides
  - Building a new feature from scratch
  - Debugging a production issue
  - Planning a release
  - Code review workflow
  - DevOps automation

---

## Technical Documentation

### Architecture

- **[Architecture Overview](/docs/architecture)** — Technical deep-dive
  - System components
  - Thread coordination model
  - Agent dispatch flow
  - Memory hierarchy
  - Data model
  - Deployment architecture

For developers who want to understand the internals or contribute to the codebase.

---

## Additional Resources

### Codebase

- **GitHub Repository:** [`lurielle-studio/cortana`](https://github.com/lurielle-studio/cortana)
- **Development Guidelines:** [`AGENTS.md`](https://github.com/lurielle-studio/cortana/blob/main/AGENTS.md)
- **Build Progress:** [`docs/build-progress-3.md`](https://github.com/lurielle-studio/cortana/blob/main/docs/build-progress-3.md)

### Community

- **Discord:** [Join our community](https://discord.gg/cortana)
- **Issues:** [Report bugs or request features](https://github.com/lurielle-studio/cortana/issues)

---

## Quick Reference

### Key Features

| Feature | Description |
|---------|-------------|
| **Multi-Agent Coordination** | Multiple AI agents collaborate in shared threads |
| **Human Approval Gate** | All agent actions require human approval |
| **Shared Memory** | AI-powered observations capture context |
| **MCP Integration** | Connect GitHub, Slack, and other tools |
| **Task Board** | Visual Kanban for tracking work |
| **Cost Controls** | Token budgets and model routing |

### Default Agents

| Agent | Role | Best For |
|-------|------|----------|
| @ceo | Strategy | Task breakdown, planning |
| @cto | Architecture | Technical decisions |
| @senior-dev | Development | Feature implementation |
| @frontend-dev | Frontend | UI/UX development |
| @devops-automator | DevOps | CI/CD, deployments |
| @code-reviewer | Review | Code quality checks |

### Task Lifecycle

```
PROPOSED → APPROVED → IN_PROGRESS → REVIEW → DONE
                ↓
            REJECTED
```

---

## Getting Help

### Documentation Not Clear?

1. Check the **[Quick Start Guide](/docs/quickstart)** for basic workflows
2. Review **[Core Concepts](/docs/concepts)** for fundamental understanding
3. Search this documentation using the search bar (top right)

### Still Need Help?

- **GitHub Issues:** [File an issue](https://github.com/lurielle-studio/cortana/issues)
- **Discord:** [Join our community](https://discord.gg/cortana)
- **Email:** Support (for managed hosting customers)

---

## Contributing

We welcome contributions to both Cortana and this documentation!

### Contributing to Docs

1. Fork the repository
2. Make your changes to the `.md` files in `/docs/`
3. Submit a pull request

See [`CONTRIBUTING.md`](https://github.com/lurielle-studio/cortana/blob/main/CONTRIBUTING.md) for guidelines.

### Contributing to Code

1. Read [`AGENTS.md`](https://github.com/lurielle-studio/cortana/blob/main/AGENTS.md) for development guidelines
2. Check open issues for good first bugs
3. Submit a pull request with tests

---

**Last updated:** March 2026  
**Version:** 1.0.0  
**Codebase:** Elixir 1.15+, Phoenix 1.8
