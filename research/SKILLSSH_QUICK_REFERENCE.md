# Skills.sh Quick Reference for Overseer CEO

## One-Liner Summary
89,028 AI agent skills via SKILL.md standard. Top for Overseer: Capability Evolver (self-improve), firecrawl (web data), Tavily (search), workflow-automation (orchestration). Risk: ClawHavoc malicious skills—scan before install.

## Must-Install for Overseer

| Skill | Installs | Primary Use | Safety |
|-------|----------|------------|--------|
| **Capability Evolver** | 35K+ | Subagent self-improvement | ⚠️ Review flag only |
| **firecrawl** | 13.7K | Web scraping, data extraction | ✓ Safe (MCP) |
| **Tavily** | 11K+ | Web search, fact-checking | ✓ Safe (MCP) |
| **workflow-automation** | 11.6K | Task orchestration | ✓ Safe |
| **task-planning** | 10.7K | Task decomposition | ✓ Safe |
| **seo-audit** | 44.2K | Market research automation | ✓ Safe |
| **Agent Browser** | 11K | Complex web automation | ✓ Safe |
| **systematic-debugging** | 31.6K | Error diagnosis | ✓ Safe |

## Installation Command (Safe)

```bash
# Install with ClawSecure pre-scan + verify flag
clawhub install --verify openclaw/skills/capability-evolver

# Check security before install
clawsecure scan --skill "capability-evolver"

# Backup first
cp ~/.openclaw/openclaw.json ~/.openclaw/openclaw.json.bak-$(date +%Y%m%d)
```

## Security Checklist (MANDATORY)

Before ANY skill install:
- [ ] Name matches official source exactly (typosquat check: "capabilty-evoler" ≠ "capability-evolver")
- [ ] ClawSecure scan passes
- [ ] Clawdex check: https://clawdex.koi.security
- [ ] No copy-paste shell scripts, password-protected ZIPs
- [ ] Author has 10K+ installs + 2+ years on ClawHub
- [ ] SKILL.md readable, no `file://`, `exec()`, `child_process`

## Cross-Compatibility

✓ All can run on Claude Code + OpenClaw + GitHub Copilot  
✓ MCP-based (Tavily, firecrawl) most portable  
⚠️ Capability Evolver optimized for OpenClaw

## PhaseD Rollout Plan

**Week 1:** firecrawl, Tavily, Capability Evolver  
**Week 2:** workflow-automation, task-planning, Agent Browser  
**Week 3:** seo-audit, systematic-debugging  
**Week 4:** Additional per need (copywriting, data-analysis, N8N)

---

**Failure Mode:** Typosquatted malicious skill installed → SSH keys + API tokens exfiltrated to attacker webhook.  
**Prevention:** ClawSecure + Clawdex scanning is NOT optional.
