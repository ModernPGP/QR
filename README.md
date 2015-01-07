QR
==

Methods of implementing support for verification / signing og PGP keys using QR codes.


QR Code URI
===========
* monkeysphere URI scheme: ``openpgp4fpr:73EE2314F65FA92EC2390D3A718C070100012282``
* ``openpgp4fpr`` OpenPGP v4 fingerprint

our proposal: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282``  
optional parameters:
* ``name``
* ``email``
* ``url``
* ``keyserver``

Example: ``pgp-fingerprint:73EE2314F65FA92EC2390D3A718C070100012282?keyserver=hkp://pool.skskeyservers.net&email=dominik@dominikschuermann.de&url=http://sufficientlysecure.org&name=Dominik``
