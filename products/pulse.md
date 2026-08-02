# Pulse

**Status:** Release evidence verified on Arc testnet

**Network:** Arc Testnet (`5042002`)

Pulse is an Arc testnet activity dashboard and research interface. Pulse v0 is intended to make a small set of current network observations easy to inspect and independently follow into block and transaction records.

## Pulse v0 scope

The release candidate covers:

* recent blocks and transaction counts;
* gas-use context for displayed blocks;
* a recent transaction feed;
* wallet-address lookup;
* contract-address lookup; and
* outbound ArcScan references for independent inspection.

The [approved QA capture](../assets/screenshots/pulse-v0-2026-07-31.png) defines the visible release-candidate surface. Features not present in that capture are not represented as part of v0.

## Research standard

Pulse separates three layers:

1. **Observed data:** values returned by the configured Arc testnet RPC at a recorded time.
2. **Derived metrics:** calculations such as transaction totals or gas-utilization ratios, using definitions in the methodology.
3. **Interpretation:** a clearly labeled research note that does not overstate a short testnet sample.

See the [Pulse v0 methodology](https://github.com/StableSignal/public-research/blob/main/methodology/pulse-v0-methodology.md) and [Observation 0001](https://github.com/StableSignal/public-research/blob/main/notes/0001-arc-testnet-observations.md).

## Public evidence gate

Pulse v0 is not marked released until the following items agree:

* a dated release-candidate screenshot;
* the recorded network and capture window;
* a verified PulseBeacon contract address;
* its successful deployment transaction and ArcScan testnet URL; and
* the machine-readable [deployment registry](../deployments/arc-testnet.json).

Those records now agree for the verified Arc testnet PulseBeacon deployment at [`0x13FBc37C40d071d9654913013C93a63F9Dc770D3`](https://testnet.arcscan.app/address/0x13FBc37C40d071d9654913013C93a63F9Dc770D3).

## Limitations

Pulse v0 is a point-in-time testnet research view. It is not a finality oracle, indexer, production uptime monitor, risk score, wallet, custody service, or transaction signer. RPC availability, short-lived reorganization, test activity, and the selected observation window can all affect what is displayed.

StableSignal is an independent project building on Arc testnet. We are not affiliated with, endorsed by, or sponsored by Circle or Arc.
