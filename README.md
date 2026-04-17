# mss_releases

Public download channel for the [Memention Software
Shop](https://mss.memention.net) macOS client.

The client's source lives in a private repo; this one exists to carry
signed, notarized `.app` bundles to anyone who wants to try MSS without
building from source.

## Download

→ [**Latest release**](https://github.com/flutter-mss/mss_releases/releases/latest)

Each release ships a versioned zip named
`MSS_<version>+<build>.zip` containing `MSS.app`. Unzip, drag to
`/Applications`, and launch — the bundle is signed with a Developer ID
and notarized, so Gatekeeper opens it without the usual right-click
dance.

## System requirements

- macOS 10.15 (Catalina) or later on Apple Silicon or Intel
- Xcode Command Line Tools + Flutter installed locally (the client
  shells out to `flutter build macos` when assembling apps from
  plugins; the bundle itself runs without them but assembling won't
  work)

First launch writes state to `~/.msstore/{cache,builds,selections}`.

## Versioning

`MAJOR.MINOR.PATCH+BUILD`:

- `MAJOR.MINOR.PATCH` is the `version:` field in the client's
  `pubspec.yaml` (semver).
- `BUILD` is the git commit count of the `mss_app` repo at release
  time, so two releases off the same semver are distinguishable.

Release notes for each version live on the [Releases
page](https://github.com/flutter-mss/mss_releases/releases); this repo
has no source code, only tags + attached binaries.

## See also

- **[Memention Software Shop](https://github.com/flutter-mss)** — the
  org and project overview
- **[mss_core](https://github.com/flutter-mss/mss_core)** — the plugin
  contract (if you're writing a plugin)
- **[mss_server](https://github.com/flutter-mss/mss_server)** — the
  registry backend
- **[mss.memention.net](https://mss.memention.net)** — the live
  registry

## License

MIT. See [LICENSE](LICENSE). The bundled binaries inherit the MIT
license of `mss_app` and its transitive open-source dependencies.
