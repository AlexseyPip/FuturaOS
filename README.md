# FuturaOS

**A modern operating system for developers, creators, and everyday users.**  
Built to compete where Windows and Linux fall short: fragmentation, bloat, and outdated user experiences.

> **"Not another hobby OS."**  
> FuturaOS is a full-featured, closed-source x86_64 operating system designed from the ground up with a hybrid kernel, a custom file system, and a next-generation desktop environment.  
> It runs on real hardware today, and it is built to scale into production use, OEM deployments, and daily drivers.

---

## 🚀 Why FuturaOS?

Windows and Linux have dominated for decades. They are powerful, but they are also heavy, fragmented, and bound to decades of legacy code.  
FuturaOS is built differently:

- **Clean architecture** – No 30-year-old UNIX baggage in the core.  
- **Modern UX** – Three desktop modes in one OS.  
- **Performance** – Lightweight kernel, fast boot times, and responsive graphics.  
- **Control** – You own your system, your identity, and your data.

---

## ✨ Key Features

"**Three desktops. One OS. No restarts.**"

**🖥️ Multi-Paradigm Window Manager**  
Switch instantly between three desktop modes without logging out:
- **Wayland Mode** – Classic floating desktop with full LVGL panel, taskbar, and system widgets.
- **Tiling Mode** – Full-screen grid for power users and developers (8px gap, `Super+Space` launcher).
- **Infinite Mode** – An infinite canvas inspired by Figma and driftwm. Pan, zoom (Ctrl+wheel), snap windows together, and move windows beyond the screen edges.

**⚡ Graphics & GPU Stack**  
- Full **DRM** + `libdrm` support.  
- **Mesa 3D Graphics Library** with LLVMpipe software rendering and VirGL hardware acceleration (QEMU/VirtIO).  
- Ready for real hardware acceleration: **Intel (iris)**, **AMD (radeonsi)**, and **NVIDIA (nouveau)**.

**🗄️ Custom File System: FFS**  
- Copy-on-Write (CoW), B-Tree indexing.  
- Built-in AES-256 encryption (ChaCha20).  
- Snapshot support for rollbacks and data recovery.

**🛒 Futura Store & Ecosystem**  
- Native `.fos` package format.  
- **FuturaID** (RSA-512 + SHA256) for decentralized identity and software signing.  
- Built-in app store with updates and secure distribution.

**🌐 Web & Networking**  
- Built-in browser with **HTTP/HTTPS (TLS 1.2+ via mbedTLS)**.  
- HTML parser, CSS engine, and QuickJS runtime.  
- Wi-Fi driver support for Intel, Ralink, and Realtek chipsets.

---

## 🧱 Architecture

| Layer | Technology |
| :--- | :--- |
| **Kernel** | FuturaKernel (Hybrid, x86_64, 64-bit) |
| **Windowing** | Yutani Compositor |
| **UI Toolkit** | LVGL + Custom C++ Shell |
| **File System** | Futura File System (FFS) |
| **Graphics** | DRM + Mesa (LLVMpipe / VirGL / Hardware) |
| **Hardware** | Intel 7-Series, xHCI/EHCI, SATA AHCI, Intel HD Audio |

---

## 📁 Repository Structure

- `base/` – Root filesystem, configs, and kernel modules.
- `apps/` – First-party applications (Terminal, File Browser, Browser, Settings).
- `kernel/` – FuturaKernel core (boot, process, memory, VFS).
- `modules/` – Loadable kernel drivers (USB, Wi-Fi, Audio, GPU).
- `services/` – System services (GPU, FS bridge, Sound).
- `tools/` – Build scripts, QEMU launchers, and flashing utilities.

---

## ⚙️ Hardware Support

FuturaOS runs on x86_64 hardware today.

**Tested on:**
- **Laptops:** HP Pavilion G6 (Intel Core i5-3230M, HD Graphics 4000).
- **Virtual Machines:** QEMU/KVM with VirtIO-GPU acceleration.

**In active development:**
- USB xHCI/HID (keyboard, mouse).
- SATA/ATA (internal and dock-driven storage).
- Intel HDA (High-Definition Audio).

---

## 🎯 Vision

FuturaOS is **not** a niche university project. It is a serious contender for the desktop space. We are targeting:

1. **Daily drivers** – People who want a fast, beautiful, and lightweight OS.
2. **Developers** – Who need tiling, infinite canvas, and a clean environment.
3. **OEMs** – Who want a modern, closed-source, and licenseable OS for their devices.

---

## 🤝 Contributing

FuturaOS is **closed-source** at the kernel level, but we welcome:

- **Bug reports** and **feature requests** via GitHub Issues.
- **Third-party application development** for the Futura Store.

---

## 📜 License

The core OS source code is **proprietary and closed-source**.  
Third-party libraries (Mesa, LLVM, LVGL, etc.) are available under their respective open-source licenses.

For commercial licensing, OEM partnerships, or custom builds, contact: **["Your Email / Contact Here"]**

---

## 🔗 Links

- [Official Website]("") *(if available)*
- [Developer Documentation](doc/README.md)
- [Hardware Compatibility](#)

---

> **Copyright © 2026 FuturaOS. All rights reserved.**
