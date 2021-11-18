# updater-snap
Example of a firmware update snap for Ubuntu Core based on the fwupd-dbus RUST library.

## Build
Just launch ```snapcraft``` on top dir, this will create updater-snap_1.0_amd64.snap 

## Install
```
snap install uefi-fw-tools
snap install updater-snap_1.0_amd64.snap --dangerous
snap connect updater-snap:fwupd uefi-fw-tools:fwupd
```
