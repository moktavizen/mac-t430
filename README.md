# MacT430

An attempt to make a T430 hackintosh.

## Hardware

Ref: https://dortania.github.io/OpenCore-Install-Guide/find-hardware.html#finding-hardware-using-linux

- CPU

```bash
model name	: Intel(R) Core(TM) i7-3632QM CPU @ 2.20GHz
```

- GPU

```bash
00:02.0 VGA compatible controller: Intel Corporation 3rd Gen Core processor Graphics Controller (rev 09)
```

- Chipset

```bash
Getting SMBIOS data from sysfs.
SMBIOS 2.7 present.

Handle 0x000E, DMI type 2, 15 bytes
Base Board Information
	Manufacturer: LENOVO
	Product Name: 2350B67
	Version: Not Defined
	Serial Number: 1ZLMB28W27V
	Asset Tag: Not Available
	Features:
		Board is a hosting board
		Board is replaceable
	Location In Chassis: Not Available
	Chassis Handle: 0x0000
	Type: Motherboard
	Contained Object Handles: 0

Handle 0x0029, DMI type 10, 6 bytes
On Board Device Information
	Type: Other
	Status: Disabled
	Description: IBM Embedded Security hardware
```

- Input

```bash
[    0.403376] input: Lid Switch as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0D:00/input/input0
[    0.403563] input: Sleep Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0E:00/input/input1
[    0.403908] input: Power Button as /devices/LNXSYSTM:00/LNXPWRBN:00/input/input2
[    1.865155] input: Hangsheng RK-R65 as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.0/0003:342D:E481.0001/input/input3
[    1.895129] input: AT Translated Set 2 keyboard as /devices/platform/i8042/serio0/input/input4
[    1.920751] input: ThinkPad Extra Buttons as /devices/platform/thinkpad_acpi/input/input5
[    1.951718] hid-generic 0003:342D:E481.0001: input,hidraw0: USB HID v1.11 Keyboard [Hangsheng RK-R65] on usb-0000:00:14.0-2/input0
[    1.952005] hid-generic 0003:342D:E481.0002: hiddev96,hidraw1: USB HID v1.11 Device [Hangsheng RK-R65] on usb-0000:00:14.0-2/input1
[    1.952309] input: Hangsheng RK-R65 System Control as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0003/input/input6
[    2.030666] input: Hangsheng RK-R65 Consumer Control as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0003/input/input7
[    2.030809] input: Hangsheng RK-R65 Keyboard as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0003/input/input8
[    2.451080] hid-generic 0003:342D:E481.0003: input,hidraw2: USB HID v1.11 Keyboard [Hangsheng RK-R65] on usb-0000:00:14.0-2/input2
[    2.451404] input: Logitech USB Receiver as /devices/pci0000:00/0000:00:1a.0/usb4/4-1/4-1.2/4-1.2:1.0/0003:046D:C52F.0004/input/input10
[    2.451670] hid-generic 0003:046D:C52F.0004: input,hidraw3: USB HID v1.11 Mouse [Logitech USB Receiver] on usb-0000:00:1a.0-1.2/input0
[    2.452135] input: Logitech USB Receiver Consumer Control as /devices/pci0000:00/0000:00:1a.0/usb4/4-1/4-1.2/4-1.2:1.1/0003:046D:C52F.0005/input/input11
[    2.502820] hid-generic 0003:046D:C52F.0005: input,hiddev97,hidraw4: USB HID v1.11 Device [Logitech USB Receiver] on usb-0000:00:1a.0-1.2/input1
[    2.530248] logitech-djreceiver 0003:046D:C52F.0004: hidraw3: USB HID v1.11 Mouse [Logitech USB Receiver] on usb-0000:00:1a.0-1.2/input0
[    2.536202] input: Video Bus as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0A08:00/LNXVIDEO:00/input/input14
[    2.609700] logitech-djreceiver 0003:046D:C52F.0005: hiddev97,hidraw4: USB HID v1.11 Device [Logitech USB Receiver] on usb-0000:00:1a.0-1.2/input1
[    2.663113] input: Logitech Wireless Mouse PID:4057 Mouse as /devices/pci0000:00/0000:00:1a.0/usb4/4-1/4-1.2/4-1.2:1.1/0003:046D:C52F.0005/0003:046D:4057.0006/input/input15
[    2.663412] input: Logitech Wireless Mouse PID:4057 Consumer Control as /devices/pci0000:00/0000:00:1a.0/usb4/4-1/4-1.2/4-1.2:1.1/0003:046D:C52F.0005/0003:046D:4057.0006/input/input16
[    2.663625] hid-generic 0003:046D:4057.0006: input,hidraw5: USB HID v1.11 Mouse [Logitech Wireless Mouse PID:4057] on usb-0000:00:1a.0-1.2/input1:1
[    2.718313] input: Logitech B330/M330/M331 as /devices/pci0000:00/0000:00:1a.0/usb4/4-1/4-1.2/4-1.2:1.1/0003:046D:C52F.0005/0003:046D:4057.0006/input/input20
[    2.718495] logitech-hidpp-device 0003:046D:4057.0006: input,hidraw5: USB HID v1.11 Mouse [Logitech B330/M330/M331] on usb-0000:00:1a.0-1.2/input1:1
[    4.073145] input: PC Speaker as /devices/platform/pcspkr/input/input22
[    4.218968] snd_hda_codec_realtek hdaudioC0D0:    inputs:
[    4.302621] input: HDA Intel PCH Mic as /devices/pci0000:00/0000:00:1b.0/sound/card0/input23
[    4.302690] input: HDA Intel PCH Dock Mic as /devices/pci0000:00/0000:00:1b.0/sound/card0/input24
[    4.302748] input: HDA Intel PCH Headphone as /devices/pci0000:00/0000:00:1b.0/sound/card0/input25
[    4.302807] input: HDA Intel PCH Dock Headphone as /devices/pci0000:00/0000:00:1b.0/sound/card0/input26
[    4.302880] input: HDA Intel PCH HDMI/DP,pcm=3 as /devices/pci0000:00/0000:00:1b.0/sound/card0/input27
[    4.302936] input: HDA Intel PCH HDMI/DP,pcm=7 as /devices/pci0000:00/0000:00:1b.0/sound/card0/input28
[    4.302998] input: HDA Intel PCH HDMI/DP,pcm=8 as /devices/pci0000:00/0000:00:1b.0/sound/card0/input29
[    4.798082] psmouse serio1: synaptics: serio: Synaptics pass-through port at isa0060/serio1/input0
[    4.838226] input: SynPS/2 Synaptics TouchPad as /devices/platform/i8042/serio1/input/input21
[    5.681531] input: TPPS/2 IBM TrackPoint as /devices/platform/i8042/serio1/serio2/input/input30
[   52.799419] input: Hangsheng RK-R65 as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.0/0003:342D:E481.0007/input/input31
[   52.886747] hid-generic 0003:342D:E481.0007: input,hidraw0: USB HID v1.11 Keyboard [Hangsheng RK-R65] on usb-0000:00:14.0-2/input0
[   52.891488] hid-generic 0003:342D:E481.0008: hiddev96,hidraw1: USB HID v1.11 Device [Hangsheng RK-R65] on usb-0000:00:14.0-2/input1
[   52.893724] input: Hangsheng RK-R65 System Control as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0009/input/input32
[   52.944711] input: Hangsheng RK-R65 Consumer Control as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0009/input/input33
[   52.945073] input: Hangsheng RK-R65 Keyboard as /devices/pci0000:00/0000:00:14.0/usb1/1-2/1-2:1.2/0003:342D:E481.0009/input/input34
[   52.981973] hid-generic 0003:342D:E481.0009: input,hidraw2: USB HID v1.11 Keyboard [Hangsheng RK-R65] on usb-0000:00:14.0-2/input2
```

