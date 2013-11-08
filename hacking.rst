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


CORS
----

Strider supports CORS so that you may call it from a browser or open a websocket to it (Socket.io initiation protocol requires it.

To enable CORS pass a `cors` configuration option when instantiating Strider.

Example:

.. code:: javascript

  var strider = require('strider');
  var config = {
    cors: {
      origin: 'http://localhost:1337',
      credentials: true,
      headers: [
        'DNT',
        'X-Mx-ReqToken',
        'Keep-Alive',
        'User-Agent',
        'X-Requested-With',
        'If-Modified-Since',
        'Cache-Control',
        'Content-Type',
        'Accept',
        'Accept-Encoding',
        'Origin',
        'Referer',
        'Pragma',
        'Cookie'
      ],
      methods: [
        'GET',
        'PUT',
        'POST',
        'DELETE',
        'OPTIONS'
      ],
      maxAge: 1728000
    }
  };
  
  var app = strider(includePath, config, function(){
    console.log("Strider is running");
  });
