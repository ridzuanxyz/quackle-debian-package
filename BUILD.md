# Building Quackle Package

This repository contains Debian packaging files for Quackle.

## Prerequisites
- Ubuntu 22.04+ or Debian 11+
- Build tools: `sudo apt install build-essential devscripts debhelper`
- Qt5 development: `sudo apt install qtbase5-dev cmake`

## Build Process

1. Clone the original Quackle source:
```bash
git clone https://github.com/quackle/quackle.git
mv quackle quackle-1.0.4
cd quackle-1.0.4
```

2. Clone this packaging repository and copy the debian files:
```bash
cd ..
git clone https://github.com/yourusername/quackle-debian-package.git
cp -r quackle-debian-package/debian quackle-1.0.4/
cd quackle-1.0.4
```

3. Build the package:
```bash
debuild -i -us -uc -b
```

The .deb package will be created in the parent directory.
