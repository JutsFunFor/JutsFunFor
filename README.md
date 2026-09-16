# Embedded FPGA engineer

I bring boards up — mostly Xilinx / AMD silicon, UltraScale+ and RFSoC, and
usually starting from nothing but a schematic, because that's often the only
documentation that exists.

Everything on this profile is open.

---

## xczu27dr-rfsoc

### [Board support package for a Xilinx XCZU27DR RFSoC →](https://github.com/JutsFunFor/xczu27dr-rfsoc)

[![The XCZU27DR RFSoC board](https://raw.githubusercontent.com/JutsFunFor/xczu27dr-rfsoc/main/board.jpg)](https://github.com/JutsFunFor/xczu27dr-rfsoc)

This board ships with a schematic and not much else — no manual, no pin list, no
worked examples. So I wrote the manual. Every interface was brought up one at a
time, and each one has a script you can actually run plus a page explaining the
pins, the registers, and the things that cost you an afternoon if nobody warns
you first.

Seven interfaces, every result measured on real hardware:

| | |
|---|---|
| **DDR4** | 4 GB, 12 of 12 PHY training stages, patterns hold with no aliasing |
| **GTY transceivers** | 8 lanes at 10.3125 Gbps through QSFP28, PRBS-31, zero bit errors |
| **RF converters** | tones at 125 and 375 MHz played out and captured back at 4.0 GSPS |
| **Gigabit Ethernet** | GEM3 + RTL8211FD at 1000 Mb full duplex, frames verified by the host NIC |
| **Clocking** | all four GTY reference inputs counted in-fabric against a known reference |
| **JTAG and I/O** | chain and DAP memory access, LEDs, and the bank-voltage question settled from the schematic |

Verilog · Tcl · Vivado · Vitis

---

## Earlier open work

Embedded computer vision and video, mostly running on small hardware.

| | |
|---|---|
| [**coffee_detection**](https://github.com/JutsFunFor/coffee_detection) | Detecting coffee inside a cup on a Raspberry Pi, comparing classical image processing against a TensorFlow 2 detection model |
| [**yolov5-main**](https://github.com/JutsFunFor/yolov5-main) | A YOLOv5 coffee detector built out of that work |
| [**yolo**](https://github.com/JutsFunFor/yolo) | YOLO training and inference, containerised for running on a server |
| [**CLIP-classification-web-app**](https://github.com/JutsFunFor/CLIP-classification-web-app) | Fine-tuning OpenAI CLIP on a custom product-image dataset, served behind a web UI for fast prototyping |
| [**jsmpeg_streaming**](https://github.com/JutsFunFor/jsmpeg_streaming) | RTSP video streaming through NAT using JSMpeg, ffmpeg and a websocket relay |

---

<sub>Verilog · Tcl · Vivado / Vitis · Python · JavaScript · Docker</sub>
