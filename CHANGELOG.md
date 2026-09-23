# Tabby MultiExec Changelog

This file records the public release history of Tabby MultiExec.

Release dates below are the dates the corresponding package versions became
available through npm.

## 1.0.3 — 2026-09-23

### Fixed

- Fixed stale terminal focus after disabling MultiExec and returning tiled
  sessions to normal tabs.
- Normal single-line paste is again confined to the selected tab after leaving
  MultiExec.
- Multiline paste after leaving MultiExec now produces exactly one confirmation
  and is sent only to the selected tab.
- Fixed a Tabby split-teardown timing issue that could leave multiple former
  panes internally marked as focused.
- Verified that MultiExec can be enabled again after returning to normal tabs
  and broadcast resumes normally.

## 1.0.2 — 2026-09-22

### Fixed

- Moved MultiExec broadcast capture to the active terminal's `sendInput()`
  boundary so Tabby-generated terminal input is preserved.
- Home and End now broadcast correctly to included panes.
- Control/navigation input tested during the release pass follows the same
  broadcast path.
- Multiline paste now prompts once on the source pane instead of independently
  prompting on destination panes.
- Approved multiline paste is forwarded only to included panes.
- Dynamic Exclude state is honored during broadcast and paste.
- Changing the active/source pane no longer disables MultiExec.
- Bare Insert is intentionally suppressed while MultiExec is active to avoid
  unintended remote application mode changes across multiple sessions.
- Shift+Insert and other modified shortcuts remain available.

## 1.0.1 — 2026-09-22

### Changed

- Added public support and documentation links.
- Updated package metadata so users can find the public Tabby MultiExec support
  repository.
- Improved the public path for documentation, bug reports, compatibility
  reports, and feature requests.

## 1.0.0 — 2026-09-22

### Added

- Initial public npm release of Tabby MultiExec.
- Persistent selective MultiExec for tiled Tabby terminal sessions.
- Dynamic per-pane Exclude controls.
- Independent MultiExec, Tile, and Tabs workflow controls.
- Persistent MultiExec state while changing the active/source terminal.
- Per-pane MultiExec state indicators.
- One-click copying of the focused terminal's complete scrollback.
- Local installation and uninstall support.
- Initial documentation, screenshots, package metadata, and license.
