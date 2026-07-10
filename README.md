# StemTube Desktop Friend — Release Assets

Backend payloads and installer for [StemTube Desktop Friend](https://github.com/benasterisk/stemtube-desktop-friend).

## Install

Download **StemTube_Desktop_Friend_1.0.1_x64-setup.exe** from the [latest release](https://github.com/benasterisk/stemtube-desktop-friend-releases/releases/latest) and run it. Nothing else to download by hand.

## How it works

On first launch, the Tauri shell detects your hardware and fetches the matching engine from this repository's release assets:

| Hardware | Assets | Size |
|---|---|---|
| NVIDIA GPU (CUDA) | `stemtube-backend-friend-gpu.zip.000` + `.001` (concatenated then extracted) | ~2.9 GB |
| CPU only | `stemtube-backend-friend-cpu.zip` | ~640 MB |

Each archive contains the full Python engine (source + virtual environment) with FFmpeg and the Deno JS runtime bundled. The shell also self-repairs the Python runtime on machines where the shipped venv is not relocatable.
