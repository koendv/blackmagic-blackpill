This is how to build the binaries for WeAct stm32f411 black pill:
```
git clone https://github.com/kdv-temp/blackmagic/
cd blackmagic
patch -p1 < ../led.patch
make PROBE_HOST=f4discovery BLACKPILL=1 ENABLE_RTT=1
```
