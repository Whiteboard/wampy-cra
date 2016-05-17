wampy-cra.js
============

[WAMP][] Challenge Response Authentication plugin for [Wampy.js][].

Description
===========

wampy-cra exposes 3 methods:

* derive_key(secret, salt, iterations = 1000, keylen = 32). Used to generate a derived key using PBKDF2 scheme.
* sign(key, challenge). Used to sign a challenge message, using a key, using SHA256 algorithm.
* auto(secret). Probably the only function you need. Used to automatically detect needed algorythm to create a
signed message, using only secret key. This function can be passed as onChallenge callback. See examples below.


[Wampy.js]: https://github.com/KSDaemon/wampy.js
[WAMP]: http://wamp-proto.org/