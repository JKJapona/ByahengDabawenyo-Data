# Agent guide

Generated data. Never edit by hand.

- Written by `scripts/publish-ota.js` in the private `ByahengDabawenyo-DataPipeline`
  repository; commits arrive from CI, not from a local edit.
- `manifest.json` is the only entry point an agent needs. Read it, stop.
- Never open `versions/**` or `staging/**` route files whole; they are large
  generated JSON. Use `rg` if a specific value must be checked.
- Versions are immutable. A published version is never rewritten; publish a new
  one instead.
- The byte contract lives in the app's `docs/data-contract.md`: exact bytes,
  UTF-8, LF, SHA-256 and length recorded in the manifest.
