# High-Speed CMOS Divide-by-32/33 Prescaler

This repository presents a high-speed, low-power dual-modulus prescaler designed in 16nm CMOS technology. The project investigates and compares various logic topologies for divide-by-2 circuits, then builds a TSPC-based divide-by-2/3 unit, and finally cascades them to implement a divide-by-32/33 prescaler. All designs were simulated using LTSpice with Predictive Technology Models (PTM) at 16nm.

---

## 📁 Repository Structure

```
├── Full_Design.asc                    # Complete prescaler circuit (divide-by-32/33)
├── LOGIC_NAND_cCMOS.asc/.asy         # Custom CMOS NAND gate (schematic/symbol)
├── LOGIC_NOR_cCMOS.asc/.asy          # Custom CMOS NOR gate (schematic/symbol)
├── LOGIC_OR_cCMOS.asc/.asy           # Custom CMOS OR gate (schematic/symbol)
├── TSPC_33GHz_2by3PSC.asc/.asy       # Divide-by-2/3 unit using TSPC logic (schematic/symbol)
├── TSPC_divide-by-2.asc              # TSPC-based divide-by-2 circuit
├── Transmission_Gate_divide-by-2.asc # Transmission Gate-based divide-by-2 circuit
├── Wang_divide-by-2.asc              # Wang topology divide-by-2 circuit
├── Prescaler Project Report.pdf      # Detailed design report (methodology, analysis, results)
├── README.md                         # This file
```

---

## 🚀 Project Summary

The goal was to design a **high-speed divide-by-32/33 prescaler** for use in **fractional-N frequency synthesizers**. To achieve this:

* ✅ Implemented divide-by-2 circuits using:

  * Transmission Gate logic
  * Source Coupled Logic (SCL)
  * Wang Topology
  * True Single Phase Clock (TSPC) Logic

* ✅ Designed a **TSPC-based divide-by-2/3 prescaler** for superior performance.

* ✅ Cascaded five divide-by-2/3 units to construct a **divide-by-32/33 prescaler**, with **CMOS logic gates** controlling the divide mode.

---

## 📊 Performance Highlights

| Parameter         | Value                         |
| ----------------- | ----------------------------- |
| Technology Node   | 16nm HP PTM CMOS              |
| Max Frequency     | 38.16 GHz (at 25°C)           |
| Power Consumption | 0.33 mW at 25 GHz             |
| Simulation Tool   | LTSpice                       |
| Divide Modes      | 32 (MODE=HIGH), 33 (MODE=LOW) |

---

## 🧠 Key Learnings

* **TSPC logic** offers the best trade-off between speed and power efficiency.
* Used **complementary CMOS logic** for compact, low-power control circuits.
* Achieved robust performance across different temperatures (0°C–80°C).

---

## 📝 References

* ASU PTM 16nm HP Model: [Link (Archived)](https://web.archive.org/web/20191221222848/http://ptm.asu.edu/modelcard/HP/16nm_HP.pm)
* Wu et al., “A Low-Power High-Speed True Single Phase Clock Divide-by-2/3 Prescaler”, IEICE Electronics Express, 2013.
* H. Wang, “A 1.8 V 3 mW 16.8 GHz Frequency Divider,” ISSCC, 2000.

---

## 📌 How to Run Simulations

1. Open `.asc` files using **LTSpice**.
2. For divide-by-2/3 units, set control input `M` (HIGH for ÷2, LOW for ÷3).
3. For the full design (`Full_Design.asc`), use the `MODE` input to switch between divide-by-32 (HIGH) and divide-by-33 (LOW).
4. Run transient analysis to verify functionality and waveform outputs.

---

## 📷 Preview

Refer to the `Prescaler Project Report.pdf` for detailed schematics, waveforms, and performance plots.

---

