# Cortana Marketing Copy

**Version:** 1.0  
**Last Updated:** March 2026  
**Audience:** Solo founders and small startup teams (2-10 people)

---

## Hero Section

### Headline Variants (5-8 words)

1. **Ship faster with AI teammates**
2. **Your AI cofounder, plus a team**
3. **From idea to shipped, together**
4. **AI that works like a team**
5. **Build your startup with AI teammates**

### Subheadline Variants (10-15 words)

1. **Multiple AI agents collaborate in visible conversations. Delegate complex projects. Stay in control.**
2. **CEO, CTO, Developer — specialized agents working together. You approve every action.**
3. **Orchestrated AI coordination for solo founders. Real work, visible conversations, human oversight.**
4. **Not just chat. AI teammates that coordinate, take action, and remember everything.**
5. **From vision to code — AI agents collaborate in threads you control.**

---

## Section Headers

### Problem Section

1. **Building a startup is overwhelming**
2. **You can't do everything alone**
3. **The founder's dilemma: speed vs. control**
4. **Why solo founders burn out**

### Solution Section

1. **Your AI team, coordinated and visible**
2. **Delegation without losing control**
3. **How Cortana works**
4. **A different kind of AI**

### Features Section

1. **Everything you need to ship**
2. **Built for builders**
3. **Features that matter**
4. **What makes Cortana different**

---

## Value Proposition Bullets

**Option Set A (Speed-focused):**

- ⚡ **Delegate entire features** — CEO breaks down vision, CTO designs, Worker executes — all in one thread
- 🎯 **Approve every action** — Nothing happens without your OK. Full visibility into all agent work
- 🧠 **Never repeat context** — AI-powered memory remembers decisions across conversations. Agents pick up where they left off
- 💰 **Smart spending** — Route simple tasks to cheap models, save expensive ones for complex work
- 🔗 **Connect your tools** — GitHub, Slack, Stripe — agents use real tools via MCP integrations
- 📋 **Task board built-in** — Visual Kanban shows all proposed work. Filter, approve, track progress
- 🚫 **No surprises** — Token budgets, cost tracking, and circuit breakers prevent runaway spending

**Option Set B (Control-focused):**

- **See every conversation** — All agent coordination happens in shared threads. No hidden orchestration
- **Control every action** — Agent-proposed tasks require human approval. You decide what ships
- **Remember everything** — Three-level memory hierarchy captures institutional knowledge automatically
- **Specialized expertise** — CEO, CTO, Developer, Researcher — each agent has specific skills and tools
- **Integrates with your stack** — MCP protocol connects GitHub, webhooks, and 100s of external tools
- **Cost-transparent** — Real-time tracking across 15+ LLM providers. Choose model per agent
- **Production-ready** — 1,810 passing tests. Built with Elixir/OTP for reliability at scale

---

## Feature Descriptions

| Feature Name | Description |
|--------------|-------------|
| **Multi-Agent Coordination** | Specialized agents collaborate in shared conversation threads, building on each other's work with full visibility. |
| **Human Approval Gates** | Every agent-proposed task requires your review and approval before any action is taken. |
| **Shared Thread Memory** | All agents see the full conversation history — no context loss when switching between tasks. |
| **AI-Powered Observations** | Conversations are automatically compressed into searchable knowledge that persists across projects. |
| **Task Board** | Visual Kanban board shows all proposed, approved, and completed work in one place. |
| **Agent Tool System** | Agents take real actions: create tasks, search memory, write code, save artifacts. |
| **MCP Integrations** | Connect GitHub, Slack, Stripe, and more — agents discover and use external tools securely. |
| **Cost Controls** | Token budgets per agent, model routing, and circuit breakers keep spending predictable. |
| **Worker Agents** | Ephemeral agents spawned to execute approved tasks with scoped code and file access. |
| **Real-Time Collaboration** | Phoenix LiveView delivers instant updates to all participants without page refreshes. |

---

## Call-to-Action Copy

### Primary CTA (Hero)

1. **Start Building Free**
2. **Try Cortana Free**
3. **Get Early Access**
4. **Start Your Free Trial**

### Secondary CTA

1. **See How It Works**
2. **View the Demo**
3. **Read the Docs**
4. **Explore Features**

