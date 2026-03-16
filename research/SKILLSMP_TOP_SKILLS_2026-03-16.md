# SkillsMP Platform & Top Claude Code Skills Research

**Date:** 2026-03-16 | **Sources:** 15+ | **Confidence:** high

## Executive Summary

SkillsMP is the largest Claude Code skill marketplace with 96K+ skills as of March 2026. The platform organizes skills by SDLC phase with quality filtering (min 2 stars). Most installed skills address: development workflow automation (TDD, code review, git), productivity (planning, memory), frontend design, security audits, and orchestration.

**Key finding:** We should prioritize 4 skill categories for Overseer:
1. **Orchestration & Routing** (Ruflo, multi-agent coordination)
2. **Development Workflow** (TDD, code review, git/PR automation)
3. **Memory & Context** (planning-with-files, session management)
4. **Security & Quality** (OWASP scanning, dependency audit)

---

## SkillsMP Platform Overview

### Scale & Growth
- **Total skills:** 96,751+ (March 2026)
- **Previous reports:** 87,427+ (January 2026), 66,541+ (January 2026)
- **Quality gate:** Minimum 2 GitHub stars required for indexing
- **Compatibility:** Claude Code, OpenAI Codex CLI, and other tools adopting SKILL.md standard

### Organization
Skills categorized by SDLC phase and domain:
- **Tools:** 129,310 exports
- **Development:** 94,135
- **Business:** 93,371
- **Data & AI:** 57,950
- **Testing & Security:** 54,042
- **DevOps:** 48,409

### Features
- AI semantic search + keyword filtering
- Category browsing with quality indicators
- Timeline visualization of skill creation trends
- Skill rating and installation metrics

**Note:** SkillsMP blocks direct scraping (403). Information gathered via secondary sources and direct research.

---

## Top Skills by Category

### Tier 1: Orchestration & Multi-Agent Systems

#### **Ruflo** (formerly Claude Flow v3)
- **Author:** ruvnet
- **GitHub:** https://github.com/ruvnet/ruflo
- **Type:** Agent orchestration platform
- **Key features:**
  - Orchestrates 60+ specialized agents (coders, testers, reviewers, architects, security auditors)
  - 21 MCP tools: teammate/spawn, teammate/coordinate, teammate/broadcast, teammate/route-task
  - Distributed swarm intelligence with fault-tolerant consensus
  - Self-learning patterns (prevents catastrophic forgetting)
  - Native Claude Code + Codex integration
  - RAG integration for knowledge retrieval
- **Best for:** Complex multi-agent workflows, cross-department coordination
- **Compatibility:** Claude Code ✓, Codex ✓
- **Status:** Active, enterprise-grade architecture
- **Relevance to Overseer:** CRITICAL — direct replacement/enhancement for our CEO orchestration layer

#### **Multi-Agent Ralph Loop**
- **GitHub:** https://github.com/alfredolopelo80/multi-agent-ralph-loop
- **Version:** v2.94.0
- **Features:**
  - Memory-driven planning
  - Multi-agent coordination
  - Agent Teams integration
  - Automatic learning loops
  - Security validation (Grade A-)
- **Best for:** Complex task orchestration with learning
- **Compatibility:** Claude Code ✓
- **Status:** Actively maintained

#### **Claude Octopus**
- **GitHub:** https://github.com/nyldn/claude-octopus
- **Type:** Multi-tentacled orchestrator for Claude Code
- **Features:**
  - Coordinates Codex CLI and Gemini CLI for parallel execution
  - Intelligent contextual routing
- **Best for:** Cross-tool parallel execution

#### **Agent Skills** (Anthropic Official)
- **Type:** Standard for Claude Code subagent coordination
- **Docs:** https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview
- **Features:**
  - Native Task Tool for spawning subagents
  - Agent Teams for shared coordination
  - Session-level context management
  - Progressive disclosure (2% of context window for skill descriptions)

---

### Tier 1: Development Workflow (TDD & Code Review)

