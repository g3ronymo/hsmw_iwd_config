This repository contains template configuration files for iwd.
This files can be used to configure iwd for the eduroam wifi at the
campus of "Hochschule Mittweida".

-------------------------------------------------------------------------------

Usage:

1. Copy the file ``eduroam.8021x`` to the directory where iwd stores its
   per network configuration files (which is normally ``/var/lib/iwd``). See
   ``man iwd.network`` for more information.
2. Edit ``eduroam.8021x``

   1. The value of ``EAP-PEAP-Phase2-Identity`` should be your email address.
   2. The value of ``EAP-PEAP-Phase2-Password`` should be your password.

-------------------------------------------------------------------------------

All configuration options are extracted from eduroam CAT, which can
be downloaded from https://cat.eduroam.org/. Eduroam CAT is a python script,
which only works with NetworkManager. A mapping from variables in the script
to iwd configuration options can be found under:
https://wiki.archlinux.org/title/Iwd#eduroam
