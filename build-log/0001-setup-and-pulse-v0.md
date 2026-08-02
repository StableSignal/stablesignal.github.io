# Build log 0001: Setup and Pulse v0

**Status:** Release evidence verified

**Network:** Arc Testnet (`5042002`)

**Date opened:** 2026-07-15

**Last updated:** 2026-08-02

## Objective

Establish the StableSignal public hub and the evidence standard for Pulse v0. Release claims should be traceable to a dated interface capture, a documented collection method, or an independently checkable Arc testnet record.

## Prepared for release

* Public hub sections for product scope, research, contract evidence, and build history.
* Machine-readable Arc testnet deployment registry with explicit verification fields.
* Pulse v0 methodology covering collection, metric definitions, reproducibility, and limitations.
* Observation 0001 structure for the dated release baseline.

Pulse v0 has passed browser QA, its approved capture is preserved with a reproducible observation, and PulseBeacon's Arc testnet deployment evidence is verified.

## Evidence gate

| Evidence | Required record | Current state |
| --- | --- | --- |
| Pulse release candidate | Dated screenshot showing network context and visible data | [Captured `2026-07-31`](../assets/screenshots/pulse-v0-2026-07-31.png) |
| PulseBeacon address | Checksummed Arc testnet contract address | [`0x13FB…770D3`](https://testnet.arcscan.app/address/0x13FBc37C40d071d9654913013C93a63F9Dc770D3) |
| Deployment transaction | Successful transaction hash and receipt | [`0x34294c…8ebf0`](https://testnet.arcscan.app/tx/0x34294c78a7062f1088724d2017149d2531c6a522c666304c09e950694338ebf0); status `1` |
| Deployment block and time | Block number and UTC timestamp from the receipt | `54,976,300`; `2026-08-02T18:37:09Z` |
| Runtime code | Non-empty code at the recorded address | Verified; `1,014` bytes |
| Explorer reference | ArcScan testnet URL resolving to the same transaction | Indexed and matched |
| Observation 0001 | Capture fields and metrics populated from the approved QA run | Reconciled and linked |

No contract is represented as deployed until the chain ID, successful receipt, resulting address, and runtime code have been checked. All copies of the address and transaction must match the machine-readable registry.

## Finalization sequence

1. Browser QA and the dated Pulse screenshot are complete.
2. The PulseBeacon receipt, chain ID, publisher, and runtime code are verified.
3. `deployments/arc-testnet.json` is populated from the verified receipt.
4. The deployment evidence is copied into this log, the public hub, and Observation 0001.
5. The screenshot, JSON, Markdown, and explorer references are checked as one release package.

## Scope boundaries

Pulse v0 is a testnet research interface, not a production monitor, wallet, custody service, transaction signer, risk rating, or statement about mainnet conditions. StableScore and later products are outside this build log.

## Related records

* [Pulse v0 scope](../products/pulse.md)
* [Arc testnet deployment registry](../deployments/arc-testnet.json)
* [Pulse v0 methodology](https://github.com/StableSignal/public-research/blob/main/methodology/pulse-v0-methodology.md)
* [Observation 0001](https://github.com/StableSignal/public-research/blob/main/notes/0001-arc-testnet-observations.md)

## Independence notice

StableSignal is an independent project building on Arc testnet. We are not affiliated with, endorsed by, or sponsored by Circle or Arc.
