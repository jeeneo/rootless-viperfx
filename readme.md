# Run ViperFX without rooting your Phone (kinda)

## What this is:
1. ViperFX on your Android without rooting it or voiding the warranty/bootloader unlocking
2. A rooted virtualized enviorment seperate from your existing Android (using closed source Virtual Master)
3. Android 7.1 (Android 9/11 wouldn't root or run VFX correctly)

## What this IS NOT:
1. A system pipe for audio for all your Audio (only what you play in the VM gets piped)
2. Rooting/reflashing your device

Instructions:

1. Download and install Virtual Master apk from release
2. Download Android 7 ROM from release
3. Create a VM with the ZIP
4. When it boots, import Magisk apk (v28.1 works)
5. It will say the VM requires restarting, let it
6. Power off the VM and in the VMs settings, enable shared folder. It will request All Files Access, grant.
7. It will create /SharedFolder in your internal storage on both the host and virtual system.
8. Download [ViperFX RE](https://github.com/WSTxda/ViperFX-RE-Releases)'s APK and [module](https://github.com/WSTxda/ViPERFX_RE/releases), copy both to /SharedFolder
9. In Virtual Master, open magisk and import that module, then install `viperfx-release.apk` and restart the VM
10. If everything was done correctly, you should be able to open ViperFX without driver issues!
    - (note: enable Legacy mode if apps don't get filtered just like a normal Android phone)

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
