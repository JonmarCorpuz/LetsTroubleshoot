# Error Overview

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Error Messages

```Bash
Calling: ['bash', '-c', 'zypper migration --no-verbose --non-interactive --gpg-auto-import-keys --no-selfupdate --auto-agree-with-licenses --allow-vendor-change --strict-errors-dist-migration --replacefiles --product SLES_SAP/15.1/x86_64 --root /system-root &>> /system-root/var/log/distro_migration.log']

Executing 'zypper --root /system-root --non-interactive --gpg-auto-import-keys  refresh'

Error retrieving metadata for 'SLE-Module-Adv-Systems-Management12-Pool':
Not ready to read within timeout.
Skipping repository 'SLE-Module-Adv-Systems-Management12-Pool' because of the above error.
Error retrieving metadata for 'SLE-Module-Adv-Systems-Management12-Updates':
Not ready to read within timeout.
Skipping repository 'SLE-Module-Adv-Systems-Management12-Updates' because of the above error.
Error retrieving metadata for 'SLE-Module-Containers12-Pool':
Not ready to read within timeout.
Skipping repository 'SLE-Module-Containers12-Pool' because of the above error.
Error retrieving metadata for 'SLE-Module-Containers12-Updates':
Not ready to read within timeout.
```

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Root Causes

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Troubleshooting Methods

![](https://github.com/JonmarCorpuz/LetsLearn/blob/main/Assets/Whitespace.png)

# Referenecs

* [SLES 12 SP5 Distribution Migration System (DMS) failed](https://www.suse.com/support/kb/doc/?id=000021338)
