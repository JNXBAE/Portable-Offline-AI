# Portable Offline AI – Setup Guide

This guide explains how to configure and run **Qwen2.5-1.5B-Instruct** locally using KoboldCpp directly from a USB flash drive.

The setup is designed for Windows computers and supports offline text generation after the required files have been downloaded.

---

## 1. Project Requirements

| Component | Specification |
|---|---|
| Operating System | Windows 10 / 11 (64-bit) |
| AI Model | Qwen2.5-1.5B-Instruct |
| Model Format | GGUF |
| Quantization | Q4_K_M |
| Model Size | Approximately 986 MB |
| Runtime | KoboldCpp |
| Runtime Version | v1.123.1 |
| Runtime Executable | koboldcpp-nocuda.exe |
| Processing | CPU / Compatible Vulkan GPU |
| Internet | Required for initial downloads only |

**Recommended:** A USB 3.0 or faster flash drive and sufficient available system RAM.

## 2. Download Required Components

### A. Download the Qwen Model

Model repository:

https://huggingface.co/bartowski/Qwen2.5-1.5B-Instruct-GGUF

Download:

`Qwen2.5-1.5B-Instruct-Q4_K_M.gguf`

Direct download:

https://huggingface.co/bartowski/Qwen2.5-1.5B-Instruct-GGUF/resolve/main/Qwen2.5-1.5B-Instruct-Q4_K_M.gguf

### B. Download KoboldCpp

Official GitHub releases:

https://github.com/LostRuins/koboldcpp/releases

For this project, the selected runtime is:

`koboldcpp-nocuda.exe`

The No-CUDA build supports CPU processing and Vulkan-compatible GPU processing.

---

## 3. USB Directory Structure

Organize the downloaded files as follows:

```text
Portable-Offline-AI/
│
├── AI_Engine/
│   └── koboldcpp-nocuda.exe
│
├── Models/
│   └── Qwen2.5-1.5B-Instruct-Q4_K_M.gguf
│
├── Config/
│
└── README.txt
```

The folder names are organizational choices. You can customize them according to your requirements.

---

## 4. Configure KoboldCpp

1. Connect your USB flash drive to your computer.
2. Open the `AI_Engine` folder.
3. Double-click `koboldcpp-nocuda.exe`.
4. The KoboldCpp configuration window will appear.
5. Browse and select the Qwen GGUF model from the `Models` folder.

### Recommended Initial Configuration

| Setting | Recommended Value |
|---|---|
| Model | Qwen2.5-1.5B-Instruct-Q4_K_M.gguf |
| Backend | Use CPU |
| GPU Layers | 0 for CPU-only |
| Context Size | 4096 |
| CPU Threads | Start with 4, then benchmark |
| Port | 5001 |

These are starting settings, not universal performance guarantees. Adjust them according to the host computer.

**Note:** The No-CUDA executable does not support CUDA. It can still support Vulkan GPU acceleration.

---

## 5. Start the AI Model

After selecting the model and configuring the settings:

1. Click the Launch button.
2. Wait for the model to load into system memory.
3. Keep the KoboldCpp terminal window open.
4. Once the server starts, open your web browser.
5. Visit:

http://localhost:5001

The local KoboldCpp interface should now be available.

---

## 6. Offline Functionality

After downloading the model and runtime, the system can generate text without an internet connection.

### Offline Capabilities

- AI text generation
- Question answering
- General writing assistance
- Summarization
- Basic coding assistance
- Conversational interaction

The quality of responses depends on the model's capabilities and the prompts provided.

No cloud-based AI API is required for local inference.

---

## 7. Portability

The project is designed to be carried on a USB flash drive.

To use it on another supported Windows computer:

1. Connect the USB flash drive.
2. Open the project directory.
3. Start KoboldCpp.
4. Select the Qwen model.
5. Configure the available processing resources.
6. Launch the local server.
7. Open the local browser interface.

**Important:** KoboldCpp still uses the host computer's CPU, RAM and optionally GPU. The USB stores the application and model; it does not provide the processing power.

Portability does not guarantee compatibility with every computer. Performance depends on the host hardware and operating system.

---

## 8. Troubleshooting

| Problem | Suggested Solution |
|---|---|
| Model not loading | Verify the GGUF file and its location |
| Out of memory | Close unnecessary applications or reduce context size |
| Slow generation | Check backend selection and CPU utilization |
| Browser not opening | Visit http://localhost:5001 manually |
| Port already in use | Select another available port |
| Application crashes | Check the terminal error and hardware compatibility |
| USB disconnects | Reconnect the drive and verify file integrity |

Keep the terminal window open when troubleshooting because KoboldCpp reports loading and runtime errors there.

---

## 9. Privacy and Security

- Model inference happens locally on the host computer.
- No external AI API is required for generation.
- Avoid exposing the local server to public networks.
- Use trusted downloads from official project sources.
- Do not disconnect the USB while the application is accessing its files.

---

## 10. Future Development

Planned improvements:

- [ ] One-click portable AI launcher
- [ ] Custom JNX AI chat interface
- [ ] Conversation history
- [ ] Local conversation memory
- [ ] PDF and document analysis
- [ ] Support for additional GGUF models
- [ ] Improved hardware detection
- [ ] Portable configuration management

---

## 11. Credits and References

**Qwen2.5**

https://github.com/QwenLM/Qwen2.5

**Hugging Face Model Repository**

https://huggingface.co/bartowski/Qwen2.5-1.5B-Instruct-GGUF

**KoboldCpp**

https://github.com/LostRuins/koboldcpp

**KoboldCpp Documentation**

https://koboldcpp.net/docs/

---

**Project:** Portable Offline AI  
**Developer:** JNXBAE  
**Repository:** https://github.com/JNXBAE/Portable-Offline-AI

*An experimental project exploring portable, private and locally powered artificial intelligence.*