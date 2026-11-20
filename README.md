# Held in Common: shared memory for teams and their AIs

**Live:** https://heldincommon.app · Docs: https://heldincommon.app/docs
**Built by:** Dan Barella, Through the Looking Glass LLC · 2026
**Source:** private. This repo is a case study.

## The problem

Your AI remembers you. Nobody's AI remembers what *we* agreed. When partners use different AIs in different chats, decisions get lost, repeated or quietly rewritten.

## What it does

Held in Common (called "Commons" inside the tools) gives a small team one record of what was agreed. Every proposal, decision and ask records who proposed it, who decided, and which AI helped.

**House rule: the AI proposes, a person decides.** Nothing becomes shared until a human says yes, and when people disagree, Commons keeps both versions instead of picking one.

## What I built

- An **MCP server with 50+ tools**, connected to Claude, ChatGPT and Grok.
- **Consent-gated writes:** proposals, accepts and declines, ranked by urgency and due date, with corrections flagged first.
- **Per-thread progress and a "baton" handoff,** so long work carries from one AI chat to the next without starting over.
- **Multiple workspaces** with GitHub sync and PR-based shipping.
- A **public docs page** whose tool list is checked against the server on every build, so it can't drift.
- **Submitted to Anthropic's connector directory;** in review as of November 2026.
- **Stripe billing,** tested end to end in test mode; deleting a paid space cancels its subscription first.

## In use

Runs daily across more than a dozen workspaces, including a 501(c)(3)'s decision record.

## Stack

Model Context Protocol · Render · Supabase · Resend · Stripe · GitHub
