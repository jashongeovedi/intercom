# Proof Artifacts

Run date: 2026-02-24 16:25:53 +07:00

Fork URL: https://github.com/jashongeovedi/intercom
Custom app label: Intercom Delivery Lane Board
Domain noun: delivery_lane
Mutating command: promote_delivery_lane
Query command: trace_delivery_lane
Payout Trac address: trac1adrllzuw67d4emzv4d0fcdp98uy5g4gfw8n4mllllyt4e0zskm3sryqsf0

## Naming rationale
- delivery_lane matches the app theme (project delivery tracking).
- promote + trace gives clear mutate/query semantics.
- command names are intentionally direct and without username suffix.

## Files
- run.log: output captured from pear runtime startup.
- run-screenshot.png: PNG render of run.log for quick visual proof.
- command-mapping.log: mapping output from protocol mapTxCommand checks.
- tx-sim.log: runtime `cli_result` capture for `/tx --command ... --sim 1` via SC-Bridge CLI.

## Commands used
- pear run . --peer-store-name proof-admin --msb-store-name proof-admin-msb --subnet-channel proof-intercom-status --dht-bootstrap 127.0.0.1:49737 --sidechannels proof-room
- /tx --command '{"op":"promote_delivery_lane","status":"MVP ready","note":"first demo"}' --sim 1
- /tx --command "trace_delivery_lane" --sim 1
