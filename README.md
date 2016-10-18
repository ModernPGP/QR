QR
==

Methods of implementing support for verification / signing og PGP keys using QR codes.


QR Code URI
===========
* monkeysphere URI scheme: generates ``OPENPGP4FPR:73EE2314F65FA92EC2390D3A718C070100012282``, but will load any string made of 10 blocks of 4 hexadecimal characters, separated by zero or more whitespace (in Python: `re.search("((?:[0-9A-F]{4}\s*){10})", data, re.IGNORECASE)`. ``openpgp4fpr`` was chosen as a short version of "OpenPGP v4 fingerprint"

This format was adopted by OpenKeyChain and others and is the current ad-hoc standard.

Deprecated proposals
====================

It was previously proposed to use: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282``  

Optional parameters:
* ``name``
* ``email``
* ``url``
* ``keyserver``

Example: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282?keyserver=hkp://pool.skskeyservers.net&email=dominik@dominikschuermann.de&url=http://sufficientlysecure.org&name=Dominik``

This scheme was abandoned because of interoperability issues with existing implementations, without significant gains in functionality. Furthermore, there were security concerns with the `url` and `keyserver` parameters that could be abuse by an attacker (the signee) to flood a keyring with data or track a victim (the signer).
