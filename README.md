# ObeliskNative

Native Linux server plugins for **ARK: Survival Evolved**.

The project is an independent initiative developing a plugin runtime for ARK's native Linux dedicated server. Its first playable prototype receives an in-game chat command and sends a reply back to the player.

## Current milestone

On 14 October 2026, a real Epic Games client reported as version 361.8 connected to the public ASE native Linux dedicated server, version 361.7. The player entered `/ping` and confirmed `pong` in the game. Ordinary chat and reconnect activity were also observed.

The current implementation passed **152 automated CTest checks**, including
the new identity and lifecycle fixtures. These checks complement the real-client
demonstration; broader lifecycle and multiplayer acceptance continues separately.

| Area | Status |
| --- | --- |
| Native Linux runtime and example plugin | Demonstrated |
| Epic in-game `/ping` → `pong` | Confirmed by a real player |
| Ordinary chat | Observed in the game |
| Reconnect activity | Observed; broader session acceptance remains pending |
| Steam client acceptance | Next validation |
| Reply separation between two players | Next validation |
| Player name and opaque native ID through `/whoami` | Confirmed by the Epic player |
| Plugin login and logout events | Observed during the real Epic session |
| Cooperative plugin control | Pause/resume, reload and stop/start verified without server restart |
| Broader logout/relogin behavior | Next validation |
| New reply presentation inside chat | Awaiting client confirmation |

## Plugin control milestone

The cooperative oPing plugin completed **13 live operator requests**, including
pause/resume, two reloads and stop/start. The game server process remained the
same throughout those requests, and the plugin finished running. This validates
the current managed plugin contract; arbitrary background-thread plugins and
installation of new plugin IDs need separate work.

## Direction

The goal is a practical plugin API for server commands, administration and gameplay extensions on Linux. Features will expand through working plugins and recorded compatibility tests.

The project is currently a prototype. Full ArkApi feature parity, Windows plugin binary compatibility and support across all ASE builds have not been established.

## Follow development

- [Progress and verified milestones](PROGRESS.md)
- [Roadmap and acceptance criteria](ROADMAP.md)
- [Public validation metrics](ANALYTICS.md)
- [In-game screenshots](media/screenshots/)

This repository contains the project presentation, public validation metrics
and development progress. The implementation remains private as part of the
project's commercial development.
