# mbed-os-example-serial-passthrough
This is a logical fork of os.mbed.com mercurial [Mbed-OS 2 example of SerialPassthrough](https://os.mbed.com/users/sarahmarshy/code/SerialPassthrough/) to use latest Mbed-OS.
This example is particularily useful when you need to pass through USB data from PC to Mbed compatible HW to UART serial component when, for example, the component needs firmware update.
You can follow instructions from [mbed-os-example-blinky](https://github.com/ARMmbed/mbed-os-example-blinky) and use this main.cpp.
For different component's UART TX/RX, you will need to change the [main.cpp code part](https://github.com/ARMmbed/mbed-os-example-serial-passthrough/blob/master/main.cpp#L8).
```
RawSerial  pc(USBTX, USBRX);
RawSerial  dev(D1, D0);
DigitalOut led1(LED1);
DigitalOut led4(LED4);
```
