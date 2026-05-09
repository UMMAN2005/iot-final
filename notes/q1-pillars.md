# Q1 — Five Scientific Pillars of IoT (Research Notes)

The five pillars per the question: Telematics, Big Data, Artificial Intelligence, Cloud,
Data Exchange. The answer should describe each and its role.

## 1. Telematics
- Definition: science of long-distance transmission of data from sensors and vehicles, combining telecom + informatics.
- Role in IoT: provides the edge of the system — physical sensors/devices that perceive the world (location, motion, temperature, vehicle state).
- Concrete example from Q2: Arvento IMT.14 / Teltonika FMB140 / Galileosky 7x. They sample GPS, fuel level, ignition, temperature — the raw observations feeding the rest of the stack.

## 2. Big Data
- Definition: technologies for storing, processing and analysing data sets too large/fast/varied for classical databases (3V: volume, velocity, variety).
- Role in IoT: a platform receives millions of telemetry messages per minute; big-data systems (Kafka streaming, Hadoop, time-series DBs like InfluxDB or ClickHouse) ingest, store, pre-aggregate.
- Example: a fleet of 10 000 Galileosky terminals sending 1 position per 30 s = 28 800 000 records/day.

## 3. Artificial Intelligence
- Definition: machine learning (supervised/unsupervised/reinforcement) and statistical modelling that infers patterns and produces predictions or decisions from data.
- Role in IoT: turns raw telemetry into actionable knowledge — predictive maintenance, eco-driving scoring, anomaly/theft detection, route optimisation, computer-vision QA, digital twins.
- Example: FMB140 reads engine RPM + fuel consumption -> ML model predicts injector failure 3 weeks ahead.

## 4. Cloud
- Definition: on-demand delivery of compute, storage, networking and managed services through the Internet (IaaS / PaaS / SaaS).
- Role in IoT: hosts the platform layer where telemetry lands, where AI models are trained, where dashboards run, and where devices are managed remotely (FOTA, configuration). Provides geographic redundancy and elastic scaling.
- Example: AWS IoT Core, Azure IoT Hub, Wialon Hosting. Galileosky 7x can forward to multiple clouds in parallel.

## 5. Data Exchange
- Definition: the communication/interoperability layer — protocols, APIs and standards that move data between heterogeneous systems.
- Role in IoT: nothing works without standardised exchange. Device level: MQTT, CoAP, HTTP/HTTPS, LwM2M, OPC-UA. Platform level: REST/GraphQL APIs, webhooks, message queues. Application level: SDKs, BI integrations.
- Example: Treyki Asset speaks BLE 5.0 to nearby beacons and TLS-MQTT to its server; Galileosky 7x sends Wialon-protocol packets over TCP and J1939 frames inside the truck.

## How the pillars connect (for conclusion paragraph)
Telematics produces the data; Data Exchange transports it across protocols; the Cloud stores
and orchestrates it at scale; Big Data structures and aggregates it; AI extracts decisions
from it. Remove any pillar and IoT collapses: without telematics there is no observation,
without data exchange there is no transport, without cloud there is no scale, without big data
the platform drowns, without AI the data is mute.
