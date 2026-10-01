# OpenWrtFi — recovery resolution

**Status:** UNFINISHED / NO VERIFIED DEPLOYABLE ARTIFACT RECOVERED

OpenWrtFi was intended as an OpenWrt-native PisoWiFi/JuanFi-style platform with:

- captive portal and local/offline operation
- coin/time sessions, pause/resume and vouchers
- ESP8266/ESP32 coin-vendo integration
- multi-vendo support
- local database/SQLite
- REST API and admin UI
- firewall/traffic authorization
- backup/restore
- target variants for Ruijie EW1200G Pro, Orange Pi Zero 3 and x86/OpenWrt PC

The project requirements were substantial and a deployable package/firmware was requested, but no recovered artifact demonstrates that all of those components were implemented, built and validated.

## Resolution

Do not label OpenWrtFi complete. A future restart should begin from a versioned source repository and deliver one target at a time with:

1. database schema and session state machine;
2. nftables/firewall authorization model;
3. captive portal and admin API;
4. simulated coin-vendo integration;
5. reproducible OpenWrt package build;
6. target-specific hardware build validation;
7. backup/restore and failure-recovery tests.

Hardware-specific binaries must never be invented or labeled verified without an actual target build.
