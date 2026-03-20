---
title: Workflows
description: Step-by-step guides for common Cortana workflows: building features, debugging, releases, code review, and DevOps automation.
sidebar:
  order: 4
---

# Workflows

This guide covers common workflows with Cortana. Each workflow includes step-by-step instructions and expected outcomes.

---

## 1. Building a New Feature from Scratch

**Time:** 30-60 minutes  
**Agents involved:** @ceo, @cto, @senior-dev, @code-reviewer

### Overview

```mermaid
flowchart TD
    A[User defines feature] --> B[@ceo breaks into tasks]
    B --> C[Human approves tasks]
    C --> D[@cto reviews architecture]
    D --> E[@senior-dev implements]
    E --> F[@code-reviewer checks quality]
    F --> G[Human reviews and deploys]
```

### Step 1: Define the Feature

Create a new channel for the feature and describe what you want to build.

```
Channel: user-auth-system

User: @ceo We need to build a complete user authentication system with:
- Email/password signup and login
- JWT tokens with refresh rotation
- Password reset flow
- Rate limiting

Create a task breakdown.
```

### Step 2: CEO Creates Tasks

The @ceo agent responds with a task breakdown:

```
@ceo: I've created the following tasks for review:

[ ] 1. Design database schema for users and sessions
[ ] 2. Implement signup endpoint with validation
[ ] 3. Implement login endpoint with JWT generation
[ ] 4. Add refresh token rotation
[ ] 5. Build password reset flow
[ ] 6. Write integration tests
[ ] 7. Set up rate limiting

Approve these to begin implementation.
```

### Step 3: Review and Approve Tasks

Go to the **Task Board** and review each task:

1. Click each task to see details
2. Check dependencies (schema before implementation)
3. Approve all tasks, or modify descriptions as needed
4. Tasks move to **APPROVED** status

**Pro tip:** Approve tasks in dependency order. The worker system respects dependencies automatically.

### Step 4: CTO Reviews Architecture (Optional)

For complex features, ask @cto to review the architecture:

```
User: @cto Review the architecture for this auth system. 
Any security concerns or design improvements?
```

@cto responds with recommendations based on best practices and memory of past decisions.

### Step 5: Workers Implement

Workers are automatically spawned for approved tasks:

1. **Task 1 (Schema)** → Worker writes schema migration
2. **Task 2 (Signup)** → Worker implements endpoint
3. **Task 3 (Login)** → Worker implements JWT logic
4. ... continues through all tasks

Each worker:
- Reads the task description
- Searches memory for relevant context
- Writes code and saves artifacts
- Marks task as **REVIEW** when done

### Step 6: Code Reviewer Checks Quality

Once implementation is complete, @code-reviewer automatically reviews:

```
@code-reviewer: Review complete for user-auth-system

✅ No hardcoded secrets detected
✅ Password hashing uses bcrypt with salt
✅ JWT implementation follows best practices
⚠️ Suggestion: Add rate limiting to login endpoint
```

### Step 7: Human Review and Merge

Review all artifacts:

1. Go to **Task Board** → Filter by **REVIEW**
2. Click each task to see code artifacts
3. Click **"Mark Done"** for each accepted task
4. For changes needed, post in channel: "@senior-dev Address the rate limiting concern"

Once all tasks are **DONE**, merge to main branch and deploy.

### Expected Artifacts

```
artifacts/
├── 01_user_schema_migration.exs
├── 02_signup_handler.ex
├── 03_login_handler.ex
├── jwt_token_module.ex
├── password_reset_handler.ex
├── auth_integration_test.exs
└── review_report.md
```

---

## 2. Debugging a Production Issue

**Time:** 10-30 minutes  
**Agents involved:** @senior-dev, @cto

### Scenario

Production logs show 500 errors on the login endpoint.

### Step 1: Report the Issue

```
User: @senior-dev Production is throwing 500 errors on /api/login.
Error starts at 2:30 PM UTC. Logs show:

[error] FunctionClauseError at login_handler.ex:45
No clause matching: login(nil, _)

Investigate and fix immediately.
```

### Step 2: Agent Investigates

The @senior-dev agent:

1. Reads the error logs
2. Uses `grep` to find the relevant code
3. Uses `search_memory` to check recent changes
4. Identifies the root cause

```
@senior-dev: Found the issue. The login_handler.ex:45 doesn't handle
nil password input. A recent frontend change sends empty string ""
instead of omitting the password field.

Root cause: Missing validation clause for empty password.

Proposed fix:
1. Add validation for empty password
2. Return 400 "Password required" instead of 500
3. Add test case for this edge case

Creating task for your approval.
```

### Step 3: Approve the Fix

A task is created:

```
Task: Fix login handler null password bug
Status: PROPOSED
Priority: HIGH

Approve to deploy fix.
```

