# Progress

## 14 October 2026 — first real-client command and reply

A native Linux ARK: Survival Evolved dedicated server received `/ping` from a real Epic Games client. The player confirmed the `pong` reply inside the game.

Tested combination:

- Epic Games client: **361.8**.
- Public ASE native Linux dedicated server: **361.7**.
- Example server plugin: **oPing**.

Ordinary chat and reconnect activity were also observed. These observations are tracked separately from the remaining session and multiplayer acceptance cases.

The baseline prototype passed **147 CTest checks** before the newer identity and lifecycle extensions. The current build passes **149/149 CTest checks**, including the identity and lifecycle fixtures. Automated coverage includes plugin loading, command dispatch, reply context lifetime and related failure cases. The demonstrated in-game command/reply path does not replace the remaining multiplayer tests.

The Epic player subsequently confirmed the name and opaque native ID shown by
`/whoami`, and the plugin received a login event during that real connection.
Broader logout/relogin behavior remains pending.

## Next acceptance cases

- Real Steam client command and reply.
- Two players with replies kept separate.
- Invalid previous contexts rejected after disconnection or reconnection.
- Broader identity and logout/relogin behavior with real players.

The current demonstration covers one Epic player. Steam acceptance, multi-player reply separation and full lifecycle behavior remain pending.

## Development scope

The project is progressing from a native Linux prototype toward a practical plugin API. The implementation remains private while this repository records project scope, verified progress and planned acceptance work.