#### **Test-Driven Development (TDD) Skill**
- **Source:** Multiple implementations available on SkillsMP
- **Upstream:** https://www.aihero.dev/skill-test-driven-development-claude-code
- **Workflow:** RED → GREEN → REFACTOR
- **Key features:**
  - Enforces failing test first (anti-pattern for default Claude)
  - Tracer bullets in vertical slices
  - Concrete examples with guidance on when TDD is valuable
  - Best practices: test behavior not implementation, public interfaces only
- **Best for:** New features, bug fixes, complex business logic, API contracts
- **Not ideal for:** Exploratory code, UI layout, simple CRUD
- **Compatibility:** Claude Code ✓
- **Stars:** [Data unavailable from SkillsMP due to scraping block]

#### **Claude Wizard**
- **GitHub:** https://github.com/vlad-ko/claude-wizard
- **Type:** Senior software architect skill
- **Pipeline:** 8-phase development workflow
- **Features:**
  - TDD enforcement
  - Adversarial code review
  - Quality gate cycles
  - Architectural guidance
- **Best for:** Complex systems, architectural decisions
- **Compatibility:** Claude Code ✓

#### **Git Workflow Skill**
- **GitHub:** https://github.com/netresearch/git-workflow-skill
- **Source:** NetResearch GmbH
- **Features:**
  - Best practices for branching, commits, PR workflows
  - Integrated with Claude Code native git tools
- **Compatibility:** Claude Code ✓
- **Status:** Community maintained

#### **Code Review & Security Pack**
- **Built-in commands:**
  - `/security-audit` — OWASP Top 10 scanning
  - `/secret-scanner` — hardcoded secrets detection
  - `/deps-check` — CVE vulnerability mapping
- **Features:**
  - Line-level reporting (file, line number, category, fix)
  - No context loss between modules
  - Catches issues traditional tools miss (auth middleware not applied to routes)
  - Dependency tree analysis (real exposure vs. noise)
- **Compatibility:** Claude Code ✓ (Official)

---

### Tier 1: Memory & Context Management

#### **planning-with-files** ⭐ MOST STARRED
- **GitHub:** https://github.com/OthmanAdi/planning-with-files
- **Stars:** 13,410+ (highest in Claude ecosystem)
- **Origin:** Manus AI methodology ($2B acquisition)
- **Architecture:**
  - `task_plan.md` — phases and progress tracking
  - `findings.md` — research notes
  - `progress.md` — session logs and error history
- **Features:**
  - Persistent markdown planning across sessions
  - Auto-recovery on `/clear` (context compaction)
  - Error tracking and session continuity
- **Best for:** Long-running projects, context management, session recovery
- **Compatibility:** Claude Code ✓
- **Relevance to Overseer:** HIGH — aligns with our session-context + HANDOVER strategy

#### **Session Memory System** (Anthropic Official)
- **Type:** Automatic cross-session context loading
- **Features:**
  - Summary injection on session start
  - Continuous background summary writing
  - Instant `/compact` (no 2-minute re-analysis)
  - Progressive disclosure of past session relevance
- **Compatibility:** Claude Code ✓ (Built-in)
- **Status:** Production

#### **Continuous Claude Context Management**
- **GitHub:** https://github.com/parcadei/Continuous-Claude-v3
- **Features:**
  - Ledger-based state tracking
  - Handoff mechanisms between sessions
  - MCP execution without context pollution
  - Isolated context windows for agent orchestration
- **Best for:** Long-running multi-session projects
- **Compatibility:** Claude Code ✓

---

### Tier 2: Frontend Design & Web Quality

#### **Frontend Design Skill** (Anthropic Official)
- **Weekly installs:** 110,000+
- **Maturity:** Production
- **Features:**
  - Distinctive typography (rejects Arial/Inter generics)
  - Cohesive color + CSS variables
  - Production-grade interfaces (avoids "AI slop")
