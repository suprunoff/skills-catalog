# Skills.sh Platform Research: Top AI Agent Skills 2026

**Date:** 2026-03-16 | **Sources:** 12+ | **Confidence:** high

## Executive Summary

Skills.sh is a Vercel-backed open skill marketplace implementing the SKILL.md standard. With **89,028+ total skills**, it powers 20+ agent platforms (Claude Code, GitHub Copilot, Cursor, OpenClaw, etc.). Top skills by installs serve development, design, automation, research, and content creation use cases.

**Key Finding:** Skills are cross-compatible via SKILL.md format. OpenClaw can install most skills via ClawHub (fork) or manual directory placement, BUT security risk is critical — ClawHavoc attack (Feb 2026) planted 341+ malicious skills using typosquatting. Verification required before install.

---

## Platform Architecture

### Format: SKILL.md Standard (Open)

All skills follow YAML frontmatter + Markdown body structure:

```yaml
---
name: skill-name (64 chars max, lowercase-hyphenated)
description: Non-empty, max 1024 chars
license: MIT/Apache/etc
author: Author name
version: 1.0.0
metadata:
  key: value
allowed-tools:
  - tool-identifier
---

# Markdown instructions (< 5000 tokens recommended)
```

**Supported Platforms (20+):**
- Claude Code
- GitHub Copilot  
- Cursor, Cline, VS Code
- Gemini, OpenAI Codex
- Windsurf
- OpenClaw (via ClawHub)

### Registry Architecture

- **Main:** skills.sh (Vercel) — 89,028 total skills
- **OpenClaw Fork:** ClawHub (clawhub.ai) — 13,729+ community skills as of Feb 2026
- **Installation:** `npx skillsadd <owner/repo>` or manual directory + restart

---

## Top Skills by Download Count

### Tier 1: Mega Installs (100K+)

| Rank | Skill | Author | Installs | Use Case |
|------|-------|--------|----------|----------|
| 1 | **find-skills** | vercel-labs | 573.1K | Skill discovery, marketplace browsing |
| 2 | **vercel-react-best-practices** | vercel-labs | 215.1K | Frontend dev standards |
| 3 | **web-design-guidelines** | vercel-labs | 169.9K | UI/UX design |
| 4 | **frontend-design** | anthropics | 162.4K | Component design patterns |
| 5 | **remotion-best-practices** | remotion-dev | 149.1K | Video generation (React) |

### Tier 2: High Value for AI Assistants (10K-45K)

#### Business Automation & Workflow
- **workflow-automation** (supercent-io): 11.6K — task orchestration, pipeline management
- **deployment-automation** (supercent-io): 10.7K — CI/CD, infrastructure
- **task-planning** (supercent-io): 10.7K — project decomposition, milestone planning
- **git-workflow** (supercent-io): 10.6K — version control best practices

#### Data Analysis & Research
- **data-analysis** (supercent-io): 12.2K — statistical patterns, visualizations
- **seo-audit** (coreyhaines31): 44.2K — SEO analysis, keyword research, SERP tracking
- **analytics-tracking** (coreyhaines31): 19.2K — conversion tracking, funnel analysis
- **pattern-detection** (supercent-io): 10.2K — anomaly detection, trend identification
- **firecrawl** (firecrawl/cli): 13.7K — web scraping, data extraction

#### Content Creation
- **copywriting** (coreyhaines31): 37.1K — marketing copy, ad text, brand voice
- **internal-comms** (anthropics): 12.9K — internal messaging, announcements
- **slack-gif-creator** (anthropics): 12.2K — visual communication aids
- **baoyu-article-illustrator** (jimliu): 10.8K — article visuals, infographics

#### API Integration & Developer Tools
- **ai-sdk** (vercel): 11.5K — Vercel AI SDK patterns
- **api-documentation** (supercent-io): 11.1K — API design, schema validation
- **api-design** (supercent-io): 10.9K — REST/GraphQL best practices

#### Personal Assistant & Agent Capability
- **brainstorming** (obra): 57.6K — ideation, solution generation, creative thinking
- **writing-plans** (obra): 29.6K — structured writing, outline creation, narrative flow
- **executing-plans** (obra): 24.7K — action sequencing, task tracking, progress monitoring
- **systematic-debugging** (obra): 31.6K — root cause analysis, troubleshooting, error diagnosis

---

## OpenClaw-Specific: ClawHub Top Skills

### Highest Installed (35K+)

