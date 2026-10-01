# ESP8266 Arcade — Recovery Resolution

**Status:** RECOVERED PRIVATELY / PUBLIC DERIVATIVE AVAILABLE

A complete ESP8266 arcade firmware artifact was recovered from private project storage.

## Recovered Architecture

The private firmware combined:

- ESP8266 access-point and captive-portal behavior;
- local HTTP serving;
- optional station-mode/NAPT networking;
- onboard flash storage concepts;
- browser-based classic-game runtime integration.

## Publication Decision

The raw recovered firmware is intentionally not distributed through public GitHub. Its embedded portal contains third-party emulator/runtime references and ROM-library workflows that are not appropriate to republish as an original portfolio artifact.

No ROMs, BIOS files, commercial game assets, or third-party emulator payloads are being published from the recovered copy.

## Public Continuation

A separate publication-safe derivative is maintained in:

**BlazingSystems-Experiments → `embedded/esp8266-arcade-public/`**

The public derivative keeps the ESP8266 captive-portal and optional NAPT architecture while using:

- generated per-device AP credentials;
- an original dependency-free browser mini-game;
- no emulator core;
- no ROM/BIOS workflow;
- no private Wi-Fi credential.

## Provenance Rule

The public derivative is described as a recovered-design continuation rather than as a byte-for-byte copy of the private firmware.

The recovered original remains in private storage for provenance only.
