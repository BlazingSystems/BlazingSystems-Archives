# Public Git History Cleanup Ledger

**Status: PARTIALLY COMPLETE — UNREACHABLE OBJECT PURGE STILL REQUIRED**

This ledger tracks public-history cleanup separately from current-branch sanitization.

## Verified current branches

### BlazingSystems-Archives

The current `main` branch is already a clean, short history containing only the repository structure, sanitized archive publication, and later resolution notes.

However, several older commit SHAs from the pre-rewrite history are still directly retrievable on GitHub. These include historical raw marine builds that were removed from the active branch.

**Required remaining action:** request GitHub-side removal/garbage collection of the unreachable historical objects after confirming no protected refs, tags, forks, or pull-request refs still point to them.

### uploadsharepayl

The public `main` branch was rebuilt from its clean initial README and now contains only two commits: the initial repository notice and the current retirement notice.

The former payload-adding commits are no longer ancestors of `main`, but their old SHAs are still temporarily retrievable.

**Required remaining action:** purge unreachable historical objects through GitHub's sensitive-data/removal support process or repository garbage collection once all refs are confirmed clean.

### samdenty-esp32-port

The current branch is intentionally limited to an upstream attribution/reference notice and retained license material. Earlier commits still contain a much larger third-party Wi-PWN tree and bundled binaries/assets.

Because the first commit already contains that upstream payload, there is no verified clean ancestor suitable for an in-place connector-only rewrite.

**Required remaining action:** rebuild the repository from a fresh root outside the current connector workflow, or replace/delete the repository, then verify old object URLs no longer resolve.

## Known historical material requiring removal

Previously retrievable Archives history included raw builds such as:

- `marine/vessel-logbook-history/V8_AUDITED_FIXED.html`
- `marine/vessel-logbook-history/V9_EXCEL_MATCHED.html`
- `marine/vessel-logbook-history/V10_FINAL_AUDITED.html`
- `marine/vessel-logbook-history/V10_3_UI_FIX_DST_MINIMAL.html`

Other historical branches or objects should also be scanned for:

- employer/client identifiers;
- credentials, keys, tokens and private network values;
- personal/private records;
- proprietary forms or production datasets;
- third-party APK/ROM/JAR/binary payloads without clear redistribution rights.

## Final cleanup procedure

1. Confirm every active branch/tag/ref points only to curated public content.
2. Create a fresh mirror/clone before destructive history work.
3. Use `git filter-repo`, a fresh-root rebuild, or an equivalent audited rewrite where still needed.
4. Re-scan all refs before force-updating.
5. Verify current README/resolution notes survive unchanged.
6. Test previously known historical commit/blob URLs.
7. If old objects remain reachable after refs are clean, use GitHub's sensitive-data removal/support process.

## Publication rule

- Employer/client/company originals stay off public GitHub.
- Non-company original work may be stored in a private repository when one is available; public GitHub receives a separate sanitized/demo edition.
- Third-party commercial or redistributed payloads are not used as archive material unless redistribution rights are clear.
- Public repositories contain only curated, sanitized, attributable, working or clearly labeled experimental material.
