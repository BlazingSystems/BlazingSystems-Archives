# Blaze Pisonet Timer — Historical Notes

**Classification:** Superseded embedded-system branch with public-safe continuation

Earlier Pisonet timer iterations explored:

- persistent timer and sales state;
- relay and coin-input handling;
- GPIO migration and boot-safety fixes;
- local web configuration;
- buzzer/audio notification experiments;
- recovery behavior across reboot and power interruption.

## Historical Result

A private embedded-audio edition was recovered and reviewed. It contains a reusable default AP password and depends on a separate embedded-audio header/media payload, so the raw source is intentionally not distributed through public GitHub.

The historical audit confirmed the timer/state/web logic was coherent enough for continued development, but a complete target-board release was not established from the original branch.

## Public-Safe Continuation

A publication-safe derivative is maintained in:

**BlazingSystems-Labs → `embedded/blaze-pisonet-timer-public/`**

The public derivative removes the private media payload, replaces the reusable AP password with a `CHANGE_ME` placeholder, preserves the recovered timer/relay/display/web logic, and ships with empty audio placeholders rather than redistributed recordings.

## Publication Policy

Raw historical firmware, user-supplied audio payloads, and historical credential values are not distributed in this public archive. This page preserves engineering history and validation lessons only.

## Related Development

The broader multi-unit architecture remains in:

**BlazingSystems-Labs → `embedded/blaze-pisonet-universal/`**

Promotion to the main Projects repository still requires exact-board compile, GPIO safety checks, persistence testing, coin-input noise testing, relay/electrical validation, and hardware endurance testing.
