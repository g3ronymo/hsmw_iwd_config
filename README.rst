This repository contains template configuration files for iwd.
This files can be used to configure iwd for the eduroam wifi at the
campus of "Hochschule Mittweida".

-------------------------------------------------------------------------------

Usage:

1. Copy the file ``hsmw.crt`` to a location where the iwd daemon can read it.
2. Copy the file ``eduroam.8021x`` to ``/var/lib/iwd``. This is the location
   where iwd will normaly look for network-configuration files (see 
   ``man iwd.network``).
3. Edit ``/var/lib/iwd/eduroam.8021x``

   1. The value of ``EAP-PEAP-CACert`` should be the complete path to the
      ``hsmw.crt`` file.
   2. The value of ``EAP-PEAP-Phase2-Identity`` should be your email address.
   3. The value of ``EAP-PEAP-Phase2-Password`` should be your password.

-------------------------------------------------------------------------------

All configuration options are extracted from eduroam CAT, which can
be downloaded from https://cat.eduroam.org/. This configuration tool is a
python script, which only works with NetworkManager. A mapping from variables
in the script to iwd configuration options can be found under:
https://wiki.archlinux.org/title/Iwd#eduroam
