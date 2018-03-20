# rpc-deploy-utility

Playbooks used for automation of the [rpc-deploy utility image](https://github.com/rcbops/rpc-deploy-utility-image).

Contains playbooks for:

* Updating firmware of supported bare metal platforms (HP, Dell, etc)
* Configuration of OBM (Out of Band Management)
* RAID configuration

These playbooks are burned into the Utility image.  The current plays that can be run are:

|State|Purpose|Data Destructive|
|-----|-------|-----------|
|preflight|Loads Utility image, applies Firmware/RAID/OBM updates for detected hardware|yes|
|provision|Installs the OS to the hardware|yes|
|firmware|Updates all firmware and then boots back into OS|no|
