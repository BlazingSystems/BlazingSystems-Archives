# Public History Cleanup Required

**Status:** ACTION REQUIRED

The current default branches have been sanitized, but earlier public commits contain withdrawn raw artifacts that can remain reachable through Git history after normal deletion.

## BlazingSystems-Archives priority paths

The following historical paths must be purged from public history rather than merely deleted from the current tree:

- `marine/vessel-logbook-history/V8_AUDITED_FIXED.html`
- `marine/vessel-logbook-history/V9_EXCEL_MATCHED.html`
- `marine/vessel-logbook-history/V10_FINAL_AUDITED.html`
- `marine/vessel-logbook-history/V10_3_UI_FIX_DST_MINIMAL.html`
- `marine/draftsight-trainer-history/`
- `embedded/blaze-pisonet-timer-history/*.ino`
- `embedded/blaze-pisonet-universal-recovered/`
- `embedded/esp8266-thermostat-recovered/`
- `games/friv-arcade-history/*.html`
- `web-runtime-history/blazeapk/*.html`
- `web-runtime-history/blazej2me/*.html`

The marine V8/V9/V10 ancestor blobs were specifically verified to contain organization/form/order-style identifiers that are not appropriate for the public portfolio.

Other removed raw artifacts are included conservatively because they were intentionally withdrawn from the public archive and normal deletion does not remove their historical blobs.

## Additional legacy repositories

Two older public repositories were also reduced to safe current-branch notices on 2026-10-01:

### `BlazingSystems/uploadsharepayl`

The former default branch exposed personal contact/social information and redistributed binary/application payloads. The current `main` branch now contains only a neutral archival notice.

Current cleanup commit: `fae34436c8ddf9221bd5821ae29a136b74a27f4a`

Historical objects from earlier commits still require a history rewrite or repository removal before they should be considered purged.

### `BlazingSystems/samdenty-esp32-port`

The former default branch was a third-party Wi-PWN-derived tree containing source, executables, drivers, application packages and generated assets. The current `main` branch now contains only an attribution notice plus the upstream license.

Current cleanup commit: `12896dc3d9d3fa146a1720da2f47358ced4607ef`

Historical objects from earlier commits still require a history rewrite or repository removal before they should be considered purged.

## Additional curated-repository history findings

### `BlazingSystems/BlazingSystems`

The current profile repository is clean, but earlier commits still contain withdrawn portfolio-migration material:

- `PROJECT_MIGRATION_AUDIT.md` — internal migration/recovery notes, including AI/tooling references that are intentionally absent from the public portfolio;
- `Friv_Offline_Arcade_SNES_PLAYABLE.html` — misplaced historical arcade payload removed from the current branch;
- `SuperNintendo.min.js` — misplaced third-party/minified arcade dependency removed from the current branch.

These paths should be removed from public history if the goal is to make the old material no longer retrievable through commit references.

### `BlazingSystems/BlazingSystems-Experiments`

The current firmware sources use public-safe placeholder credentials, but two earlier commits contained a reusable fixed AP password:

- `embedded/esp8266-ap-led-controller/esp8266_ap_led_controller_fixed_v2.ino`
  - introduced with a fixed AP password in commit `b66718362634`;
  - replaced with a placeholder in commit `11bfd8ac9bd4`.
- `embedded/esp8266-relay-controller/esp8266_relay_controller.ino`
  - introduced with a fixed AP password in commit `a522a9456daa`;
  - replaced with a placeholder in commit `fbcc03718bc8`.

Do not copy the historical credential values into documentation. History cleanup should either remove the affected historical blobs and re-add the current sanitized files, or use a reviewed replacement-text rewrite that removes the old secret values from all refs.

The completed history review of `BlazingSystems-Projects` and `BlazingSystems-Labs` did not identify comparable company/client data or fixed production credentials in their existing commit sets.


## Other curated-repository history targets

### `BlazingSystems/BlazingSystems`

Historical profile commits contain files that were later removed from the public default branch:

- `Friv_Offline_Arcade_SNES_PLAYABLE.html`
- `SuperNintendo.min.js`
- `PROJECT_MIGRATION_AUDIT.md`

The arcade files were misplaced payloads rather than profile content. The internal migration audit is also not intended as public portfolio material and contains internal process language that should not remain in public history.

### `BlazingSystems/BlazingSystems-Experiments`

Earlier revisions of the following firmware files contained a reusable demo Wi-Fi password that has since been replaced by placeholders on the current branch:

- `embedded/esp8266-relay-controller/esp8266_relay_controller.ino`
- `embedded/esp8266-ap-led-controller/esp8266_ap_led_controller_fixed_v2.ino`

The current files are sanitized, but the superseded credential-bearing blobs should be removed from public history during the rewrite.

## Required cleanup method

Perform history rewrites from fresh local mirrors/clones using `git filter-repo` or an equivalent audited process. Review the rewritten repositories before any force update.

After rewriting:

1. verify the current sanitized notes and resolution documents are preserved;
2. scan all refs for confidential identifiers, credentials, private keys, personal data and redistributed third-party binaries/assets;
3. force-update only after confirming the rewritten history is correct;
4. expire local reflogs / garbage-collect local copies as appropriate;
5. if sensitive objects remain retrievable from GitHub after the rewrite, follow GitHub's sensitive-data removal/support process.

Do not treat current-branch deletion or replacement commits as proof that historical content has been purged.

## Preservation rule

Private originals that are safe and owned by the project may be retained in a private archive. Employer/client material, credentials, private router backups, private keys, proprietary forms, and unlicensed third-party binaries should remain outside GitHub unless there is clear authorization to store them.

Public repositories should contain sanitized engineering notes, synthetic demonstrations, attribution-safe references and publication-safe source only.
