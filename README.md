# Smartphone (/spg/) Notes

Notes distilled from `/spg/` (Smartphone General, 4chan `/g/`-style,
"GrapheneOS Edition") — phone research/comparison tools, and de-googling /
custom-ROM / privacy tooling for Android. Complements this series'
[cyberpunk-privacy-notes](https://github.com/abdussamikhan1999-stack/cyberpunk-privacy-notes)
repo, which covers privacy more generally.

See [LINKS.md](LINKS.md) for the full raw link list.

## Researching a phone before buying

- **GSMArena / Kimovil / PhoneDB** — spec-search and comparison tools;
  GSMArena is the most established, PhoneDB is the more obscure/complete
  database for oddball or regional devices.
- **GSMArena / PhoneArena / NotebookCheck** — the standard review sites for
  actual hands-on impressions rather than raw spec sheets.
- **Frequency checkers** (frequencycheck.com, kimovil's checker,
  willmyphonework.net) — critical if you're importing a phone or switching
  carriers/countries: confirms the phone's radio bands actually match what
  your carrier uses, since a phone can look identical on spec sheets but
  silently drop to 3G/no-5G on the wrong network due to band mismatch.
- **Visual size comparison** (phonesized.com, PhoneArena's size tool) — for
  judging actual in-hand size/ergonomics before buying, since spec-sheet
  dimensions alone are hard to picture.

## De-googling / custom ROMs / privacy hardening

**Before flashing anything**: the thread's own warning is the single most
important line here — **carrier-variant phones often have locked
bootloaders** and can't run custom ROMs at all; check bootloader-unlock
status for your specific carrier variant before buying with a ROM in mind.

- **GrapheneOS** — the security-hardened de-Google Android fork most
  identified with this general (it's this thread's "edition"). Two
  official install paths: a **web installer** (browser + WebUSB, easiest,
  verifiable via boot key hash so you don't have to blindly trust their
  server) or **command-line/fastboot** (for people who want to understand
  every step rather than trust a script). Their own docs explicitly warn
  that third-party install guides are often outdated/wrong — use the
  official installer.
- **LineageOS** — the most widely-supported general-purpose custom ROM
  (huge device list), less security-hardened than GrapheneOS but broader
  device compatibility and a more "normal Android, just de-bloated"
  experience.
- **iodéOS** and **crDroid** — other custom ROM options with their own
  device support lists; worth comparing against GrapheneOS/LineageOS for
  your specific device if one isn't supported.
- **postmarketOS** — a genuinely different category: mainline **Linux**
  (not Android) on phones, aimed at device longevity/software freedom
  rather than privacy hardening specifically — much more DIY/immature, and
  for a different goal (running actual desktop Linux components — GNOME/
  KDE/Phosh — on a phone) than the Android-based ROMs above.
- **XDA Forums** — the long-standing general clearinghouse for
  device-specific rooting/ROM discussion; check here for anything
  device-specific the general links don't cover.

## Making a de-googled phone actually usable day-to-day

- **F-Droid** — the open-source Android app store/repository, the default
  app source once you've left Google Play behind.
- **Plexus** (plexus.techlore.tech) — crowdsourced compatibility database
  (11,000+ apps) rating how well *regular* (non-open-source) apps work
  without Google Play Services or with **microG** (an open-source
  reimplementation of just enough Play Services to satisfy apps that check
  for it). Check here before assuming your banking app etc. will work.
- **Universal Android Debloater (Next Generation)** — a cross-platform
  (Rust, GUI) desktop tool that strips unnecessary system apps from a
  **stock, non-rooted** ROM over ADB — useful if you're not ready to flash
  a full custom ROM but still want the bloatware gone. Community-maintained
  safe-to-remove package list, not a root exploit.
- **Blokada / NextDNS** — OS-wide ad/tracker blocking via VPN-profile or
  DNS-level filtering, working across all apps rather than per-browser.
- **gearjail.neocities.org** — a community-maintained index covering ROM
  flashing basics, a curated custom-ROM list with device-specific setup
  notes, Android privacy-hardening guides, firewall configuration, and a
  writeup specifically on **/e/OS** (another de-googled/privacy-focused
  Android distribution not otherwise mentioned in this thread).

## The joke link, explained

**trygalaxy.com** ("Try out a real OS on your iPhone") is actually
**Samsung's own official marketing tool** — a browser-based emulation of
Samsung's One UI that lets iPhone users try the Android/One UI experience
without buying a device. The general is using it as a jab at iOS, not
recommending it as privacy tooling — it's a genuine Samsung product demo,
included here for accuracy since it's easy to mistake for something else.
