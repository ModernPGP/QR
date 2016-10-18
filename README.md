QR
==

Methods of implementing support for verification / signing og PGP keys using QR codes.


QR Code URI
===========
* monkeysphere URI scheme: generates ``OPENPGP4FPR:73EE2314F65FA92EC2390D3A718C070100012282``, but will load any string made of 10 blocks of 4 hexadecimal characters, separated by zero or more whitespace (in Python: `re.search("((?:[0-9A-F]{4}\s*){10})", data, re.IGNORECASE)`. ``openpgp4fpr`` was chosen as a short version of "OpenPGP v4 fingerprint"

our proposal: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282``  
optional parameters:
* ``name``
* ``email``
* ``url``
* ``keyserver``

Example: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282?keyserver=hkp://pool.skskeyservers.net&email=dominik@dominikschuermann.de&url=http://sufficientlysecure.org&name=Dominik``
