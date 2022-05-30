1. Copy the file ``hsmw.crt`` to a location where the iwd daemon can read it.
2. Copy the file ``eduroam.8021x`` to ``/var/lib/iwd``. This is the location
   where iwd will normaly look for network-configuration files (see 
   ``man iwd.network``).
3. Edit ``/var/lib/iwd/eduroam.8021x``
   1. The value of ``EAP-PEAP-CACert`` should be the complete path to the
      ``hsmw.crt`` file.
   2. The value of ``EAP-PEAP-Phase2-Identity`` should be your email address.
   3. The value of ``EAP-PEAP-Phase2-Password`` should be your password.