# FreeFileSync Setup

This guide explains how to configure **FreeFileSync** and **RealTimeSync** to automatically backup important user folders from one device to another over the local network.

## Prerequisites

- Install **FreeFileSync** on both Destination and Source Device.
- Ensure both Destination and Source Device are connected to the same network.

---

# Destination Device - Backup Server Setup

Destination Device will act as the backup destination.

## 1. Create a Backup Account

Create a local Windows user account:

- **Username:** `backupsvc`
- **Password:** *(Choose a strong password)*

This account will be used by the Source Device to access the shared backup folders.

---

## 2. Create Backup Folders

Create the following folder structure:

```
Backups
│
├── Desktop
├── Documents
├── Downloads
├── Music
├── Pictures
├── Videos
└── Versioning
```

## 3. Share Each Folder

> **Note:** Only the **Backups** folder needs to be shared. The subfolders (Desktop, Documents, Downloads, Pictures, Music, Videos, and Versioning) will inherit the shared access automatically and **do not need to be shared individually**.

1. Right-click the **Backups** folder.
2. Select **Properties**.
3. Open the **Sharing** tab.
4. Click **Advanced Sharing**.
5. Check **Share this folder**.
6. Set the **Share Name** to `Backups`.
7. Click **Permissions**.
8. Set **Everyone** to:
   - ✅ Read
   - ❌ Change
   - ❌ Full Control
9. Click **Apply**.
10. Click **OK**.

---

# Source Device - Client Setup

Source Device is the computer that will automatically back up its files.

---

## 1. Connect to Destination Device

Press:

```
Windows + R
```

Enter:

```
\\Destination Device Name
```

Example:

```
\\IT04
```

When prompted:

**Username**

```
backupsvc
```

**Password**

```
(Password created on Destination Device)
```

✔ Check:

```
Remember my credentials
```

This allow automatic reconnection for future backups.

---

## 2. Open FreeFileSync

Run **FreeFileSync** as **Administrator**.

---

## 3. Configure Folder Pairs

For each important folder, create one synchronization pair.

Example:

| Left Side (Source) | Right Side (Destination) |
|--------------------|--------------------------|
| Desktop | \\Destination Device\Desktop |
| Documents | \\Destination Device\Documents |
| Downloads | \\Destination Device\Downloads |
| Pictures | \\Destination Device\Pictures |
| Music | \\Destination Device\Music |
| Videos | \\Destination Device\Videos |

**Important**

The Source and Destination folders should match.

Example:

```
Desktop
      ↓
Desktop
```

Not:

```
Desktop
      ↓
Documents
```

---

## 4. Configure Synchronization Settings

Click the **Gear Icon** beside the **Synchronize** button.

### Synchronization

Select:

```
Mirror
```

Mirror mode creates an exact backup of the source folder.

---

### Delete and Overwrite

Choose:

```
Versioning
```

Then select the **Versioning** folder created on Destination Device.

Example:

```
\\Destination Device\Versioning
```

Versioning keeps previous copies of modified or deleted files instead of permanently deleting them.

Click **OK** to save the settings.

---

## 5. Perform the Initial Synchronization

Click:

```
Synchronize
```

Wait until the synchronization finishes successfully.

---

## 6. Save as a Batch Job

Click:

```
File
→ Save as Batch Job...
```

Enable:

- ✅ Run minimized
- ✅ Auto-close

Leave the remaining settings at their defaults.

Click:

```
Save As...
```

---

### Recommended Save Location

Create:

```
C:\Sync
```

Save the batch job (`.ffs_batch`) inside this folder.

Example:

```
C:\Sync\Backup.ffs_batch
```

---

# Configure RealTimeSync

Open **RealTimeSync**.

Drag the saved `.ffs_batch` file into the RealTimeSync window.

The configured folders will automatically load.

Click:

```
Start
```

Once everything is working:

```
File
→ Save As...
```

Save the `.ffs_real` file inside:

```
C:\Sync
```

Example:

```
C:\Sync\Backup.ffs_real
```

---

# Start RealTimeSync Automatically

Press:

```
Windows + R
```

Enter:

```
shell:startup
```

Press **Enter**.

Locate the `.ffs_real` file inside:

```
C:\Sync
```

Right-click it and select:

```
Show more options
→ Create shortcut
```

Copy the shortcut into the Startup folder.

Now, every time Source Device starts, RealTimeSync will automatically launch in the background and monitor the configured folders.

---

# Hide the FreeFileSync Shortcuts

To prevent users from easily opening the applications:

1. Select both:
   - FreeFileSync
   - RealTimeSync

2. Press:

```
Ctrl + X
```

3. Move them into:

```
C:\Sync
```

The Startup shortcut will continue to work even after moving the applications.

---

# Result

Once completed:

- Laptop 2 automatically starts RealTimeSync after login.
- File changes are monitored in real time.
- Files are mirrored to Laptop 1.
- Deleted or modified files are stored in the Versioning folder.
- Users do not need to manually start backups.

---

# Notes

- Both laptops must be connected to the same network.
- Laptop 1 must be powered on and accessible.
- Do not rename or move the shared folders after configuring FreeFileSync.
- Keep the `backupsvc` password secure.
- Periodically verify that backups are completing successfully.

## Version History

| Version | Date | Changes |
|--------|------|--------|
| 1.0 | 2026-07-01 | Initial version |