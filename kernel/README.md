prequisites :

sudo apt install libelf-dev
sudo apt install libssl-dev

install linux kernel source package:
# install kernel package
sudo apt install linux-source-4.19
# extract linux kernel source
tar xvf /usr/src/linux-source-4.19.tar.xz
cd linux-source-4.19
# patch it with rt patch
xzcat /usr/src/linux-patch-4.19-rt.patch.xz | patch -p1
# apply default config
xzcat /usr/src/linux-config-4.19/config.amd64_rt_amd64.xz > .config
# disable module signing support
disable module signing support
# build it
make -j8
# make a brake...

