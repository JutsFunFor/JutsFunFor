## FPGA board bring-up and embedded vision

I build board support packages for AMD/Xilinx FPGAs, with runnable tests, pin maps, and measurements from real hardware.

### FPGA board support

**[XCZU27DR RFSoC](https://github.com/JutsFunFor/xczu27dr-rfsoc)** · MIT

A board support package with Vivado Tcl scripts for JTAG, DDR4, QSFP28, Gigabit Ethernet, clocking, and RF converter loopback. On the board, all 12 DDR4 PHY training stages passed, all eight GTY lanes ran at 10.3125 Gbps with zero observed PRBS-31 bit errors, and the RF loopback recovered 125 MHz and 375 MHz tones.

[Measured results](https://github.com/JutsFunFor/xczu27dr-rfsoc#what-was-actually-measured) · [Setup and first test](https://github.com/JutsFunFor/xczu27dr-rfsoc#getting-started) · [Board photo](https://github.com/JutsFunFor/xczu27dr-rfsoc/blob/main/board.jpg)

**[ALIVU13P accelerator card](https://github.com/JutsFunFor/alivu13p)** · Apache-2.0

Board bring-up for an AMD/Xilinx XCVU13P card, with Vivado designs and Linux host-side tools. Verified PCIe Gen3 enumeration, DMA to BRAM and UltraRAM, and read/write tests across all four DDR4 channels. The status table shows which interfaces have been tested on hardware and which have only been built.

[Interface status](https://github.com/JutsFunFor/alivu13p/blob/main/STATUS.md) · [Hardware validation log](https://github.com/JutsFunFor/alivu13p/blob/main/docs/validation-2026-09-17.md)

### Earlier computer vision and video projects

- [CLIP classification web app](https://github.com/JutsFunFor/CLIP-classification-web-app) fine-tunes CLIP on a custom product-image dataset and serves it through a web UI.
- [Coffee detection on Raspberry Pi](https://github.com/JutsFunFor/coffee_detection) compares classical vision with a TensorFlow 2 model. [YOLOv5 coffee detector](https://github.com/JutsFunFor/yolov5-main) continues that work.
- [JSMpeg streaming](https://github.com/JutsFunFor/jsmpeg_streaming) streams RTSP video to a browser with FFmpeg and a WebSocket relay.
- [YOLO training and inference](https://github.com/JutsFunFor/yolo) packages both workflows in Docker.
