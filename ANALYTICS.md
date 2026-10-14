# Public validation metrics

Updated 14 October 2026. These are observed development results, not projections
of market share, revenue or full API coverage.

| Metric | Verified result |
| --- | --- |
| Current automated CTest cases | 152 passed / 152 total |
| Earlier command prototype baseline | 147 passed / 147 total |
| Real client platform tested | Epic Games |
| Tested client / native server versions | 361.8 / 361.7 |
| In-game command and reply | `/ping` → `pong` confirmed |
| Copied player information | `/whoami` name and opaque native ID confirmed |
| Plugin login and logout delivery | Observed during the real Epic session |
| Ordinary chat | Confirmed by the player |
| Baseline disconnect/relogin | Confirmed by the player |
| Steam client validation | Pending |
| Reply separation between two real players | Pending |
| Broader lifecycle and clean shutdown validation | Pending |
| Cooperative plugin management | 13 real-server requests; server process unchanged |
| Plugin transitions exercised | Pause/resume, two reloads, stop/start and status |
| Plugin generations loaded in the live test | 4; final generation running |
| Direct chat reply presentation | Startup verified; real-client UI check pending |

The real-client results currently cover one Epic player. Automated fixtures
include separate command origins, but those fixtures do not replace a real
two-player acceptance test. No complete ArkApi parity or production stability
claim is made.

For the context behind each result, see [Progress](PROGRESS.md).