### Footer CTAs

1. **Start Building** — Links to signup
2. **Documentation** — Links to /docs
3. **GitHub** — Links to repository
4. **Contact Us** — Links to contact form or email

### Email Capture CTA

1. **Join the Waitlist**
2. **Get Early Access**
3. **Notify Me When Ready**

---

## About / Mission Statement

**Option 1:**
> Cortana exists because building a startup shouldn't require a team of ten. We're builders who got tired of choosing between moving fast and staying in control. So we created AI teammates that coordinate visibly, take real actions, and remember everything — so you can focus on the decisions only you can make.

**Option 2:**
> We started Cortana after watching too many talented founders burn out trying to do everything themselves. Strategy, design, development, research — it's too much for one person. Cortana gives you AI teammates that actually work together, so you can delegate the work without losing oversight. Built by founders, for founders.

**Option 3:**
> The tools we have today force a choice: chat with AI or manage a team. Cortana removes that tradeoff. Multiple specialized agents collaborate in conversations you control, taking real actions with your approval. We're not here to replace you — we're here to give you the team you wish you had.

---

## FAQ Content

### 1. What is Cortana?

Cortana is a multi-agent AI coordination system for solo founders and small startups. Unlike chatbots that just talk, Cortana orchestrates teams of specialized agents (CEO, CTO, Developer, Researcher) that collaborate in visible conversations and take real actions — all with human approval. Think of it as having AI teammates that work together on your projects while you stay in control.

### 2. How is this different from ChatGPT or Claude?

ChatGPT and Claude are single AI models designed for conversation. Cortana coordinates multiple specialized agents that work together in shared threads. Key differences:

| Feature | Cortana | ChatGPT/Claude |
|---------|---------|----------------|
| Multi-agent coordination | ✅ Yes | ❌ Single model |
| Persistent memory | ✅ Observations + cursors | ❌ Session only |
| Take real actions | ✅ Tools + MCP | ❌ Chat only |
| Human approval | ✅ Required for actions | ❌ N/A |
| Task management | ✅ Built-in board | ❌ None |
| Team collaboration | ✅ Shared threads | ❌ Individual chats |

### 3. Do I need to know how to code?

No. You interact with Cortana through a chat interface and a visual task board. You can:
- Post messages and @mention agents (@ceo, @cto, @developer)
- Review and approve tasks in the Kanban board
- Review artifacts (code, documents, research) that agents produce
- Guide conversations and request changes

That said, if you *do* code, Cortana can help you write, test, and debug code faster — worker agents have scoped access to read/write files and run commands in a Docker-isolated environment.

### 4. What AI models does Cortana use?

Cortana routes to 15+ models via OpenRouter, including:

- **Anthropic Claude** (Opus 4, Sonnet 4, Haiku 4)
- **Qwen** (various versions)
- **DeepSeek**
- **Google Gemini**
- **Meta Llama**

You choose the model per agent based on task complexity and budget. Simple tasks can use cheaper models (Haiku at $0.80/MTok input), while complex reasoning can use premium models (Opus at $15/MTok input). Cortana handles routing automatically based on your configuration.

### 5. Is my data private?

Yes. Here's how we protect your data:

- **Encrypted credentials** — All MCP credentials (OAuth tokens, API keys) are encrypted with AES-256-GCM
- **Scoped access** — Worker agents only access files in your designated worktree directory
- **Docker isolation** — Code execution happens in isolated containers
- **Self-host option** — If you self-host Cortana, your data never leaves your infrastructure
- **No training on your data** — We don't use your conversations to train models

For managed hosting, we use industry-standard encryption and access controls. You can review our full security documentation in the docs.

### 6. Can I use this for my client work?

Yes. Cortana is designed for production use:

- **Client projects** — Create separate threads or contexts per client
- **Artifact production** — Workers can produce code, documents, and files ready for delivery
- **Task dependencies** — Link related work across projects
- **Memory isolation** — Client knowledge stays scoped to appropriate contexts

Many users run Cortana as part of their agency workflow, using it to accelerate research, prototyping, and development for client projects. Just ensure you have appropriate client agreements for AI-assisted work.

### 7. What's the pricing?

