# Question 1 — The Five Scientific Pillars of IoT and Their Roles (25 pts)

The Internet of Things is built on five scientific pillars that together turn physical
phenomena into automatic decisions: telematics, data exchange, cloud computing, big data and
artificial intelligence. Each pillar plays a distinct role, and the chain only works when all
five are present.

The first pillar is **telematics**, a discipline that combines telecommunications and
informatics in order to transmit data captured from physical sensors over long distances. In
an IoT project telematics is the edge: the actual hardware that perceives the world and
delivers the very first measurement. A Teltonika FMB140 reading the engine RPM, the fuel level
and the GPS coordinates of a truck, an Arvento Treyki Asset reporting the position of a
container or a person, a Galileosky 7x relaying tachograph data over LTE — all of these are
telematic devices, and without them the rest of the stack would have nothing to operate on.
The role of telematics is therefore to generate observations and to push them out of the
physical environment into the digital world.

The second pillar is **data exchange**, the layer that defines how observations travel between
heterogeneous systems. Telematic devices speak a wide range of protocols — MQTT, CoAP,
HTTP/HTTPS, LwM2M, BLE, NB-IoT, the J1939 vehicle bus, the proprietary Wialon protocol —
and platforms expose their own REST and GraphQL APIs, message queues and webhooks. Data
exchange is the discipline that ensures these protocols speak to each other reliably and
securely. Without standardised data exchange a Galileosky terminal would not be able to send
its frames to a Wialon server, and a back-end could not push them onward to an enterprise
ERP. The role of this pillar is interoperability: it allows independently designed
components to behave as a single system.

The third pillar is **cloud computing**, the on-demand provision of compute, storage,
networking and managed services through the Internet. The cloud is what hosts the IoT
platform: it is where the telemetry lands, where the device fleet is managed, where firmware
is deployed over the air and where dashboards are served to end users. Cloud also gives the
project geographic redundancy and elastic scaling, so that a fleet expanding from one thousand
to one million trackers can be supported without redesigning infrastructure. AWS IoT Core,
Microsoft Azure IoT Hub and Wialon Hosting are concrete examples; the Galileosky 7x described
in Question 2 can forward the same data to several such clouds in parallel. The role of the
cloud pillar is therefore centralisation and scale.

The fourth pillar is **big data**, the family of technologies designed for data sets that are
too large, too fast or too varied for classical relational databases — the well-known volume,
velocity and variety. A relatively small IoT project of ten thousand Galileosky devices
sending one position every thirty seconds already produces close to thirty million records
per day; real industrial fleets reach billions. Streaming platforms such as Apache Kafka,
distributed time-series databases such as InfluxDB or ClickHouse, and batch frameworks such
as Spark are what allow the platform to ingest, retain and pre-aggregate this stream without
losing any record. The role of big data is to make the firehose of telemetry queryable.

The fifth pillar is **artificial intelligence**, the set of machine-learning and statistical
methods that infer patterns and produce predictions or decisions from data. Once telemetry
has been received, exchanged, stored and aggregated, AI is what finally turns it into
actionable knowledge. From the same FMB140 stream that records engine RPM and fuel
consumption, an ML model can predict an injector failure three weeks before it happens; from
Galileosky J1939 data it can score driving behaviour or detect theft; from Treyki BLE
proximity it can build digital twins of warehouses. The role of AI is to extract decisions
from the data, closing the loop that telematics opened.

These five pillars form a directed chain. Telematics generates observations, data exchange
transports them, the cloud stores and orchestrates them, big data structures and aggregates
them, and artificial intelligence extracts decisions that flow back to actuators or human
operators. Remove any pillar and the chain breaks: without telematics there is no
observation, without data exchange no transport, without cloud no scale, without big data the
platform drowns in raw records, and without AI the data, however neatly stored, remains mute.
The Internet of Things, in other words, is exactly the integrated system in which all five of
these scientific pillars operate together.
