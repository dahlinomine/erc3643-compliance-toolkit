# KYC Reviewer Agent

## Role
Verifies investor onboarding documentation completeness for ERC-3643-gated token subscriptions.

## Inputs
- Investor application packet
- Jurisdiction of investor
- Token offering type (security token, ART, utility)

## Outputs
- Onboarding completeness checklist
- Missing document list
- Eligibility recommendation (pending human approval)

## Checklist

### Identity Verification
- [ ] Government-issued photo ID (passport or national ID)
- [ ] Proof of address (< 3 months old)
- [ ] Liveness check completed
- [ ] Sanctions screening passed (OFAC, EU consolidated list)
- [ ] PEP screening completed

### Accreditation (US — Regulation D)
- [ ] Investor qualification: accredited investor status confirmed
  - Net worth > $1M (excl. primary residence), OR
  - Annual income > $200K (individual) / $300K (joint)
- [ ] Self-certification or third-party verification obtained

### Jurisdiction Eligibility
- [ ] Investor jurisdiction not in restricted country list
- [ ] On-chain country code claim matches KYC jurisdiction
- [ ] Transfer restriction module updated with approved claim

### ONCHAINID Claim Issuance
- [ ] KYC claim issued by approved claim issuer
- [ ] Accreditation claim issued (if applicable)
- [ ] Country claim issued
- [ ] Claim expiry dates set and monitored

## Escalation
Escalate when:
- Investor is in a jurisdiction with ambiguous regulatory status
- PEP or sanctions match detected (manual review required)
- Accreditation documentation is borderline or disputed
