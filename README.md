# Understanding 3GPP Document Structure

This repo breaks down how to navigate and understand 3GPP technical documents, particularly for 5G NR and LTE.

## 📚 1. What is 3GPP?

The 3rd Generation Partnership Project (3GPP) develops global telecom standards for mobile systems, including LTE and 5G NR.

## 📄 2. Document Types

- **Technical Specifications (TS):** Normative; defines what must be implemented
- **Technical Reports (TR):** Informative; explore feasibility or studies

| Type | Purpose | Example |
|------|---------|---------|
| TS   | Implementation standard | TS 38.211 (Physical Channels) |
| TR   | Study/feasibility | TR 38.913 (NR Requirements)     |

## 🧩 3. Numbering Scheme

Each spec is labeled `XX.YYY`:
- `XX`: Series domain (e.g., 38 = 5G NR, 36 = LTE)
- `YYY`: Specific document ID

### Example:
- TS 38.331 → RRC for 5G NR
- TS 36.321 → MAC layer for LTE

## 🔍 4. Layered Spec Mapping (5G NR)

| Layer | Spec No. | Description |
|-------|----------|-------------|
| PHY   | 38.211–38.215 | Modulation, coding, channel access |
| MAC   | 38.321 | Scheduling, HARQ |
| RLC   | 38.322 | Segmentation, retransmission |
| PDCP  | 38.323 | Header compression, ciphering |
| RRC   | 38.331 | Connection setup, mobility |
| NAS   | 24.501 | 5G Core signaling |

## 🧠 5. How I Use These Specs

> During my wireless projects, I referred to TS 38.331 to decode RRC messages in logs and used TS 38.321 to understand uplink scheduling behavior.

## 🔗 6. Helpful Links

- [3GPP Portal](https://www.3gpp.org/DynaReport)
- [TS 38 Series Specs](https://www.3gpp.org/ftp/Specs/archive/38_series/)
