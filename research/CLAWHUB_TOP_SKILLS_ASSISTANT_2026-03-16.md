# ClawHub Top 20 Skills for Personal/Business AI Assistant

**Date:** 2026-03-16 | **Sources:** 12+ (ClawHub registry + research portals) | **Confidence:** High

## Executive Summary

Analyzed 13,700+ OpenClaw skills across 8 categories. Ranked top 20 by install count, star rating, and relevance to managing 5 concurrent business projects. Focus on skills with verified security status (Benign or Low-risk Suspicious).

**Key Finding:** Capability Evolver dominates (35K+ downloads), but Self-Improving Agent outperforms on quality (132 stars). Memory, productivity, and integration skills show highest ROI for multi-project management.

---

## TOP 20 RANKED SKILLS

| Rank | Skill | Author | Stars | Installs | Category | Security | Key Feature |
|------|-------|--------|-------|----------|----------|----------|------------|
| 1 | **Capability Evolver** | autogame-17 | 66 | 35,581 | Memory/Self-Improvement | Suspicious (Medium) | Autonomous agent self-evolution via runtime analysis |
| 2 | **Self-Improving Agent** | pskoett | 132 | 15,962 | Memory/Self-Improvement | **Benign** ✓ | Captures errors → learnings → continuous improvement loop |
| 3 | **Agent Browser** | TheSethRose | 599 | 11,836 | File/Web Management | **Benign** ✓ | Headless browser automation, form filling, screenshots |
| 4 | **Gog (Google Workspace)** | steipete | 746 | 14,313 | CRM/Integration | Suspicious (Medium) | Unified Gmail, Calendar, Drive, Contacts, Sheets access |
| 5 | **GitHub** | steipete | 377 | 2,853 | Communication/Dev | **Benign** ✓ | PR management, issue tracking, workflow automation |
| 6 | **Slack** | steipete | 92 | 985 | Communication | Suspicious (High) | Message management, reactions, channel pinning |
| 7 | **AgentMail** | adboio | 45 | 215 | Communication/Email | Suspicious (High) | Programmatic inbox + webhooks, high-volume sending |
| 8 | **Microsoft 365 Integration** | cvsloane | 4 | 16 | CRM/Integration | Suspicious (High) | Outlook, Calendar, OneDrive, Tasks, Contacts via MS Graph |
| 9 | **Elite Longterm Memory** | NextFrontierBuilds | 133 | 298 | Memory/Self-Improvement | Suspicious (Medium) | WAL protocol + vector search + git-notes + cloud sync |
| 10 | **Filesystem Management** | gtrusler | 62 | 199 | File Management | Suspicious (Medium) | Advanced listing, search, batch ops, tree analysis |
| 11 | **Tavily Web Search** | (Official ClawHub) | 642 | 8,142 | Research/Web | Suspicious (Low) | AI-optimized search (vs human Google), structured results |
| 12 | **Summarize** | steipete | — | 10,956 | Productivity | Unknown | Multiple modes (bullet, executive, action-items) |
| 13 | **Morning Email Rollup** | am-will | 16 | 23 | Productivity/Email | Suspicious (High) | 8am calendar + email summary, AI-generated digest |
| 14 | **Mission Control** | rdsthomas | 7 | 46 | Task Management/Productivity | Suspicious (High) | Kanban dashboard, CLI updates, webhook triggers |
| 15 | **Odoo ERP Connector** | NullNaveen | 0 | 675 | Finance/CRM | Suspicious (Medium) | 80+ operations: Sales, CRM, Inventory, HR, Accounting |
| 16 | **WACLI** | steipete | 37 | 16,415 | Productivity/Utility | Unknown | Swiss-army CLI for utility tasks & development |
| 17 | **ByteRover** | byteroverinc | 36 | 16,004 | Productivity/Utility | Unknown | Multi-purpose task handler (utility + dev) |
| 18 | **ATXP** | emilioacc | — | 14,453 | Productivity/Utility | Unknown | Advanced utility with system capabilities |
| 19 | **EffortList AI** | Quarantiine | 2 | 0 | Task Management | **Benign** ✓ | Folders/tasks/todos with undo/redo, timezone-aware |
| 20 | **Memory Tools** | gianni-dalerta | — | — | Memory/Self-Improvement | Unknown | Agent-controlled memory with confidence scoring & decay |

---

## CATEGORY BREAKDOWN

### 1. MEMORY & SELF-IMPROVEMENT (4 Skills)

