# Changelog

## 2.8.0 (2024-01-22)

### Features

- --debug option now does not remove the uac-data.tmp directory created in the destination directory. This is the location where temporary and debugging data is stored during execution.

### Artifacts

- files/applications/box_drive.yaml: Renamed to box.yaml.
- files/applications/box.yaml: Added collection support for Box log files [macos].
- files/applications/wget.yaml: Added collection support for wget hsts file. This file is used to store the HSTS cache for the wget utility [aix, esxi, freebsd, linux, macos, netbsd, openbsd, solaris] (by [firexfly](https://github.com/firexfly)).
- files/browsers/brave.yaml: Updated collection support for Flatpak version [linux].
- files/browsers/chrome.yaml: Updated collection support for Flatpak version [linux].
- files/browsers/edge.yaml: Updated collection support for Flatpak version [linux].
- files/browsers/opera.yaml: Updated collection support for Flatpak version [linux].
- files/browsers/vivaldi.yaml: Updated collection support for Flatpak version [linux].
- files/packages/pkg_contents.yaml: Added collection support for package table of contents files [openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- files/system/desktop.yaml: Added collection support for GUI shortcut files (.desktop) of users [freebsd, linux, netbsd, openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- files/system/etc.yaml: Added "master.passwd" and "spwd.db" to the exclude_name_pattern list as they contain the hashed passwords of local users [freebsd, netbsd, netscaler, openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- files/system/etc.yaml: Added exclusion for the group shadow files 'gshadow' and 'gshadow-'. Those files contain password hashes for groups [linux] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- files/system/xsession_errors.yaml: Updated collection support for OpenBSD systems [openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- live_response/network/ndp.yaml: Added collection support for kernel's IPv6 network neighbor cache [freebsd, netbsd, openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).
- live_response/network/nft.yaml: Added collection support for complete nftables ruleset [linux] (by [sanderu](https://github.com/sanderu)).
- live_response/network/ss.yaml: Updated collection support for processes listening on UDP ports/sockets [android, linux].
- live_response/vms/vmctl.yaml: Added collection support for information about running virtual machines on the OpenBSD using the native virtualization system [openbsd] (by [Herbert-Karl](https://github.com/Herbert-Karl)).

### Fixes

- Offline disk image mount point path was part of the file structure in [root] (by [maxspl](https://github.com/maxspl)).
- Collected data was not being properly archived by tar in AIX systems.

### Profiles

- profiles/offline.yaml: New 'offline' profile that can be used during offline collections (by [randomaccess3](https://github.com/randomaccess3)).

### Tools

- statx source code was moved to a dedicated repository at https://github.com/tclahr/statx
