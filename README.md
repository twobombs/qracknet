# QrackNet: Qrack, ProjectQ, SimulaQron on OpenCL

![](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)

- Qrack - Qbit OCL Hardware Emulation Stack > https://github.com/vm6502q/qrack
- ProjectQ - QC Interconnect, Qrack OCL fork > https://github.com/vm6502q/ProjectQ
- SimulaQron - Qbit Networking stack > https://github.com/SoftwareQuTech/SimulaQron
- PennyLane - ProjectQ plugin > https://github.com/XanaduAI/pennylane-pq
- Elastic Search/Lucene Interface for data interconnect

Build on top of CUDA-CLuster
- WebVNC, CUDA 11.0+ & OpenCL 1.2+ with NV, AMD & Intel HW support

Deploy single instances of QrackNet worker images by directly invoking docker worker images or deploy on your favorite orchestrator
- docker run -d --mount type=bind,source=/var/log/qrack,target=/var/log/qrack twobombs:supreme-cpu
- docker run --gpus all --device=/dev/dri:/dev/dri -d --mount type=bind,source=/var/log/qrack,target=/var/log/qrack twobombs:cosmos-gpu1

Deploy WebUI controller images by invoking docker controller image,or deploy in similar fashion on your favorite (k8s/k3d/k3s/docker compatible) orchestrator
- docker run --gpus all --privileged -p 6080:6080 -v /var/run/docker.sock:/var/run/docker.sock:ro --device=/dev/dri:/dev/dri -d twobombs/qracknet:controller

* use --gpus all for NVidia-Docker hosts, in addition --privileged will expose all devices, and thus all GPUs in the system, eg: Intel iGPUs

/me did none of the coding: just created this stack so that you don't need to - this is a work in progess

Code from the following awesome companies and initiatives are included in this container

![](https://user-images.githubusercontent.com/12692227/57654809-61c07f00-75d5-11e9-9005-38d60d8d4db4.png)

All rights belong to their respective owners.
