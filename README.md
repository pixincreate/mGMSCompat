# GMSCompat

Magisk Module for adding GMS compatibility layer for vanilla android devices like LineageOS and etc., I'm newbie, not sure how it goes

I assume this module requires Zygisk since GMSCompat by GrapheneOS makes use of prebuilt `GmsCompatConfig.apk`, `config-holder` and many other as such.

[Note]  
I've added `functions.sh` which is based on `mmt-ex` (as of now, for showcase of course!). Hence, `customize.sh` is dependent on `mmt-ex`!  

## Roadmap (may be?)

- During installation of module, the module should check whether GMS is already installed by checking its installation directory
  - If possible, check the granted system level permmissions for confirmation (I might learn any othe refficient way to check its installation sometime in future)
- If `true`, `abort` the installation process
- Make changes to the respective directories and install necessary apps to get this working
- 1st 2 references added below are not enough to get mGMSCompat working. There're many changes needed to be done to get this working
- I'm open for suggesstions and inputs from devs in this field because, I don't think this can directly be implemented directly since I need to put my hands into the `frameworks_base` which I don't think is accessible within `root` folder

## Few more thoughts on GMSCompat after using GrapheneOS 

- mGMSCompat requires root access to work while GOS requires the bootloader to be locked to pass the Play Integrity API.
- I'm not sure whether its the ROM side thing or something different. What I mean by this is that if locking bootloader is necessary after installing GMSCompat, then it defeats the purpose of this project. 
- Looking forward to learn more things regarding this.

## For reference

- [VoltageOS/packages_apps_GmsCompat](https://github.com/VoltageOS/packages_apps_GmsCompat)
- [VoltageOS/external_GmsCompatConfig](https://github.com/VoltageOS/external_GmsCompatConfig)
- [VoltageOS/frameworks_base](https://github.com/VoltageOS/frameworks_base)
- [SandboxedGooglePlayCompatibilityLayerCommits](https://gist.github.com/thestinger/ee536cbd1ca674b94dde05831192c348)