- **Workflow:** Design → Craft → Accessibility → Performance
- **Compatibility:** Claude Code ✓
- **Note:** Most widely adopted skill in ecosystem

#### **Web Quality Skills** ⭐
- **Author:** Addy Osmani (Chrome engineering lead)
- **GitHub:** (part of web-quality-skills collection)
- **Stars:** 496+
- **Coverage:** 6 skills for full spectrum of web optimization
- **Features:**
  - Performance best practices from Chrome team
  - Accessibility compliance (100+ ARIA rules)
  - UX and semantic HTML guidance
  - Reduced-motion support, keyboard navigation, heading hierarchy
- **Compatibility:** Claude Code ✓

#### **React Best Practices Skill**
- **Part of:** web-quality-skills collection
- **Focus:** Performance, patterns, component design
- **Compatibility:** Claude Code ✓

---

### Tier 2: Security & Compliance

#### **OWASP Top 10:2025 Skill**
- **GitHub:** https://github.com/agamm/claude-code-owasp
- **Year:** 2025-2026 updated
- **Coverage:**
  - OWASP Top 10:2025
  - ASVS 5.0 (Application Security Verification Standard)
  - Agentic AI security patterns (NEW)
  - 20+ language-specific security quirks
- **Best for:** Security-first development, compliance audits
- **Compatibility:** Claude Code ✓
- **Status:** Actively maintained

#### **Snyk MCP Server** (Security Integration)
- **Type:** MCP server for vulnerability management
- **Features:**
  - Real-time CVE database
  - Dependency scanning
  - Fix recommendations
- **Integration:** Claude Desktop + Claude Code
- **Status:** Production

---

### Tier 2: Documentation & API Design

#### **OpenAPI Spec Generator Skill**
- **Type:** API documentation automation
- **Features:**
  - Reads route handlers
  - Generates OpenAPI 3.0/3.1 specs
  - Swagger UI integration
  - SDK generation potential
- **Best for:** RESTful API documentation
- **Compatibility:** Claude Code ✓

#### **Documentation Generation Workflow**
- **Approach:** Read code, infer types (TypeScript/JS), write docs
- **Output formats:**
  - JSDoc (IDE tooltips)
  - OpenAPI specs
  - README files
- **Quality:** Reflects actual code behavior, not memory
- **Compatibility:** Claude Code ✓

---

### Tier 3: Emerging & Specialized

#### **Remotion Video Production Skill**
- **Type:** Video code generation
- **Workflow:** Natural language → Remotion React code → Remotion Studio preview → MP4 render
- **Best for:** Automated video generation
- **Compatibility:** Claude Code ✓
- **Status:** Emerging (2026)

#### **Google Workspace Integration (GWS)**
- **Release:** March 2026 (Anthropic + Google)
- **Type:** CLI for dynamic Google Workspace API discovery
- **Features:**
  - Dynamic API surface discovery
  - Unified interface to all Google APIs
  - Simplified authentication
- **Best for:** G Suite automation
- **Compatibility:** Claude Code ✓
- **Status:** Brand new

---

## Skills by Use Case (for Overseer)

### CEO Orchestration Layer
**Required skills:**
- ✓ **Ruflo** (multi-agent swarm orchestration)
- ✓ **Agent Skills** (native subagent spawning)
- ✓ **Multi-Agent Ralph Loop** (learning + routing)
- ✓ **planning-with-files** (session memory)

### Development Workflow
**Required skills:**
- ✓ **TDD Skill** (enforce red-green-refactor)
- ✓ **Git Workflow Skill** (branching, PR, commits)
- ✓ **Code Review Pack** (security, OWASP, CVEs)
- ✓ **OWASP Top 10:2025** (compliance + language-specific)

### Quality Gates
**Required skills:**
- ✓ **Frontend Design** (UI/UX quality)
- ✓ **Web Quality Skills** (accessibility, performance)
- ✓ **Snyk MCP** (dependency + vulnerability scanning)

