# 🌌 Ambience Open Source Project

### 📜 Project Overview
The **Ambience Open Source Project** is a systematic research initiative dedicated to the development and optimization of an integrated operating system environment specifically for the **RISC-V** architecture. By harmonizing kernel-level performance with a streamlined user-space infrastructure, Ambience aims to provide a robust, modular, and high-efficiency ecosystem for the next generation of open-source hardware.

### 🎓 Maintainer's Statement
This project is currently spearheaded and maintained by a **secondary school student**. While driven by academic passion and a commitment to the RISC-V ecosystem, the project recognizes that technical mastery is a continuous journey. 

We maintain a posture of intellectual humility and welcome rigorous peer review. We earnestly invite experts, researchers, and developers within the community to provide guidance, suggest optimizations, and contribute to the codebase. Your mentorship is highly valued.

---

### 🚀 Hardware Support Matrix
Currently, the **StarFive VisionFive 2** (including its subsequent hardware revisions) serves as the primary reference platform for the Ambience Project. While the project is architected for portability within the RISC-V 64-bit ISA, other hardware platforms remain untested and are not officially supported at this stage.

---

### 🛠 Build Methodology
The project utilizes a modular build system designed for reproducibility. Please ensure your workspace is initialized via the `repo` tool:

1.  **Synchronization**:
    ```bash
    repo init -u https://github.com/Ambience-Open-Source-Project/platform-manifest.git
    repo sync
    ```
2.  **Environment Setup**:
    Navigate to the build directory and initialize the shell environment:
    ```bash
    cd build
    source ./setenv.sh
    ```
3.  **Synthesis**:
    ```bash
    make
    ```
Upon successful compilation, the synthesized bootloader images and the root filesystem (RootFS) will be available in the `out/build/` directory at the project root.

---

### 📂 Repository Architecture
| Repository | Description |
| :--- | :--- |
| **`platform-manifest`** | Centralized XML manifests for multi-repository synchronization. |
| **`platform-build`** | The core logic layer and Makefiles for the unified build system. |
| **`platform-linux`** | Tailored Linux kernel sources optimized for the RISC-V 64-bit architecture. |
| **`platform-assets`** | Static system configurations, initialization scripts, and binary resources. |
| **`platform-busybox`** | Minimalist user-space utilities providing essential system commands. |
| **`platform-glibc`** | The core C library providing the foundational API for the system. |
| **`platform-gcc`** | Optimized GNU Compiler Collection for RISC-V cross-compilation. |
| **`platform-limine`** | Advanced, multiprotocol bootloader for modern RISC-V deployments. |

---

### ⚖️ Legal Disclaimer & Licensing
**Ambience Open Source Project** is a composite project consisting of various independent components. 
* **Licensing**: Each repository within this organization is governed by its own respective license (e.g., GPL, LGPL, MIT). Users must refer to the `LICENSE` or `COPYING` file within each individual repository for specific terms.
* **Nomenclature**: The naming convention of certain repositories (e.g., prefixing with `platform-`) is inspired by the **Android Open Source Project (AOSP)** structure. This is a purely architectural choice intended to provide a familiar and organized hierarchy for developers accustomed to complex build environments; this project is **not** a fork of AOSP nor is it affiliated with Google LLC.
* **Warranty**: This software is provided "as is," without warranty of any kind, express or implied.

---
**Maintained by [FengHeting (MicroFish)](https://github.com/FengHeting)**
