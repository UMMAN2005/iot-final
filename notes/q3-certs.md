# Q3 — Certificates and Their Security Coverage (Research Notes)

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

## Mapping: certificate -> security type
- ISO/IEC 27001  -> data storage + transmission (organisational ISMS)
- ISO/IEC 30141  -> hardware + communication (architecture)
- ETSI EN 303 645 -> software + data + communication (consumer device)
- CE / RED       -> hardware safety + communication + (2025) cybersecurity
