# StableSignal public hub

Static GitHub Pages site for StableSignal, an independent research and product lab building stablecoin research, analytics, and migration tools, starting on Arc testnet.

StableSignal is an independent project building on Arc testnet. We are not affiliated with, endorsed by, or sponsored by Circle or Arc.

## Architecture

Plain HTML and CSS with no build step, backend, database, analytics, external assets, or paid infrastructure.

## Run locally

Open `index.html` directly, or run this from the repository root:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose `main` and `/ (root)`, then save.
4. Verify `https://stablesignal.github.io/`.

`.nojekyll` ensures the files are served directly. This repository intentionally has no `CNAME`.

## Updating public proof

1. Put the approved, dated Pulse screenshot in `assets/screenshots/`.
2. Populate `deployments/arc-testnet.json` from the verified deployment receipt. Confirm chain ID `5042002`, successful receipt status, the resulting checksummed address, runtime code, block number, UTC time, and ArcScan testnet URL.
3. Copy the same values into the proof, contract-registry, and build-log sections in `index.html` and into `build-log/0001-setup-and-pulse-v0.md`.
4. Populate the release window and metrics in `public-research/notes/0001-arc-testnet-observations.md` from the approved QA capture.
5. Parse the JSON, confirm every local and external link, and search for `Pending`, `Awaiting`, and `null` before publication. Every remaining occurrence must be intentional.
6. Retain the testnet and independence disclaimers beside Arc context and in the footer.

The machine-readable deployment registry is the source of truth for contract evidence. The hub and build log are human-readable copies and must match it exactly.

Never publish keys, seed phrases, `.env` files, private implementation details, internal notes, or personal information.
