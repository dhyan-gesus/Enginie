# Enginie for Android

The Android app is a Trusted Web Activity: a thin wrapper that opens the live site full screen.
It was generated with [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap) from
`twa-manifest.json`. The signing key is kept outside this repository and must never be committed.

To rebuild: copy `twa-manifest.json` into an empty folder, raise `appVersionCode`, run
`bubblewrap update`, then `gradlew assembleRelease bundleRelease` and sign the outputs.

For the app to open without a browser bar, `https://dhyan-gesus.github.io/.well-known/assetlinks.json`
must list the app's signing certificate. That file lives in the `dhyan-gesus.github.io` repository.