### Documentation
**Optional skills:**
- ✓ **OpenAPI Spec Generator** (API docs)
- ✓ **Documentation Generation Workflow** (code → docs)

### Marketing & Design (CMO)
**Optional skills:**
- ✓ **Frontend Design** (distinctive UI)
- ✓ **Web Quality Skills** (UX compliance)

---

## Compatibility Matrix: Overseer Setup

| Skill | Claude Code | OpenClaw | Tatyana | Notes |
|-------|:-----------:|:--------:|:-------:|-------|
| Ruflo | ✓ | ? | ✗ | Agent orchestration, not compatible with OpenClaw config |
| Agent Skills | ✓ | ? | ✗ | Native to Claude Code, may not work in OpenClaw |
| TDD | ✓ | ? | ✗ | Code workflow, Claude Code only |
| Git Workflow | ✓ | ? | ✗ | Git tools, Claude Code only |
| planning-with-files | ✓ | ? | ✗ | File-based, works with Claude Code's file API |
| Code Review Pack | ✓ | ? | ✗ | Built-in security tools, Claude Code only |
| OWASP Top 10:2025 | ✓ | ? | ✗ | Security knowledge base, Claude Code workflow |
| Frontend Design | ✓ | ? | ✗ | UI/code generation, Claude Code only |
| Web Quality Skills | ✓ | ? | ✗ | Quality auditing, Claude Code focused |
| OpenAPI Generator | ✓ | ? | ✗ | API documentation, Claude Code workflow |

**Legend:** ✓ = Confirmed compatible | ? = Unknown/untested | ✗ = Not compatible

**Note:** OpenClaw has separate skill ecosystem (ClawHub). Tatyana uses OpenClaw, not Claude Code directly. Skills are primarily Claude Code (Claude Code context) and OpenAI Codex CLI focused.

---

## Key Insights

### 1. Orchestration is Solved
Ruflo (Claude Flow v3) is production-grade agent orchestration that directly maps to our Overseer architecture. It already handles:
- 60+ specialized agents (coders, testers, reviewers, architects)
- Task routing and delegation
- Multi-agent consensus
- Learning/pattern preservation

**Action:** Research integrating Ruflo or adopting its patterns for CEO → C-level agent routing.

### 2. Memory-Driven Planning Works
planning-with-files is most-starred skill (13,410⭐) because it solves the core context problem. We already implement this with HANDOVER + session-context.md. Skill is validated and proven.

**Action:** Study its patterns for session recovery. Consider adopting its three-file approach if not already.

### 3. Quality Gates Are Available
OWASP + Frontend Design + Web Quality form a quality gate pipeline that matches our quality-gates.md rules:
- Security: OWASP Top 10:2025 + CVE scanning
- Frontend: Design principles + accessibility (WCAG)
- Performance: Web quality optimization

**Action:** Install and test OWASP skill for CTO agent during code review phase.

### 4. Git/PR Automation is Mature
Git Workflow Skill + Code Review Pack + PR session management are production-grade. Our current git commit process via CEO could be enhanced.

**Action:** Evaluate Git Workflow Skill for COO agent (git operations, PR workflows).

### 5. Skill Ecosystem is Young But Growing
- 96K+ skills with high variance in quality
- Min 2-star filter eliminates most junk
- Most useful skills are 50-500 stars range (curated, not mainstream)
- Security skills need manual verification (36% of published skills have vulnerabilities)

**Action:** When adopting new skills, run Cisco AI Skill Scanner + manual review (see quality-gates.md).

---

## Recommended Adoption Plan

### Phase 1: Research & Validation (This Sprint)
- [ ] Study Ruflo architecture for agent orchestration patterns
- [ ] Review planning-with-files methodology vs. our HANDOVER system
- [ ] Test Git Workflow Skill on bridge or buxbot projects
- [ ] Evaluate OWASP Top 10:2025 skill for CTO review phase

