# Public validation metrics

Updated 14 October 2026. These are observed development results, not projections
of market share, revenue or full API coverage.

| Metric | Verified result |
| --- | --- |
| Current automated CTest cases | 156 passed / 156 total |
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
| Earlier oPing control-run generations | 4; final generation running |
| Direct chat reply presentation | Startup verified; real-client UI check pending |
| Essentials hot installation/control | 11 real-server requests; game process unchanged |
| Essentials utility commands | Real-library fixtures pass; in-game replies pending |
| Offline permission/wallet foundation | Persistence, expiry, rollback and concurrency tested |
| Migration inspection tests | 46 passed; inspect/dry-run only, no live apply |
| Cooperative modules currently running | 6 |
| Four-module lifecycle increment | 32 requests; game process unchanged after core upgrade |
| Session invalidation regressions | Wrong token/epoch, nested calls and successor-session reads/sends rejected |
| New game query/chat/home effects | Native startup and fixtures pass; real-client acceptance pending |
| Shop/kit fulfillment | Disabled pending verified complete delivery |

The real-client results currently cover one Epic player. Automated fixtures
include separate command origins, but those fixtures do not replace a real
two-player acceptance test. No complete ArkApi parity or production stability
claim is made.

For the context behind each result, see [Progress](PROGRESS.md).
