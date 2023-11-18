# Lisa-PROM

The Lisa CPU and 2/5 IO boards use a 256 x 8 bipolar PROM. The CPU card uses it as a video state machine as well as storing the unique serial number of the machine. The 2/5 IO card uses it as a floppy disk state machine. The 2/10 IO card does not use a PROM (it uses the Apple IWM chip instead).

Several types of PROMs can be used such as the 6309, 7118, 82S136, 74S471, 74LS471, or 28L22. But they are all difficult to program as you need access to select vintage EPROM programmers.

Arcade machines also use PROMs. The arcade community has recently switched to using EPROMs as a replacement and it has largely worked well.

![An oblique view photo of a Lisa CPU board with lots of IC's soldered in. A larger EPROM sits atop a smaller circuit board that is plugged into a socket below.](https://github.com/RolandJuno/Lisa-PROM/blob/main/Lisa%20PROM.jpg)

## Assembly

You'll need a 28 pin DIP socket for the EPROM on top of the board. For the bottom, I used 2 x 10 strips of turned (rounded) breakaway header pins. These pins won't stress the sockets on your board as much as machined (square) pins will. Observe the silkscreen for which side to solder the socket and pins on. Observe the notch for orientation.

I used a Winbond 27C512-45 EEPROMs for my boards because they're fast. A slower EPROM is likely to not work. Since you're only using 256 bytes of a 64 KByte device, you'll need to copy the concatenate the contents of the EPROM 256 times.