### Phase 2: Integration (Next Sprint)
- [ ] Install planning-with-files on Overseer CEO session (test)
- [ ] Install Git Workflow Skill in CTO prompt templates
- [ ] Integrate OWASP skill into code-review agent (tester/reviewer)
- [ ] Audit Web Quality Skills for CMO design review

### Phase 3: Refinement (2-3 Weeks)
- [ ] Tune Ruflo patterns for our C-suite structure (CTO, COO, CMO, Штырлиц)
- [ ] Create CEO → agent delegation skill (task routing)
- [ ] Document skill selection criteria in knowledge/

---

## Risks & Mitigations

| Risk | Mitigation |
|------|-----------|
| **Skill churn:** Skills become abandoned, dependency breaks | Lock to verified stars (>50), monthly health checks, use pinned GitHub refs |
| **Security:** 36% of published skills have vulnerabilities | Pre-install scan (Cisco AI Skill Scanner), manual SKILL.md review, no secrets in skills |
| **Version conflicts:** Skill depends on outdated library | Check GitHub issues for compatibility, run tests on target Claude Code version |
| **Context bloat:** Too many skills exceed 2% budget | Lazy-load skills (invoke only when needed), progressive disclosure |
| **Over-automation:** Skills create unmaintainable complexity | Document why each skill is adopted, quarterly review of usage metrics |

---

## Sources

[SkillsMP Platform](https://skillsmp.com)
[SkillsMP Review 2026 - SmartScope](https://smartscope.blog/en/blog/skillsmp-marketplace-guide/)
[SkillsMP 96,751+ Skills - Medium by Julio Pessan](https://medium.com/@julio.pessan.pessan/skillsmp-this-96-751-claude-code-skills-directory-7dec2eabc338)
[SkillsMP 87,427+ Skills - Medium by Joe Njenga](https://medium.com/ai-software-engineer/skillsmp-this-87-427-claude-code-skills-directory-just-exploded-but-with-one-annoying-problem-ec4af66b78cb)
[Top 10 Claude Code Skills 2026 - Composio](https://composio.dev/content/top-claude-skills)
[Best Claude Code Skills 2026 - Firecrawl](https://www.firecrawl.dev/blog/best-claude-code-skills)
[Top 8 Claude Skills - Snyk](https://snyk.io/articles/top-claude-skills-developers/)
[10 Must-Have Skills 2026 - Medium by unicodeveloper](https://medium.com/@unicodeveloper/10-must-have-skills-for-claude-and-any-coding-agent-in-2026-b5451b013051)
[Ruflo GitHub](https://github.com/ruvnet/ruflo)
[planning-with-files GitHub](https://github.com/OthmanAdi/planning-with-files)
[Claude Wizard GitHub](https://github.com/vlad-ko/claude-wizard)
[Git Workflow Skill GitHub](https://github.com/netresearch/git-workflow-skill)
[OWASP Top 10 Skill GitHub](https://github.com/agamm/claude-code-owasp)
[Claude Code Agent Skills - Anthropic Docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
[Claude Code Documentation](https://code.claude.com/docs/en/skills)
[Frontend Design Skill - Anthropic GitHub](https://github.com/anthropics/claude-code/blob/main/plugins/frontend-design/skills/frontend-design/SKILL.md)
[Web Quality Skills via Snyk](https://snyk.io/articles/top-claude-skills-ui-ux-engineers/)
[Claude Code Session Memory](https://code.claude.com/docs/en/common-workflows)

---

## Notes for CEO Review

This research identifies high-value skills that directly map to Overseer's architecture:

1. **Ruflo** is not a threat but a reference implementation. We can adopt its patterns or use it as an orchestration layer.
2. **planning-with-files** validates our HANDOVER/session-context approach. We're on the right track.
3. **OWASP + Git Workflow + Code Review Pack** fill gaps in our quality-gates.md.
4. **No must-install skills** — all are enhancements. Prioritize research over adoption speed.

**Next action:** Assign Штырлиц (research-agent) to deep-dive Ruflo patterns. CEO to decide integration strategy based on complexity vs. value tradeoff.