**Capability Evolver** (35K+ installs) — **CRITICAL FOR AGENT TEAMS**
- **Description:** Meta-skill that allows OpenClaw agents to inspect their own runtime history, identify failures/inefficiencies, and autonomously write code or update memory to improve performance.
- **Features:**
  - Auto-Log Analysis: scans memory and history for error patterns
  - Self-Repair: detects crashes, suggests patches
  - GEP Protocol: standardized evolution with reusable assets
  - Command: `/evolve` or `node index.js`
  - Modes: Mad Dog (autonomous) or --review flag (approval before changes)
- **Security Flag:** ClawHub Security flagged as suspicious — review scan before use
- **Use Case:** Tatyana agent self-improvement, Overseer agent refinement loops

### Efficiency Trio (Recommended)

1. **GOG (Google Workspace)** — 14K+ installs
   - Integrates: Gmail, Calendar, Drive, Docs, Sheets, Contacts
   - Use Case: Tatyana calendar management, email integration, document storage

2. **Mission Control** — Schedule/task management layer
   - Manages deadlines, reminders, escalations
   - Pairs with GOG for full office integration

3. **Capability Evolver** — (discussed above)

### Search Automation Stack

1. **Tavily** — Web search, research, data extraction
   - Cross-compatible with Claude via MCP
   - 11K+ installs on ClawHub
   - Use Case: Overseer research automation, fact verification

2. **Agent Browser** — 11K installs
   - Programmatic browser control
   - Complex web interactions (logins, multi-step flows)
   - Use Case: Data scraping, form automation, compliance checks

3. **N8N Workflow Integration**
   - Connects to n8n automation platform
   - Triggers business workflows across apps/APIs
   - Use Case: CRM sync, invoice generation, customer notifications

---

## Skills Ranked by Use Case Match

### For Tatyana (Personal/Business AI Assistant)

**Critical (Must-Have):**
1. **Capability Evolver** — Self-improvement, adaptive learning
2. **GOG** — Calendar, email, document access
3. **brainstorming** — Creative ideation for decision support
4. **executing-plans** — Task sequencing and tracking

**High-Value (Should-Have):**
5. **writing-plans** — Draft emails, documents, reports
6. **systematic-debugging** — Troubleshooting user issues
7. **internal-comms** — Team notifications, status updates
8. **copywriting** — Marketing messages, customer comms

**Nice-to-Have:**
9. **data-analysis** — Personal metrics, spending patterns
10. **analytics-tracking** — Usage metrics, goal progress

### For Overseer (CEO AI Agent, Orchestration)

**Critical (Must-Have):**
1. **Capability Evolver** — Subagent capability evolution
2. **workflow-automation** — Agent pipeline orchestration
3. **seo-audit** / **analytics-tracking** — Market research automation
4. **firecrawl** — Web scraping for competitive intelligence
5. **task-planning** — Decompose complex tasks for agents

**High-Value (Should-Have):**
6. **Tavily** (web search) — Real-time fact-checking, research
7. **Agent Browser** — Complex web automation, form submission
8. **N8N Workflow** — Cross-department task routing
9. **systematic-debugging** — Agent troubleshooting, error analysis
10. **api-design** — Integration architecture decisions

**Nice-to-Have:**
11. **deployment-automation** — Infrastructure as Code reviews
12. **git-workflow** — Code review orchestration

---

## Cross-Compatibility Matrix

| Skill | Claude Code | GitHub Copilot | Cursor | OpenClaw | Claude Codex | Notes |
|-------|------------|----------------|--------|----------|-------------|-------|
| find-skills | ✓ | ✓ | ✓ | ✓ | ✓ | Universal |
| Capability Evolver | ✓ | △ | △ | **✓✓** | ✓ | OpenClaw native |
| Tavily | ✓ | ✓ | ✓ | ✓ (via MCP) | ✓ | Via MCP possible |
| GOG | ✓ | △ | △ | **✓✓** | △ | OpenClaw + OAuth |
| Agent Browser | ✓ | △ | △ | **✓✓** | ✓ | Playwright-based |
| N8N | ✓ | △ | △ | **✓✓** | ✓ | Webhook-native |
| brainstorming | ✓ | ✓ | ✓ | ✓ | ✓ | Universal |
| executing-plans | ✓ | ✓ | ✓ | ✓ | ✓ | Universal |

**Legend:**
- ✓ = Works native
- ✓✓ = Optimized for
- △ = Requires adapter/workaround
- (blank) = Not recommended

---

## OpenClaw Skill Installation Guide

### Method 1: ClawHub UI (Safest)

