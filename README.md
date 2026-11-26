# FPGA board bring-up and embedded vision

I build and test FPGA board support on the bench. Below are the two boards I work on, what I measured, and the test records. My camera projects began with a question from a coffee machine: is there coffee in the cup?

| [XCZU27DR RFSoC](https://github.com/JutsFunFor/xczu27dr-rfsoc) | [ALIVU13P accelerator](https://github.com/JutsFunFor/alivu13p) |
| --- | --- |
| [![XCZU27DR board on the bench with loopback cables attached](https://raw.githubusercontent.com/JutsFunFor/xczu27dr-rfsoc/main/board.jpg)](https://github.com/JutsFunFor/xczu27dr-rfsoc) | [![ALIVU13P Virtex UltraScale+ accelerator card](https://raw.githubusercontent.com/JutsFunFor/alivu13p/main/board.png)](https://github.com/JutsFunFor/alivu13p) |
| Eight GTY lanes tested at 10.3125 Gbps. RF loopback recovered tones at 125 and 375 MHz. [See the measurements](https://github.com/JutsFunFor/xczu27dr-rfsoc#what-was-actually-measured). | PCIe DMA to BRAM and UltraRAM, plus read/write tests on all four DDR4 channels. [Read the bench log](https://github.com/JutsFunFor/alivu13p/blob/main/docs/validation-2026-09-17.md). |

## From camera to inference

- [CLIP classification web app](https://github.com/JutsFunFor/CLIP-classification-web-app) fine-tunes CLIP on a custom product-image dataset and serves it through a web UI.
- [Coffee detection on Raspberry Pi](https://github.com/JutsFunFor/coffee_detection) compares classical vision with a TensorFlow 2 model. [YOLOv5 coffee detector](https://github.com/JutsFunFor/yolov5-main) continues that work.
- [JSMpeg streaming](https://github.com/JutsFunFor/jsmpeg_streaming) streams RTSP video to a browser with FFmpeg and a WebSocket relay.
- [YOLO training and inference](https://github.com/JutsFunFor/yolo) packages both workflows in Docker.
