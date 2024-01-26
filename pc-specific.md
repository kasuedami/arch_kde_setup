## Medion laptop

### Wifi disconnetion problem

Probably caused by iwlwifi driver power saving default settings.
The problem seems to be mitigated by setting options for iwlwifi and iwlmvm kernel modules.
For a permanent solution create the file **/etc/modprobe.d/iwlwifi.conf** with the following contents:

options iwlwifi uapsd_diable=0
options iwlmvm power_scheme=1