Click **Approve**. The worker:
1. Adds validation clause
2. Writes test case
3. Runs tests locally
4. Saves fix as artifact

### Step 4: Review and Deploy

Review the fix:

```
@senior-dev: Fix complete. Changes:
- login_handler.ex: Added validation for empty password
- login_handler_test.exs: Added test case

All tests passing. Ready to deploy.
```

Click **Mark Done**, then deploy via your CI/CD pipeline.

### Step 5: Post-Mortem (Optional)

After the fix, create a post-mortem task:

```
User: @cto Document this incident and propose prevention measures.

@cto: [Creates observation and suggests]:
1. Add input validation to all auth endpoints
2. Implement contract testing between frontend and backend
3. Add alerting for 5xx error rate > 1%
```

---

## 3. Planning a Release

**Time:** 20-40 minutes  
**Agents involved:** @ceo, @cto

### Overview

Plan a release with @ceo coordinating tasks and @cto reviewing technical readiness.

### Step 1: Request Release Planning

```
User: @ceo Plan our Q2 release. Target date: June 15.
Features to include:
- User authentication (new)
- Dashboard redesign (updated)
- API rate limiting (new)
- Mobile responsive improvements (updated)

Create a release plan with timeline.
```

### Step 2: CEO Creates Release Tasks

```
@ceo: Release plan created for Q2 (target: June 15)

Tasks:
[ ] 1. Complete user authentication system (Dep: none, Due: May 1)
[ ] 2. Dashboard redesign implementation (Dep: none, Due: May 15)
[ ] 3. API rate limiting (Dep: auth system, Due: May 20)
[ ] 4. Mobile responsive improvements (Dep: dashboard, Due: May 25)
[ ] 5. Integration testing (Dep: all features, Due: June 1)
[ ] 6. Performance testing and optimization (Dep: task 5, Due: June 5)
[ ] 7. Documentation update (Dep: all features, Due: June 10)
[ ] 8. Release candidate and final review (Dep: all, Due: June 12)

Critical path: Auth → Rate limiting → Integration testing
Buffer: 3 days for unexpected issues
Risk: Mobile improvements may delay if dashboard takes longer
```

### Step 3: CTO Reviews Technical Feasibility

```
User: @cto Review the Q2 release plan. Any technical risks?

@cto: Reviewing plan...

Risks identified:
1. Auth system integration with rate limiting may need extra time
   → Suggest: Start rate limiting design now, implement after auth is stable
2. Mobile responsive work depends on dashboard completion
   → Suggest: Parallel tracks for mobile (CSS-only) and dashboard (JS)
3. Integration testing compressed into 1 week
   → Suggest: Extend to 10 days, start writing tests earlier

Recommendation: Push release to June 18 for 3-day buffer
```

### Step 4: Adjust and Approve

Update tasks based on CTO feedback:

1. Extend integration testing to 10 days
2. Adjust mobile and dashboard to run in parallel
3. Update release target to June 18
4. Approve all tasks

### Step 5: Track Progress Weekly

Create a weekly check-in:

```
User: @ceo What's the status of Q2 release?

@ceo: [Queries task board and reports]:
✅ Task 1 (Auth): DONE
🟡 Task 2 (Dashboard): IN_PROGRESS (80%, tracking to due date)
🟡 Task 3 (Rate limiting): IN_PROGRESS (40%, blocked on auth completion)
⏳ Task 4 (Mobile): Not started (waiting on dashboard)
⏳ Task 5-8: Pending

Overall: On track, 2-day buffer remaining
```

---

## 4. Code Review Workflow

**Time:** 15-30 minutes  
**Agents involved:** @senior-dev, @code-reviewer

### Scenario

A developer (or worker) has completed a feature and needs a code review before merging.

### Step 1: Request Review

```
User: @code-reviewer Review the PR for the authentication feature.
PR: https://github.com/lurielle-studio/cortana/pull/123

Check for:
- Security vulnerabilities
- Code quality and best practices
- Test coverage
```

### Step 2: Agent Reviews Code

@code-reviewer reads the PR diff and analyzes:

```
@code-reviewer: Review complete for PR #123

✅ Security:
- Password hashing uses bcrypt with cost=12
- JWT tokens have appropriate expiration (15min access, 7d refresh)
- No hardcoded credentials detected

⚠️ Issues:
1. login_handler.ex:142 — Missing error handling for database timeout
   → Suggest: Wrap in try/rescue, return 503 with retry-after header

2. token_module.ex:89 — Token secret loaded from environment
   → Suggest: Add validation to ensure SECRET_KEY is set at startup

3. Tests — Integration test coverage at 78%
   → Suggest: Add test for refresh token rotation edge case

📈 Code Quality: A-
- Good function decomposition
- Clear variable names
- Consistent style
```

### Step 3: Developer Addresses Feedback

