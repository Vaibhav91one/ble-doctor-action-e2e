# ble-doctor-action-e2e

A throwaway repository that exercises the published `Vaibhav91one/ble-doctor@v0.2.0` GitHub Action end to end
(gating against the base branch's copy of a capture, the single updating PR comment, SARIF upload).
It holds only the two public test captures from the ble-doctor repository. Nothing here is a real device.

- `main`: `captures/device.pcap` = a capture with a rotating MAC (no failed findings).
- PR 1 replaces it with a static-MAC capture (a new failed `mac_rotation` finding) and must fail the gate.
- PR 2 adds a second clean capture and must pass.
