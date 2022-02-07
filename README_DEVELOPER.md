This the build recipe for binaries for WeAct stm32f411 black pill:

```
git clone https://github.com/blackmagic-debug/blackmagic
git clone https://github.com/koendv/blackmagic-blackpill
wget -O rtt.patch https://github.com/blackmagic-debug/blackmagic/commit/c3c4ad99a6407024cae6de59a83c8a30fd9748e3.patch
cd blackmagic
patch -p1 < ../blackmagic-blackpill/led.patch
patch -p1 < ../blackmagic-blackpill/srst.patch
patch -p1 < ../rtt.patch
make PROBE_HOST=f4discovery BLACKPILL=1 ENABLE_RTT=1
```

For the firmware with added experimental risc-v support:

```
git clone -b ruabmbua https://github.com/UweBonnes/blackmagic
git clone https://github.com/koendv/blackmagic-blackpill
wget -O rtt.patch https://github.com/blackmagic-debug/blackmagic/commit/c3c4ad99a6407024cae6de59a83c8a30fd9748e3.patch
cd blackmagic
patch -p1 < ../blackmagic-blackpill/led.patch
patch -p1 < ../blackmagic-blackpill/srst.patch
patch -p1 < ../rtt.patch
make PROBE_HOST=f4discovery BLACKPILL=1 ENABLE_RTT=1
```
