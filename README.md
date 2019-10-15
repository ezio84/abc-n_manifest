ABC rom
=====================

Tip and tricks:

Repo init command:

	repo init -u https://github.com/ezio84/abc_manifest.git -b q

Sync source (for future syncs, if you have errors, try "repo sync --force-sync")

	repo sync

To build, use the build_rom.sh script in the "scripts" tree or:

	. build/envsetup.sh
	make clean
	brunch "abc_taimen-user" 2>&1 | tee build.log


To flash the first time: remove pin, flash stock factory img, flash boot.img with fastboot, then boot to stock recovery and adb sideload the OTA zip you got in the out folder. Before rebooting wipe data.


=====================
