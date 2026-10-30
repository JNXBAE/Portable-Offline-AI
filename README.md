# 🚀 JNX Portable Offline AI

### Your Personal AI Assistant. Anywhere. Anytime. Even Without Internet.

A portable, locally running AI text-generation system powered by **Qwen2.5-1.5B-Instruct GGUF** and **KoboldCpp**.

JNX Portable Offline AI is an experimental project that explores running Large Language Models (LLMs) directly from a USB flash drive, allowing users to generate AI responses locally without depending on cloud-based AI services.

---

## 🌟 Project Overview

The main objective is to build a lightweight and portable AI environment that can be carried on a USB drive and used across compatible Windows computers.

The project uses a quantized Qwen2.5 language model in GGUF format and KoboldCpp as its local inference engine.

**Core concept:**

- Portable AI environment.
- Local AI text generation.
- CPU-based processing.
- No cloud API dependency.
- Offline operation after initial downloads.

## 🧠 Technology Stack

| Component | Technology |
|---|---|
| AI Model | Qwen2.5-1.5B-Instruct |
| Model Format | GGUF |
| Quantization | Q4_K_M |
| Model Size | Approximately 986 MB |
| Inference Engine | KoboldCpp |
| Runtime | koboldcpp-nocuda.exe |
| Processing | CPU / Supported Vulkan GPU |
| Platform | Windows 10 / 11 |

## ✨ Key Features

- **Portable AI:** Store the model and runtime on a USB flash drive.
- **Offline Generation:** Generate text without an internet connection after downloading the components.
- **Local Processing:** Run AI inference using the host computer's processing resources.
- **Lightweight Model:** Uses a quantized 1.5B parameter Qwen model.
- **Configurable Runtime:** Select models and adjust processing settings through KoboldCpp.
- **Privacy Focused:** No external AI API is required for local inference.

## 📦 Required Components

### 1. Qwen2.5-1.5B-Instruct

The language model responsible for generating AI responses.

- Model: Qwen2.5-1.5B-Instruct-Q4_K_M.gguf
- Format: GGUF
- Quantization: Q4_K_M
- Size: Approximately 986 MB

**Download:** [Hugging Face – Qwen2.5 GGUF](https://huggingface.co/bartowski/Qwen2.5-1.5B-Instruct-GGUF)

### 2. KoboldCpp

A lightweight local inference engine used to load and run the GGUF model.

- Runtime: koboldcpp-nocuda.exe
- Backend: CPU-compatible build
- Interface: Local browser-based interface

**Download:** [KoboldCpp – GitHub Releases](https://github.com/LostRuins/koboldcpp/releases)

## 🗂️ Project Structure

```text
Portable-Offline-AI/
│
├── README.md
├── .gitignore
├── LICENSE
│
├── docs/
│   └── setup-guide.md
│
└── screenshots/
    ├── 1.png
    ├── 2.png
    ├── 3.png
    └── 4.png
```

The model and executable are downloaded separately and stored on the USB drive rather than committed to this repository.

## ⚙️ Installation and Setup

### Step 1 – Download the model

Download the Qwen2.5 GGUF model from Hugging Face.

### Step 2 – Download KoboldCpp

Download the `koboldcpp-nocuda.exe` runtime from the official GitHub releases.

### Step 3 – Prepare your USB drive

Create folders for the runtime and model, then place the downloaded files in their respective folders.

### Step 4 – Configure the model

1. Open KoboldCpp.
2. Select the Qwen GGUF model.
3. Configure the CPU processing options.
4. Set the context size and other runtime parameters.
5. Launch the model.

### Step 5 – Start generating text

Open your browser and access the local KoboldCpp interface.

Default example:

```text
http://localhost:5001
```

For detailed instructions, see [Setup Guide](docs/setup-guide.md).

## 💻 System Requirements

| Requirement | Recommendation |
|---|---|
| Operating System | Windows 10 / 11 64-bit |
| RAM | 8 GB or more |
| Processor | Modern multi-core CPU |
| Storage | USB drive with sufficient free space |
| USB Interface | USB 3.0 or faster recommended |
| Internet | Initial downloads only |

Actual performance depends on the host computer, available memory, backend and USB transfer speed.

## 🔒 Privacy and Offline Operation

JNX Portable Offline AI is designed for local inference.

- No cloud AI service is needed for text generation.
- No API key is required.
- The model runs using the host computer's resources.
- Internet connectivity is not required once all components are downloaded.

Keep the local server restricted to trusted local access.

## 🖼️ Screenshots

Screenshots of the KoboldCpp configuration and project setup are available in the [`screenshots/`](screenshots/) directory.

## 🛠️ Future Development Roadmap

- [ ] One-click portable AI launcher.
- [ ] Custom JNX AI chat interface.
- [ ] Local conversation history.
- [ ] Persistent AI memory.
- [ ] PDF and document analysis.
- [ ] Support for multiple GGUF models.
- [ ] Automatic hardware detection.
- [ ] Improved portable configuration.
- [ ] Additional offline AI capabilities.

## 🤝 Contributions

Suggestions, feedback and improvements are welcome.

If you find an issue or have an idea for improving the project, feel free to open a GitHub issue.

## 🙏 Credits and Acknowledgements

- [Qwen](https://github.com/QwenLM/Qwen2.5) – Language model.
- [Hugging Face](https://huggingface.co/) – Model hosting.
- [KoboldCpp](https://github.com/LostRuins/koboldcpp) – Local inference engine.

This is an independent community project and is not officially affiliated with Alibaba, Qwen or KoboldCpp.

## 👨‍💻 Developer

**JNXBAE**

GitHub: [@JNXBAE](https://github.com/JNXBAE)

Project Repository: [Portable-Offline-AI](https://github.com/JNXBAE/Portable-Offline-AI)

---

### 💡 Project Vision

*"AI should not always depend on the cloud. Intelligence should be portable, private and accessible."*

**JNX Portable Offline AI – Bringing Local AI Everywhere.**