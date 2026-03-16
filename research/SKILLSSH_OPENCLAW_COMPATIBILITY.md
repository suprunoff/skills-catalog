# Skills.sh ↔ OpenClaw: Installation & Compatibility Guide

**Date:** 2026-03-16 | **Relevance:** High | **Confidence:** high

## TL;DR: Can Skills.sh Skills Run on OpenClaw?

**YES** — with conditions:

- SKILL.md format is identical across platforms (Vercel standard)
- ClawHub is OpenClaw's fork of Skills.sh (13,729+ skills)
- Most skills work on OpenClaw + Claude Code + GitHub Copilot
- Some skills require OpenClaw-specific wrappers (OAuth, local tools)
- **Security mandatory:** ClawHavoc (Feb 2026) planted 341+ malicious skills

---

## Format Compatibility: SKILL.md is Universal

### Standard SKILL.md Structure (All Platforms)

```yaml
---
name: my-skill
description: What this skill does
author: Author Name
version: 1.0.0
license: MIT
metadata:
  platforms: ["claude-code", "openclaw", "github-copilot"]
  dependencies: ["node >= 16"]
allowed-tools:
  - "web-search"
  - "file-read"
---

# Markdown instructions
This skill teaches agents to [capability].

## Usage
```agent
/my-skill --arg value
```

## Configuration
- `API_KEY`: Set this in environment
```

### What Works Out-of-Box on OpenClaw

✓ **YAML frontmatter:** name, description, author, version, license, metadata  
✓ **Markdown body:** Any text, examples, best practices  
✓ **allowed-tools:** Standard tool names  
✓ **Supporting files:** scripts/, references/, assets/ directories  
✓ **Platform independence:** Code written for "agent" not platform-specific  

### What Requires OpenClaw Adaptation

