# hfi1-firmware
Firmware for Intel Omni-Path hfi1 fabric interface

## Upstream Source

Intel delivers hfi1 firmware as binary RPMs. In order to create the upstream
source for Debian, the RPMs are extracted into a filesystem and tarred up.

```
# mkdir hfi1-firmware-0.9
# cd hfi1-firmware-0.9
# rpm2cpio ~/hfi1-firmware-0.9-59.noarch.rpm | cpio -ivd
# rpm2cpio ~/hfi1-firmware_debug-0.9-59.noarch.rpm | cpio -ivd
# cd ..
# tar czf hfi1-firmware_0.9-50.orig.tar.gz hfi1-firmware-0.9
```

## License

hfi1-firmware has a proprietary license and EULA. Redistribution is permitted,
but the binaries may not be reverse engineered or modified.

See usr/share/doc/hfi1-firmware/LICENSE and usr/share/doc/hfi1-firmware/LICENSE-chf_smbus_mc.

-- Brian T. Smith <bsmith@systemfabricworks.com>
