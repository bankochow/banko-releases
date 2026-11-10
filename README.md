# Banko Chow release control

This public repository is for release-control workflows only. The website, the iOS app, and the Android app stay in the private repository `bankochow/banko-app`.

Nothing in a commit here may be app source, photos of guests, a signing key, a store credential, or a build output.

The build that runs today (the site, a debug Android package, and an iOS simulator build) still lives with the private app. Shipping workflows move here once they can fetch that private source without copying it into this repository.
