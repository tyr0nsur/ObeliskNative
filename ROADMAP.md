# Roadmap

Updated 14 October 2026. The goal is matching commands, results, permissions,
limits and persistence of defined ASE plugin versions with original native Linux
implementations, without incorporating their source. Each module closes through recorded behavior,
client acceptance and migration checks, rather than a whole-suite percentage.

| Stage | Scope | Current position |
| --- | --- | --- |
| 1 | Commands and cooperative plugin management | Epic ping/identity confirmed; Six modules active; managed lifecycle verified; command UI, Steam and two-player checks pending |
| 2 | Accounts, permissions and economy | Offline roles/wallets and scoped authority decisions tested; trusted live identity and administrative integration pending |
| 3 | Shop, kits, sales and rewards | Catalogs, receipt state and exact stack-delta verification tested; native complete evidence and live subject mapping pending |
| 4 | Homes, player tools, chat and announcements | Session homes, whispers/global messages and scoped position bindings implemented; client acceptance, durable identity and cross-map scheduling pending |
| 5 | Dino, structure and tribe tools | Mounted/aimed/native group ID queries implemented; client acceptance, enumeration, ownership and individual decision hooks pending |
| 6 | Migration and pilot packaging | Inspect/dry-run implemented; reviewed import/source ports, clean stop and reproducible deployment pending |

The dated research inventory tracks 157 catalog entries, including the framework
and possible duplicates. Additional repository/forum references are separate.
It does not close unlisted/private products or undocumented behavior. A plugin's
presence in that inventory does not imply implemented or accepted parity.

## Client and lifecycle acceptance

- Validate a real Steam client alongside the existing Epic result.
- Connect two players and confirm directed replies reach their intended player.
- Check utility command text, arguments and UTF-8 presentation in-game.
- Exercise logout/relogin, interrupted login and stale session/context rejection.
- Preserve ordinary chat and character/world data through the checks.

## Module acceptance

Permissions need a verified account namespace and explicit administrative
control. Wallet persistence alone does not prove item delivery. Shop/kits need
receipts and recovery for uncertain world changes. Homes need stale-session and
permission checks before teleporting. Broadcasts need managed game-thread work;
dino/structure/tribe policies need their specific native actions verified.

## Migration

Migration inspection reports supported data, mappings and blocked fields before
any import. Existing permissions and player identifiers need explicit mappings;
unknown extensions cannot be silently dropped. Native Linux source ports require
adaptation and recompilation. Windows DLL binary compatibility is not established.

## Pilot release

Complete extended runs, update/restart checks and clean shutdown after the
observed stopping abort. Package a reproducible install, record supported native
builds and real client combinations, and define the commercial support scope.
The implementation remains private; this repository records presentation and
verified progress.
