---
layout: manpage
title: What's New
meta: 2.8.0
---

## 2.8.0

### Deprecation warnings

The following list of features have been deprecated and will *not* be available in Cobbler 3.0. Users depending on one of these features should stick to the 2.8.x (LTS) series. If you'd like to maintain one of these features in 3.x and beyond, then please reach out to the developers through GitHub or the mailinglist.

- MySQL backend
- CouchDB backend
- Monit support
- Platforms: s390/s390x and ia64
- Field names: subnet, bonding_master, bonding
- Func integration
- Koan LiveCD
- Koan LDAP configuration
- redhat_management (Spacewalk/Satellite)
- Remote kickstart files/tempaltes (other than on the Cobbler server)
- The concurrent use of ``parent`` and ``distro`` on subprofiles

### Feature improvements

- Integrated ``pyflakes`` into the build system and fixed all reported issues
- Integrated Travis CI into the build system (``make qa``)
- Allow https method in repo management (\#1587)
- Add support for Ubuntu 16.04
- Add support for the ``ppc64le`` architecture
- Backport gpxe mac search argument
- Added support for fixed DHCP IPs when using vlan over bond
- Add support for Django 1.7.x and 1.8.x

### Bugfixes

- Allow the use of relative paths when importing a distro (\#1613)
- Fix /etc/xinetd.d/rsync check (\#1651)
- Exit with a appropiate message when signature file can't be parsed
- Handle cases where virt-install respond to --version on stderr (Koan)