```
User: @senior-dev Address the code review feedback for PR #123

@senior-dev: Making changes:
1. Adding database timeout handling to login_handler.ex
2. Adding SECRET_KEY validation at app startup
3. Adding test for refresh token rotation

Committing fixes to PR branch.
```

### Step 4: Re-Review

```
User: @code-reviewer Re-review PR #123 after fixes

@code-reviewer: All issues addressed

✅ Security vulnerabilities: None
✅ Code quality: Improved to A
✅ Test coverage: 85% (meets team standard)

Recommendation: APPROVE for merge
```

### Step 5: Merge and Deploy

1. Approve the PR in GitHub
2. Merge to main branch
3. Deploy via CI/CD pipeline
4. Update task status to **DONE**

---

## 5. DevOps Automation Workflow

**Time:** 30-60 minutes  
**Agents involved:** @devops-automator, @cto

### Scenario

Set up CI/CD pipeline for automated testing and deployment.

### Step 1: Request CI/CD Setup

```
User: @devops-automator Set up CI/CD for our Elixir app.
Requirements:
- Run tests on every PR
- Deploy to staging on merge to main
- Deploy to production on release tag
- Use GitHub Actions
- Dockerize the application
```

### Step 2: DevOps Agent Proposes Implementation

```
@devops-automator: CI/CD setup plan created

Tasks:
[ ] 1. Create Dockerfile optimized for Elixir (multi-stage build)
[ ] 2. Create docker-compose.yml for local development
[ ] 3. Create GitHub Actions workflow for tests
[ ] 4. Create GitHub Actions workflow for staging deploy
[ ] 5. Create GitHub Actions workflow for production release
[ ] 6. Set up environment secrets (DATABASE_URL, SECRET_KEY)

Approve to begin implementation.
```

### Step 2: CTO Reviews Infrastructure Plan

```
User: @cto Review the CI/CD infrastructure plan. Any concerns?

@cto: Reviewing...

Recommendations:
1. Add caching for Mix dependencies (speeds up tests by ~40%)
2. Add Elixir version matrix (test on 1.14, 1.15)
3. Add health check endpoint for deployment verification
4. Add rollback mechanism for failed production deploys
```

### Step 3: Approve Tasks with Revisions

Incorporate CTO feedback into tasks:

1. Add Mix dependency caching to workflow
2. Add Elixir version matrix
3. Create health check endpoint task
4. Add rollback workflow

Approve all tasks.

### Step 4: Implementation and Testing

Workers implement:

```
Worker: Created artifacts:
- Dockerfile (multi-stage, 180MB final image)
- docker-compose.yml (app, db, redis)
- .github/workflows/ci.yml (test on PR)
- .github/workflows/deploy-staging.yml
- .github/workflows/deploy-prod.yml
- lib/app/health_check.ex
- .env.example (template for secrets)

All files ready for review.
```

### Step 5: Human Review and Configuration

Review artifacts and configure secrets:

1. Review Dockerfile and workflows
2. Add secrets in GitHub repository settings:
   - `DATABASE_URL`
   - `SECRET_KEY_BASE`
   - `DEPLOY_TOKEN` (for production)
3. Mark tasks as **DONE**

### Step 6: Test the Pipeline

```
User: @devops-automator Create a test PR to verify the CI pipeline

Worker: Created PR #124 "Test CI pipeline"
        → GitHub Actions running...
        → Tests passed on Elixir 1.14 and 1.15
        → Build time: 3m 20s (with caching)

CI pipeline verified working.
```

### Step 7: Deploy to Production

When ready for release:

1. Create release tag: `git tag v1.0.0 && git push --tags`
2. Production workflow triggers automatically
3. Deploys to production with health check verification
4. Posts success/failure to channel

---

## Workflow Tips

### Parallel Workflows

Multiple tasks can run in parallel if they don't have dependencies:

```
Approved: Task A (independent)
Approved: Task B (independent)
Pending:  Task C (depends on A and B)

→ Workers for A and B run simultaneously
→ Worker for C waits for both to complete
```

### Async Collaboration

Humans don't need to be present for agent work:

```
9:00 AM: User approving tasks before meetings
9:05 AM: Workers executing while user is in meetings
12:00 PM: User returns, reviews completed work
```

### Interrupting Workflows

Need to stop a workflow?

1. Go to **Task Board**
2. Find the task in **IN_PROGRESS**
3. Click **"Cancel Task"**
4. Agent posts confirmation and stops work

### Resuming Workflows

Workers remember context via cursors:

```
Worker on Task A: 50% complete, user cancels
→ Worker saves progress observation
→ Later: Approve Task A again
→ New worker resumes from saved observation
```

---

**Related:**
- [Quick Start Guide](/docs/quickstart) — Get started in 5 minutes
- [Core Concepts](/docs/concepts) — Understand the system
- [Agent Reference](/docs/agents) — Agent capabilities
- [Architecture Overview](/docs/architecture) — Technical internals
