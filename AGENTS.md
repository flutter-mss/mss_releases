# mss_releases

Public download channel for the Memention Software Shop macOS client.
**No source here** — only release tags with signed + notarized `MSS.app`
zips attached, plus a release-notes template.

The client's source lives in the private `flutter-mss/mss_app` repo.
`make publish` there uploads the current notarized zip as a tagged release
to this repo.

## Rules that aren't obvious from one file

- **Template tokens**: `RELEASE_NOTES_TEMPLATE.md` uses `__FOO__` tokens
  that `mss_app`'s `make publish` substitutes at release time (e.g.
  `__SHA__`, `__CHECKSUM__`). Edit the final release body via
  `gh release edit` or the GitHub UI for anything richer.
- **Tag format**: `v<semver>+<build>` where `<semver>` is the `version:`
  field from `mss_app/pubspec.yaml` and `<build>` is
  `git rev-list --count HEAD` on `mss_app` at release time.
- **Gatekeeper posture**: bundles are Developer ID-signed and stapled so
  first-launch quarantine opens without the right-click-open dance. Keep
  it that way; unsigned builds surface scary prompts and defeat the
  distribution purpose of this repo.

## Dev loop

Nothing to build here. To cut a new release, work from `mss_app`:

```bash
cd ../mss_app
make notarize
make publish
```
