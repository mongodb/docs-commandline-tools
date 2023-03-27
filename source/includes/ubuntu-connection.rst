Ubuntu 18.04 may use a non-standard DNS resolver. If so, when you try to
connect to the MongoDB server, the shell returns an error message like:

.. code-block:: shell

  error parsing uri: lookup <HOSTNAME> on 127.0.0.53:53: cannot unmarshal DNS message

To resolve the problem, edit ``/etc/resolv.conff`` to point to a
different DNS resolver.
