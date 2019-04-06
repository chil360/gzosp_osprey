
GZOSP Pie for Osprey
====================

Current Status
--------------

What's working?
 - Bluetooth
 - Camera (except HDR)
 - Camcorder
 - RIL
 - WiFi
 - Storage
 - 4G
 - Camera HDR
 - Selinux Enforcing
 - VoLTE (credits to [@nicorg2515](https://github.com/nicorg2515))

Download
--------

Downloads for GZOSP are available here at [AndroidFileHost](https://androidfilehost.com/?w=files&flid=291559).

Build Instructions
------------------
Create a build directory

	mkdir gzosp
	cd gzosp

Initialize your local repository using the GZOSP trees, use a command like this:

    repo init -u https://github.com/GZOSP/manifest.git -b 9.0

Now create a local_manifests directory

    mkdir .repo/local_manifests

Copy my local manifest 'osprey.xml' to the 'local_manifests' directory.

Then to sync up:

    repo sync -c -f --force-sync

OR, for those with limited bandwidth/storage:

    repo sync -c -f --no-clone-bundle --no-tags --force-sync --optimized-fetch --prune

Apply Patches

    Place patch.sh and all *.patch files in your build directory. Run the patch.sh script to apply the patches.

Now start the build...

```bash
# Go to the root of the source tree...
$
# ...and run to prepare our devices list
$ . build/envsetup.sh
# ... now run
$ lunch gzosp_osprey-userdebug
$ make gzosp
```

Please see the [GZOSP github](https://github.com/GZOSP) for further information.
