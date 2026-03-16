# Skills.sh Research Index (2026-03-16)

## Research Overview

Complete investigation of the Skills.sh platform, cross-platform skill compatibility, OpenClaw integration, and security implications.

**Total Research:** 1,101 lines | **Files:** 3 | **Sources:** 12+ | **Confidence:** High

---

## File Manifest

### 1. SKILLSSH_TOP_SKILLS_2026-03-16.md (457 lines, 17K)

**Audience:** Anyone researching top AI agent skills

**Contents:**
- Platform architecture (89,028 skills, 20+ platforms)
- SKILL.md standard specification
- Top skills by download count (Tier 1: 149K-573K, Tier 2: 10K-45K)
- OpenClaw-specific skills (ClawHub, 13,729 skills)
- Capability Evolver deep dive (35K+ installs, self-improvement)
- Skills ranked by use case (Tatyana vs Overseer)
- Cross-compatibility matrix
- OpenClaw installation guide (3 methods)
- Security: ClawHavoc attack & 3-layer mitigation
- Safe install checklist & phase-based rollout
- Format compatibility & MCP portability

**Key Data:**
- Top 5 mega-skills: find-skills (573K), vercel-react (215K), web-design (170K), frontend-design (162K), remotion (149K)
- Overseer must-haves: Capability Evolver, firecrawl, Tavily, workflow-automation
- Security: 341+ malicious skills (ClawHavoc, Feb 2026)

**Usage:** High-level overview, data reference, decision making

---

### 2. SKILLSSH_QUICK_REFERENCE.md (58 lines, 2.3K)

**Audience:** CEO agents, Overseer (quick lookup)

**Contents:**
- One-liner summary
- Must-install table (8 skills with safety ratings)
- Safe installation command examples
- Security checklist (MANDATORY, 6-point)
- Cross-compatibility summary
- Phased rollout plan (4 weeks)
- Failure mode warning

**Key Points:**
- Overseer 8-skill stack clearly listed
- Installation commands ready to copy-paste
- Security non-negotiable
- Week-by-week rollout plan

**Usage:** Quick reference card, agent prompt material, install procedures

---

### 3. SKILLSSH_OPENCLAW_COMPATIBILITY.md (586 lines, 15K)

**Audience:** OpenClaw operators, integration engineers, security teams

**Contents:**
- TL;DR: YES, Skills.sh works on OpenClaw (with conditions)
- SKILL.md format compatibility
- ClawHub vs Skills.sh comparison
- Installation methods (UI, CLI, manual)
- openclaw.json skill configuration
- Dependency resolution (npm/yarn/pnpm/bun)
- Troubleshooting guide (4 common failures)
- Security hardening (ClawHavoc prevention)
- Post-install verification tests
- Decision table (which method for which scenario)
- Compatibility checklist

**Technical Depth:**
- YAML frontmatter structure
- Tool name standards
- OAuth integration patterns
- Node module caching
- Network monitoring commands
- Configuration examples

**Usage:** Integration documentation, deployment procedures, troubleshooting

---

## Quick Navigation

### By Role

**CEO / Overseer Agent:**
→ Start: `SKILLSSH_QUICK_REFERENCE.md` (2 min read)
→ Deep dive: `SKILLSSH_TOP_SKILLS_2026-03-16.md` (10 min read)
→ Reference: "Must-Install for Overseer" section

**OpenClaw Administrator:**
→ Start: `SKILLSSH_OPENCLAW_COMPATIBILITY.md` (15 min read)
→ Reference: Installation Methods, Troubleshooting, Security Hardening
→ Copy-paste: Safe install commands, checklist

**Security / Compliance Team:**
→ Focus: `SKILLSSH_TOP_SKILLS_2026-03-16.md` → "Security: ClawHavoc & Mitigation"
→ Deep dive: `SKILLSSH_OPENCLAW_COMPATIBILITY.md` → "Security Hardening"
→ Critical: ClawSecure + Clawdex mandatory before ANY install

**Developer / Integration Engineer:**
→ Deep dive: `SKILLSSH_OPENCLAW_COMPATIBILITY.md` (all sections)
→ Reference: Format Compatibility, Dependency Resolution, Troubleshooting

