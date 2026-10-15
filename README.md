# Orbeat bank templates

The signed file the [Orbeat](https://github.com/bugzza99) Android app downloads, at most once a
day, to read bank and wallet messages on the phone. It holds only the **shapes** of those
messages: fixed words, number slots, and where the amount and merchant sit. It holds no
personal data, and the app sends nothing when it downloads it.

- `v1/templates.json`: the templates (schema 1).
- `v1/templates.json.sig`: an Ed25519 signature of the exact bytes of `templates.json`.

The app refuses any file whose signature does not match its built-in public key, whose version
is not newer than the one it has, or that needs a newer app. A refused file changes nothing.

Public key (base64): `eliA24zcvuqG9qRLkLp1jC5yMsNFlI898yChaGmLCn0=`

Files here are built and signed from the app's private repository; do not edit them by hand.
