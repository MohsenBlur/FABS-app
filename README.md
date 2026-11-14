# FABS: Fast Android Backup System

Back up everything on your Android phone to your Windows PC, check that every file arrived intact, and put it back
on a phone later. No accounts, no cloud.

**The first release is on its way.** When it's out, it will be on the [Releases page](https://github.com/MohsenBlur/FABS-app/releases).

## What it does

- **Copies every photo, video and file you can reach on the phone, SD card included,** to a folder on your PC, over a
  USB cable or Wi-Fi.
- **Checks every file.** Each copy is read back from your PC's drive and compared with the phone's, so you know the
  backup is complete, not just that it ran.
- **Updates only what changed.** The next backup of the same phone copies just the new and changed files. Files you
  delete from the phone stay in the backup, and earlier versions of changed files are kept too.
- **Puts a backup back on a phone**, the old one or a new one. It never deletes or overwrites anything on the phone:
  when the phone already has a different file with the same name, both are kept.
- **Checks a backup without the phone.** Double-click "Check this backup.cmd" in the backup folder at any time.
- **Archives an old phone into one file**, or a few parts that fit on USB sticks, DVDs or Blu-ray discs. Every file is
  checked and keeps its exact name, and FABS can put the archive back on a phone. A backup you already have can be
  turned into an archive too.

## What you need

- A Windows 10 (version 2004 or later) or Windows 11 PC, 64-bit.
- An Android phone with **USB debugging** turned on. FABS shows you how, step by step.
- Over Wi-Fi: Android 11 or newer. A USB cable works with older phones too, and is usually faster.

## What it can't do

- **Apps' own data** (chat history inside apps, game saves, settings) can't be copied without rooting the phone. Use
  each app's own backup for that. For WhatsApp chats, use WhatsApp's own backup.
- **Apps' own folders aren't put back yet** (for example WhatsApp's photos and voice notes on newer phones). They
  stay safe in the backup, and FABS lists them.
- **Photos that are only in the cloud** (for example in Google Photos and no longer on the phone) aren't on the phone,
  so FABS can't copy them.

## Privacy

FABS works between your phone and your PC only. It has no accounts and sends nothing to the internet: no analytics,
no crash reporting, no update checks. Your backups are ordinary files in a folder you choose.

Questions? See the [FAQ](FAQ.md).

## About this repository

This repo hosts the releases. The source is kept in a private repository; only the built app is published here.
