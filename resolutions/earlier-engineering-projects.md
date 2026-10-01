# Earlier Engineering Projects — Sanitized Resolution Notes

This document records older BlazingSystems project directions that predate the current portfolio. Original source is not published here unless it has been independently reviewed and sanitized.

## Arduino Shake-Sensor Control Exercise

**Period:** 2023  
**Status:** Early microcontroller exercise

A basic Arduino input/output exercise used a vibration/shake sensor to control digital outputs.

**Restart path:** treat this as a small fundamentals example only. If rebuilt, add proper debounce/filtering, fail-safe output state, and a clear wiring diagram.

---

## Ethernet Firmware-Recovery / Auto-Flashing Study

**Period:** Early 2024  
**Status:** Recovery workflow study

Explored direct-Ethernet firmware recovery using TFTP-style workflows and file transfer into embedded devices.

**Public-safety rule:** do not publish device passwords, serials, MAC-specific recovery images, ISP firmware, or configuration files copied from deployed equipment.

**Restart path:** document only vendor-supported recovery procedures and use clean lab hardware/firmware images.

---

## ESP8266 as AVR ISP Programmer

**Period:** 2024  
**Status:** Concept / incomplete implementation

Explored using an ESP8266 as a network-accessible programmer for AVR microcontrollers.

**Restart path:**
1. define supported AVR targets and voltage levels;
2. isolate programming transport from the web interface;
3. validate reset/SPI timing;
4. support verified firmware images only;
5. add checksum and failed-flash recovery behavior.

---

## ESP8266 Modular Diagnostics / Utility Tool

**Period:** 2024  
**Status:** Concept family

Historical experiments combined a small display/web UI with storage, GPIO, IR, Wi-Fi scanning, UART and optional external peripherals.

The public archive intentionally excludes packet-disruption/deauthentication functions and third-party firmware/assets.

**Restart path:** build a diagnostics-only tool around passive Wi-Fi scanning, GPIO, UART, IR, storage and optional NFC peripherals. Keep radio features compliant with local law and limited to owned/authorized equipment.

---

## Vehicle Control Web Interface

**Period:** Late 2024  
**Status:** Discontinued prototype

Explored a Wi-Fi-accessible microcontroller interface for a vehicle-related relay/control concept.

**Why it remains archived:** vehicle ignition/control creates safety, fail-safe, authorization and liability requirements beyond a casual embedded prototype.

**Restart path:** if revisited, use it only as a bench-top low-voltage control demonstrator. Do not connect a public prototype directly to vehicle ignition or safety-critical circuits. Use fresh credentials generated at setup rather than hard-coded defaults.

---

## Android / Mobile PisoWiFi Controller Study

**Period:** 2025  
**Status:** Architecture study

Explored using an Android device with OTG USB Ethernet, VLAN tagging, DHCP/DNS services and a local captive portal as a compact network controller.

**Restart path:** reproduce the design on isolated lab networking first. Prefer supported Linux/OpenWrt components for long-running routing/firewall duties, and use fresh deployment-specific credentials.

---

## Cellphone Rental Controller

**Period:** 2025  
**Status:** Unfinished system concept

Architecture combined:

- Orange Pi Zero 3 controller/server;
- coin-slot input;
- display/buttons for device selection;
- timed phone-rental sessions;
- Android-side application restrictions during the paid session.

**Restart path:**
1. define the threat model and user/administrator separation;
2. use supported Android Device Owner/kiosk APIs;
3. keep payment logic and device-control logic separately testable;
4. design safe session expiry and power-loss recovery;
5. test only on owned/authorized devices.

---

## ThinkPad T480 BIOS Recovery Study

**Period:** 2025  
**Status:** Hardware-recovery study

Explored recovery of a non-booting laptop using official firmware extraction and external SPI programming.

**Public-safety rule:** never publish full dumps copied from personal machines or random donor systems because they may contain serial numbers, UUIDs, management-engine data, device identity information, or other machine-specific content.

**Restart path:** use official vendor firmware and preserve machine-specific regions only through a private, verified recovery workflow.

---

## Delivery Label Generator

