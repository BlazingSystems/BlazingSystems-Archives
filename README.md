# BlazingSystems — Engineering Archive

A sanitized record of superseded designs, discontinued branches, and lessons learned during earlier BlazingSystems development work.

This repository is **not** a raw backup. Public archive material is limited to engineering notes, milestone descriptions, validation findings, and resolution plans that are safe to publish.

Public-history cleanup and remaining unreachable-object removal are tracked in [HISTORY_REWRITE_REQUIRED.md](HISTORY_REWRITE_REQUIRED.md).

## Archive Purpose

The archive supports three goals:

1. preserve useful technical lessons from earlier iterations;
2. document why a design was superseded or paused;
3. provide a clear restart path if the project is revisited.

Raw employer/customer files, proprietary forms, production credentials, private router backups, private keys, personal records, and unreviewed historical source are intentionally excluded.

## Historical Areas

### Marine / Reporting Tools

Earlier reporting and training iterations contributed to the current public portfolio demonstrations. Historical notes describe feature progression and design decisions only; operational records and company-specific templates are not published.

### Embedded / Pisonet

Earlier timer branches explored persistent timing, GPIO migration, local web control and audio/buzzer behavior. The maintained public branch is developed separately in **BlazingSystems-Labs**.

### Browser Runtime Research

Earlier BlazeAPK and BlazeJ2ME milestones document the progression of browser-based compatibility research. Current experimental branches are maintained in **BlazingSystems-Experiments**.

### Browser Games / Launcher Studies

Earlier arcade iterations explored local launchers, game-library interfaces and emulator-oriented workflows. Public portfolio editions exclude commercial ROMs, BIOS files, copied game assets and third-party payloads.

## Earlier Engineering Projects

A consolidated sanitized record of earlier projects from 2023 onward is maintained in:

- [Earlier Engineering Projects](resolutions/earlier-engineering-projects.md)

It documents restart paths without publishing old credentials, private firmware dumps, disruptive wireless features, or third-party assets.

## Resolution Records

The `resolutions/` directory contains design summaries and restart plans for projects where a publishable final implementation is not available.

Topics include:

- OpenWrtFi architecture;
- Huawei HG8145v5 firmware/OpenWrt research;
- ESP8266 TOTP / 2FA;
- Dell Wyse 5070 homelab;
- five-sided ESP32 LED cube;
- ESP32 I2S noise-threshold controller;
- ESP8266 relay music sequencer;
- multi-node weather/flood monitoring;
- MaSiCA machine-fault analysis;
- remote LAN gateway concepts;
- older Pisonet/controller branches;
- motorcycle ESP32/LVGL HUD;
- BlazeTube ESP8266 repeater/browser-terminal concept;
- ESP8266 Arcade recovery and public-safe captive-portal derivative.

## Archive Standard

A public archive entry should contain:

- project objective;
- historical design direction;
- known failure or limitation;
- lessons learned;
- safe restart/completion path;
- no confidential or proprietary operational material.

If an older source artifact is rediscovered, it should first be reviewed privately. Only a sanitized, publication-safe derivative should be added to public GitHub.

## Related Repositories

- [Projects](https://github.com/BlazingSystems/BlazingSystems-Projects)
- [Labs](https://github.com/BlazingSystems/BlazingSystems-Labs)
- [Experiments](https://github.com/BlazingSystems/BlazingSystems-Experiments)
- [Portfolio Catalog](https://github.com/BlazingSystems/BlazingSystems/blob/main/PROJECTS.md)
