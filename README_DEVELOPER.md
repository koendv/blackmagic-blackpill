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
- runs on STM32F401CCU6, STM32F401CEU6 and STM32F411CEU6.

```
make clean
make PROBE_HOST=blackpillv2 ENABLE_RTT=1
```




