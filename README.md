# Banko Chow release control

This public repository is for release-control workflows only. The website, the iOS app, and the Android app stay in the private repository `bankochow/banko-app`.

Nothing in a commit here may be app source, photos of guests, a signing key, a store credential, or a build output. Workflows must not upload IPAs or APKs as Actions artifacts (this repo is public).

Order tests run on public `bankochow/banko-ci`. The private app repo does not run GitHub Actions, so it does not burn private Actions minutes or fill Actions storage.

## iOS TestFlight (free public Actions)

Workflow: `.github/workflows/ios-testflight.yml`

1. Add the repository secrets listed at the top of that workflow file (signing material + App Store Connect API key + a read token for private `bankochow/banko-app`).
2. Actions → **iOS TestFlight** → **Run workflow**.
3. Choose the `banko-app` ref (default `main`).
4. The macOS job builds, signs, and uploads with `altool`. Processing then appears in App Store Connect → TestFlight.

A browser session on App Store Connect is not used by this job. Android shipping stays local for now.
