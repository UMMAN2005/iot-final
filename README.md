# IoT-Final — Exam Preparation

Study materials for an Internet-of-Things exam consisting of four questions worth 100 points
total. Each answer is constrained to a maximum of two pages and is written in flowing prose
(tables and bullet points are kept to a minimum, in line with the exam's expectations).

## The four questions

The original prompt is in [`questions.txt`](./questions.txt). In short:

1. **(25 pts)** The five scientific pillars of IoT — telematics, big data, AI, cloud and
   data exchange — and the role each one plays.
2. **(35 pts)** At least four telematic / IoT devices with technical specifications and the
   role each plays in an arbitrary IoT project (IMT11, IMT14, IMT53, Treyki, GTS and the
   like).
3. **(15 pts)** At least four certificates with their purpose, classified by security type
   (software, hardware, data transmission, communication, data storage).
4. **(25 pts)** Applications of IoT in business-oriented and government-oriented projects,
   with three specific government examples.

## Repository layout

```
IoT-Final/
|-- questions.txt              the original exam prompt
|-- answers/                   final two-page answers (prose)
|   |-- q1-pillars.md
|   |-- q2-devices.md
|   |-- q3-certs.md
|   `-- q4-apps.md
`-- notes/                     research scratchpads behind each answer
    |-- q1-pillars.md
    |-- q2-devices.md
    |-- q3-certs.md
    `-- q4-apps.md
```

The files in `answers/` are the polished exam responses (each ~700-840 words, i.e. roughly
two pages). The matching files in `notes/` capture the raw research — datasheet excerpts,
specifications, source URLs and certificate scopes — used to draft the answers, kept so the
underlying facts can be re-checked or extended later.

## What each answer covers

- **Q1 — pillars:** five paragraphs, one per pillar, each with a concrete device example
  pulled from Q2, plus a closing paragraph that explains how the five pillars chain into a
  single IoT pipeline.
- **Q2 — devices:** four real telematic devices described in technical detail and mapped to
  their IoT role: Arvento IMT.14 (industrial vehicle tracker), Arvento Treyki Asset
  (cordless personal/asset locator), Teltonika FMB140 (advanced GPS + dual-CAN tracker) and
  Galileosky 7x (multi-protocol heavy-duty terminal). The notes file additionally documents
  IMT.11, IMT.53 and FMB920 as alternates.
- **Q3 — certificates:** ISO/IEC 27001 (organisational ISMS), ISO/IEC 30141 (IoT reference
  architecture), ETSI EN 303 645 (consumer IoT cybersecurity baseline), CE/RED (EU radio
  + cybersecurity) and the regional CCC / FCC marks, each mapped to the security types it
  actually covers.
- **Q4 — applications:** business families (Industrial IoT, fleet, smart agriculture,
  retail/healthcare) plus three concrete government deployments — Singapore's Smart Nation
  programme, Smart City Barcelona (with hard numbers from the Sentilo platform) and
  Estonia's e-Estonia / X-Road interoperability layer.

## Spaced repetition

A companion Anki deck named `IoT-Final-Exam` was generated alongside the written answers,
containing 25 active-recall cards spread across the four questions (pillars, device specs,
certificate scopes, government deployment metrics). The deck lives in the local Anki
collection rather than in this repo.

## Working notes

The repository was prepared with the help of Claude Code; the `.gitignore` excludes the
`.claude/` harness directory so that local agent state never lands in version control.
