# MicroBenchmark-Releases

This repo hosts **only built distribution artifacts** for the
[MicroBenchmark](https://github.com/AISmithLab/MicroBenchmark) desktop app —
the `.dmg`, signed `.app.tar.gz`, and the `latest.json` the app's
auto-updater checks. No source code lives here, on purpose:
`MicroBenchmark` is a private repo (it holds benchmark answer keys and other
data that must not be public), but Tauri's updater plugin needs a public,
unauthenticated `latest.json` to check against. This repo exists solely to
give it one.

Releases here are published automatically by
[`.github/workflows/release.yml`](https://github.com/AISmithLab/MicroBenchmark/blob/main/.github/workflows/release.yml)
in the private repo, on every `v*` tag.
