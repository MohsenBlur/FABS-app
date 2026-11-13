# FAQ

### Why does my phone need USB debugging?

It's the only way a PC can read all of the phone's files and check them exactly, without installing an app on the
phone. FABS uses it to copy and check files and never changes your phone's settings. You can turn USB debugging off
again when you're done.

### Is it safe?

Yes. A backup never changes your files on the phone. To copy quickly, FABS puts a small helper program in the
phone's temporary folder; it does nothing on its own, and the backup report and Settings offer to remove it. Putting a
backup back only adds files and never deletes or replaces anything.

### Windows warns about the installer. Why?

The installer isn't code-signed yet, so Windows SmartScreen may show "Windows protected your PC". Choose
**More info**, then **Run anyway**. The installer needs no administrator rights and installs for your user only.

### USB or Wi-Fi?

A cable is the fastest and most reliable: a USB 3 cable and port can copy more than 200 MB per second. Over Wi-Fi,
the phone and the PC must be on the same network. If your PC is on Wi-Fi itself, letting the phone join the PC's own
**mobile hotspot** is often two to three times faster than going through the router. FABS shows how.

### What is "Turbo Wi-Fi"?

An optional setting that can copy a little faster over Wi-Fi, using a direct, encrypted connection between the phone
and the PC. It's off by default. If it doesn't work on your network, copying carries on over the normal connection.

### Where are my backups?

In the folder you choose. Each phone's files keep their folder structure (DCIM, Pictures, Download, …), so you can
open them in File Explorer like any other files. A hidden `.fat` folder inside holds FABS's own records; leave it
there so that updates and checks work.

### Some file names look different on the PC.

Windows doesn't allow some characters in names that Android allows (for example `:` or `?`), and it treats `Photo.jpg`
and `photo.jpg` as the same name. FABS adjusts such names slightly and lists every change in the report. When you
put the backup back on a phone, the original names are used again wherever the phone allows them; any name that has to
change is listed in the report.

### Can I pause a backup?

Yes. Everything copied so far is kept and checked. Continue later from the start screen; FABS picks up where it
stopped.

### Does it back up my WhatsApp chats?

It copies WhatsApp's photos, videos and its chat backup files, but WhatsApp encrypts those with a key it keeps itself.
To restore your chats, use WhatsApp's own backup. Turning on WhatsApp's end-to-end encrypted backup and keeping its
password or key safe gives you a backup you control.

### How do I remove FABS?

Uninstall it from Windows Settings › Apps. Your backups stay where they are.
