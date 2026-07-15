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

1. Put verified screenshots in `assets/screenshots/`.
2. Update the proof, deployed-contracts, and build-log sections in `index.html`.
3. Add the verified address, transaction hash, and ArcScan URL to `deployments/arc-testnet.json`.
4. Replace matching placeholders in `build-log/0001-setup-and-pulse-v0.md`.
5. Confirm every link and retain the independence disclaimer beside Arc context and in the footer.

Never publish keys, seed phrases, `.env` files, private implementation details, internal notes, or personal information.
