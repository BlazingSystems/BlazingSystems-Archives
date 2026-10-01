# Public Git History Cleanup Ledger

**Status: ACTION REQUIRED**

The current default branches are curated, but some earlier commits still contain material that should not remain publicly retrievable. Deleting files from the latest branch does not remove those blobs from Git history.

## Priority 1 — BlazingSystems-Archives

Rewrite history to remove historical raw project files that were superseded by sanitized notes or public-safe derivatives, especially:

- `marine/vessel-logbook-history/V8_AUDITED_FIXED.html`
- `marine/vessel-logbook-history/V9_EXCEL_MATCHED.html`
- `marine/vessel-logbook-history/V10_FINAL_AUDITED.html`
- `marine/vessel-logbook-history/V10_3_UI_FIX_DST_MINIMAL.html`
- historical Draft Reading Trainer raw builds;
- historical Pisonet source branches that predate the public-safe editions;
- historical ESP8266 thermostat recovery material;
- historical arcade/runtime payloads and emulator research artifacts that may contain third-party assets or deployment-specific data.

Current sanitized notes should remain.

## Priority 2 — uploadsharepayl

The current branch is only a retirement notice, but earlier commits contain third-party application payloads that are still reachable through Git history.

Rewrite the repository to retain only the archival notice. Do not re-publish those binaries in the portfolio or private GitHub archive unless redistribution rights are independently established.

## Priority 3 — samdenty-esp32-port

The current branch is only an upstream attribution/reference notice, but earlier commits contain a large third-party Wi-PWN source tree plus executables, drivers, images, and an APK.

Rewrite the repository so public history retains only the attribution/reference notice and upstream license where appropriate. Do not present the upstream project as original BlazingSystems work.

## Procedure

1. Make a fresh local mirror or clone of each affected repository.
2. Review the removal paths before rewriting.
3. Use `git filter-repo` or an equivalent audited history-rewrite workflow.
4. Scan all rewritten refs for:
   - employer/client identifiers;
   - credentials, keys, tokens and private network values;
   - personal/private records;
   - proprietary forms or production datasets;
   - third-party APK/ROM/JAR/binary payloads without clear redistribution rights.
5. Confirm the intended sanitized README/resolution notes remain.
6. Force-update public refs only after the rewritten history has been reviewed.
7. Re-check direct historical commit/blob URLs after the rewrite. If sensitive objects remain reachable through GitHub caching or detached refs, use GitHub's sensitive-data removal/support process.

## Publication Rule

- Employer/client/company originals: keep off public GitHub.
- Non-company original work: store privately when a private repository is available and publish a separate sanitized/demo edition.
- Third-party commercial or redistributed payloads: do not use the private archive as a redistribution dump; keep only material you have the right to store and redistribute.
- Public repositories: only curated, sanitized, attributable, working or clearly labeled experimental material.