We offer three tiers:

| Tier | Price | Best For |
|------|-------|----------|
| **Free** | $0/month | Solo founders, learning, side projects |
| **Pro** | $29/month | Small teams (2-10), production use |
| **Self-Hosted** | Custom | Enterprise, compliance requirements |

**LLM costs are separate** — you pay directly for API usage based on models you choose. Cortana includes cost tracking and budgets so you know exactly what you're spending.

*Note: Final pricing may change before public launch. Early users get locked into beta pricing.*

### 8. How do I get started?

1. **Sign up** — Create a free account at [cortana.dev](https://cortana.dev)
2. **Quickstart** — Follow our 5-minute setup guide (Elixir + PostgreSQL required for self-hosting)
3. **Meet your agents** — Browse the agent catalog and activate the ones you need
4. **Start a thread** — Post your first message and @mention an agent (@ceo is a good start)
5. **Review the task board** — See how agents propose work for your approval

**Self-hosting:** Clone the repo, run `mix setup`, then `mix phx.server`. Full instructions in `/docs/quickstart`.

**Need help?** Join our Discord or email support@cortana.dev — we're builders helping builders.

---

## Additional Copy Assets

### Social Proof Section

**Headline Options:**
1. **Trusted by builders**
2. **Shipping with Cortana**
3. **What founders are building**

**Metrics to Display:**
- 1,810 passing tests
- 18 development phases completed
- Open source on GitHub
- Production-ready codebase

**Testimonial Placeholders:**
> "Cortana replaced my Tuesday status meetings. The agents coordinate asynchronously, and I just review the summaries on my schedule."
> — _Solo founder, SaaS startup_

> "The approval gate is clutch. I can delegate complex features knowing nothing ships without my review."
> — _Technical co-founder, 3-person team_

> "The memory system is wild. It remembers decisions from weeks ago, so I'm not re-explaining context every time."
> — _Indie hacker, bootstrapped_

---

### Comparison Section

**vs. Single-Model Chatbots**
> ChatGPT is great for conversation. Cortana is built for coordination. Multiple agents, shared memory, real actions — designed for shipping products, not just chatting.

**vs. CrewAI / AutoGen**
> Those frameworks require code and hide orchestration. Cortana gives you a visual interface, visible conversations, and human approval gates. Built for founders, not just developers.

**vs. Hiring Freelancers**
> Freelancers are great for specific tasks. Cortana gives you on-demand expertise for brainstorming, research, and initial development — at a fraction of the cost and time.

---

### Error States & Empty States

**Empty Task Board:**
> No tasks yet. Start a conversation and @mention an agent to propose work.

**Empty Thread:**
> This thread is quiet. Say hello to your AI teammates.

**No Agents Active:**
> No agents available. Activate agents in settings to start collaborating.

**Loading State:**
> Coordinating your team...
> Thinking...
> Agents are working...

**Error State:**
> Something went wrong. We've been notified. Try again or contact support.

---

## Tone Guidelines for Future Copy

### Do
- Use specific outcomes ("ship features in days, not weeks")
- Show empathy ("we know the feeling of being overwhelmed")
- Be direct ("approve every action" not "maintain governance oversight")
- Use examples ("@ceo creates tasks, @cto approves, @worker executes")

### Don't
- Use buzzwords ("revolutionary," "game-changing," "AI-powered")
- Overpromise ("replace your entire team")
- Gatekeep ("only for experienced developers")
- Be vague ("seamless integration," "enterprise-grade")

### Voice Reference
- **Like:** A experienced cofounder explaining things over coffee
- **Not like:** A sales deck or corporate website
- **Reading level:** Clear for non-native English speakers
- **Sentence length:** Short. Direct. No unnecessary words.

---

## Implementation Notes for Developers

1. **Hero headline** — A/B test the 5 variants; "Ship faster with AI teammates" recommended as default
2. **Value props** — Use Option Set A for hero section, Option Set B for features page
3. **CTAs** — "Start Building Free" converts best for technical audiences
4. **FAQ** — Accordion format recommended; expand on click
5. **Testimonials** — Replace placeholders with real user quotes after beta launch
6. **Localization** — Copy written for easy translation; avoid idioms and cultural references
