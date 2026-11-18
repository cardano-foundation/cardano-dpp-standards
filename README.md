# Digital Product Passport on Cardano

## The Problem

The EU Ecodesign for Sustainable Products Regulation (ESPR) mandates Digital Product Passports (DPP) across many product categories, with the first mandatory passports (certain batteries, under the Batteries Regulation) due from 18 February 2027. Other sectors phase in through product-specific delegated acts. Penalties for non-compliance are set by each member state and must be effective, proportionate and dissuasive. Turnover-based fines on the scale seen under GDPR (4%) are a useful benchmark for the risk involved. Companies must provide transparent, verifiable product information such as, materials, origin, manufacturing details, usage history, and disposal guidance throughout entire supply chains.

The challenge? Supply chains involve multiple competing organizations without a central authority: manufacturers, suppliers, distributors, recyclers, and regulators. Traditional centralized databases can't provide:

- Multi-party trust when stakeholders don't trust each other  
- Data permanence beyond organizational changes (required: product lifetime + 10 years)  
- Tamper-proof records for regulatory audits and anti-counterfeiting  
- Cross-border interoperability for global supply chains  
- Privacy-respecting transparency (disclose only what's needed, when needed)

See [Regulatory & Standards References](#regulatory--standards-references) for the regulations, EU timelines and CEN-CENELEC standards behind this work.

---

## Repository Contents

This repository provides a comprehensive blueprint for implementing Digital Product Passports on Cardano—a blockchain platform uniquely positioned for enterprise DPP requirements through its energy efficiency (99.9% more efficient than proof-of-work chains), predictable low costs, and formal verification capabilities.

- **Solution Patterns** with cost analysis, code examples, and implementation guides
- **Industry Personas** mapping business needs to technical solutions
- **Decision Framework** for pattern selection
- **DPP Cardano Problem Statement** – [CPS-0035](#cardano-problem-statement-cps-0035), assigned a number and in review

**Living Document:**  
This repository is maintained by a working group of companies implementing DPP solutions on Cardano. The group meets monthly for technical Q&A sessions to address implementation challenges, share learnings, and refine best practices. Content is continuously updated based on real-world feedback and community input.

---

## Cardano Problem Statement (CPS-0035)

The problem statement for DPP on Cardano has been assigned **CPS-0035: Digital Product Passports** and is in the Cardano Improvement Proposal process. It is maintained in the CIPs repository rather than here:

- Discussion and review: [cardano-foundation/CIPs PR #1114](https://github.com/cardano-foundation/CIPs/pull/1114)
- Latest text: [CPS-0035/README.md](https://github.com/david-a-clark/CIPs/blob/master/CPS-0035/README.md)

<!-- Once PR #1114 is merged, replace the "Latest text" link with https://cips.cardano.org/cps/CPS-0035 -->

---

## DPP User Personas (Draft)

Profiles mapping business needs to technical solutions:

- **Clara Müller** – Compliance-first textile manufacturer seeking cost-effective ESPR compliance  
- **Sophie Laurent** – Automotive battery supply chain manager coordinating multi-stakeholder lifecycle tracking  
- **Marco Rossi** – Global retailer CTO managing millions of SKUs at scale  
- **Marina Silva** – Plastic recovery operations documenting verified environmental impact  
- **Dr. Javier Ortega** – Integration provider bridging ERP systems to blockchain  

Each persona includes goals, requirements, pain points, and recommended solution patterns.

---

## DPP on Cardano — Solution Blueprint (Draft)

A modular library of architectural patterns with complete implementation guidance:

### Four Solution Patterns:

#### Static Passport Anchor (~0.2 ADA/product)
- For stable product data with rare updates  
- One-time compliance setup for SMEs  
- Includes: Registration flows, verification processes, versioning strategies  
- Code examples: JavaScript registration service, Aiken validator

#### Anchored Proof (~0.2 ADA/update)
- Privacy-preserving certificates with selective disclosure  
- Keep ERP/PIM data confidential while providing verifiable proofs  
- Includes: Merkle tree proofs, access control patterns, auditor workflows  
- Code examples: Privacy proof creation, verification API

#### Event Log (~0.25 ADA/batch)
- Append-only lifecycle history across multiple organizations  
- IoT integration, multi-party submissions, compliance audit trails  
- Includes: Event batching, timeline reconstruction, certificate issuance  
- Code examples: Event batch recording, historical verification

#### High Throughput (~0.3 ADA/1k products)
- Enterprise-scale operations for millions of products  
- Sub-second QR scan responses with caching infrastructure  
- Includes: Bulk processing, partition strategies, consumer-facing performance  
- Code examples: Bulk ingestion, fast verification service

---

### Decision Framework

- Interactive decision matrix (when to use each pattern. Please note that multiple patterns can be used combined together, depends on the requirements)  
- Trade-off analysis: complexity vs. cost vs. privacy vs. throughput   
- Persona-to-pattern mapping for quick identification

---

### Technical Deep-Dives

- Versioning strategies: Burn-and-mint vs. mint-only approaches  
- Data structures: Merkle Trees (default) and Merkle Patricia Tries  
- Standards alignment: GS1 Digital Link, CIP-25/68, JSON-LD, EPCIS 2.0  
- On-chain vs. off-chain architecture: What to anchor, what to keep private

---

### Implementation Guidance

- Component flows  
- Sample on-chain metadata structures (JSON/CBOR)  
- Skeleton code in JavaScript and Aiken  
- Storage options (IPFS, IAGON, S3)

---

## Why Cardano for DPP?

### Technical Advantages:

- Predictable low fees – Sustainable economics at enterprise scale  
- 99.9% energy efficient – Aligns with EU sustainability mandates  
- Deterministic execution – UTxO model provides reliable smart contract behavior  
- Native token standards – Built-in NFT capabilities (CIP-25 - without smart contract complexity), (CIP-68 - smart contract required)  
- Formal verification – Mathematical proofs for critical compliance logic  
- Long-term permanence – Decentralized network ensures data outlives any single organization

### Use Cases:

- EU Battery Passport compliance (automotive, energy storage)  
- Textile traceability (fashion, apparel)  
- Electronics lifecycle management  
- Luxury goods authentication  
- Plastic waste recovery certification

---

## Getting Started

1. Identify your persona – Review the user personas to find your use case  
2. Choose your pattern – Use the decision matrix in the blueprint  
3. Start small – Pilot with a product subset  
4. Iterate and scale – Refine based on feedback  
5. Contribute back – Share learnings with the community

---

## Current Status & Roadmap

- Version: 0.1 Draft (WIP)  
- Status: Open for community feedback and contributions

### Working Group Members

The working group meets monthly. Organisations currently listed as members:

- Plastiks.io – Recyclable/recovery solutions  
- Tokenance – Complete DPP solution provider (luxury watch integration)  
- Blazar Labs – Textile industry DPP (Moldova vertical expertise)  
- Zengate Global – Traceability platforms  
- Agrow Labs – Agricultural traceability (Official CF Partner)  
- LW3 – Blockchain-based DPP expansion  
- Vetrii – Vehicle and battery tokenization through blockchain-based smart passports

---

## Join the Working Group

The DPP on Cardano working group meets monthly to:

- Share implementation experiences and challenges  
- Discuss emerging regulatory requirements  
- Refine technical patterns and best practices  
- Coordinate ecosystem development  
- Align on standards and interoperability

To Join: Open an issue titled "Working Group Participation Request" with your organization, role, industry focus, and implementation status.

---

## Regulatory & Standards References

The key regulations, standards and EU resources this work aligns with. These are also cited in [CPS-0035](#cardano-problem-statement-cps-0035).

### EU regulation & timelines

- [Regulation (EU) 2024/1781 – ESPR](https://eur-lex.europa.eu/eli/reg/2024/1781/oj/eng): the Ecodesign for Sustainable Products Regulation, the framework for DPPs across product categories
- [Regulation (EU) 2023/1542 – Batteries Regulation](https://eur-lex.europa.eu/eli/reg/2023/1542/oj): battery passports mandatory from 18 February 2027 for EV, light-transport (e-bike, e-scooter) and industrial batteries above 2 kWh
- [European Commission – Digital Product Passport & indicative timeline](https://single-market-economy.ec.europa.eu/single-market/digital-product-passport_en#dpp-timeline): sector roll-out as delegated acts are adopted
- [EU DPP Registry](https://single-market-economy.ec.europa.eu/single-market/digital-product-passport/dpp-registry_en): live since 20 July 2026, with a public testing environment; holds identifiers and registration metadata, while passport content stays with the economic operator or DPP service provider
- [European Parliament study (2024)](https://www.europarl.europa.eu/RegData/etudes/STUD/2024/757808/EPRS_STU(2024)757808_EN.pdf)

### European DPP standards (CEN-CENELEC JTC 24)

All eight "Digital Product Passport – Framework and System" standards, developed under Standardisation Request M/604, are published ([CEN-CENELEC listing](https://standards.cencenelec.eu/ords/f?p=205:32:::::FSP_ORG_ID,FSP_LANG_ID:3342699,25&cs=1FC22FDE02FD51137ADC6BE8CA4E10E8F)):

| Standard | Scope |
|---|---|
| EN 18216 | Data exchange protocols |
| EN 18219 | Unique identifiers |
| EN 18220 | Data carriers (e.g. QR codes) |
| EN 18221 | Data storage, archiving and persistence |
| EN 18222 | APIs |
| EN 18223 | System interoperability |
| EN 18239 | Access rights, information security and business confidentiality |
| EN 18246 | Data authentication, reliability and integrity |

The first six are cited as harmonised standards under Commission Implementing Decision (EU) 2026/1736; see the Commission's timeline for the remaining two.

### Reference architecture & EU initiatives

- [CIRPASS-2](https://cirpass2.eu/): EU-funded DPP reference architecture (D4.1 v1.1); recommends immutable passport records with timestamped updates, and an HTTP + Verifiable Credential model with DIDs as an optional overlay

### Identification & data standards

- [GS1 Digital Link](https://www.gs1.org/standards/gs1-digital-link): resolves product identifiers (GTINs) from QR/NFC scans to online information
- [GS1 EPCIS 2.0](https://www.gs1.org/standards/epcis) (ISO/IEC 19987): supply chain event capture
- [W3C Verifiable Credentials 2.0](https://www.w3.org/TR/vc-data-model-2.0/) and [SD-JWT (RFC 9901)](https://www.rfc-editor.org/info/rfc9901/): carrying the passport and selective disclosure of fields

### Cardano standards 

- [CIP-25](https://cips.cardano.org/cip/CIP-0025) and [CIP-68](https://cips.cardano.org/cip/CIP-0068): Cardano token/NFT metadata standards (CIP-68 allows structured updates via datum)
---

## Contributing

We welcome contributions in:

- Additional persona profiles and use cases  
- New architectural patterns  
- Implementation examples and code  
- Standards alignment updates  
- Real-world deployment experiences

## 📝 Contribution Guidelines

Please follow our [CONTRIBUTING.md](./CONTRIBUTING.md) for best practices and submission process. 
