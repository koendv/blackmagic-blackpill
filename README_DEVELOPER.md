This is how the binaries are built:

For WeAct stm32f411 black pill:
```
git clone https://github.com/kdv-temp/blackmagic/
cd blackmagic
patch -p1 < ../led.patch
make PROBE_HOST=f4discovery BLACKPILL=1 ENABLE_RTT=1
```
For stm32f4discovery:
```
git clone https://github.com/kdv-temp/blackmagic/
cd blackmagic
make PROBE_HOST=f4discovery ENABLE_RTT=1
```