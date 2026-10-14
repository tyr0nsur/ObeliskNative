# Roadmap

Updated 14 October 2026. Each milestone is completed through its acceptance criteria.

## 1. Multiplayer command acceptance

- Validate `/ping` and its reply with a real Steam client.
- Connect two players and confirm each command reply reaches its intended player.
- Repeat disconnect/reconnect tests and verify previous invocation contexts cannot send replies.
- Preserve ordinary chat throughout these cases.

Completion requires recorded client observations for each case, alongside the relevant automated checks.

## 2. Player and lifecycle interface

- Validate the identity information exposed to a plugin against real clients.
- Establish accepted login and logout behavior, including failed or interrupted connections.
- Document the lifetime of copied player information and invocation contexts.
- Verify identity and lifecycle extensions in the game.

Player name/native ID and typed login/logout have been observed with a real
Epic player. Broader relogin, interrupted connections and Steam acceptance
remain pending.

## 3. First useful administration plugin

- Current milestone: status, pause/resume, two reloads and stop/start of the
  cooperative oPing plugin verified in 13 real-server requests.
- Stop callback admission and drain active work before releasing plugin code.
- Server process unchanged across those requests; keep expanding failure and
  extended-run acceptance before broadening the supported plugin contract.
- Add installation/discovery of new plugin IDs and define a separate protocol
  for plugins that own background workers.

- Select one concrete need with a server operator.
- Deliver a small plugin with predictable configuration and permissions.
- Test its normal operation, failure behavior and cleanup.
- Publish a compatibility statement and an operator guide appropriate to the delivered feature.

## 4. Reproducible pilot release

- Package the runtime and example plugins for a reproducible installation.
- Record supported server builds and tested client combinations.
- Complete extended server runs, restart checks and update checks.
- Investigate the observed abort during server shutdown and validate a clean
  stop before a pilot release.
- Define the support and maintenance scope before offering a pilot release.

## 5. Broader plugin ecosystem

Extend the API according to validated plugin needs: administration, permissions, event handling and gameplay features. Evaluate plugin migration from other ecosystems after the native Linux interface is stable.
