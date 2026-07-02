# FreeFileSync Tool Reference

## FreeFileSync

FreeFileSync is an open-source folder comparison and synchronization tool. It is used to copy, mirror, or synchronize files between two locations, such as local folders, network shares, or external drives.

**Used in this guide for:**
- Creating automatic backups
- Synchronizing user folders to a backup server

---

## RealTimeSync

RealTimeSync is a companion application included with FreeFileSync.

Unlike FreeFileSync, it does not copy files. Instead, it monitors one or more folders for changes and automatically launches a saved FreeFileSync batch job when a change is detected.

---

## Mirror Synchronization

Mirror is a one-way synchronization method.

Changes made in the source folder are replicated to the destination folder, making the destination an exact copy of the source.

---

## Versioning

Versioning preserves deleted or overwritten files by moving them to a designated versioning folder instead of permanently removing them.

This provides protection against accidental deletions and unwanted file changes.

---

## Batch Job (.ffs_batch)

A `.ffs_batch` file stores the synchronization configuration created in FreeFileSync.

It allows synchronization to run automatically without user interaction.

---

## RealTimeSync Configuration (.ffs_real)

A `.ffs_real` file stores the monitoring configuration used by RealTimeSync.

It contains:
- Folders to monitor
- Delay before synchronization
- Associated batch job

---

## Supported Locations

FreeFileSync can synchronize files between:

- Local folders
- Network shared folders
- External drives
- NAS devices
- FTP/SFTP servers
- Cloud storage (via mounted drives)

---

## Official Website

https://freefilesync.org/

---

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | 2026-07-02 | Initial version |