```
1. Open OpenClaw dashboard
2. Go to Skills → Search "skill-name"
3. Click "Install"
4. Fill required config fields (API keys, endpoints)
5. Save → Restart agent if prompted
```

### Method 2: ClawHub Registry CLI

```bash
# List available
clawhub search "capability evolver"

# Install with safety check
clawhub install --verify openclaw/skills/capability-evolver

# Backup before risky installs
cp ~/.openclaw/openclaw.json ~/.openclaw/openclaw.json.bak-YYYYMMDD
```

### Method 3: Manual (Advanced)

```bash
# Create skill directory
mkdir -p ~/.openclaw/skills/my-skill

# Copy SKILL.md and support files
# Then restart: systemctl restart openclaw
# or: openclaw gateway restart
```

### Config Inheritance (openclaw.json)

```json
{
  "skills": {
    "install": {
      "nodeManager": "npm",  // npm | pnpm | yarn | bun
      "registry": "clawhub",
      "verify": true
    }
  }
}
```

---

## Security: ClawHavoc & Mitigation

### ClawHavoc Attack (Feb 2026)

**Scope:** 341+ malicious skills on ClawHub (1,184 discovered across all registries)

**Attack Pattern:**
- Typosquatted names ("capabilty-evoler" vs "capability-evolver")
- Hidden prerequisites (password-protected ZIPs, shell scripts)
- Data exfiltration: SSH keys, API tokens, browser session data
- Targets: OpenClaw operators, Overseer agents, bot credentials

**Vulnerable Use Cases:**
- Auto-installing skills without verification
- Copy-pasting installation commands from unverified sources
- Installing from non-official ClawHub URLs

### Mitigation: 3-Layer Verification

**Layer 1: Pre-Install Scanning**

Use **ClawSecure** (GitHub: ClawSecure/clawsecure-openclaw-security):
```bash
pip install clawsecure
clawsecure scan --skill "capability-evolver"
# Output: OWASP ASI 10/10 coverage, 55+ threat patterns
```

Or **Clawdex** (koi.security):
- Web: https://clawdex.koi.security
- Input: skill name or ClawHub URL
- Database: Koi's malicious skill registry

**Layer 2: Manual Verification (CEOs Requirement)**

Before installing ANY skill:
1. ✓ Check official ClawHub/GitHub repo for typos in skill name
2. ✓ Read SKILL.md source code — no suspicious file I/O or network calls
3. ✓ Verify author reputation (stars, install count, update history)
4. ✓ NO copy-paste install scripts from non-official sources
5. ✓ NO password-protected ZIPs or external downloads

**Layer 3: Runtime Monitoring**

```bash
# Monitor OpenClaw for suspicious activity
openclaw-security-monitor watch --skill "*"
# Detects: ClawHavoc signatures, memory poisoning, CVE-2026-25253
```

**Installation Safeguards:**
- Always backup `~/.openclaw/openclaw.json` before installs
- Use `--review` flag with Capability Evolver (not Mad Dog mode)
- Rotate API keys after installing new skills
- Audit `~/.openclaw/skills/*/` for suspicious scripts/binaries

---

## Installation Workflow for Overseer CEO Agent

### Safe Install Checklist

```markdown
## Before Installing Any Skill

- [ ] Name matches official source exactly (no typos)
- [ ] ClawSecure scan: PASS
- [ ] Clawdex check: NOT in malicious registry
- [ ] SKILL.md review: no file://, exec(), child_process
- [ ] Author: +10K installs, +2 years on ClawHub, no gaps
- [ ] Backup: `cp ~/.openclaw/openclaw.json bak-<DATE>`
- [ ] Dry-run: Install in test agent first, 24h monitoring

## After Install

- [ ] Restart: `openclaw gateway restart`
- [ ] Verify: List installed skills with `clawhub list`
- [ ] Monitor: 7 days for unexpected outbound traffic
- [ ] Audit: Check skill logs for errors or warnings
```

### Recommended Skill Install Order (Overseer)

**Phase 1: Foundation (Week 1)**
1. Capability Evolver (self-improvement)
2. firecrawl (web data)
3. Tavily (search)

**Phase 2: Automation (Week 2)**
4. workflow-automation
5. task-planning
6. Agent Browser

**Phase 3: Integration (Week 3)**
7. N8N Workflow (external systems)
8. GOG (office productivity)

**Phase 4: Intelligence (Week 4)**
9. seo-audit / analytics-tracking
10. systematic-debugging
11. data-analysis

---