**Period:** Early 2026  
**Status:** Concept / no verified final artifact

Planned a desktop/PWA-style tool that imports spreadsheet delivery manifests, generates printable labels, and exports PNG/JPG label images.

**Restart path:**
1. define a neutral CSV/XLSX import schema;
2. validate field mapping and duplicate handling;
3. provide a template designer;
4. generate labels locally without cloud upload;
5. include synthetic sample manifests only.

---

## Mobile Service / Diagnostic Workstation Study

**Period:** 2024  
**Status:** Research only

Explored repurposing an older tablet as a portable service workstation for firmware recovery, serial/programming tools and storage diagnostics.

**Publication boundary:** do not include recovered customer data, bypass tooling, credentials, or unauthorized wireless-disruption functions in a public portfolio.

---

## General Restart Rule

For any older project in this document:

1. recover original source privately if available;
2. remove credentials, personal/device identity data and third-party assets;
3. separate legitimate diagnostics/control from risky or unauthorized functionality;
4. create a clean public implementation using synthetic test data;
5. document validation honestly before promoting it out of Archives.


---

## NodeMCU Custom Firmware / Flashing Tool

**Period:** 2023–2024  
**Status:** Historical tooling study

Explored custom NodeMCU firmware builds with file, GPIO, UART and network modules plus a desktop flashing workflow.

**Restart path:** use vendor/open-source build systems with license notices, publish only clean firmware configurations, and keep device credentials or customer firmware images out of source control.

---

## Blynk-Connected Wi-Fi Device Study

**Period:** 2024  
**Status:** Cloud-control experiment

Explored Arduino/PlatformIO device control through Blynk-style mobile/cloud connectivity.

**Publication boundary:** never commit Wi-Fi credentials, device tokens, cloud secrets or real endpoint identifiers.

**Restart path:** move credentials to first-run configuration or environment-specific secrets, provide an offline/local-control fallback, and document cloud-service dependencies.

---

## Wireless Diagnostics / Interference Experiment

**Period:** 2024  
**Status:** Discontinued risky experiment

Historical work included Wi-Fi disruption/jamming ideas. That functionality is intentionally **not** published in this portfolio.

**Safe replacement path:** limit any future version to passive scanning, channel occupancy visualization, signal-strength logging, packet statistics on owned networks, and authorized diagnostic tasks.

---

## LiteBeam 5AC Recovery Study

**Period:** 2025  
**Status:** Firmware-recovery study

Explored vendor recovery/TFTP procedures for a wireless bridge device.

**Publication boundary:** do not redistribute vendor firmware images unless licensing clearly permits it, and do not publish device-specific credentials/config backups.

**Restart path:** document the vendor-supported recovery sequence, recovery IP layout, checksum verification and rollback procedure using clean lab hardware.

---

## ESPHole

**Period:** 2026  
**Status:** SANITIZED PUBLIC LAB AVAILABLE

ESP8266 network experiment combining DNS filtering/sinkhole behavior, captive setup, local block/allow lists, DNS forwarding/cache and repeater/NAT concepts.

The recovered raw source remains private because it used reusable default credentials. A sanitized public edition is now maintained in:

**BlazingSystems-Labs → `networking/esphole/`**

The public Lab generates/persists first-boot credentials and contains no private deployment configuration. Exact-board compile, DNS/NAPT behavior, recovery, and multi-client hardware validation remain.

---

## BlazeTube

**Period:** 2026  
**Status:** SANITIZED PUBLIC LAB AVAILABLE

ESP8266 browser-session/repeater experiment exploring synchronized destination control, local session persistence, NAPT behavior and optional YouTube API/player integration.

The recovered raw source remains private because its original defaults included fixed setup/admin credentials and deployment assumptions. A sanitized public edition is now maintained in:

**BlazingSystems-Labs → `networking/blazetube-esp8266/`**

The public Lab removes bundled credentials, uses user-supplied service keys where applicable, keeps account cookies/login state out of firmware, and documents that the ESP8266 is not a full remote-browser or remote-desktop engine. Compile, service-integration and multi-client hardware validation remain.

