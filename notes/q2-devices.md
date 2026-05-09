# Q2 — Telematic / IoT Devices (Research Notes)

## 1. Arvento IMT.11 (vehicle tracking, basic)
**Vendor:** Arvento (Turkey) | **Source:** globtel.az
- Operating temp: -20 C ... +75 C
- Dimensions: 56 x 63 x 19 mm | Weight: 38 g
- Battery: Li-Polymer 900 mAh backup
- Power supply: 12-24 VDC
- GSM module: u-blox SARA-G340 (internal antenna)
- GSM bands: quad-band 850/900/1800/1900 MHz; LTE bands 3/7/20
- GPS: internal antenna
- Use: light vehicle / fleet tracking, theft recovery, basic dispatch
- IoT role: edge sensor — periodically uploads position/speed to a fleet server (telematics pillar)

## 2. Arvento IMT.14 (vehicle tracking, extended)
- Operating temp: -40 C ... +75 C (industrial range)
- Dimensions: 103 x 68.5 x 19 mm | Weight: 105 g
- Battery: Li-Polymer 900 mAh backup
- Power: 12-24 VDC; nominal 40-50 mA, peaks 200-250 mA
- GSM module: u-blox SARA-G340
- 2-band 2G (900/1800), LTE (band 3/7/20), Class 3 (23 dBm) and Class 4 (33 dBm)
- Use: heavy-duty fleet, harsh climates (cold-chain trucks)
- IoT role: more digital inputs than IMT.11 -> integrates ignition, accident, odometer signals; bridges vehicle CAN events to backend (data exchange pillar)

## 3. Arvento IMT.53 (container tracking)
**Source:** Easytrack leaflet (descr. via search) + Course-Hero references
- Specially designed for container & long-haul transit conditions
- Long-life autonomous battery (intended for sea/rail container freight)
- Use: maritime & multimodal cargo monitoring, customs seal status
- IoT role: low-power asset tracker -> uploads geo-fenced alerts to logistics platform (cloud + big-data pillars)

## 4. Arvento Treyki Asset (people / asset tracker)
**Source:** arvento.com (official PDF, 2025)
- Internal battery: Li-polymer 2000 mAh (cordless, install-free)
- IP68 (dustproof / submersible)
- GNSS + Assist-GNSS (A-GPS) for fast fix
- BLE 5.0, 6-axis accelerometer
- Geofences: 1000 circular + polygonal
- FOTA and SMS firmware update
- Real-time location, speed-violation, event alerts; BLE sensors supported
- Use: lone-worker safety, valuable cargo, child / elderly tracking
- IoT role: tiny edge node; pairs with BLE sensors -> mesh sensing into cloud

## 5. Teltonika FMB920 (slim, smart, compact)
**Source:** Teltonika datasheet (PDF)
- Module: Teltonika TM2500 (GSM/GPRS/GNSS/Bluetooth)
- GNSS: GPS, GLONASS, Galileo, BeiDou, SBAS, QZSS, DGPS, A-GPS — 33-channel; sensitivity -165 dBm; pos. accuracy < 2.5 m CEP
- 2G quad-band 850/900/1800/1900 MHz; GPRS class 12 (<= 240 kbps)
- Bluetooth 4.0 + LE; supports temp/humidity sensors, OBD-II dongle, BLE beacons
- Inputs: 1 DIN + 1 DOUT + 1 AIN; backup 170 mAh; 6-30 VDC
- Memory: 128 MB flash; Micro-SIM, Micro-USB
- Dimensions: 79 x 43 x 12 mm | 54 g | IP54 | -40 ... +85 C
- Scenarios: green-driving, over-speeding, jamming detection, GNSS fuel counter, crash, geofence
- Sleep modes: GPS / Online Deep / Deep / Ultra-Deep
- FOTA, Configurator, FMBT mobile app
- Certs: CE/RED, E-Mark, EAC, RoHS, REACH
- Use: light commercial vehicles, insurance UBI, rental, courier, taxi
- IoT role: bidirectional — uploads telemetry, receives DOUT commands (engine immobilizer) -> realises actuation in IoT loop

