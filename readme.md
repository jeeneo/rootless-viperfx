# Run ViperFX without rooting your Phone (kinda)
Tested on Android 15/OneUI 7

## What this is:
1. ViperFX on your Android without rooting it or voiding the warranty/bootloader unlocking
2. A rooted virtualized environment (Android 7.1) separate from your existing Android (using closed source Virtual Master)

## What this IS NOT:
1. An audio pipe for your system (only what you play in the VM gets piped)
2. Rooting/reflashing your device

## Limitations
1. Only audio played inside the VM will be filtered (hopefully obvious)
2. If you use local files, your music library (MP3s, FLACs, etc) has to be moved to your Internal Storage, external storage isn't supported. This is an app limitation. You could probably edit the APK to support external storage but that's outside the scope of this guide.
3. Battery is probably going to get drained, it is what it is.

## Disclaimer:
Virtual Master is closed-source. Use at your own risk.

----

## Instructions:
1. Download both `virtualmaster.apk` and the `rom zip` from [releases](https://github.com/jeeneo/rootless-viperfx/releases/tag/latest) (also download [Magisk](https://github.com/topjohnwu/Magisk/releases/tag/v28.1))
3. Create a new VM using the import tool, select the ZIP you downloaded.
4. When it boots, add the Magisk apk from the apps menu (v28.1 works)
5. It will prompt you to restart the VM, allow
6. Power off the VM and in the VMs settings, enable shared folder. It will request All Files Access, grant.
7. It will create `/SharedFolder` on the Internal Storage for both the host and virtual system.
8. Download [ViperFX RE](https://github.com/WSTxda/ViperFX-RE-Releases)'s APK and [module](https://github.com/WSTxda/ViPERFX_RE/releases), copy both to `/SharedFolder`
9. Start the VM and open Magisk, then import the module, and install `viperfx-release.apk`, finally restart the VM.
10. If everything was done correctly, you should be able to open ViperFX without driver issues!
    - (note: enable Legacy mode if some apps don't get filtered just like a normal Android phone)

(also note: you can increase refresh rate from 60 to 120 in VM settings for a smoother/faster experience)

## Issues
Some apps like Poweramp don't support adding symlinked directories (which is what `/SharedFolder` is). If you want to add your media library to the VM without copying all of it, try:

1. Move your existing Music library to `/SharedFolder`
2. In the VM, rename the symlinked folder `SharedFolder` to `SharedFolderAlt` (or something similar)
3. Create an empty `SharedFolder` and add that in your players scan directory (in Poweramp don't use SAF picker, use it's own internal picker)
4. After the folder has been added, close your media player delete that folder
5. Rename `SharedFolderAlt` back to `SharedFolder`
6. Open your media player and it should scan it fine.

----

## Who's it for?
1. Those who own a phone but can't root it (eg. North American Samsung S24)
   - and don't want to pay for a paid unlock or risk bricking it
2. Those who play music locally (FLAC, MP3) but want VFX
3. Cannot buy another phone at the present moment

(this is me)

## Streaming
I've tested
 - Spotify
 - Tidal
 - Deezer

All worked correctly.

## Okay, but... why?
I don't know, I liked VFX on my rooted Tab S9 but using a tablet for media seemed clunky to say the least, and didn't want to carry another phone just for music. This is meant to be a temporary fix for people who cannot root their phone, until they can buy a new one where rooting is an option. And a fun experiment as well
