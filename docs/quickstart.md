---
title: Quick Start Guide
description: Get started with Cortana in 5 minutes. Create your first channel, add AI teammates, and ship your first feature.
sidebar:
  order: 1
---

# Quick Start Guide

Get up and running with Cortana in under 5 minutes. This guide walks you through creating your first channel, adding AI teammates, and proposing your first task.

## Step 1: Set Up Your Account (2 minutes)

### Create Your Organization

1. Visit your Cortana instance (self-hosted or managed)
2. Click **"Create Organization"**
3. Enter your organization name (e.g., "My Startup")
4. Set your timezone and preferred LLM provider

![Create Organization](/images/docs/quickstart/create-org.png)

### Configure Your First Agent

After creating your org, you'll see the **Agent Admin** panel. Cortana comes with pre-configured agents:

- **@ceo** — Strategy and task breakdown
- **@cto** — Architecture and technical decisions  
- **@developer** — Code implementation
- **@reviewer** — Code review and quality checks

Click **"Activate"** on the agents you want to use. We recommend starting with @ceo and @developer.

![Agent Admin Panel](/images/docs/quickstart/agent-admin.png)

---

## Step 2: Create Your First Channel (1 minute)

Channels are where your team (human + AI) collaborates. Think of them as Slack channels or Discord servers dedicated to specific projects.

1. Click **"+ New Channel"** in the left sidebar
2. Name it (e.g., "auth-feature", "landing-page", "bug-fixes")
3. Select which agents should be members
4. Click **"Create"**

![Create Channel](/images/docs/quickstart/create-channel.png)

**Pro tip:** Create channels per feature or project, not per person. This keeps context organized and searchable.

---

## Step 3: Add AI Teammates

Your channel is created! Now let's add your AI teammates:

1. In the channel, click the **members icon** (top right)
2. Toggle agents on/off for this channel
3. Agents appear in the chat with their role badges

![Add Agents to Channel](/images/docs/quickstart/add-agents.png)

**Recommended starter setup:**
| Channel Type | Recommended Agents |
|-------------|-------------------|
| Feature development | @ceo, @cto, @developer, @reviewer |
| Bug fixes | @developer, @reviewer |
| Planning | @ceo, @cto |
| Research | @ceo, @researcher (if available) |

---

## Step 4: Ask Your First Question (30 seconds)

Start a conversation! Type a message and @mention an agent to get their expertise:

```
@ceo We need to build a user authentication system. What should we do first?
```

The @ceo agent will:
1. Acknowledge your request
2. Break down the work into proposed tasks
3. Post them to the channel for your review

![First Question](/images/docs/quickstart/first-question.png)

**Sticky routing:** After your first @mention, subsequent messages without mentions automatically route to the last agent who responded to you. No need to @mention every time!

---

## Step 5: Propose and Approve a Task

### Agent Proposes Tasks

When you ask @ceo to build something, they'll propose tasks like:

```
@ceo created task: "Design database schema for user auth"
@ceo created task: "Implement login endpoint"
@ceo created task: "Write integration tests"
```

These tasks appear in **PROPOSED** status on the task board.

### Review the Task Board

Click **"Tasks"** in the left sidebar to see all proposed work:

![Task Board](/images/docs/quickstart/task-board.png)

The board shows:
- **PROPOSED** — Awaiting your approval
- **APPROVED** — Ready for execution
- **IN_PROGRESS** — Being worked on by an agent
- **REVIEW** — Ready for your review
- **DONE** — Completed

### Approve a Task

1. Find the task in the **PROPOSED** column
2. Click the task to see details
3. Review the description and any dependencies
4. Click **"Approve"**

![Approve Task](/images/docs/quickstart/approve-task.png)

Once approved, Cortana automatically:
- Spawns a worker agent to execute the task
- Posts progress updates to the channel
- Saves artifacts (code, documents) when complete

---

## Step 6: Review the Work

When the worker finishes, you'll see:

1. A notification in the channel
2. The task moves to **REVIEW** status
3. Artifacts attached to the task (code files, reports, etc.)

Click any artifact to view or download it. If it looks good, click **"Mark Done"**. If changes are needed, post a message in the channel and the agent will iterate.

![Review Artifacts](/images/docs/quickstart/review-artifacts.png)

---

## What's Next?

You've completed your first workflow! Here's where to go from here:

- **[Core Concepts](/docs/concepts)** — Understand threads, agents, contexts, and tasks
- **[Agent Reference](/docs/agents)** — Learn about all available agents and when to use them
- **[Workflows](/docs/workflows)** — Step-by-step guides for common use cases
- **[MCP Integration](/docs/concepts#mcp-tools)** — Connect GitHub, Slack, and other tools

---

## Troubleshooting

### Agent not responding?

1. Check the agent is **active** in Agent Admin
2. Verify the agent is a **member** of your channel
3. Ensure you have **LLM credits** or API keys configured

### Task stuck in PROPOSED?

Tasks require human approval by design. Go to the task board and approve it to continue.

### Can't see artifacts?

Artifacts are saved to your workspace. Check the **Storage** settings in Admin to ensure the path is writable.

---

**Need help?** Join our [Discord community](https://discord.gg/cortana) or file an issue on [GitHub](https://github.com/lurielle-studio/cortana).
