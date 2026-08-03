# StableSignal public hub

Static GitHub Pages site for StableSignal, an independent research and product lab building stablecoin research, analytics, and migration tools, starting on Arc testnet.

StableSignal is an independent project building on Arc testnet. We are not affiliated with, endorsed by, or sponsored by Circle or Arc.

## Architecture

The public hub uses plain HTML and CSS with no application backend, database, analytics, external assets, or paid infrastructure. The compiled Pulse frontend is served from `pulse/` as static files alongside the hub. A scheduled GitHub Pages workflow captures a 20-block Arc testnet snapshot server-side and replaces `pulse/latest.json` in the deployed artifact every 15 minutes; a failed capture leaves the prior successful deployment online.

Primary routes:

* `/` — StableSignal hub;
* `/pulse/` — interactive Pulse public beta;
* `/products/pulse.html` — formatted Pulse scope and limitations; and
* `/build-log/0002-pulse-public-beta.html` — public-beta release record.

External links in HTML must use `target="_blank"` with `rel="noopener noreferrer"`. Internal navigation stays in the current tab.

## Run locally

Open `index.html` directly, or run this from the repository root:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, select **GitHub Actions**.
3. Run the **Deploy StableSignal Pages** workflow or push to `main`.
4. Verify `https://stablesignal.github.io/` and confirm `pulse/latest.json` has a recent UTC head-block timestamp.

`.nojekyll` ensures the files are served directly. This repository intentionally has no `CNAME`.

## Updating public proof

1. Put the approved, dated Pulse screenshot in `assets/screenshots/`.
2. Populate `deployments/arc-testnet.json` from the verified deployment receipt. Confirm chain ID `5042002`, successful receipt status, the resulting checksummed address, runtime code, block number, UTC time, and ArcScan testnet URL.
3. Copy the same values into the proof, contract-registry, and build-log sections in `index.html` and the applicable build-log record.
4. Populate the release window and metrics in `public-research/notes/0001-arc-testnet-observations.md` from the approved QA capture.
5. Parse the JSON, confirm every local and external link, confirm external HTML links have safe new-tab attributes, and search for `Pending`, `Awaiting`, and `null` before publication. Every remaining occurrence must be intentional.
6. Retain the testnet and independence disclaimers beside Arc context and in the footer.

The machine-readable deployment registry is the source of truth for contract evidence. The hub and build log are human-readable copies and must match it exactly.

Never publish keys, seed phrases, `.env` files, private implementation details, internal notes, or personal information.
