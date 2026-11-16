# Banko Chow release control

This public repository is for release-control workflows only. The website, the iOS app, and the Android app stay in the private repository `bankochow/banko-app`.

Nothing in a commit here may be app source, photos of guests, a signing key, a store credential, or a build output.

Order tests run on public `bankochow/banko-ci`. The private app repo does not run GitHub Actions, so it does not burn private Actions minutes or fill Actions storage.

Signed iOS and Android releases are built locally from `bankochow/banko-app` for now. Shipping workflows can move here later if they check out that private source at run time without copying it into this repository.
