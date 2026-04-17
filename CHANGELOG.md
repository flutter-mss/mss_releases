# Changelog

Release notes for the MSS macOS client.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/);
versions are the `mss_app` semver + git commit count suffix.

## [Unreleased]

## [0.1.0] - 2026-04-17

First public release. Signed + notarized for macOS.

### Highlights

- Browse the public registry at `mss.memention.net` anonymously.
- Sign in to unlock plugin and interface authoring tabs.
- Assemble custom Flutter desktop apps from registered plugins with one
  click — the client clones sources, generates a project, and runs
  `flutter build macos` locally.
- Reference bundles available in the registry:
  `demo_photoapp`, `demo_flappybird`, `demo_alternative_physics`.

### Requirements

- macOS 10.15+ (Apple Silicon or Intel)
- Flutter + Xcode Command Line Tools for the assembly step