❌ **Claude Code APIs:** Uses official Claude API calls (don't work on OpenClaw)  
❌ **GitHub Copilot UI:** VS Code extension UI elements (don't exist on OpenClaw)  
❌ **Direct OAuth:** Assumes Azure AD, Google OAuth (OpenClaw uses different auth layer)  
❌ **File paths:** Assumes `/home/user/.vscode/` (OpenClaw uses `~/.openclaw/`)  

---

## ClawHub: OpenClaw's Forked Registry

### What is ClawHub?

- **URL:** https://clawhub.ai
- **Stats:** 13,729+ community skills (as of Feb 2026)
- **Source:** Fork of Skills.sh with OpenClaw-specific metadata
- **Installation:** Via ClawHub UI or `clawhub` CLI
- **Format:** SKILL.md + OpenClaw field extensions

### ClawHub vs Skills.sh

| Aspect | Skills.sh | ClawHub |
|--------|-----------|---------|
| **URL** | skills.sh | clawhub.ai |
| **Total skills** | 89,028 | 13,729 |
| **Target platform** | Multi-agent | OpenClaw only |
| **Install method** | `npx skillsadd` | `clawhub install` |
| **Security scanning** | Not built-in | Koi's Clawdex integration |
| **Malicious skills** | Same as ClawHub (shared source) | ClawHavoc 341+ (Feb 2026) |
| **Auth layer** | Platform-specific | OpenClaw OAuth providers |
| **Tool names** | MCP-standard | OpenClaw extensions |

### Top ClawHub Skills (Overlapping with Skills.sh)

All major Skills.sh skills are available on ClawHub:

| Skill | Skills.sh | ClawHub | Status |
|-------|-----------|---------|--------|
| Capability Evolver | Yes | **35K+ (top)** | OpenClaw native |
| GOG | Yes | **14K+** | OpenClaw optimized |
| Tavily | Yes | 11K+ | Works via MCP |
| Agent Browser | Yes | 11K+ | OpenClaw native |
| firecrawl | Yes | 13.7K | Works via MCP |
| workflow-automation | Yes | 11.6K | Generic |
| seo-audit | Yes | 44.2K | Works everywhere |
| brainstorming | Yes | 57.6K | Generic |

---

## Installation Methods: Skills.sh → OpenClaw

### Method 1: ClawHub UI (Recommended - Safest)

```
Step 1: Open OpenClaw dashboard → http://localhost:8080
Step 2: Navigate to Skills section
Step 3: Search "capability evolver"
Step 4: Click "Install" or "Get Started"
Step 5: Fill required config (API keys, oauth tokens)
Step 6: Click "Save"
Step 7: Restart OpenClaw if prompted
        systemctl restart openclaw
        # or: openclaw gateway restart
```

**Advantages:**
- UI shows dependency info
- Pre-validates compatibility
- Logs installation to `~/.openclaw/skills/`
- Can disable/remove from UI

### Method 2: ClawHub CLI (Fastest)

```bash
# Pre-scan with ClawSecure (mandatory)
clawhub scan "capability-evolver"
# Expected output: OWASP ASI 10/10, no threats

# List available skills
clawhub search "evolver"

# Install with verification
clawhub install --verify openclaw/autogame-17/capability-evolver

# List installed
clawhub list

# Verify post-install
clawhub info "capability-evolver"
```

**Safe sequence:**
```bash
# 1. Backup config
cp ~/.openclaw/openclaw.json ~/.openclaw/openclaw.json.bak-$(date +%Y%m%d)

# 2. Pre-scan
clawsecure scan --skill "capability-evolver"

# 3. Install
clawhub install --verify openclaw/skills/capability-evolver

# 4. Restart
openclaw gateway restart

# 5. Monitor (7 days)
tail -f ~/.openclaw/logs/skills.log
```

### Method 3: Manual Installation (Advanced)

For custom or local skills:

```bash
# 1. Create skill directory
mkdir -p ~/.openclaw/skills/my-custom-skill

# 2. Create SKILL.md
cat > ~/.openclaw/skills/my-custom-skill/SKILL.md << 'SKILL'
---
name: my-custom-skill
description: My custom OpenClaw skill
author: Me
version: 1.0.0
---

# My Skill
This skill does X.
SKILL

# 3. (Optional) Add supporting files
mkdir -p ~/.openclaw/skills/my-custom-skill/scripts
cp myscript.js ~/.openclaw/skills/my-custom-skill/scripts/

# 4. Restart
openclaw gateway restart

# 5. Verify installation
clawhub list | grep my-custom
```

**OpenClaw will:**
- Auto-discover SKILL.md in `~/.openclaw/skills/*/`
- Parse YAML frontmatter
- Load instructions into agent context
- Register allowed-tools

---

## OpenClaw Config: skills Section

### openclaw.json Configuration

```json
{
  "skills": {
    "enabled": true,
    "install": {
      "nodeManager": "npm",  // npm | pnpm | yarn | bun
      "registry": "clawhub",  // Which registry to use
      "verify": true,         // Pre-install security check
      "autoUpdate": false     // Don't auto-update
    },
    "directories": [
      "~/.openclaw/skills",          // Primary
      "~/.openclaw/workspace/skills"  // Workspace-specific
    ],
    "allowedSources": [
      "clawhub.ai",
      "github.com/openclaw/skills",
      "skills.sh"  // For direct Skills.sh installs
    ],
    "security": {
      "scanOnInstall": true,
      "requireSignature": false,  // If true, needs GPG
      "maliciousDatabase": "koi"   // Use Koi's ClawHavoc DB
    }
  }
}
```

### Node Manager Configuration

```json
{
  "skills": {
    "install": {
      "nodeManager": "npm",
      "npmOptions": {
        "registry": "https://registry.npmjs.org",
        "timeout": 30000,
        "fetch-retries": 3
      }
    }
  }
}
```

---

## Cross-Platform Skill Anatomy

### Universal Skill (Works Everywhere)

```yaml
---
name: brainstorming
description: Generate creative ideas through structured prompts
author: Obra
metadata:
  platforms: ["claude-code", "openclaw", "github-copilot", "cursor"]
  tags: ["creative", "ideation", "universal"]
---

# Brainstorming Skill

Use systematic techniques to generate ideas.

## Technique: SCAMPER
- Substitute: What if I replaced X with Y?
- Combine: What if I merged X with Y?
- Adapt: How could I adapt this for...?
```

**Why it works:**
- No platform-specific APIs
- Pure Markdown instructions
- Agent-agnostic language
- No file I/O, no network calls

### OpenClaw-Specific Skill

```yaml
---
name: gog-workspace-integration
description: Integrate Google Workspace with OpenClaw
author: OpenClaw
platforms: ["openclaw"]
metadata:
  openclawSpecific: true
  authType: "oauth:google"
  permissions: ["drive.read", "calendar.read", "gmail.send"]
required-env:
  - GOOGLE_CLIENT_ID
  - GOOGLE_CLIENT_SECRET
allowed-tools:
  - "openclaw:oauth-provider"
  - "openclaw:file-sync"
---

# GOG Skill

Configure OpenClaw's integration layer with Google Workspace.

## OAuth Setup
```openclaw
/configure oauth:google
  --client-id $GOOGLE_CLIENT_ID
  --client-secret $GOOGLE_CLIENT_SECRET
```
```

**Why OpenClaw-specific:**
- Uses OAuth provider layer (not built into Skills.sh)
- File sync via OpenClaw's tools
- Requires OpenClaw config API

---

## Dependency Resolution: npm vs Local

### Node Module Dependencies

Skills can declare npm dependencies in `package.json`:

```json
{
  "name": "@openclaw/skills-package",
  "dependencies": {
    "axios": "^1.6.0",
    "lodash": "^4.17.0"
  }
}
```

OpenClaw's `nodeManager` will:
1. Read `package.json`
2. Run `npm install` (or `yarn`, `pnpm`, `bun`)
3. Make modules available to skill code
4. Cache in `~/.openclaw/node_modules/`

**Config in openclaw.json:**
```json
{
  "skills": {
    "install": {
      "nodeManager": "npm",
      "cacheDir": "~/.openclaw/node_modules"
    }
  }
}
```

---

## Troubleshooting: Skills.sh → OpenClaw Failures

### Symptom 1: "Skill not found after install"

**Causes:**
- SKILL.md not in correct path
- Typo in skill name
- openclaw.json not reloaded

**Fix:**
```bash
# Verify SKILL.md exists
ls ~/.openclaw/skills/capability-evolver/SKILL.md

# Check if registered
clawhub list | grep -i capability

# Restart with force-reload
openclaw gateway restart --force
systemctl restart openclaw

# Check logs
tail -f ~/.openclaw/logs/skills.log
```

### Symptom 2: "Allowed-tool not recognized"

**Cause:** Skill references tool that doesn't exist in OpenClaw

**Fix:**
```yaml
# Bad (Claude Code only)
allowed-tools:
  - "github-code-search"  # Not in OpenClaw

# Good (OpenClaw standard)
allowed-tools:
  - "web-search"
  - "file-read"
  - "firecrawl"  # MCP-compatible
```

### Symptom 3: "OAuth token expired after skill install"

**Cause:** Skill rotated credentials during self-update (Capability Evolver)

**Fix:**
```bash
# Use --review flag for Capability Evolver (NOT Mad Dog mode)
clawhub install --verify \
  --flag review \
  openclaw/autogame-17/capability-evolver

# Restart
openclaw gateway restart

# Monitor for any outbound API calls
ps aux | grep -i openclaw
curl -s http://localhost:8081/telemetry/network | jq .
```

### Symptom 4: "Skill install hangs or slow"

**Cause:** npm/yarn network slowness, large dependency tree

**Fix:**
```bash
# Use faster package manager
openclaw config set skills.install.nodeManager pnpm

# Increase timeout
openclaw config set skills.install.npmOptions.timeout 60000

# Clear cache and retry
rm -rf ~/.openclaw/node_modules ~/.npm
clawhub install --verify --fresh openclaw/skills/tavily
```

---

## Security Hardening: ClawHavoc Prevention

### Pre-Install: ClawSecure + Clawdex

```bash
# Step 1: Scan with ClawSecure
clawsecure scan --skill "capability-evolver"
# Expected: OWASP ASI 10/10, no threat patterns

# Step 2: Check Clawdex (online)
curl -s https://clawdex.koi.security/api/check/capability-evolver | jq .

# Step 3: Manual SKILL.md inspection
cat ~/.openclaw/skills/capability-evolver/SKILL.md | grep -E "file://|exec\(|child_process|webhook|exfiltrate"
# Result: (empty = safe)

# Step 4: Verify author
clawhub info capability-evolver | grep -A5 author
```

### Post-Install: 7-Day Monitoring

```bash
# Watch for suspicious files
find ~/.openclaw/skills/capability-evolver -type f \
  -name "*.zip" -o -name "*.exe" -o -name "*.sh" | grep -v node_modules

# Monitor outbound network
tcpdump -i any -n "dst port 443 or dst port 80" | grep -v api.anthropic.com

# Check API key usage
grep -r "export.*KEY\|setenv.*TOKEN" ~/.openclaw/

# Audit skill logs
cat ~/.openclaw/logs/skills.log | grep -i "error\|warn\|exec\|spawn"
```

### Installation Safeguards

```json
{
  "skills": {
    "security": {
      "scanOnInstall": true,
      "requireSignature": true,
      "maliciousDatabase": "koi",
      "blockPatterns": [
        "password-protected-zip",
        "curl.*-o.*-k",
        "ssh-keygen",
        "webhook.*token"
      ],
      "sandbox": true
    }
  }
}
```

---

## Verification: Skill Functionality Tests

After installation, verify skill actually works:

```bash
# Test 1: Skill is registered
openclaw agent list-skills | grep "capability-evolver"

# Test 2: Skill initialization
openclaw agent invoke --skill "capability-evolver" --dry-run

# Test 3: Skill dependency check
ls ~/.openclaw/node_modules/@openclaw/capability-evolver/

# Test 4: Skill output (if safe test available)
echo '{"query": "help"}' | openclaw skill:capability-evolver

# Test 5: No unexpected files created
find ~/.openclaw -mmin -5 -type f | grep -v logs/ | head
```

---

## Decision Table: Which Installation Method?

| Scenario | Method | Reason |
|----------|--------|--------|
| First-time OpenClaw user | ClawHub UI | Safest, guided, visual feedback |
| Installing 1 skill | CLI (`clawhub install`) | Fast, single command, scannable |
| Installing 5+ skills | Script (loop `clawhub install`) | Repeatable, logged, consistent |
| Custom/internal skill | Manual (`~/.openclaw/skills/`) | Full control, no registry dependency |
| Production OpenClaw | All methods + monitoring | Defense in depth |
| Compromised OpenClaw | Clean install from backup | No workaround |

---

## Quick Compatibility Checklist

```markdown
## Before Installing Skill on OpenClaw

- [ ] Skill listed on ClawHub (not just Skills.sh)?
- [ ] SKILL.md is readable, no obfuscation?
- [ ] ClawSecure scan: PASS (0 threats)?
- [ ] Clawdex check: NOT in malicious registry?
- [ ] Author: 100+ downloads, 1+ year history?
- [ ] allowed-tools match OpenClaw tool names (not Claude Code)?
- [ ] No hardcoded file paths (/home/user/, /Users/)?
- [ ] No platform-specific imports (VS Code, Copilot)?
- [ ] Config backup: `~/.openclaw/openclaw.json.bak-$(date +%Y%m%d)`?
- [ ] Post-install: monitor network 7 days?

If ALL YES: Install. If ANY NO: Skip or modify skill.
```

---

## Summary: Skills.sh + OpenClaw

**Compatible:** Yes, via ClawHub fork + SKILL.md standard  
**Effort:** Low (most skills work out-of-box)  
**Risk:** HIGH (ClawHavoc 341+ malicious skills)  
**Mitigation:** ClawSecure + Clawdex (mandatory)  
**Recommended:** Phase-based rollout (foundation → automation → integration)

**Overseer Skills.sh → OpenClaw Stack:**
1. **Core:** Capability Evolver, firecrawl, Tavily, workflow-automation
2. **Research:** seo-audit, analytics-tracking, data-analysis
3. **Integration:** Agent Browser, N8N, GOG
4. **Safety:** All via ClawHub UI + ClawSecure pre-scan

---

## Sources

- [ClawHub - OpenClaw's Skill Registry](https://clawhub.ai)
- [Skills.sh - Multi-Platform Skill Marketplace](https://skills.sh)
- [SKILL.md Format Specification](https://agentskills.io/specification)
- [How to Install OpenClaw Skills (2026)](https://openclawskill.cc/blog/how-to-install-openclaw-skills)
- [ClawHavoc Attack Analysis](https://www.esecurityplanet.com/threats/hundreds-of-malicious-skills-found-in-openclaws-clawhub/)
- [ClawSecure Security Scanner](https://github.com/ClawSecure/clawsecure-openclaw-security)
- [Clawdex Malicious Skill Detection](https://clawdex.koi.security)

---

**Document Status:** Research Complete | **Confidence:** High | **Updated:** 2026-03-16
