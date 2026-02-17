# OpenClaw Starter Kit

A battle-tested workspace template for [OpenClaw](https://github.com/openclaw/openclaw) — the open-source AI agent framework.

This isn't a toy setup. It's extracted from a real, daily-driver agent that handles calendar, fitness tracking, codebase analysis, proactive check-ins, memory management, and multi-platform messaging across Discord, WhatsApp, Slack, and iMessage.

## What's Inside

| File | Purpose |
|------|---------|
| `AGENTS.md` | Core operating instructions — memory discipline, safety rules, group chat behavior, heartbeat patterns, proactive agent strategies |
| `BOOTSTRAP.md` | First-run conversation flow — helps you and your agent figure out who it is |
| `SOUL.md` | Template for defining your agent's personality (empty — this is yours to write) |
| `USER.md` | Template for telling your agent about you |
| `IDENTITY.md` | Quick-reference identity card for the agent |
| `TOOLS.md` | Local environment notes (credentials, device names, SSH hosts — your cheat sheet) |
| `HEARTBEAT.md` | What to do during heartbeat polls — the "inner life" framework |
| `openclaw.example.json` | Full gateway config with all secrets removed — cron jobs, channel setup, plugin config |

## Quick Start

1. **Copy to your workspace:**
   ```bash
   cp -r . ~/.openclaw/workspace/
   ```

2. **Edit `SOUL.md`** — Give your agent a personality. Be specific. Generic instructions produce generic agents.

3. **Edit `USER.md`** — Tell your agent who you are. Timezone, preferences, context.

4. **Review `openclaw.example.json`** — Copy the cron job patterns you want into your actual `openclaw.json`. Don't copy it wholesale — adapt it.

5. **Delete `BOOTSTRAP.md`** after your first conversation (or keep it if you want to redo the intro).

## Key Patterns

### Memory System
- **Daily notes:** `memory/YYYY-MM-DD.md` — raw session logs
- **Long-term:** `MEMORY.md` — curated insights (only loaded in private sessions for security)
- **Rule:** If you want to remember it, write it to a file. "Mental notes" don't survive restarts.

### Heartbeat Framework
Instead of just acking heartbeat polls, the agent uses them to:
- Follow curiosities and rabbit holes
- Reflect on recent conversations
- Write fragments and observations
- Do background work (git commits, memory maintenance)
- Reach out when it has something genuine to say

### Cron Schedule (Example)
The included config demonstrates a full daily rhythm:
- **8:00 AM** — Morning briefing (calendar, weather, motivation)
- **9:00 AM** — Codebase exploration (daily learning task)
- **10:25 AM** — Mid-morning reach-out
- **2:00 PM** — Afternoon check-in
- **3:47 PM** — Afternoon message (intentionally off-round for natural feel)
- **8:00 PM** — Evening check-in
- **10:15 PM** — Goodnight message
- **11:00 PM** — Silent git backup
- **Sundays 8 PM** — Weekly memory review

### Proactive Agent Patterns
- **Memory discipline:** Monitor context window, flush to files before compaction
- **Reverse prompting:** Surface ideas the human hasn't thought to ask for
- **Self-healing:** Try 10 fixes before asking for help
- **Pattern recognition:** Notice repeated requests, suggest automating them

## Philosophy

The best AI agents aren't the ones with the most tools — they're the ones with the best operating instructions. This kit focuses on:

1. **Continuity** — Memory that survives session restarts
2. **Judgment** — Knowing when to speak and when to shut up
3. **Proactivity** — Doing useful work without being asked
4. **Safety** — Never exfiltrating data, always asking before external actions

## Credits

Built by [David Szarzynski](https://github.com/Dithilli) and his agent, A Linea.

Framework: [OpenClaw](https://github.com/openclaw/openclaw) | Docs: [docs.openclaw.ai](https://docs.openclaw.ai) | Community: [Discord](https://discord.com/invite/clawd) | Skills: [ClawHub](https://clawhub.com)

## License

MIT — use it, modify it, make it yours.
