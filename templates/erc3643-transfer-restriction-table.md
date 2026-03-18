# ERC-3643 Transfer Restriction Table Template

> Map your token's transfer restriction rules to on-chain compliance module parameters.

---

## Token Details

| Field | Value |
|-------|-------|
| Token name | `[TOKEN NAME]` |
| Token symbol | `[SYMBOL]` |
| Contract address | `[0x...]` |
| Compliance module | `[0x...]` |
| Identity registry | `[0x...]` |

---

## Investor Eligibility Rules

| Rule | Parameter | Value | On-Chain Module |
|------|-----------|-------|-----------------|
| Minimum accreditation level | `investorType` claim | `ACCREDITED` or `QUALIFIED` | `MaxBalance` / custom |
| Minimum KYC level | `kycLevel` claim | `LEVEL_2` | Identity Registry |
| Jurisdiction whitelist | `country` claim | `[list of ISO-3166 codes]` | `CountryRestrict` |
| Jurisdiction blacklist | `country` claim | `[list of ISO-3166 codes]` | `CountryRestrict` |
| Maximum investor count | N/A | `[NUMBER]` | `MaxInvestors` |
| Minimum holding period (lockup) | Transfer timestamp | `[DAYS]` days | `TimeExchangeLimits` |
| Per-investor maximum balance | Token balance | `[AMOUNT]` | `MaxBalance` |
| Minimum transfer amount | Transfer value | `[AMOUNT]` | custom |

---

## Claim Requirements Matrix

| Claim Type | Required | Claim Issuer | Expiry |
|------------|----------|-------------|--------|
| KYC verified | Yes | `[ISSUER ADDRESS]` | 12 months |
| Accreditation | Yes (US investors) | `[ISSUER ADDRESS]` | 24 months |
| Country code | Yes | `[ISSUER ADDRESS]` | No expiry |
| AML cleared | Yes | `[ISSUER ADDRESS]` | 12 months |
| Institutional investor | Conditional | `[ISSUER ADDRESS]` | 24 months |

---

## Restricted Jurisdictions

```
# Jurisdictions where this token cannot be offered or transferred to
# ISO 3166-1 alpha-2 country codes

RESTRICTED:
  - US  # Adjust based on Reg S / Reg D election
  - IR  # Iran (OFAC)
  - KP  # North Korea (OFAC)
  - RU  # Russia (sanctions)
  - SY  # Syria (OFAC)
  - CU  # Cuba (OFAC)
```

---
*Customize based on your specific token offering, jurisdiction, and legal structure.*