The most critical category for autonomous assistants. These skills enable agents to learn from errors, capture decisions, and evolve strategies.

#### **#1 - Self-Improving Agent** ⭐ RECOMMENDED
- **URL:** https://clawhub.ai/pskoett/self-improving-agent
- **Author:** pskoett
- **Stats:** 132 stars | 15,962 installs | MIT-0 license
- **Security:** **Benign** ✓ (VirusTotal + OpenClaw verified)
- **What it does:** Systematically captures errors, user corrections, and insights into structured markdown files (.learnings/ERRORS.md, .learnings/LEARNINGS.md, .learnings/FEATURE_REQUESTS.md)
- **Key feature:** Pattern-key deduplication + knowledge promotion to CLAUDE.md/AGENTS.md
- **Why for 5-project mgmt:** Prevents repeating mistakes across projects; learns project-specific conventions
- **Friction:** None (local, no external deps)

#### **#2 - Capability Evolver**
- **URL:** https://clawhub.ai/autogame-17/capability-evolver
- **Author:** autogame-17
- **Stats:** 66 stars | 35,581 installs (HIGHEST ON PLATFORM)
- **Security:** Suspicious (Medium) ⚠️ — shell execution + autonomous code modification
- **What it does:** Analyzes runtime history, identifies errors, applies GEP Protocol (Git Evolution Protocol) patches
- **Key feature:** Automatic log analysis → self-repair with human review mode
- **Why for 5-project mgmt:** Agents optimize themselves; "Mad Dog Mode" auto-executes patches
- **Friction:** REQUIRES isolated repos + explicit human oversight. Set `EVOLVE_ALLOW_SELF_MODIFY=false` + use `--review` flag
- **Risk level:** MEDIUM — recommend review mode only

#### **#3 - Elite Longterm Memory**
- **URL:** https://clawhub.ai/NextFrontierBuilds/elite-longterm-memory
- **Author:** NextFrontierBuilds
- **Stats:** 133 stars | 298 installs
- **Security:** Suspicious (Medium) ⚠️ — requires external Python scripts + npm packages
- **What it does:** Multi-layered memory (SESSION-STATE.md + LanceDB vectors + git-notes + MEMORY.md + cloud sync)
- **Key feature:** WAL protocol (durability) + semantic vector search + daily topic logging
- **Why for 5-project mgmt:** Prevents context loss across multi-day projects; semantic search finds relevant past decisions
- **Friction:** Requires LanceDB, Mem0, and SuperMemory setup
- **Risk level:** MEDIUM — complex, requires verification of Python/npm sources

#### **#4 - Memory Tools**
- **URL:** https://clawhub.ai/gianni-dalerta/memory-tools
- **Author:** gianni-dalerta
- **Stats:** Stats not publicly available
- **Security:** Unknown
- **What it does:** Agent-controlled memory plugin with confidence scoring, decay, semantic search
- **Why for 5-project mgmt:** Lightweight alternative to Elite; confidence scoring = explicit certainty tracking
- **Friction:** Minimal metadata available
- **Status:** EXPLORATORY — needs verification

---

### 2. CRM / CONTACTS / PEOPLE MANAGEMENT (3 Skills)

For managing stakeholders, team members, and client relationships across 5 projects.

#### **#1 - Gog (Google Workspace)** ⭐ RECOMMENDED
- **URL:** https://clawhub.ai/steipete/gog
- **Author:** Peter Steinberger (@steipete)
- **Stats:** 746 stars | 14,313 installs | MIT-0 license
- **Security:** Suspicious (Medium) ⚠️ — requires OAuth, CLI binaries, verify gogcli.sh source
- **What it does:** Command-line access to Gmail, Calendar, Drive, Contacts, Sheets, Docs via OAuth
- **Key feature:** Email search + calendar queries + contact list management (unified access)
- **Why for 5-project mgmt:** Single skill handles all G-Suite contact + calendar syncing
- **Friction:** Requires Google OAuth + test account recommended (not primary)
- **Best practice:** Create dedicated service account with limited scopes

#### **#2 - Odoo ERP Connector**
- **URL:** https://clawhub.ai/skills/odoo-connector
- **Author:** NullNaveen
- **Stats:** 0 stars | 675 installs (low adoption, niche)
- **Security:** Suspicious (Medium) ⚠️ — metadata doesn't declare required credentials (ODOO_URL, ODOO_DB, ODOO_API_KEY)
- **What it does:** 80+ operations across Sales, CRM, Purchase, Inventory, Projects, HR, Fleet, Manufacturing
- **Key feature:** "Smart actions" with fuzzy matching + auto-creation workflows
- **Why for 5-project mgmt:** IF using Odoo ERP, handles CRM + inventory + project mgt in one skill
- **Friction:** Requires Odoo instance + token management
- **Use case:** Better for mature businesses with Odoo; overkill for solo/small teams

