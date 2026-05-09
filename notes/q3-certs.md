# Q3 — Certificates and Their Security Coverage (Research Notes)

The exam asks for >=4 certificates with purpose AND security types: HW / SW / data-storage /
data-transmission / communication. Picked 6 (will use 5 in answer).

## ISO/IEC 27001:2022 — Information Security Management System (ISMS)
- Source: iso.org/standard/27001
- Purpose: holistic management standard for protecting confidentiality, integrity, availability of information.
- Scope: organisation-wide ISMS — policies, risk assessment, controls (Annex A), continuous improvement.
- Security categories covered: SOFTWARE policies, DATA STORAGE (encryption, access control, retention), DATA TRANSMISSION (confidentiality controls), HUMAN/PROCESS layer.
- Relevance to IoT: every cloud platform receiving telemetry must run an ISMS to protect that data.

## ISO/IEC 30141:2024 — IoT Reference Architecture
- Source: iso.org/standard/88800
- Purpose: architectural standard, not security-only; defines the conceptual layers (device, gateway, network, platform, application, business) and trust/reliability domains.
- Security categories: HARDWARE, COMMUNICATION, DATA TRANSMISSION (architecture mandates trust boundaries between layers).
- Relevance: gives designers a common vocabulary for describing where security must be enforced in an IoT system.

## ETSI EN 303 645 v3.1.3 — Cyber Security for Consumer IoT
- Source: etsi.org
- Purpose: baseline cybersecurity provisions for all consumer IoT devices (smart locks, cameras, wearables, smart-home).
- 13 provisions: no universal default passwords; vulnerability disclosure; keep software updated; securely store sensitive params; communicate securely; minimise attack surface; ensure software integrity; protect personal data; system resilience; examine telemetry data; easy user data deletion; easy installation/maintenance; validate input data.
- Security categories: SOFTWARE updates, HARDWARE root-of-trust, DATA STORAGE (no hardcoded credentials), DATA TRANSMISSION (TLS), COMMUNICATION integrity.
- Relevance: EU baseline IoT consumer security standard; UK PSTI Act and California SB-327 align to it.

## CE / RED (Radio Equipment Directive 2014/53/EU + Delegated Act 2022/30)
- Source: ec.europa.eu
- Purpose: mandatory EU conformity mark for any radio equipment (cellular, BLE, Wi-Fi, LoRa) placed on the EU market.
- From 1 August 2025: cybersecurity articles 3.3(d/e/f) enforceable — network protection, personal-data/privacy protection, fraud protection.
- Security categories: HARDWARE (EMC + safety), COMMUNICATION (radio spectrum), DATA TRANSMISSION (cyber from Aug-2025), DATA STORAGE (private credentials).
- Relevance: every Arvento/Teltonika/Galileosky tracker in Q2 carries CE/RED.

## CCC (China Compulsory Certificate) — GB standards
- Purpose: mandatory Chinese certificate for ~150 product categories, including IT, telecom and IoT terminals; covers safety + EMC + sometimes RF spectrum (SRRC) and information security (MLPS).
- Issuer: CNCA / CQC.
- Security categories: HARDWARE safety (electric shock, fire), COMMUNICATION (EMC, RF), increasingly DATA STORAGE for IT products under Multi-Level Protection Scheme.
- Relevance: required for sale of any IoT device on the Chinese market.

## FCC Part 15 / 22 / 24 / 27 — USA
- Purpose: U.S. Federal Communications Commission rules for unintentional and intentional radio emitters.
- Part 15: limits unintentional/intentional radiators (Wi-Fi, BLE, sub-GHz). Part 22/24/27 covers cellular.
- Security categories: HARDWARE (RF), COMMUNICATION (spectrum coexistence). No data-layer security.
- Relevance: required for U.S. market entry of any wireless IoT device.

## ISO/IEC 27701:2019 — Privacy Information Management (extension of 27001)
- Purpose: extension of 27001 specifically for personal-data processing controllers/processors; aligns with GDPR.
- Security categories: DATA STORAGE & DATA TRANSMISSION of personal data, plus PROCESS/legal compliance.
- Relevance: when an IoT project tracks people (e.g. Treyki), 27701 is the certifying standard.

---

## Mapping: certificate -> security type
- ISO/IEC 27001  -> data storage + transmission (organisational ISMS)
- ISO/IEC 30141  -> hardware + communication (architecture)
- ETSI EN 303 645 -> software + data + communication (consumer device)
- CE / RED       -> hardware safety + communication + (2025) cybersecurity
- CCC            -> hardware safety + EMC + communication
- FCC            -> hardware + communication (RF emissions only)
- ISO/IEC 27701  -> data storage / personal-data privacy

## Picks for the 2-page answer (5)
1. ISO/IEC 27001 — organisational data security management
2. ISO/IEC 30141 — IoT reference architecture
3. ETSI EN 303 645 — consumer IoT cybersecurity
4. CE / RED — EU radio + cybersecurity
5. CCC + FCC — regional hardware/communication marks (briefly grouped)
