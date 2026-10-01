# BlazeTube ESP8266 — Resolution Record

## Project Status

**ARCHIVED / REBUILD CANDIDATE**

A recoverable ESP8266 firmware artifact exists for a local Wi-Fi repeater and shared browser-terminal concept. The raw recovered source is intentionally **not** published in this public archive because it contains fixed setup/administrative credential defaults and deployment-specific network assumptions.

## Historical Objective

The project explored whether one ESP8266 could combine:

- AP + STA operation;
- NAPT/NAT internet sharing;
- a local administration page;
- a small set of configurable browser destinations;
- persistent local configuration.

## Publication Decision

The original recovered firmware is retained outside public GitHub. This repository records only the engineering direction and restart requirements.

A future public portfolio edition should:

1. generate unique first-boot credentials per device or require explicit provisioning;
2. avoid hard-coded administrative passwords;
3. keep upstream Wi-Fi credentials out of source control;
4. clearly separate routing/repeater behavior from browser/session behavior;
5. document ESP8266 RAM, TLS, captive-portal and modern-web limitations;
6. use neutral example URLs and synthetic configuration;
7. be compiled and tested on the stated ESP8266 core/board before promotion to Labs.

## Technical Boundary

An ESP8266 can host a local control interface and, with a compatible network stack, provide limited AP/STA routing. It is not a general-purpose remote desktop or full browser engine, and a public rebuild should not imply that login cookies or arbitrary modern browser sessions can be transparently hosted by the microcontroller.

## Provenance

This record documents a newly recovered historical artifact without claiming that a sanitized replacement is the original source. If development resumes, the public implementation should be treated as a new continuation/rebuild.
