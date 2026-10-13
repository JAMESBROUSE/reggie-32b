# REGGIE-V6 (32B): Sovereign Industrial Cybersecurity & Physical Telemetry Engine

[![Hugging Face GGUF](https://img.shields.io/badge/HuggingFace-GGUF%20Quantized-yellow)](https://huggingface.co/Bigchilli1978/reggie-v6-32b-GGUF)
[![Base Model](https://img.shields.io/badge/Base%20Model-Qwen2.5--Coder--32B--Instruct-blue)](https://huggingface.co/Qwen/Qwen2.5-Coder-32B-Instruct)
[![White Paper](https://img.shields.io/badge/White%20Paper-brousegroup.ca-blue)](https://brousegroup.ca/reggie.html)
[![License](https://img.shields.io/badge/License-Apache%202.0-green.svg)](LICENSE)

**REGGIE-V6 (32B)** is an autonomous cybersecurity, industrial infrastructure, and hardware-sentinel LLM. Built on top of `Qwen/Qwen2.5-Coder-32B-Instruct`, it was fine-tuned with custom low-rank adapters (LoRA) and quantized to 4-bit medium (`Q4_K_M`) via a sovereign local streaming pipeline in C++.

* **Full Architecture White Paper & Journey:** [https://brousegroup.ca/reggie.html](https://brousegroup.ca/reggie.html)
* **Raw White Paper:** [`WHITE_PAPER.md`](WHITE_PAPER.md)
* **Pre-quantized 19.9 GB GGUF:** [Bigchilli1978/reggie-v6-32b-GGUF](https://huggingface.co/Bigchilli1978/reggie-v6-32b-GGUF)
* **LoRA Adapters:** [Bigchilli1978/reggie-v6-32b](https://huggingface.co/Bigchilli1978/reggie-v6-32b)

---

## 🚀 Quickstart: 1-Click Run with Ollama

Run REGGIE-V6-32B directly on local workstation hardware (~20 GB VRAM or VRAM + system RAM offloading):

```bash
ollama run hf.co/Bigchilli1978/reggie-v6-32b-GGUF:reggie-v6-32b-Q4_K_M.gguf
```

Or clone this repository, download `reggie-v6-32b-Q4_K_M.gguf`, and run:

```bash
ollama create reggie -f Modelfile
ollama run reggie
```

---

## 🏗️ System Architecture & Physical Telemetry

Unlike traditional software-only coding models, REGGIE-V6-32B integrates:
1. **Physical Hardware Sentinels**: Tethers directly to ESP32 microcontrollers over UART/WebSockets, parsing raw 802.11 management frames, deauthentication flood spikes, beacon anomalies, and physical environmental metrics.
2. **Deterministic SCADA Reasoning**: Evaluates Modbus, DNP3, and IEC-60870 industrial network packet captures against zero-trust baselines.
3. **C++ Streaming Tensor Fusion**: Overcomes the 65 GB memory wall of merging 32B models in FP16 on consumer hardware by streaming low-rank delta matrices directly into quantized tensor chunks without CPU memory thrashing.

---

## 📊 Benchmark Highlights

| Task / Domain | Baseline Qwen2.5-Coder-32B | REGGIE-V6 (32B) | Delta |
| :--- | :---: | :---: | :---: |
| **802.11 Deauth / Frame Anomaly Triaging** | 61.4% | **94.8%** | **+33.4%** |
| **SCADA / Modbus Packet Parsing** | 72.0% | **91.5%** | **+19.5%** |
| **ESP32 Serial JSON Log Triage** | 68.2% | **96.2%** | **+28.0%** |
| **Standard Python / C++ Exploit Remediation**| 88.5% | **89.1%** | **+0.6%** |

---

## 📜 License
Apache 2.0. Base model weights subject to the Qwen License Agreement.
