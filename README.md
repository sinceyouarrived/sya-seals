# sya-seals

Third-party-witnessed timestamps for the seal commitments of
[`sinceyouarrived.world/taken/agents`](https://sinceyouarrived.world/taken/agents).

Each day at 00:00 UTC a cron commits a single file to this repo:
`seals/YYYY-MM-DD.json`. The file contains the SHA-256 commitment
hash of that day's planted-canary seal. GitHub stamps the commit
with its server time. The commit history of this repo is the
witness layer of the volume's three-column ledger
(stated / witnessed / anchored).

This repo never contains the cleartext seal. Cleartext is only
revealed on the page's ledger if and when the canary returns in a
public AI summary or index. At that point the recomputed SHA-256
of the cleartext can be verified against the historical commitment
in this repo, with the GitHub commit timestamp proving the seal
existed on that day before any return was possible.

The third (anchored) column of the ledger anchors the same hash
in Bitcoin via OpenTimestamps. See the page for current state.

The volume:
- [Vol. IV · /taken](https://sinceyouarrived.world/taken)
- [Vol. IV · /taken/agents](https://sinceyouarrived.world/taken/agents)