- Audio

```bash
**** List of PLAYBACK Hardware Devices ****
card 0: PCH [HDA Intel PCH], device 0: ALC3202 Analog [ALC3202 Analog]
  Subdevices: 1/1
  Subdevice #0: subdevice #0
card 0: PCH [HDA Intel PCH], device 3: HDMI 0 [HDMI 0]
  Subdevices: 1/1
  Subdevice #0: subdevice #0
card 0: PCH [HDA Intel PCH], device 7: HDMI 1 [HDMI 1]
  Subdevices: 1/1
  Subdevice #0: subdevice #0
card 0: PCH [HDA Intel PCH], device 8: HDMI 2 [HDMI 2]
  Subdevices: 1/1
  Subdevice #0: subdevice #0
```

- Network

```bash
  *-network
       description: Ethernet interface
       product: 82579LM Gigabit Network Connection (Lewisville)
       vendor: Intel Corporation
       physical id: 19
       bus info: pci@0000:00:19.0
       logical name: enp0s25
       version: 04
       serial: 00:21:cc:cd:c6:26
       size: 100Mbit/s
       capacity: 1Gbit/s
       width: 32 bits
       clock: 33MHz
       capabilities: pm msi bus_master cap_list ethernet physical tp 10bt 10bt-fd 100bt 100bt-fd 1000bt-fd autonegotiation
       configuration: autonegotiation=on broadcast=yes driver=e1000e driverversion=6.13.8-arch1-1 duplex=full firmware=0.13-3 ip=192.168.1.7 latency=0 link=yes multicast=yes port=twisted pair speed=100Mbit/s
       resources: irq:28 memory:f1500000-f151ffff memory:f153b000-f153bfff ioport:5080(size=32)
  *-network
       description: Wireless interface
       product: Centrino Advanced-N 6205 [Taylor Peak]
       vendor: Intel Corporation
       physical id: 0
       bus info: pci@0000:03:00.0
       logical name: wlp3s0
       version: 34
       serial: 92:0e:13:4b:22:07
       width: 64 bits
       clock: 33MHz
       capabilities: pm msi pciexpress bus_master cap_list ethernet physical wireless
       configuration: broadcast=yes driver=iwlwifi driverversion=6.13.8-arch1-1 firmware=18.168.6.1 6000g2a-6.ucode latency=0 link=no multicast=yes wireless=IEEE 802.11
       resources: irq:29 memory:f0c00000-f0c01fff
```

- Drive

```bash
  *-sata
       description: SATA controller
       product: 7 Series Chipset Family 6-port SATA Controller [AHCI mode]
       vendor: Intel Corporation
       physical id: 1f.2
       bus info: pci@0000:00:1f.2
       version: 04
       width: 32 bits
       clock: 66MHz
       capabilities: sata msi pm ahci_1.0 bus_master cap_list
       configuration: driver=ahci latency=0
       resources: irq:24 ioport:50a8(size=8) ioport:50bc(size=4) ioport:50a0(size=8) ioport:50b8(size=4) ioport:5060(size=32) memory:f1538000-f15387ff
```

These EFI's doesn't include the macOS dmg file, so it needs to be
[downloaded](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/linux-install.html#downloading-macos) first.

- The Ventura EFI is based on QuanticalityIsHere's [EFI](https://github.com/QuanticalityIsHere/lenovo-t430-efi).
