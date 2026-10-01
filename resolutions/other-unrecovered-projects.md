# Other older projects with no verified artifact recovered

These projects exist in historical planning, code discussions, or partial implementations, but no trustworthy final source/build is currently available for public continuation.

They are intentionally **not reconstructed from memory and mislabeled as originals**. Where possible, the completion path is documented so a future recovered source can be audited and resumed correctly.

## ESP32 / WS2812 Five-Sided LED Cube

**Status:** UNRECOVERED SOURCE / DESIGN PRESERVED

Historical design included:
- five LED-matrix faces
- ESP32 controller
- AP-based local setup portal
- optional STA mode only when an app needs Internet access
- OTA/firmware upgrade workflow
- per-face or whole-cube app selection
- power-saving behavior that disables Wi-Fi when unnecessary
- battery-status indication

**Resolution path:**
1. Recover the original ESP32 sketch or any later exported package.
2. Confirm actual matrix dimensions and physical wiring order.
3. Separate the core matrix-mapping layer from app/effect modules.
4. Validate AP/STA power-state transitions and OTA rollback behavior.
5. Hardware-test current draw, thermal behavior, and battery cutoff before production use.

## ESP32 I2S Noise-Threshold Penalty Controller

**Status:** PARTIAL HISTORICAL IMPLEMENTATION / FINAL ARTIFACT NOT RECOVERED

Historical work included both a single-node baseline and a later multi-node ESP-NOW direction with:
- I2S microphone input
- loudness/RMS thresholding
- relay penalty output
- addressable status LEDs
- local AP/STA configuration portal
- scheduled active windows / NTP
- multi-node loudest-node reporting

**Known unfinished items from the historical work:**
- stable ESP-NOW MAC pairing/discovery
- long-duration packet-loss testing
- threshold calibration across microphones
- false-trigger/noise filtering
- relay fail-safe and reboot behavior

**Resolution path:**
Recover the original node/master sketches first. Resume from those real files rather than synthesizing a replacement from memory.

## ESP8266 Relay Music Sequencer

**Status:** HISTORICAL CODE/DESIGN / FINAL ARTIFACT NOT RECOVERED

Historical design:
- three relays
- 120 BPM baseline
- low/mid/high audio-band-driven patterns
- fallback/random sequence behavior

**Resolution path:**
1. Recover the original sketch if possible.
2. Replace simplistic frequency heuristics with a validated FFT or filter-bank implementation if true band detection is still required.
3. Add non-blocking timing so relay sequencing and audio analysis can run together.
4. Protect mechanical relays from excessive switching; solid-state outputs may be more suitable for rapid light effects.

## Multi-Node Weather / Flood Thesis System

**Status:** DESIGN / PRE-THESIS WORK PRESERVED; FINAL FIRMWARE NOT RECOVERED

Historical architecture included:
- 2–3 initial sensor nodes plus one master
- fixed weather sensors
- master-only SD-card archive
- node-side temporary buffering
- acknowledgement before local deletion
- dynamic discovery / congestion checks
- multi-hop forwarding
- deduplication / TTL
- read-only local Wi-Fi portal
- deterministic warnings
- no SBC requirement
- later LoRa preference for longer-range deployment

**Resolution path:**
1. Recover any master/node sketches, BOMs, or test documentation.
2. Freeze a first-deployment hardware BOM.
3. Define one packet schema and sequence-number/ACK protocol.
4. Build a two-node + one-master bench test before adding routing complexity.
5. Validate SD corruption recovery and offline data reconciliation.
6. Only then add multi-hop, solar, cellular, or OTA features.

## MaSiCA Machine-Fault Analyzer Thesis

**Status:** CONCEPT / ARCHITECTURE PRESERVED; NO VERIFIED FINAL SOURCE

Historical concept used MCU sensor nodes plus an SBC/master to combine:
- sound
- vibration
- current
- temperature
- dataset synchronization
- camera placement guidance

**Resolution path:**
Treat it as a data-collection and fault-classification research project first. Recover any original node code/dataset schema before implementing ML. Establish a repeatable labeled dataset and baseline signal-processing method before adding camera/AI features.

## Older Arduino Mega Centralized Pisonet Controller

**Status:** HISTORICAL IMPLEMENTATION EVIDENCE / SOURCE FILE NOT CURRENTLY RECOVERED

Historical work confirms that an Arduino Mega 2560 implementation existed using a color TFT interface, DS3231 RTC, relay/LED/button control for multiple computer stations, timeout handling, clock-setting controls, and buzzer feedback.

The actual source file has not been recovered into the current Library/GitHub set, so the public archive does not recreate or relabel a newly written sketch as the original.

The later ESP8266 **Blaze Pisonet Universal** work remains the active successor. If the Mega source is recovered, preserve it privately, audit credentials/contact information, then publish only a sanitized historical copy or technical summary.

## Motorcycle ESP32 / LVGL HUD

**Status:** CONCEPT / NO VERIFIED ARTIFACT

Recover original display/UI source before resuming. If restarted, validate display readability, power conditioning, vibration resistance, weather sealing, and safe non-distracting interaction before road use.

## ESP8266 Remote LAN Access / Tunnel Gateway

**Status:** ARCHITECTURE DISCUSSION / NO COMPLETED ARTIFACT

Historical concept:
- ESP8266 joins an Internet-connected Wi-Fi network
- device provides remote access to selected local router/admin web interfaces
- outbound persistent connection to a public relay/VPS
- authenticated restricted HTTP/HTTPS gateway
- LAN target whitelist

**Resolution path:**
Do not expose arbitrary LAN forwarding. If revived, use a narrowly scoped authenticated outbound tunnel, explicit target allowlist, encrypted transport, rate limits, and a revocation mechanism. An ESP32/Linux gateway may be more practical than ESP8266 for robust TLS/proxy workloads.

## Older Coin-Operated Water-Vending Controller

**Status:** HISTORICAL SOURCE DISCUSSION / FINAL ARTIFACT NOT RECOVERED

Historical requirements included:
- coin pulse input
- pump/relay control
- LED/status output
- configurable GPIO and vend duration
- web-based configuration
- remaining-time display

**Resolution path:**
Recover the original sketch first. If not recoverable, treat any future implementation as a new project rather than claiming continuity with the missing source. Hardware validation must include relay/pump current, coin bounce filtering, brownout recovery, watchdog behavior, and safe default output states.

---

## Recovery policy

If an original source file, ZIP, firmware image, or documented build from any project above is later recovered:

1. preserve the recovered original privately and record its hash/provenance;
2. audit it privately for credentials, personal data, employer/client material, copyrighted payloads and device-specific secrets;
3. compare it against the historical requirements;
4. publish only a sanitized, redistribution-safe derivative or documentation note;
5. migrate a cleaned active copy into Labs only if development resumes;
6. promote to Projects only after real validation.

A newly written approximation must never replace or be presented as the missing historical artifact.
