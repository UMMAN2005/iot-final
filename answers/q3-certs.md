# Question 3 — Certificates Relevant to IoT Devices and Their Security Types (15 pts)

An IoT device cannot be sold or trusted without a chain of certifications that prove different
security properties: that the radio emissions are safe, that the firmware is hardened, that
the back-end protects user data, and that the architecture itself is reliable. Below I describe
five certificates and standards I would actually require for an IoT product, and for each I
identify the security category it really covers — hardware, software, communication, data
transmission or data storage.

The most foundational organisational certificate is **ISO/IEC 27001:2022 — Information Security
Management System**. It is not a technical product certificate but a management certificate
awarded to a company that has built an ISMS: a documented set of policies, risk assessments
and Annex A controls that protect the confidentiality, integrity and availability of every
piece of information the organisation handles. In an IoT project ISO/IEC 27001 is what proves
that the back-end cloud receiving the trackers' telemetry encrypts data at rest, controls who
can access it, audits every operation, and continuously improves. In terms of security types
it covers software policies, data storage (encryption, retention, access control) and data
transmission (TLS, key management) — essentially the entire data layer of the project.

A purely architectural certificate is **ISO/IEC 30141:2024 — Internet of Things Reference
Architecture**. It does not certify a device, it certifies that a product or system has been
designed against an internationally agreed model. The standard describes the IoT in terms of
six logical entities (device, gateway, network, platform, application and business) and
defines trust and reliability boundaries between them. By following ISO/IEC 30141 a designer
guarantees that hardware roots-of-trust, secure communication channels and access control
points are placed where the architecture demands them. The security types it touches are
therefore hardware (root-of-trust at the device entity), communication (between gateway and
platform) and data transmission (across network entities).

For consumer IoT devices specifically the dominant cybersecurity standard is **ETSI EN 303 645
v3.1.3** (the EU baseline that the UK Product Security Act and California SB-327 also align
with). It contains thirteen baseline provisions, the best-known of which are the prohibition
of universal default passwords, the obligation to keep software updated, to securely store
sensitive parameters, to communicate securely, to ensure software integrity, to protect
personal data and to validate input data. ETSI EN 303 645 is therefore the certificate that
actually attacks every layer of device security at once: hardware (root-of-trust storage),
software (signed updates, integrity verification), data storage (no hard-coded keys) and
data transmission (TLS) and communication (minimised attack surface).

Even before software security comes the radio: in the European Union, every wireless device
must carry the **CE mark with the Radio Equipment Directive (2014/53/EU)**. RED tests
electromagnetic compatibility, electrical safety and efficient use of the radio spectrum;
since 1 August 2025 articles 3.3(d), 3.3(e) and 3.3(f) of the Delegated Act 2022/30 also
require manufacturers to demonstrate network protection, personal-data and privacy protection
and fraud protection in software. CE/RED therefore covers hardware safety, communication
(spectrum and EMC), and — since 2025 — data transmission and storage from a cybersecurity
angle. Every Teltonika, Arvento and Galileosky device described in Question 2 carries this
mark.

Taken together these five certificates form a layered security envelope around an IoT product.
CE/RED certify the hardware and the radio. ETSI EN 303 645 certifies the device
firmware and the on-device handling of secrets. ISO/IEC 30141 certifies the architecture in
which all the entities are arranged. ISO/IEC 27001 finally certifies the organisation that
operates the cloud back-end and protects the stored and transmitted user data. A serious IoT
project should be able to point to at least one certificate in each of those layers; otherwise
some part of the security chain is unproved.
