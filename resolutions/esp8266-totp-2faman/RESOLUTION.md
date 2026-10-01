# 2FAMan ESP8266 TOTP — Recovery Resolution

**Status:** HISTORICAL IMPLEMENTATION EVIDENCE / SOURCE NOT CURRENTLY RECOVERED

Conversation history confirms that working-source iterations existed under filenames including `sketch_nov18a.ino` and `sketch_dec7a.ino`. The actual source files are not currently present in the public repositories or verified Library recovery set, so no replacement code is being fabricated.

## Historical Scope

The project combined:

- ESP8266 local access point and web administration;
- DS1302 RTC;
- small OLED display;
- persistent account/configuration storage using EEPROM and JSON/SPIFFS-era code;
- account cycling and one-time-password display;
- Base32-decoding work;
- deep-sleep / low-power experiments in some iterations.

## Known Validation Problems

Historical development also recorded:

- conflicting DS1302 library APIs;
- OLED constructor/address mismatches;
- duplicate pasted sketches causing compile conflicts;
- SPIFFS/config-file errors;
- inconsistent JSON/config structures;
- TOTP generation that was not verified against RFC 6238 test vectors.

Because the authenticator algorithm was not independently verified, the historical implementation must not be represented as a trustworthy production authenticator.

## Resolution

If the original source is recovered, preserve it privately first and audit it for stored secrets before any publication. A public continuation should use one pinned RTC library, a versioned configuration schema, modern filesystem APIs where appropriate, and automated RFC 6238 test-vector validation before storing real accounts.

No real 2FA secrets, seed values, account identifiers, or private configuration files are archived here.
