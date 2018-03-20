# rpc-deploy-utility

Playbooks used for automation of the [rpc-deploy utility image](https://github.com/rcbops/rpc-deploy-utility-image).

Contains playbooks for:

* Updating firmware of supported bare metal platforms (HP, Dell, etc)
* Configuration of OBM (Out of Band Management)
* RAID configuration

These playbooks are burned into the Utility image.  The current plays that can be run are:

|State|Purpose|Data Destructive|
|-----|-------|-----------|
|firmware|Updates all firmware and then boots back into OS|no|
|preflight|Preps machine for OS, updates firmware, configures RAID, configures OBM|yes|
|raid|Removes all partitions and sets up RAID array|yes|
