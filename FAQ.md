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

An archive is saved in a new folder of its own inside the folder you choose, as one file or a few parts. To look at
its files, open it with 7-Zip (see "How do I open an archive without FABS?").

### Some file names look different on the PC.

Windows doesn't allow some characters in names that Android allows (for example `:` or `?`), and it treats `Photo.jpg`
and `photo.jpg` as the same name. In a normal backup, FABS adjusts such names slightly and lists every change in the
report. When you put the backup back on a phone, the original names are used again wherever the phone allows them; any
name that has to change is listed in the report.

An archive keeps every name exactly; see "Why do some names change when I open the archive in Windows?".

### Can I pause a backup?

Yes. Everything copied so far is kept and checked. Continue later from the start screen; FABS picks up where it
stopped.

### Normal backup or archive?

A normal backup is a folder of files you can open and update. An archive saves the whole phone as one file, or a few
parts. To make one, choose **Archive an old phone (one file)…** on the start screen, or **Make an archive of this
backup…** on a backup you already have (no phone needed).

| | Normal backup (folder) | Archive (one file) |
|---|---|---|
| Best for | a phone you still use | a phone you are retiring, selling or giving away |
| Look at photos straight away | yes, in File Explorer | open the archive first (for example with 7-Zip) |
| Update later with new photos | yes | no: an archive is a snapshot. Make a new archive, or a normal backup. |
| Copy to a USB stick, cloud or disc | thousands of files, so slow | one file or a few parts, so fast and tidy |
| Names Windows can't hold, and names that differ only in capital letters | renamed for Windows (listed in the report) | kept exactly |
| Files over 4 GB on a FAT32 USB stick | can't be copied | stored in pieces, put back whole |
| Put back on a phone with FABS | yes | yes |
| Check without the phone | yes | yes |

FAT32 is a drive format common on USB sticks; it can't hold files over 4 GB. An archive isn't compressed, so it takes
about as much space as the files. Once an archive made from a backup is checked, FABS offers to delete that backup; it
never deletes it on its own.

### How do I open an archive without FABS?

With the free [7-Zip](https://www.7-zip.org): it opens every part on its own, so you can look at or extract the files
of any part. A file bigger than a part is stored in pieces (for example `video.mp4.fat-piece-01-of-02` and
`video.mp4.fat-piece-02-of-02`). To join them, extract every part into one folder, open Command Prompt in that folder,
and run the `copy /b` lines from "About this archive.txt" (in the archive's folder). That file has the lines for up to
five such files; if there are more, putting them back with FABS is easier.

To put files back on a phone, use FABS: it joins the pieces for you and uses the original names.

### Why parts, and which size?

Parts are easier to copy, burn and upload than one huge file, and each part opens on its own: if one part is lost or
damaged, only the files stored in it (including big files that have a piece in it) are affected. When you archive a
phone (**Archive an old phone (one file)…**), you choose:

- **Automatic (one file)** (the default). On a drive that can't hold files over 4 GB (FAT32, common on USB sticks), it
  is **Automatic (4 GB parts)** instead.
- **One file**: the tidiest, for a drive that can hold big files.
- **4 GB parts (USB sticks, DVDs)**: one part per 4.7 GB DVD.
- **25 GB parts (Blu-ray)**: one part per 25 GB Blu-ray disc.
- **Custom size…**: at least 256 MB. If you type a size a little over what a DVD holds, FABS warns you.

In a OneDrive folder, FABS suggests parts: they upload more reliably than one big file. Files bigger than a part are
stored in pieces, and FABS puts them back whole.

**Make an archive of this backup…** chooses by itself: one file, or 4 GB parts on a FAT32 drive.

### I have parts on several DVDs: how do I put files back?

Copy the parts from every disc into one folder on your PC. Their names don't matter: FABS recognizes each part by
what's inside it. Then choose **Open a backup or archive…** on the start screen, pick any one of the parts, and
choose **Put back on a phone…**. If parts are missing, FABS tells you which ones before anything is copied to the
phone, and offers **Find the missing parts…** (choose the folder or disc that holds them) or **Put back the others
now**. You can put the rest back later, once you find them. If the last part is the one that's missing, FABS may not be
able to name it: the report then says that not every part of the archive is here.

For DVDs, choose **4 GB parts (USB sticks, DVDs)** when you archive a phone. An archive made from a backup comes in
4 GB parts only when you save it on a FAT32 drive.

### Why do some names change when I open the archive in Windows?

The archive keeps every name exactly as it was on the phone. Windows doesn't allow some of them (for example names
with `:` or `?`), and it treats `Photo.jpg` and `photo.jpg` as the same name, so programs that open the archive on
Windows have to change them:

- 7-Zip replaces characters Windows doesn't allow with `_`. If 7-Zip asks whether to replace a file that's already
  there, usually two files on the phone had names that differ only in capital letters: choose to rename (7-Zip's
  **Auto Rename** button) to keep both. It can also be an earlier copy of a file that FABS copied again, for example
  because it changed while the archive was made. FABS always puts back the right copy.
- If you use the `tar` command that comes with Windows (typed in Command Prompt), it skips files whose names use
  another alphabet or an emoji (for example Japanese names on an English Windows). Use 7-Zip instead.
- Very rarely, the phone had a file and a folder with the same name at different times, and some programs can't
  extract both. "About this archive.txt" says when this happens; put those files back with FABS.

When FABS puts the archive back on a phone, it uses the original names wherever the phone allows them; any name that
has to change is listed in the report.

### How do I check an archive?

In FABS, choose **Check archive** on the archive in the start screen's list. It reads every part back, checks every
file in it, and tells you which files are affected if anything is damaged or missing. No phone is needed and nothing
is changed. This works for archives you added with **Open a backup or archive…** too, even parts copied back from
discs.

Without FABS, double-click "Check this archive.cmd" in the archive's folder: it compares every part with the list in
"SHA256SUMS.txt". It shows no progress while it reads a part (about 10 minutes per 100 GB on a USB 3 drive). On Linux,
`sha256sum -c SHA256SUMS.txt` in the archive's folder does the same.

### Can I password-protect an archive?

Not yet. An archive isn't encrypted, so anyone who has its files can open them. Until then, keep it on encrypted
storage, for example a USB drive encrypted with BitLocker To Go (Windows Home can open such a drive but can't encrypt
one), or another encrypted drive or cloud folder.

### Does it back up my WhatsApp chats?

It copies WhatsApp's photos, videos and its chat backup files, but WhatsApp encrypts those with a key it keeps itself.
To restore your chats, use WhatsApp's own backup. Turning on WhatsApp's end-to-end encrypted backup and keeping its
password or key safe gives you a backup you control.

### How do I remove FABS?

Uninstall it from Windows Settings › Apps. Your backups stay where they are.
