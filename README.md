# 📡 Understanding 3GPP Document Structure

This repository explains how to navigate and interpret **3GPP specifications**, particularly for **5G NR and LTE**, and shows how I apply these standards in real-world wireless systems projects.

---

## 📘 What is 3GPP?

The **3rd Generation Partnership Project (3GPP)** develops global standards for cellular technologies including 4G LTE and 5G NR. These standards are published in two forms:

- **Technical Specifications (TS):** Normative documents that define how systems must behave.
- **Technical Reports (TR):** Informative studies on use cases, architecture options, and feasibility.

| Type | Purpose                | Example                        |
|------|------------------------|--------------------------------|
| TS   | Implementation standard | TS 38.211 (Physical Channels) |
| TR   | Feasibility study       | TR 38.913 (NR Requirements)    |

---

## 🔢 3GPP Numbering System

Each document is numbered `XX.YYY`:
- `XX` = Series (e.g., 38 for 5G NR, 36 for LTE)
- `YYY` = Specific document ID

**Example:** `TS 38.331` refers to the 5G NR Radio Resource Control (RRC) specification.

---

## 🧩 5G NR Layered Specification Mapping (with Full Names)

3GPP organizes its protocol stack by layers. Each layer has a defined function and corresponding specification.

| **Protocol Layer**                          | **3GPP Spec** | **Description**                                                                 |
|--------------------------------------------|---------------|---------------------------------------------------------------------------------|
| Physical Layer (PHY)                       | TS 38.211–215 | Modulation, coding, and physical channel definitions                            |
| Medium Access Control (MAC)                | TS 38.321     | Uplink/downlink scheduling, HARQ, random access procedures                      |
| Radio Link Control (RLC)                   | TS 38.322     | Segmentation, reassembly, retransmission control                               |
| Packet Data Convergence Protocol (PDCP)    | TS 38.323     | Header compression, encryption, integrity protection                            |
| Radio Resource Control (RRC)               | TS 38.331     | Connection setup/release, mobility management, beam configuration              |
| Non-Access Stratum (NAS)                   | TS 24.501     | UE-to-core signaling for session and mobility management                        |

---

## 🧪 How I Use These Specs in Real Projects

### 🛰️ 5G Scheduling & Modem Protocol Optimization
- Referred to **TS 38.321 (MAC layer)** to implement a **Weighted Round Robin scheduler** in the `srsRAN` 5G stack.
- Benchmarked performance across 500+ test cases and improved uplink fairness by ~25%.

### 🔐 Jamming Attacks on LTE Stack
- Analyzed synchronization breakdowns under jamming using **TS 36.331 (RRC)**.
- Verified HARQ behavior with **TS 36.321** during MAC-layer retransmission under RF stress.

### 🧠 Batteryless Wireless Sensor Network Simulation
- Built a modular simulator aligning with **RLC and PDCP behaviors** from TS 38.322 and TS 38.323.
- Handled packet segmentation/reassembly for energy-constrained nodes.

### 🌐 Traffic & Packet Analysis with Wireshark
- Used **TS 38.331** to decode RRC messages from packet captures.
- Verified PDCP encryption and integrity against **TS 38.323** specs.

---

## 🔗 Helpful Resources

- 📄 [3GPP Specs Archive](https://www.3gpp.org/ftp/Specs/)
- 🔍 [DynaSpec Search Tool](https://www.3gpp.org/DynaReport)
- 🧪 [srsRAN 5G Stack](https://github.com/srsran/srsRAN_5G)
- 🖥️ [Wireshark Protocol Reference](https://www.wireshark.org/docs/dfref/)

---

## 🎯 About This Repo

This project demonstrates both theoretical understanding and practical application of 3GPP standards. It's a personal effort to bridge the gap between **spec interpretation** and **hands-on development** in modern wireless systems.

---