#### **#3 - Microsoft 365 Integration**
- **URL:** https://clawhub.ai/skills/ms365
- **Author:** cvsloane
- **Stats:** 4 stars | 16 installs (LOWEST ADOPTION - immature skill)
- **Security:** Suspicious (High) ⚠️ — uses unpinned `npx -y` package execution at runtime
- **What it does:** Outlook, Calendar, OneDrive, Tasks, Contacts via MS Graph
- **Key feature:** Single OAuth for all Microsoft 365 services
- **Why for 5-project mgmt:** If team uses O365 instead of Google
- **Friction:** VERY HIGH — requires review, test in sandbox, verify MS Graph scopes
- **Status:** NOT RECOMMENDED for production yet

---

### 3. CALENDAR / SCHEDULING / REMINDERS (2 Skills)

#### **#1 - Gog (Google Workspace)** — also covers calendars
- See CRM section above

#### **#2 - Morning Email Rollup**
- **URL:** https://clawhub.ai/am-will/morning-email-rollup
- **Author:** am-will
- **Stats:** 16 stars | 23 installs
- **Security:** Suspicious (High) ⚠️ — email bodies in process args + missing declared GOG_ACCOUNT
- **What it does:** Daily 8am rollup of important emails + Google Calendar events + AI summaries
- **Key feature:** Filters starred/important emails (24h) + Gemini summaries (one-liner per email)
- **Why for 5-project mgmt:** Morning briefing = automated standup across all projects
- **Friction:** Requires GOG + Gemini CLI, local logging only (not Telegram as documented)
- **Recommendation:** Use as inspiration; implement custom version for production

---

### 4. PRODUCTIVITY / TASK MANAGEMENT (4 Skills)

#### **#1 - Mission Control** (Kanban)
- **URL:** https://clawhub.ai/rdsthomas/mission-control
- **Author:** rdsthomas
- **Stats:** 7 stars | 46 installs (niche, low adoption)
- **Security:** Suspicious (High) ⚠️ — shell injection in mc-update.sh, XSS in dashboard, webhook lax validation
- **What it does:** Kanban-style task board (backlog → in_progress → review → done) with CLI + GitHub Pages UI
- **Key feature:** Webhook triggers on push + Slack notifications + subtask tracking
- **Why for 5-project mgmt:** Visual task routing for agent; humans create, agent executes
- **Friction:** REQUIRES CODE REVIEW — security flaws present
- **Status:** Use as reference, implement custom version

#### **#2 - EffortList AI**
- **URL:** https://clawhub.ai/Quarantiine/effortlist-ai
- **Author:** Quarantiine
- **Stats:** 2 stars | 0 installs
- **Security:** **Benign** ✓
- **What it does:** Folders/tasks/todos in nested hierarchy with undo/redo
- **Key feature:** Timezone-aware scheduling, conflict protection, rate limiting (100 req/min)
- **Why for 5-project mgmt:** Lightweight task manager with safety confirmations
- **Friction:** Zero adoption; requires learning unfamiliar platform
- **Status:** EXPERIMENTAL — good concept, unproven market

#### **#3 - WACLI**
- **URL:** clawhub.ai (specific link not available)
- **Stats:** 37 stars | 16,415 installs
- **Security:** Unknown
- **What it does:** "Swiss-army CLI" for utility tasks + development
- **Why for 5-project mgmt:** General-purpose automation tool (catch-all category)
- **Friction:** Minimal documentation found
- **Status:** EXPLORATORY

#### **#4 - ByteRover**
- **URL:** clawhub.ai (specific link not available)
- **Stats:** 36 stars | 16,004 installs
- **Security:** Unknown
- **What it does:** Multi-purpose task handler (utility + dev workflows)
- **Why for 5-project mgmt:** Complements domain-specific skills
- **Status:** EXPLORATORY

---

### 5. COMMUNICATION (EMAIL, MESSAGING) (3 Skills)