## Format Compatibility: SKILL.md → OpenClaw

### What Works Out-of-Box

✓ YAML frontmatter (name, description, license, author, metadata)  
✓ Markdown instructions (< 5000 tokens)  
✓ Dependency declaration (allowed-tools, runtime requirements)  
✓ Supporting files: scripts/, references/, assets/

### What Requires Adaptation

- **Claude Code ↔ OpenClaw:** Skill.md identical, but API calls may differ
  - Claude Code: uses official APIs (Claude, GitHub, Vercel)
  - OpenClaw: adds OAuth providers, local tools, custom transports
  
- **MCP vs Direct Tools:** OpenClaw prefers MCP servers (Anthropic standard)
  - Tavily: Works via MCP + native OpenClaw skill
  - Firecrawl: Works via MCP + native skill
  - Custom APIs: Wrap in MCP for portability

### Best Practice for Cross-Compatibility

```yaml
---
name: my-skill
description: Works on Claude Code + OpenClaw + GitHub Copilot
metadata:
  platforms: ["claude-code", "openclaw", "github-copilot"]
  tested: "2026-03-16"
  mcp-compatible: true
allowed-tools:
  - "web-search"  # MCP-standard tool names
  - "web-crawler"
---

# Instructions written platform-agnostically
# Reference MCP tools, not platform-specific APIs
```

---

## Research Output Contract & MCP Memory

### Key Takeaways (for CEO Memory)

1. **Skills.sh has 89K+ skills** — not a niche marketplace
   - Top 5 skills: 149K-573K installs (dev/design focused)
   - For AI agents: brainstorming (57K), executing-plans (24K), Capability Evolver (35K on ClawHub)

2. **Capability Evolver is critical** for agent self-improvement
   - 35K+ installs on OpenClaw's ClawHub
   - Enables autonomous capability evolution
   - Security flagged — requires --review before deploy

3. **ClawHavoc (Feb 2026) is real threat**
   - 341+ malicious skills via typosquatting
   - Data exfiltration: SSH keys, API tokens
   - Mitigation: ClawSecure + Clawdex scanning mandatory

4. **Cross-platform skill reuse possible** via SKILL.md
   - Claude Code ↔ OpenClaw ↔ GitHub Copilot (formats identical)
   - MCP-based skills most portable (Tavily, Firecrawl)
   - Custom adapters needed for OAuth/local tools

5. **Recommended Overseer skill stack:**
   - Core: Capability Evolver, firecrawl, Tavily, workflow-automation
   - Research: seo-audit, analytics-tracking, data-analysis
   - Integration: Agent Browser, N8N, GOG

6. **Installation safe path:**
   - ClawSecure pre-scan (mandatory)
   - Manual SKILL.md code review
   - Backup OpenClaw config before installs
   - Phase-based rollout (foundation → automation → integration → intelligence)

---

## Sources

- [Agent Skills Directory Overview](https://skills.sh)
- [SKILL.md Specification - Anthropic](https://agentskills.io/specification)
- [skill.md: An open standard for agent skills](https://www.mintlify.com/blog/skill-md)
- [How to Install OpenClaw Skills (2026): Step-by-Step + Fixes](https://openclawskill.cc/blog/how-to-install-openclaw-skills)
- [Setting Up Skills In Openclaw](https://nwosunneoma.medium.com/setting-up-skills-in-openclaw-d043b76303be)
- [Capability Evolver — ClawHub](https://clawhub.ai/autogame-17/capability-evolver)
- [OpenClaw Tavily Integration: Add Web Search to Your AI Agent](https://www.heyuan110.com/posts/ai/2026-03-05-openclaw-tavily-integration/)
- [Hundreds of Malicious Skills Found in OpenClaw's ClawHub](https://www.esecurityplanet.com/threats/hundreds-of-malicious-skills-found-in-openclaws-clawhub/)
- [ClawHavoc Poisons OpenClaw's ClawHub With 1,184 Malicious Skills](https://cyberpress.org/clawhavoc-poisons-openclaws-clawhub-with-1184-malicious-skills/)
- [GitHub - ClawSecure/clawsecure-openclaw-security](https://github.com/ClawSecure/clawsecure-openclaw-security)
- [GitHub - VoltAgent/awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills)
- [Top 10 OpenClaw Skill Recommendations: 2026](https://help.apiyi.com/en/openclaw-skill-recommendations-2026-en.html)

---

**Research completed:** 2026-03-16 12:00 UTC  
**Next review:** 2026-04-16 (skills ecosystem evolves weekly)
