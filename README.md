# RPI-FFMPEG OpenWRT feed

## Description

This feeds add a custom RPI variant of ffmpeg (https://github.com/jc-kynesim/rpi-ffmpeg/).


## Usage

This repository is intended to be layered on-top of an OpenWrt buildroot. If you do not have an OpenWrt buildroot installed, see the documentation at: [OpenWrt Buildroot – Installation](https://openwrt.org/docs/guide-developer/build-system/install-buildsystem) on the OpenWrt support site.

To install this feed and all its package definitions, run the following in your OpenWRT root-folder:
```
echo "src-git rpiffmpeg https://github.com/marcusfolkesson/rpi-ffmpeg-openwrt-feed.git" >> ./feeds.conf
./scripts/feeds update rpiffmpeg
./scripts/feeds install -a -p rpiffmpeg
```

In case of that the `ffmpeg` packages is already installed (part of the openwrt-packages repository), you have to uninstall it first:

```
./scripts/feeds uninstall ffmpeg
```

And then force install this feed:
```
./scripts/feeds install -f -p rpiffmpeg ffmpeg
```

# Patches

Please submit any patches against the rpi-ffmpeg--openwrt-feed repository via pull request.
