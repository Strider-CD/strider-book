Hacking Strider
===============

Auth
----

Currently Strider supports two kinds of authentication, cookie and basic. In
the near future, Hawk will be added.

Cookie authentication is done by posting to ``/login`` with a payload of
``email`` and ``password``. Content-type is ``www-form-urlencoded``. You then
have a session cookie.

.. note:: say something about expiration...

Basic auth is done by sending the header ``"Authorization: basic " +
base64(username + ":" + password)``. This must be done for every request that
requires authentication.