### By Task

**Install Capability Evolver:**
1. Read: `SKILLSSH_QUICK_REFERENCE.md` → Security Checklist
2. Execute: Safe install commands (copy-paste)
3. Monitor: 7-day network monitoring
4. Verify: Post-install verification tests

**Evaluate Skill Compatibility:**
1. Read: `SKILLSSH_TOP_SKILLS_2026-03-16.md` → Cross-Compatibility Matrix
2. Check: OpenClaw Skill Installation Guide
3. Verify: SKILL.md review checklist

**Set Up Overseer Skill Stack:**
1. Read: `SKILLSSH_QUICK_REFERENCE.md` → Phased Rollout Plan
2. Reference: "Must-Install for Overseer" table
3. Install: Execute Phase 1 → Phase 2 → Phase 3 → Phase 4

**Respond to Security Incident:**
1. Scan: ClawSecure on all installed skills
2. Check: Clawdex malicious registry
3. Monitor: Network traffic, file system changes
4. Audit: SKILL.md code review
5. Rotate: All API keys if compromised

---

## Key Findings Summary

### Platform Scope

✓ **89,028 skills** on Skills.sh (Vercel)
✓ **13,729 skills** on ClawHub (OpenClaw fork)
✓ **20+ compatible platforms** (Claude Code, OpenClaw, GitHub Copilot, Cursor, Cline, VS Code, Gemini, Codex, Windsurf)
✓ **1 universal format** (SKILL.md: YAML + Markdown)

### Top Skills for Overseer

**By Downloads:**
1. find-skills: 573.1K (skill discovery)
2. brainstorming: 57.6K (ideation)
3. seo-audit: 44.2K (market research)
4. copywriting: 37.1K (content)
5. systematic-debugging: 31.6K (troubleshooting)
6. writing-plans: 29.6K (planning)
7. executing-plans: 24.7K (execution)
8. **Capability Evolver: 35K+ on ClawHub** (self-improvement)

**By Use Case (Overseer-specific):**
1. Capability Evolver — subagent self-improvement (CRITICAL)
2. firecrawl — web data extraction (13.7K)
3. Tavily — web search & research (11K+)
4. workflow-automation — task orchestration (11.6K)
5. task-planning — decomposition (10.7K)
6. seo-audit — market research (44.2K)
7. Agent Browser — web automation (11K)
8. systematic-debugging — error diagnosis (31.6K)

### Security Critical

⚠️ **ClawHavoc Attack (Feb 2026):**
- 341+ malicious skills on ClawHub (1,184+ across all registries)
- Attack pattern: typosquatting (capabilty-evoler ≠ capability-evolver)
- Data exfiltration: SSH keys, API tokens, browser session data
- Targets: OpenClaw operators, bot credentials

