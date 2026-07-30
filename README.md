# Open-PDK-Hub 🚀

A centralized workspace for open-source Process Design Kits (PDKs) targeting ASIC physical design, VLSI research, and block-level implementation. 

Finding and configuring the right PDK for physical design (PD) experiments often requires hunting across multiple academic and foundry repositories. **Open-PDK-Hub** aggregates both predictive (research-only) and manufacturable (silicon-proven) nodes into a single repository using Git submodules and the SiliconCompiler LambdaPDK collection.

---

## 🛠️ Included Technologies

This hub supports a wide range of technology nodes, from 180nm legacy processes down to 2nm Gate-All-Around (GAA) predictive models.

### Predictive PDKs (Academic & Research Only, No Tape-out)
These kits model advanced nodes and are ideal for exploring physical design flows, placement strategies, and static timing constraints at the cutting edge.

| Node | Name | Transistor Type | Source / Notes |
| :--- | :--- | :--- | :--- |
| **2nm** | GT2N | GAAFET | via LambdaPDK |
| **3nm** | ASAP3 / PKP3 | GAA Nanosheet | *Reference only (Private academic access)* |
| **5nm** | ASAP5 | FinFET/GAAFET | Submodule: `elllusion/ASAP5_for_KLayout` |
| **7nm** | ASAP7 | FinFET | via LambdaPDK |
| **45nm**| FreePDK45 | Planar CMOS | via LambdaPDK |

### Manufacturable PDKs (Real Silicon)
These kits are supported by foundries and Multi-Project Wafer (MPW) shuttle programs for actual silicon fabrication.

| Node | Name | Specialization | Source / Notes |
| :--- | :--- | :--- | :--- |
| **90nm** | Sky90FD | FDSOI | Submodule: `google/sky90fd-pdk` |
| **130nm**| Sky130 | General Purpose / Mixed Signal | via LambdaPDK |
| **130nm**| IHP130 | SiGe BiCMOS (RF/High Freq) | via LambdaPDK |
| **180nm**| GF180MCU | High Voltage / Mixed Signal | via LambdaPDK |

---

## ⚙️ Prerequisites

To utilize the PDKs in this hub, ensure you have the following installed in your environment:
*   **Python 3.8+** (Required for LambdaPDK and environment management)
*   **Git** (For submodule initialization)
*   An RTL-to-GDSII toolchain such as **OpenROAD** or **OpenLane**

---

## 🚀 Installation & Setup

Because this repository uses submodules and Python packages to pull in the heavy PDK data, do not download the ZIP file directly from GitHub. Use Git to clone the repository properly.

### 1. Clone the Repository
```bash
git clone --recursive [https://github.com/YOUR_USERNAME/open-pdk-hub.git](https://github.com/YOUR_USERNAME/open-pdk-hub.git)
cd open-pdk-hub
