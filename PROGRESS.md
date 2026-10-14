# Progress

## 14 October 2026 — first real-client command and reply

A native Linux ARK: Survival Evolved dedicated server received `/ping` from a real Epic Games client. The player confirmed the `pong` reply inside the game.

Tested combination:

- Epic Games client: **361.8**.
- Public ASE native Linux dedicated server: **361.7**.
- Example server plugin: **oPing**.

Ordinary chat and reconnect activity were also observed. These observations are tracked separately from the remaining session and multiplayer acceptance cases.

The baseline prototype passed **147 CTest checks** before the newer identity and lifecycle extensions. The subsequent suite-module build passed **156/156 CTest checks**, including the identity and lifecycle fixtures. Automated coverage includes plugin loading, command dispatch, reply context lifetime and related failure cases. The demonstrated in-game command/reply path does not replace the remaining multiplayer tests.

The Epic player subsequently confirmed the name and opaque native ID shown by
`/whoami`, and the plugin received a login event during that real connection.
The plugin also received a typed logout event after that real session.
Typed relogin and interrupted-session behavior remain pending.

## Next acceptance cases

- Real Steam client command and reply.
- Two players with replies kept separate.
- Invalid previous contexts rejected after disconnection or reconnection.
- Broader identity and logout/relogin behavior with real players.

The current demonstration covers one Epic player. Steam acceptance, multi-player reply separation and full lifecycle behavior remain pending.

## Development scope

The project is progressing from a native Linux prototype toward a practical plugin API. The implementation remains private while this repository records project scope, verified progress and planned acceptance work.

## 14 October 2026 — cooperative plugin lifecycle

Thirteen operator requests on the actual ARK server exercised status, pause,
resume, two plugin reloads, stop and start. The game server process stayed the
same throughout the requests. Four plugin generations loaded, with oPing
running at the end.

The current contract requires managed-only cooperative plugins. It closes
callback admission and drains active work and user-data cleanup before releasing
code. Failed cleanup retains the library. Private workers need a separate protocol. New plugin IDs are now covered by
the utility-package deployment described below.

The runtime also includes an independently checked route to deliver the response
inside the player's chat. Its server startup passes; the visible client UI and
separation between two real players remain pending. The previous notification
reply does not establish this new presentation.

TheIsland now uses recovered gameplay configuration while preserving the current
world and character files. This does not represent a recovery of historical
player saves, which were not available. Full server shutdown acceptance remains
pending after the observed abort during stopping.


## 14 October 2026 — first utility package and suite foundations

The current build passes **156/156 CTest cases**, including real-library
integration of ObeliskNative Essentials. It provides configurable `/help`,
`/rules`, `/motd` and `/serverinfo`, help topics and opt-in case-insensitive
argument routing. Existing exact command registrations retain their behavior.

The actual server started with oPing alone. Essentials was then installed and
started as a new plugin ID. Eleven successful operator requests exercised
status, pause/resume, reload and stop/start without changing the game process.
Both packages ended running. TheIsland and the current profile/configuration
were preserved. The new utility replies still require an in-game client check.

The private offline store now tests roles, explicit deny precedence, membership
expiry, integral balances, transaction rollback, operation deduplication,
concurrent connections and reopening persistence. It is not connected to live
player authorization or purchases.

An original inspect/dry-run migration tool passed **46 script tests** for copied
Permissions/ArkShop configurations and offline databases. It reports unknown
fields, integer conflicts and required identity/permission mappings, with
redacted output by default. It does not apply data to a live server. At that milestone, shop item delivery, homes, broadcasts and
dino/structure/tribe actions remained future stages. The next entry records
the subsequent session-home, chat and query implementations.


## 14 October 2026 — four more native modules

After a core upgrade, Shop/Kits, Advanced Chat, World Tools and Session Homes
were installed and started while the server was already running. Thirty-two
successful operator requests exercised their managed lifecycles without changing
the game process. All six modules ended running. TheIsland, protected access,
70 slots and the current profile were preserved.

The current build passes 156 CTest cases, including real-library fixtures and
regressions for session invalidation during nested calls. 214 SDK guardrails and
66 manager checks pass. Fresh SDK installation/consumer layout checks also pass.

Chat now has observed-session listing, global messages and whispers. Session
homes use saved character positions, a guarded self-only engine movement path,
and cooldown. They disappear on reconnect or plugin reload. World Tools read
current position, native tribe ID, mounted dino IDs and aimed structure ID.
These bindings pass mapped startup checks; visible query/message/movement
acceptance with real clients remains pending.

Shop/Kits exposes informational catalogs. Private reservations, exact receipt
state, kit quotas/cooldowns, rollback and interrupted delivery handling are
tested. The native item function can report success after partial delivery,
so purchases and kit fulfillment remain disabled until quantity-specific
receipts are verified. Persistent homes, cross-map chat, full world enumeration
and permission-checked dino/structure/tribe mutations remain subsequent stages.

## 14 October 2026 — beta guide and session-home recovery

The beta announcement now includes all **20 current chat commands** and an
attached guide with **88 pending acceptance cases**, expected results and a
report template. It covers Epic/Steam, two-player privacy, reconnects, chat,
catalogs, world queries, session homes and coordinated plugin transitions.
See the [Discord announcement](https://discord.com/channels/1511110561331544085/1511127623432933497/1559970839938474014).

Session Homes now recovers capacity from disconnected histories when a complete
validated session list is available. Incomplete lists preserve points and
cooldowns. Real-library regressions pass, and the updated plugin was reloaded
on the live server without restarting the game process. In-game `/help` now
lists the complete command inventory. The latest checks pass 156 CTests and
214 SDK guardrails; documentation and these checks do not accept any of the
pending client cases. The whole-server shutdown issue remains unresolved.

## 14 October 2026 — original gameplay parity foundations

The target is matching observable ASE plugin behavior with original native Linux
implementations. A dated inventory now tracks 157 public catalog entries across
official, free and paid ASE categories. It distinguishes the framework,
potential duplicate products and additional repository/forum references; it is
not a census of every plugin or a claim of complete parity. Each reference has
pending syntax, limits, persistence, presentation and client acceptance work.

Private command authorization now requires an explicit trusted principal and
current command scope, reads fresh permission decisions and rejects expiry or
principal/configuration changes. Private delivery verification compares exact
variant quantities and inventory stack increments; partial or unknown outcomes
stay blocked without an automatic refund or second grant. Real database tests
cover these boundaries. Neither foundation is connected to live authorization
or shop/kit fulfillment yet.

The current full build passes **158/158 CTests** and **214 SDK guardrails**.
Focused identity and inventory research checked the actual native executable
without enabling grants or claiming authenticated account correlation. The
laboratory still runs six modules and 20 commands. Further parity requires
verified native adapters and actual Steam/Epic gameplay acceptance.