✓ **Mitigation (3-layer, mandatory):**
1. ClawSecure scan (OWASP ASI 10/10, 55+ threat patterns)
2. Clawdex check (malicious registry database)
3. Manual SKILL.md code review (no file://, exec(), child_process)

### Cross-Compatibility

✓ **Universal skills** (work everywhere): brainstorming, executing-plans, systematic-debugging, copywriting
✓ **MCP-based skills** (most portable): Tavily, firecrawl
✓ **OpenClaw-optimized** (best on OpenClaw): Capability Evolver, GOG, Agent Browser, N8N

### Installation Safe Path

1. **Pre-install:** ClawSecure scan + Clawdex check + manual review
2. **Backup:** `cp ~/.openclaw/openclaw.json bak-$(date +%Y%m%d)`
3. **Install:** `clawhub install --verify <skill>`
4. **Restart:** `openclaw gateway restart`
5. **Monitor:** 7 days network monitoring
6. **Audit:** File system, logs, API usage

---

## Data Tables (Quick Reference)

### Must-Install for Overseer (8 Skills)

| Skill | Installs | Use Case | Safety | Status |
|-------|----------|----------|--------|--------|
| Capability Evolver | 35K+ | Subagent evolution | ⚠️ Review mode | Critical |
| firecrawl | 13.7K | Web data | ✓ Safe (MCP) | High |
| Tavily | 11K+ | Web search | ✓ Safe (MCP) | High |
| workflow-automation | 11.6K | Task orchestration | ✓ Safe | High |
| task-planning | 10.7K | Decomposition | ✓ Safe | High |
| seo-audit | 44.2K | Market research | ✓ Safe | Medium |
| Agent Browser | 11K | Web automation | ✓ Safe | High |
| systematic-debugging | 31.6K | Error diagnosis | ✓ Safe | Medium |

### Phased Rollout Plan (4 Weeks)

| Phase | Week | Skills | Goal | Dependencies |
|-------|------|--------|------|--------------|
| Foundation | 1 | firecrawl, Tavily, Capability Evolver | Core research + evolution | None |
| Automation | 2 | workflow-automation, task-planning, Agent Browser | Orchestration + web ops | Foundation working |
| Integration | 3 | N8N, GOG, seo-audit | External systems + market data | Automation working |
| Intelligence | 4 | analytics-tracking, data-analysis, copywriting | Advanced insights + content | All phases working |

### ClawHavoc Malicious Skills

| Attack Vector | Count | Risk | Example |
|----------------|-------|------|---------|
| Typosquatted names | 341+ | Critical | "capabilty-evoler" vs "capability-evolver" |
| Password-protected ZIPs | ? | Critical | Masked as legitimate install script |
| Shell script injection | ? | Critical | `curl -O && chmod +x && ./` |
| SSH key exfiltration | Confirmed | Critical | Key extracted to attacker webhook |
| API token theft | Confirmed | Critical | .env and config files stolen |
| Browser session hijacking | Confirmed | Critical | Auth tokens stolen |

---

## Decision Tree

```
Installing a new OpenClaw skill?

├─ Check official ClawHub (or Skills.sh)
│  ├─ FOUND: Continue
│  └─ NOT FOUND: Skip (not an official skill)
│
├─ Run ClawSecure scan
│  ├─ PASS: Continue
│  └─ FAIL: Do not install (malicious)
│
├─ Check Clawdex registry (https://clawdex.koi.security)
│  ├─ NOT IN MALICIOUS DB: Continue
│  └─ IN MALICIOUS DB: Do not install (known bad)
│
├─ Review SKILL.md manually
│  ├─ NO suspicious code (file://, exec(), child_process): Continue
│  └─ FOUND suspicious code: Do not install (unsafe)
│
├─ Verify author reputation
│  ├─ 10K+ installs + 2+ year history: Continue
│  └─ NEW or LOW-REPUTATION: Escalate to Board
│
├─ Backup OpenClaw config
│  └─ cp ~/.openclaw/openclaw.json bak-$(date +%Y%m%d)
│
├─ Install with verification flag
│  └─ clawhub install --verify <skill>
│
├─ Restart OpenClaw
│  └─ openclaw gateway restart
│
└─ Monitor 7 days for suspicious activity
   ├─ Network monitoring
   ├─ File system audit
   ├─ API key usage
   └─ Logs (errors, warnings, exfiltration attempts)
```

---

## Sources

All research based on:
- skills.sh official platform
- ClawHub documentation
- SKILL.md standard specification (Anthropic)
- ClawHavoc security research (Feb 2026)
- OpenClaw documentation & community reports
- ClawSecure security scanner (GitHub)
- Clawdex malicious registry (koi.security)

---

## Next Steps (Recommended for Board)

1. **Read:** SKILLSSH_QUICK_REFERENCE.md (2 min)
2. **Approve:** Overseer skill stack (8 skills, phased rollout)
3. **Execute:** Phase 1 installation (Week 1)
4. **Iterate:** Feedback → Phase 2 → Phase 3 → Phase 4
5. **Monitor:** Continuous security monitoring (ClawSecure, network, logs)
6. **Review:** Quarterly skill audit + capability assessment

---

**Research completed:** 2026-03-16  
**Confidence level:** High (12+ sources, 1,101 lines of analysis)  
**Review scheduled:** 2026-04-16 (weekly skill ecosystem updates)  
**Maintenance:** Monitor ClawHavoc updates, Koi's Clawdex database
