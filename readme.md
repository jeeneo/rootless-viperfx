# Run ViperFX without rooting your Phone (kinda)

## What this is:
1. ViperFX on your Android without rooting it or voiding the warranty/bootloader unlocking
2. A rooted virtualized environment separate from your existing Android (using closed source Virtual Master)
3. Android 7.1 (Android 9/11 wouldn't root or run VFX correctly)

## What this IS NOT:
1. A system pipe for audio for all your Audio (only what you play in the VM gets piped)
2. Rooting/reflashing your device

## Limitations
1. Only audio played inside the VM will be filtered (hopefully obvious)
2. If you use local files, your music library has to be moved to `/SharedFolder` in your Internal storage, external storage isn't supported. This is an app limitation. You could probably edit the APK to support external storage but that's outside the scope of this guide.

## Disclaimer:
Virtual Master is closed-source. Use at your own risk.

----

## Instructions:
1. Download and install Virtual Master apk from releas
2. Download Android 7 ROM zip from release
3. Create a new VM using the import tool, select the ZIP you downloaded.
4. When it boots, import Magisk apk (v28.1 works)
5. It will prompt you to retstart the VM, allow
6. Power off the VM and in the VMs settings, enable shared folder. It will request All Files Access, grant.
7. It will create `/SharedFolder` on the Internal Storage for both the host and virtual system.
8. Download [ViperFX RE](https://github.com/WSTxda/ViperFX-RE-Releases)'s APK and [module](https://github.com/WSTxda/ViPERFX_RE/releases), copy both to `/SharedFolder`
9. In Virtual Master, open magisk and import that module, then install `viperfx-release.apk` and restart the VM
10. If everything was done correctly, you should be able to open ViperFX without driver issues!
    - (note: enable Legacy mode if apps don't get filtered just like a normal Android phone)

## Issues
Some apps like Poweramp don't support adding symlinked directories (which is what `/SharedFolder` is)
If you want to add your media library to the VM without copying all of it, try:

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
 - Spotify
 - Tidal
 - Deezer
All opened correctly but I'll test streaming later

## Okay, but... why?
I don't know, I liked VFX on my rooted Tab S9 but using a tablet for media seemed clunky to say the least, and didn't want to carry another phone just for music. This is meant to be a temporary fix for people who cannot root their phone, until they can buy one they can. And a fun experiment as well
