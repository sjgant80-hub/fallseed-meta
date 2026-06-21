# FallSeed · Meta

> **The monitor seed.** A sovereign single-HTML PWA that pulls the live registry, subscribes to the cross-seed mesh, and shows the FallSeed estate as a living population.

**Live:** https://sjgant80-hub.github.io/fallseed-meta/

## What this is

fallseed-meta is to the FallSeed estate what an etcd dashboard is to a Kubernetes cluster: a window onto what exists, what's running, what's healthy. It is the seed whose substrate is the lift hierarchy itself.

## Tabs

- **Welcome** — at-a-glance counts of the estate
- **Population** — every seed in the registry, grouped by level (L0/L1/L2/L3/L4 + tools). Click any to visit.
- **Lineage tree** — parent → child fork graph as a visual tree
- **Live mesh** — fellow seeds online RIGHT NOW (via fall-signal · refreshed every 10s)
- **Smoke test** — runs in-browser HTTP checks against every seed URL · pass/fail with timing
- **Visit any seed** — iframe-embed any registered seed for inspection (same-origin = mesh works between them)
- Build · LLM Providers · Inspect · Settings · Install (standard FallSeed shape)

## Architecture invariants

- One HTML file · IDB primary · BroadcastChannel mesh (`fall-meta` + `fall-signal`)
- Pulls live registry from `raw.githubusercontent.com/sjgant80-hub/fall-registry`
- Subscribes to all four mesh message types (hello / ping / pong / request-response)
- Exposes `introspect` cross-seed handler
- 8-provider LLM cascade with streaming (for the Build tab)
- No telemetry · no analytics · no remote write

## Cosmology

Prime **1279**, spine-clean mod 127 = 9 = 3². Category **meta** (not a level in the lift hierarchy — it's the *observer* of the hierarchy). Mesh channel `fall-meta`. Seal **◊·κ=1**.

## When this becomes most useful

When the population includes seeds by more than one author. At that point the lineage tree shows real forks, the mesh shows real cross-author discovery, and the smoke test catches third-party deploy regressions in addition to your own.

## Licence

MIT © Simon Gant.
