# ERC-3643 Compliance Toolkit

> A practitioner's toolkit for RWA tokenization compliance — agent configs, regulatory templates, and SOUL.md agents for ERC-3643 implementations.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

---

## What's in this repo

| Path | What it contains |
|------|------------------|
| `agents/` | SOUL.md agents for compliance workflows |
| `agent.yaml` | gitagent manifest with full regulatory compliance section |
| `templates/` | Regulatory document templates (FINRA, SEC, MiCA) |
| `workflows/` | SkillsFlow YAML pipelines for token issuance and audit |

---

## Regulatory Coverage

| Regulation | Jurisdiction | Relevance |
|------------|-------------|----------|
| FINRA 3110 | US | Supervisory systems for broker-dealers holding tokenized securities |
| FINRA 4511 | US | Books and records requirements for digital asset transactions |
| SEC 17a-4 | US | Electronic recordkeeping — applies to tokenized securities platforms |
| SR 11-7 | US | Model risk management for algorithmic compliance checks |
| MiCA Art. 16–21 | EU | Issuer obligations for asset-referenced tokens |
| ERC-3643 / T-REX | Global | On-chain identity and transfer restriction standard for compliant security tokens |

---

## Quick Start

```bash
# Install gitagent CLI
npm install -g gitagent

# Validate this repo's agent manifest
gitagent validate

# Run the compliance auditor agent
gitagent run -a claude-code --agent agents/compliance-auditor.md

# Export to your preferred framework
gitagent export -f openai       # OpenAI
gitagent export -f crewai       # CrewAI
gitagent export -f lyzr         # Lyzr
```

---

## Agents

### `compliance-auditor`
Reviews token smart contracts and issuance documentation against ERC-3643 transfer restriction requirements, FINRA recordkeeping obligations, and MiCA issuer disclosures.

### `kyc-reviewer`
Verifies investor onboarding documentation completeness — identity verification, accreditation status, and jurisdiction eligibility under applicable securities law.

### `transfer-restriction-advisor`
Analyzes proposed token transfer scenarios against on-chain identity registry (ONCHAINID) rules and off-chain regulatory transfer restriction tables.

---

## Templates

- `templates/finra-supervisory-procedures.md` — Template supervisory procedures document for broker-dealers
- `templates/sec-17a4-records-policy.md` — Electronic recordkeeping policy template
- `templates/mica-issuer-disclosure.md` — MiCA Art. 19 white paper disclosure checklist
- `templates/erc3643-transfer-restriction-table.md` — Transfer restriction mapping template

---

## Contributing

PRs welcome. Issues and discussions open. If you're building RWA infrastructure and hit a compliance gap not covered here, open an issue.

---

## Author

**Alhassan Mohammed** — RWA tokenization consultant specializing in ERC-3643 implementations and digital asset compliance.

- GitHub: [@dahlinomine](https://github.com/dahlinomine)
