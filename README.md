# Quackle - Crossword Game AI Package

A custom-built Debian package of Quackle 1.0.4 for Ubuntu/Debian-based systems.

## Important Legal Notice

**This is a redistribution package only. No source code modifications were made.**

- **Original Software:** Quackle 1.0.4 from https://github.com/quackle/quackle
- **Original Authors:** Jason Katz-Brown, John O'Laughlin, John Fultz, Matt Liberty, and contributors
- **Original License:** GNU General Public License v2 or later (GPL-2+)
- **Package Maintainer:** Ridzuan Yusop (packaging only, no code changes)

This repository contains only Debian packaging files (`debian/` directory contents) and pre-compiled binary packages. The original Quackle source code remains unchanged and is available at the upstream repository.

## License Information

### Original Software License
Quackle is licensed under the GNU General Public License v2 or later (GPL-2+). The complete license text is available at:
- https://www.gnu.org/licenses/gpl-2.0.html
- https://www.gnu.org/licenses/gpl-3.0.html

### Packaging License
The Debian packaging files (debian/control, debian/rules, etc.) in this repository are also licensed under GPL-2+, maintaining compatibility with the original software license.

### Source Code Availability
As required by the GPL license:
- **Original source code:** Available at https://github.com/quackle/quackle
- **Packaging source:** Available in this repository's debian/ directory
- **No source code was modified** during the packaging process

## What is Quackle?

Quackle is a world-class crossword game artificial intelligence and analysis tool featuring:
- Advanced move generator and game simulator
- Support for multiple lexicons (CSW19, NWL18, TWL06, OSPS, etc.)
- Multi-language support (English, French, Greek, Korean, Turkish, and more)
- Detailed game analysis and strategy tools
- Custom Scrabble tile "Q" icon for desktop integration

## Download

### Binary Package
Download from [Releases](https://github.com/ridzuanxyz/quackle-debian-package/releases/latest): `quackle_1.0.4-3_amd64.deb`

### File Verification (Recommended)
Checksums are provided with each release for integrity verification:

```bash
# Verify SHA256 (recommended)
sha256sum -c CHECKSUMS.txt

# Or verify manually
sha256sum quackle_1.0.4-3_amd64.deb
```

## Installation

### Prerequisites
- Ubuntu 22.04+ / Debian 11+ / ZorinOS 17.3+ (amd64 architecture)
- Qt5 libraries (usually pre-installed)

### Install the Package

```bash
# Download from releases page, then:
sudo apt install ./quackle_1.0.4-3_amd64.deb
```

Alternative methods:
```bash
# Using dpkg
sudo dpkg -i quackle_1.0.4-3_amd64.deb
sudo apt-get install -f

# Using gdebi
sudo apt install gdebi-core
sudo gdebi quackle_1.0.4-3_amd64.deb
```

## Usage

```bash
# Launch application
quackle

# View manual
man quackle
```

Or find "Quackle" in your applications menu under "Games" with the Q tile icon.

## Building from Source

This package was built from the upstream source without modifications:

```bash
# Get original source
git clone https://github.com/quackle/quackle.git
cd quackle

# Build following upstream instructions
cd quacker
mkdir build && cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr ..
cmake --build .
```

For Debian packaging, see the `debian/` directory in this repository.

## Package Details

- **Version:** 1.0.4-3 (upstream 1.0.4, package revision 3)
- **Architecture:** amd64 (64-bit Intel/AMD)
- **Package Size:** ~22 MB
- **Installed Size:** ~87 MB
- **Dependencies:** Qt5 libraries, standard system libraries

## Files Included

The package installs files to standard Debian locations:
- **Executable:** `/usr/bin/quackle`
- **Data files:** `/usr/share/quackle/data/`
- **Documentation:** `/usr/share/man/man1/quackle.1`
- **Desktop integration:** `/usr/share/applications/quackle.desktop`
- **Icons:** `/usr/share/icons/hicolor/*/apps/quackle.png`

## Compatibility

Tested on:
- ✅ ZorinOS 17.3
- ✅ Ubuntu 22.04+ (Jammy and newer)
- ✅ Debian 11+ (Bullseye and newer)
- ✅ Linux Mint 21+

**Requirements:** 64-bit (amd64) architecture, Qt5 libraries

## Troubleshooting

### Missing Dependencies
```bash
sudo apt-get install -f
```

### Data File Issues
The package includes a wrapper script for proper data file location:
```bash
cd /usr/share/quackle
quackle-bin
```

### Version Pinning
Prevent automatic updates if needed:
```bash
sudo apt-mark hold quackle
```

## Uninstallation

```bash
sudo dpkg -r quackle
# or
sudo apt purge quackle
```

## Contributing

This is a packaging-only repository. For Quackle software issues:
- **Upstream issues:** https://github.com/quackle/quackle/issues
- **Packaging issues:** Open an issue in this repository

To contribute to Quackle itself, visit the upstream repository.

## Copyright and Legal

### Original Software Copyright
Copyright © 2004-2025 Quackle contributors (Jason Katz-Brown, John O'Laughlin, John Fultz, Matt Liberty, and others)

### Packaging Copyright  
Copyright © 2025 Ridzuan Yusop <ridzuanxyz@gmail.com>

### License Compliance
This package complies with GPL-2+ requirements:
- ✅ Original license preserved
- ✅ Source code availability maintained  
- ✅ License text included
- ✅ Copyright notices preserved
- ✅ No modifications to original source code

### Disclaimer
This package is provided "as is" without warranty. The package maintainer is not affiliated with the original Quackle developers and provides packaging services only.

---

**Package Maintainer:** Ridzuan Yusop  
**Build Date:** September 12, 2025  
**Upstream Source:** https://github.com/quackle/quackle