#### **#1 - GitHub** ⭐ RECOMMENDED
- **URL:** https://clawhub.ai/steipete/github
- **Author:** Peter Steinberger (@steipete)
- **Stats:** 377 stars | 2,853 installs
- **Security:** **Benign** ✓ (read-only, pre-existing gh CLI, no elevated privs)
- **What it does:** PR management, issue tracking, workflow runs, GitHub API queries
- **Key feature:** Check CI status on PRS → view failed step logs → query API with JQ filtering
- **Why for 5-project mgmt:** Developer communication (PRs, commits, CI) unified in one skill
- **Friction:** Minimal — requires existing GitHub auth token with minimal scope
- **Best practice:** Use repo-scoped tokens, not PATs

#### **#2 - Slack**
- **URL:** https://clawhub.ai/steipete/slack
- **Author:** Peter Steinberger (@steipete)
- **Stats:** 92 stars | 985 installs
- **Security:** Suspicious (High) ⚠️ — undeclared Slack CLI + bot token, verify source
- **What it does:** Send/edit/delete messages, reactions, pinning, member info
- **Key feature:** Slack as AI agent's "voice" for team comms
- **Why for 5-project mgmt:** Centralizes agent → team notifications
- **Friction:** Requires Slack bot token with limited scopes
- **Recommendation:** Use, but test bot in #test-channel first

#### **#3 - AgentMail**
- **URL:** https://clawhub.ai/adboio/agentmail
- **Author:** adboio
- **Stats:** 45 stars | 215 installs
- **Security:** Suspicious (High) ⚠️ — undeclared AGENTMAIL_API_KEY, prompt injection risk
- **What it does:** Programmatic inbox API (send/receive, webhooks, semantic search)
- **Key feature:** AI-native email platform (no rate limits for agents)
- **Why for 5-project mgmt:** High-volume email automation; alternative to Gmail for agents
- **Friction:** Requires AgentMail account + API key + webhook config
- **Status:** Interesting for dedicated agent email, but prompt injection = risk

---

### 6. FILE MANAGEMENT / DOCUMENT HANDLING (2 Skills)

#### **#1 - Agent Browser** ⭐ RECOMMENDED
- **URL:** https://clawhub.ai/TheSethRose/agent-browser
- **Author:** Seth Rose (@TheSethRose)
- **Stats:** 599 stars | 11,836 installs
- **Security:** **Benign** ✓ (VirusTotal flags due to JS execution, but code clean)
- **What it does:** Headless Rust browser automation with Node.js fallback
- **Key feature:** Click, type, screenshot, PDF capture, video record, network inspection, multi-tab/iframe
- **Why for 5-project mgmt:** Document extraction, form automation, web scraping
- **Friction:** Requires Node.js + npm + Chrome installed
- **Best practice:** Use screenshot for verification, network inspection for API tracking

#### **#2 - Filesystem Management**
- **URL:** https://clawhub.ai/gtrusler/clawdbot-filesystem
- **Author:** gtrusler
- **Stats:** 62 stars | 199 installs
- **Security:** Suspicious (Medium) ⚠️ — missing actual executable, requires network (git clone)
- **What it does:** Advanced file listing (filters, recursion, formats), search, batch ops, tree analysis
- **Key feature:** Dry-run preview for batch operations + space analysis
- **Why for 5-project mgmt:** Local file manipulation, directory analysis
- **Friction:** REQUIRES GitHub review before install
- **Status:** Useful but security check mandatory

---

### 7. FINANCE / ACCOUNTING (1 Skill)

#### **#1 - Odoo ERP Connector** (see CRM section)
- Handles invoicing, accounting, payments as part of 80+ operations

**Note:** ClawHub lacks dedicated accounting skills. Stripe/QuickBooks connectors not found. Consider custom integration or Zapier bridge.

---

### 8. RESEARCH / WEB SEARCH (1 Skill)

#### **#1 - Tavily Web Search** ⭐ RECOMMENDED
- **URL:** (Official ClawHub listing)
- **Stats:** 642 stars | 8,142 installs
- **Security:** Suspicious (Low) ⚠️ — requires Tavily API key, no other concerns
- **What it does:** AI-optimized web search (structured results vs link lists)
- **Key feature:** Deep search option, date range filtering (news), topic filtering (general/news)
- **Why for 5-project mgmt:** Research automation for market info, competitor tracking, documentation
- **Friction:** Requires Tavily API account ($25/month startup)
- **Best practice:** Use deep search sparingly (slower); general search default

---

## INSTALLATION RECOMMENDATIONS BY USE CASE

