ABC rom
=====================

Tip and tricks:

Repo init command:

	repo init -u https://github.com/ezio84/abc_manifest.git -b r

Sync source (for future syncs, if you have errors, try "repo sync --force-sync")

	repo sync

Generate your signature keys and move them into vendor/security folder:
https://github.com/ezio84/scripts/tree/r/signed%20build

To build, use the build_rom.sh script in the "scripts" tree or:

	. build/envsetup.sh
	make clean
	brunch "abc_taimen-user" 2>&1 | tee build.log


To flash the first time: remove pin, flash stock factory img, flash boot.img with fastboot, then boot to stock recovery and adb sideload the OTA zip you got in the out folder. Before rebooting wipe data.


=====================
