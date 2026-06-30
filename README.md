# FuturaOS

**A modern, closed-source x86_64 operating system from the ground up.**  
Built for stability, performance, and a developer-first desktop experience.

> **⚠️ Disclaimer:** This repository serves as the official landing page, documentation hub, and release distribution center for FuturaOS. The core system source code is proprietary and closed-source. This is **not** a hobbyist open-source fork; it is a commercial-grade operating system developed under a unified architecture.

---

## 🚀 Overview

FuturaOS is not "just another hobby OS". It is a purpose-built, high-performance operating system written in C and C++. It features a custom microkernel architecture (FuturaKernel), a hybrid window manager, and a built-in application store.

We are redefining what a modern OS should be: **Stability without bloat, performance without compromise.**

---

## ✨ Key Features

**🖥️ Multi-Paradigm Window Manager**
Switch seamlessly between three entirely different desktop modes **without restarting the session**:
- **Wayland Mode** — Classic floating desktop with LVGL panel, taskbar, and system widgets.
- **Tiling Mode** — Full-screen grid for developers and power users (gap 8px, `Super+Space` launcher).
- **Infinite Mode** — A Figma/DriftWM-inspired infinite canvas. Pan, zoom (Ctrl+wheel), snap windows together, and move windows beyond the screen edges.

**⚡ Graphics & GPU Stack**
- Full **DRM** (Direct Rendering Manager) + `libdrm` support.
- **Mesa 3D Graphics Library** with **LLVMpipe** (software OpenGL 3.1) and **VirGL** support (hardware acceleration via QEMU/VirtIO).
- Ready for hardware acceleration: **Intel (i915/iris)**, **AMD (radeonsi)**, and **NVIDIA (nouveau)**.

**🗄️ Custom Futura File System (FFS)**
- Copy-on-Write (CoW), B-Tree indexing.
- Built-in AES-256 Encryption (ChaCha20).
- Snapshot support for system rollback and data recovery.

**🛒 Futura Store & Ecosystem**
- Package manager with `.fos` (Futura OS) packages.
- Built-in **FuturaID** (RSA-512 + SHA256) for a decentralized identity and software signing.

**🌐 Networking & Web**
- Built-in web browser with **HTTP/HTTPS (TLS 1.2+) support via mbedTLS**.
- HTTP/1.0 engine, HTML parser, CSS subset, and JavaScript engine (QuickJS).
- Wi-Fi stack driver support (Intel, Ralink, Realtek).

---

## 🧱 Architecture

| Layer | Technology |
| :--- | :--- |
| **Kernel** | FuturaKernel (x86_64, 64-bit) |
| **Windowing** | Yutani Compositor |
| **UI Toolkit** | LVGL (Embedded UI) + Custom C++ Shell |
| **File System** | Custom FFS |
| **Graphics** | DRM + Mesa (LLVMpipe / VirGL) |
| **Hardware** | Intel 7-Series, xHCI/EHCI, SATA AHCI |

---

## 📁 Repository Structure

- `base/` — Root filesystem image, configuration files, and kernel modules.
- `apps/` — First-party system applications (Terminal, File Browser, Web Browser, Settings).
- `kernel/` — FuturaKernel core (boot, process, memory management, VFS).
- `modules/` — Hardware drivers (USB, Wi-Fi, Audio, GPU).
- `services/` — System services (GPU manager, Filesystem bridge, Sound).
- `tools/` — Build scripts, QEMU launchers, and flashing utilities.

---

## ⚙️ Hardware Support (Tested)

FuturaOS targets x86_64 hardware.

**Works on:**
- **Laptops:** HP Pavilion G6 (Intel Core i5-3230M, Intel HD Graphics 4000).
- **Virtual Machines:** QEMU/KVM (with VirtIO-GPU acceleration).

**Ongoing driver development:**
- USB xHCI/HID (keyboard/mouse).
- SATA/ATA (supports SATA/SSD via dock or internal).
- High-Definition Audio (Intel HDA).

---

## 🎯 Vision

FuturaOS is not attempting to "replace Linux or Windows". Instead, we are building the **next-generation desktop for developers and power users**, focusing on:

1.  **Radical User Experience** – No one else offers three window manager modes in one OS.
2.  **Memory Safety & Performance** – Custom, lightweight kernel stack without the historical bloat of UNIX.
3.  **Open Infrastructure, Closed Core** – The source is proprietary, but the ecosystem (packages, apps, documentation) is open and accessible.

---

## 🤝 Contributing & Support

Since FuturaOS is a **closed-source** project, we do not accept direct Pull Requests modifying the kernel or core files. However, we welcome:

- **Bug reports** and **feature requests** via GitHub Issues.
- **Third-party application development** for the Futura Store via the FOS SDK.

---

## 📜 License & Commercial Use

The source code in this repository (excluding third-party libraries like Mesa, LLVM, and LVGL) is **closed-source and proprietary**.

- ❌ You **may not** redistribute, reverse engineer, or modify the kernel/OS images without a commercial license.
- ✅ You **may** use the OS images for testing and evaluation.

For commercial licensing, OEM partnerships, or custom builds, please contact: **[Your Email / Contact Here]**

---

## 🔗 Links

- [Official Website](#) *(if you have one, otherwise remove)*
- [Developer Documentation](doc/README.md)
- [Hardware Requirements & Compatibility](#)

---

> **Copyright © 2026 FuturaOS. All rights reserved.******