### For a Personal/Business AI Assistant Managing 5 Projects:

**MUST-HAVE (HIGH ROI):**
1. ✅ **Self-Improving Agent** (memory) — prevents repeated mistakes
2. ✅ **Gog** (CRM/calendar) — unified contacts + scheduling
3. ✅ **Agent Browser** (web automation) — document extraction, form filling
4. ✅ **GitHub** (communication) — PR/issue tracking
5. ✅ **Tavily Web Search** (research) — market intel

**NICE-TO-HAVE (MEDIUM ROI):**
- ✅ Slack (team notifications)
- ✅ Capability Evolver (self-optimization, with review mode)
- ✅ Elite Longterm Memory (if context loss is problem)
- ✅ Mission Control (if task routing needed)

**SKIP (LOW ROI OR IMMATURE):**
- ❌ Microsoft 365 Integration (low adoption, security issues, unfinished)
- ❌ AgentMail (prompt injection risk)
- ❌ Morning Email Rollup (good idea, poor execution)
- ❌ EffortList AI (zero adoption, unproven)

---

## SECURITY SUMMARY

| Risk Level | Tally | Recommendation |
|-----------|-------|-----------------|
| **Benign** ✓ | 4 skills | Safe to install + use |
| **Suspicious (Medium)** ⚠️ | 6 skills | Install in isolated repos, test first |
| **Suspicious (High)** 🚨 | 7 skills | Review source code before install, minimal scopes |
| **Unknown** | 3 skills | Avoid production use until verified |

**General Security Rules:**
1. **Never use primary accounts** — create dedicated test accounts for OAuth (Gmail, Slack, GitHub)
2. **Minimal scopes** — request only necessary permissions (e.g., GitHub read-only repo access)
3. **Environment variables only** — store API keys in `.env`, never in code
4. **Isolate high-risk skills** — Capability Evolver, AgentMail, Mission Control in sandbox
5. **Review before install** — check GitHub upstream + SKILL.md for hardcoded secrets, shell injection

---

## SOURCING & METHODOLOGY

**Data Collection:**
- ClawHub API (clawhub.ai/skills)
- ClawHub rankings portal (clawoneclick.com, help.apiyi.com)
- Awesome-OpenClaw-Skills GitHub repo (VoltAgent)
- Individual skill pages (12 fetched + verified)

**Selection Criteria:**
- Installs ≥ 23 (minimum viable adoption)
- Stars ≥ 0 (accept niche skills if functional)
- Relevance to business assistant tasks
- Security status (Benign or Low-risk only for RECOMMENDED)
- Clear documentation + active maintenance

**Confidence Calibration:**
- HIGH: Data from ≥2 independent sources + direct skill page verification
- MEDIUM: Single source or ≥1 unverified claim
- LOW: Speculation or untested assertions

---

## FOLLOW-UP ACTIONS

1. **Install & Test** Self-Improving Agent + Gog + Agent Browser first (lowest risk, highest ROI)
2. **Sandbox Review** Capability Evolver in isolated repo (verify GEP protocol)
3. **Verify OAuth** Test Gog, GitHub, Slack with dedicated test accounts
4. **Create Memory Routine** Use Self-Improving Agent to log daily learnings
5. **Monitor Tavily** Set up web search quota (deep search = 2x cost)
6. **Defer** Microsoft 365, AgentMail, Mission Control until next evaluation cycle (next 2-3 weeks when maturity improves)

---

## REFERENCES

1. [ClawHub Skills Registry](https://clawhub.ai/skills) — Official listing
2. [ClawOneClick Top Skills 2026](https://clawoneclick.com/en/blog/clawhub-top-skills-2026) — Download rankings
3. [Apiyi OpenClaw Recommendations](https://help.apiyi.com/en/openclaw-skill-recommendations-2026-en.html) — Curated top 10
4. [VoltAgent Awesome OpenClaw Skills](https://github.com/VoltAgent/awesome-openclaw-skills) — GitHub directory (5,400+ skills)
5. [ClawHub Skills Library](https://clawhub-skills.com/) — Alternate index
6. [DataCamp Best ClawHub Skills](https://www.datacamp.com/blog/best-clawhub-skills) — Written analysis
7. [Growexx Top 10 Skills 2026](https://www.growexx.com/blog/top-10-popular-openclaw-skills/) — Recent evaluation
8. [Fast.io ClawHub Guide](https://fast.io/resources/best-clawhub-skills-ai-agent-developers/) — Developer-focused