## 6. Teltonika FMB140 (advanced + CAN)
**Source:** powerfleet.ma datasheet (PDF, French)
- 2-in-1 advanced GPS tracker + integrated CAN data processor
- LV-CAN200 / ALL-CAN300 software options
- Reads CAN-bus: fuel level, total consumption, odometer, vehicle speed, RPM, accelerator pedal, AdBlue, engine life, airbag
- 3 DIN, 1 negative input, 2 DOUT, 2 AIN, 2 CAN, 1-Wire, Micro-SIM + eSIM
- Same TM2500 module (GSM 2G quad + GPS+GLONASS+Galileo+BeiDou)
- Backup: 170 mAh Li-Ion; power 10-30 VDC; consumption 6-35 mA
- Dimensions: 65 x 56.6 x 20.6 mm | 55 g | IP41 | -40 ... +85 C
- Certs: CE/RED, E-Mark, EAC, RoHS, MTBF, REACH
- Use: trucks, heavy vehicles, agriculture, electric, special machines
- IoT role: deep vehicle integration — bridges vehicle CAN to cloud platform, enabling predictive maintenance & fuel analytics (AI + big-data pillars)

## 7. Galileosky 7x (advanced terminal, J1939 CAN)
**Source:** wialon.com integration page
- Cellular: 2G / 3G / 4G LTE
- Dual-SIM, BLE, blackbox memory, voice calls
- GLONASS + GPS, multi-server forwarding, built-in odometer
- Reads 13 400 CAN-bus parameters via SAE J1939 (driver activity, tachograph mode, FMS data)
- Wialon-supported features: accelerometer, ADC, camera, eco-driving, Garmin nav, RFID/iButton, alarm button, tachograph DDD download, TCP comms, remote SMS / GPRS management
- Tag set: ds1923 (1-Wire), DS18B20 temp, refrigerator zones (DataCold/ThermoKing/Mitsubishi), tyre-pressure (TPMS), modbus, RS-485 fuel sensors, Omnicom
- Use: heavy logistics, refrigerated transport, mining, public transport
- IoT role: gateway tier — aggregates many bus protocols (CAN, RS-232/485, 1-Wire, BLE, Modbus) and forwards to multiple cloud servers (data-exchange pillar)

---

## Quick comparison table (for the answer)
| Device | Class | Comms | Key feature | IoT role |
|---|---|---|---|---|
| IMT.11 | Light vehicle tracker | 2G/LTE | Compact, low-cost | Telematics edge node |
| IMT.14 | Extended-range vehicle tracker | 2G/LTE | -40 C industrial | Telematics in harsh climates |
| IMT.53 | Container tracker | 2G + GNSS | Long-life battery, asset focus | Logistics asset edge node |
| Treyki Asset | Personal/asset locator | GNSS + BLE 5.0 | IP68, 1 000 geofences | Low-power edge + BLE mesh |
| FMB920 | Compact GPS | 2G + BT 4.0 | UBI insurance, crash detection | Bidirectional edge (DOUT) |
| FMB140 | Pro GPS + CAN | 2G + BT + 2x CAN | Reads ECU fuel, RPM, AdBlue | Deep vehicle gateway |
| Galileosky 7x | Heavy-duty terminal | 2G/3G/LTE + dual-SIM | 13 400 J1939 CAN points | Multi-protocol gateway |

## Pick for the 2-page answer (4 devices, max coverage)
1. **Arvento IMT.14** — extended industrial telematics
2. **Arvento Treyki Asset** — personal/cargo locator
3. **Teltonika FMB140** — pro GPS + CAN data integration
4. **Galileosky 7x** — multi-protocol IoT gateway
