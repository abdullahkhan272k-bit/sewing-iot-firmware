# How to publish a firmware update

The stations check version.txt every day between 16:30 and 17:30. When it is different from the version inside their firmware, they download Sewing_IoT.ino.bin from the release "firmware" and install it.

Links used by the stations:

- Firmware: https://github.com/abdullahkhan272k-bit/sewing-iot-firmware/releases/download/firmware/Sewing_IoT.ino.bin
- Version: https://raw.githubusercontent.com/abdullahkhan272k-bit/sewing-iot-firmware/refs/heads/main/version.txt

For each update:

1. Build the firmware with FW_VERSION set to the new number, for example 4.5.2.
2. Rename the build file Sewing_IoT_v3_1.ino.bin to Sewing_IoT.ino.bin.
3. Open the release "firmware", click Edit, delete the old Sewing_IoT.ino.bin, attach the new one and click Update release.
4. Then edit version.txt to exactly the same number and commit it.

The number in version.txt must always be the same as FW_VERSION inside the uploaded file. Otherwise every station reinstalls the same firmware every day.
