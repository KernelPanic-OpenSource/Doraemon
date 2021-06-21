# Doraemon Kernel
## Kernel Version
Linux:
```bash
4.4.205
```
## Compile
Add Dpkg Architecture
```bash
dpkg --add-architecture i386
```
Update repo:
```bash
sudo apt-get update
```
Install Packages:
```bash
sudo apt-get install -y git ccache automake flex lzop bison gperf build-essential zip curl zlib1g-dev zlib1g-dev:i386 g++-multilib python-networkx libxml2-utils bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev squashfs-tools pngcrush schedtool dpkg-dev liblz4-tool make optipng maven libssl-dev pwgen libswitch-perl policycoreutils minicom libxml-sax-base-perl libxml-simple-perl bc libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev libgl1-mesa-dev xsltproc unzip libssl-dev
```
ENV Setup:
```bash
export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=~/kernel/toolchain/aarch64-linux-android-4.9/bin/aarch64-linux-android-
export CROSS_COMPILE_ARM32=~/kernel/toolchain/arm-linux-androideabi-4.9/bin/arm-linux-androideabi-
```
start compile:
```bash
make O=out <defconfig>
```
```bash
make O=out -j$(nproc --all)
```
## Credit

