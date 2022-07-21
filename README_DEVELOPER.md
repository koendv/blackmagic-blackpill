This the build recipe for binaries for WeAct stm32f411 black pill:

```
git clone https://github.com/koendv/blackmagic-blackpill
git clone https://github.com/blackmagic-debug/blackmagic
cd blackmagic
patch -p1 <  ../blackmagic-blackpill/blackpill.patch
```
The patch

- makes the LED blink if the probe is active
- support for the NRST pin
- support for stm32f401cc and stm32f411ce

For WeAct stm32f411 black pill with 512k flash and 96k ram:
```
make clean
make PROBE_HOST=blackpillv2 ENABLE_RTT=1
```

For a black pill with stm32f401cc with 256k flash and 64k ram:

```
make clean
make PROBE_HOST=blackpillv2 BLACKPILL_F401CC=1 ENABLE_RTT=1
```

For a black pill with stm32f411ce with 512k flash and 128k ram:

```
make clean
make PROBE_HOST=blackpillv2 BLACKPILL_F411CE=1 ENABLE_RTT=1
```

These three only differ in the amount of ram and flash.

