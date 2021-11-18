# updater-snap
Example of a firmware update snap for Ubuntu Core based on the fwupd-dbus RUST library. Strictly confined.

## Build
Just launch ```snapcraft``` on top dir, this will create updater-snap_1.0_amd64.snap 

## Install
```
snap install uefi-fw-tools
snap install updater-snap_1.0_amd64.snap --dangerous
snap connect updater-snap:fwupd uefi-fw-tools:fwupd
```

## Run
```
sudo updater-snap.fwupd-test
```

## Notes
If you want to have a look on what the example is doing, the RUST code is located in src/main.rs (based on https://github.com/pop-os/fwupd-dbus/blob/master/examples/example.rs)
