# Question 2 — Telematic / IoT Devices and Their Role in an IoT Project (35 pts)

A telematic device is the physical edge of an Internet-of-Things project: it perceives the
physical world (location, motion, temperature, vehicle CAN bus, identification of a person or
parcel) and pushes that information to a back-end through a wireless channel. Below I describe
four devices that I would actually combine in a logistics-and-personnel monitoring project.
Together they cover all common edge roles — light vehicle tracking, harsh-environment fleet
telematics, deep vehicle integration, and personal/asset localisation — so they illustrate how
heterogeneous edge hardware feeds a single IoT platform.

The **Arvento IMT.14** is a vehicle-mounted GPS/GSM tracker built by the Turkish manufacturer
Arvento for harsh-climate fleet operations. It works between -40 C and +75 C, weighs 105 g
and is packaged in a 103 x 68.5 x 19 mm enclosure. It draws power from the 12-24 VDC vehicle
electrical system and is backed by a 900 mAh Li-Polymer battery so that it survives ignition
loss and theft attempts. The cellular side is built around a u-blox SARA-G340 module that
covers quad-band GSM (850/900/1800/1900 MHz) and three LTE bands (3, 7, 20), so the device
remains reachable across European and CIS networks. Inside an IoT project this device plays
the role of a telematics edge sensor: every few seconds it samples GPS coordinates, speed,
ignition state and shock events, then forwards them over GPRS or LTE to a fleet-management
server, where the data is stored, visualised and used by analytics services. It is therefore
the source feeding both the telematics and data-exchange pillars of the IoT stack.

The **Arvento Treyki Asset** is a cordless, install-free locator the size of a matchbox. It is
powered by an internal 2000 mAh Li-Polymer cell, sealed to IP68 (so it survives dust, rain
and short submersion) and equipped with GNSS plus assist-GNSS (A-GPS) for fast cold-start
fixes. It also carries Bluetooth Low Energy 5.0 and a six-axis accelerometer, supports up to
1000 circular and polynomial geofences, accepts firmware updates over the air (FOTA) and
can be reconfigured by SMS. In an IoT project the Treyki Asset is the low-power edge node
attached to a container, a tool case or a person. It is the device that reports a stolen
parcel or a lone worker who has fallen, and through its BLE radio it can also act as a
gateway to nearby BLE temperature, humidity or beacon sensors — building a small mesh of edge
devices around itself.

The **Teltonika FMB140** is a far more capable in-vehicle terminal. It combines the same
TM2500 GSM/GNSS/Bluetooth module that powers the rest of the FMB family with two integrated
CAN interfaces and either the LV-CAN200 or ALL-CAN300 firmware. Through these CAN interfaces
the device reads the vehicle's own ECU and reports fuel level, total consumption, odometer,
real wheel speed, engine RPM, accelerator pedal position, AdBlue level, engine life-time
counter and even airbag status. It supports GPS, GLONASS, Galileo and BeiDou simultaneously
on a 33-channel receiver with -165 dBm sensitivity and better than 2.5 m CEP positional
accuracy. It exposes three digital inputs, two digital outputs, two analog inputs and a 1-Wire
bus on a 65 x 56.6 x 20.6 mm body that operates from -40 C to +85 C and accepts both a
Micro-SIM and an eSIM. It is regulated under CE/RED, E-Mark, EAC and RoHS. In an IoT project
the FMB140 plays the role of a deep vehicle gateway: it does not merely report position, it
extracts the truck's own diagnostic stream and turns it into structured CAN-data telemetry,
which on the back-end feeds predictive-maintenance and fuel-analytics services — bridging the
telematics, big-data and AI pillars.

The **Galileosky 7x** is the most capable of the four. Manufactured by Galileosky, it supports
2G, 3G and 4G LTE simultaneously, with dual SIM, BLE, voice calls and a built-in blackbox
memory used as a buffer when the network is unavailable. Through a J1939 CAN-bus reader it can
expose up to 13 400 vehicle parameters and additionally accepts inputs from RS-232/RS-485 fuel
and temperature sensors, 1-Wire DS1923 and DS18B20 sensors, Modbus devices, refrigerator
controllers (DataCold, ThermoKing, Mitsubishi), TPMS pressure sensors, RFID/iButton readers,
and Garmin in-cab navigation displays. It can also forward the same data to several servers
in parallel. In an IoT project the Galileosky 7x is the multi-protocol gateway: it
aggregates a heterogeneous bus of in-vehicle and on-cargo sensors and uploads them to one or
more cloud platforms, anchoring the cloud and data-exchange pillars.

Considered together, these four devices cover the full edge of a real IoT project: the
IMT.14 handles ordinary vehicles, the Treyki Asset extends visibility to people and unpowered
cargo, the FMB140 extracts fine-grained vehicle diagnostics, and the Galileosky 7x consolidates
everything else and pushes it into the cloud — where big-data and AI services can finally
turn the raw sensor stream into operational decisions.
