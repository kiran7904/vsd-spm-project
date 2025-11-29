# Digital VLSI SoC Design and Planning – Final Project Report

**Design Name:** `spm` – Small Processing Module  
**Author:** Kiran Kumar Siripurapu  
**PDK:** Skywater 130nm Open PDK (sky130A)  
**Flow:** OpenLane 2 – Complete RTL to GDSII  
**Environment:** GitHub Codespaces  

**Final Signoff Status: DRC = 0 | Timing Met | CVC Passed | Tapeout-Ready**

---

## 1. Project Overview

This project successfully demonstrates a **complete open-source ASIC physical design flow** using **OpenLane** on the **Sky130A** PDK.  
The design `spm` was taken from RTL through synthesis, floorplanning, placement, CTS, routing, and full signoff verification — all inside GitHub Codespaces.

**All required signoff checks passed:**
- **DRC (Magic):** 0 errors
- **STA (OpenSTA):** Setup & Hold timing met
- **CVC:** Layout matches synthesized netlist
- Final GDSII generated and verified

---

## 2. RTL Source Code

**File:** `submission/RTL/spm.v`  
[Click here to view spm.v](submission/RTL/spm.v)

---

## 3. Synthesis Results (Yosys)

Synthesis completed successfully. Key reports:

- [Area Report](submission/Synthesis/1-synthesis.AREA_0.stat.rpt)
- [Timing Summary](submission/Synthesis/2-syn_sta.summary.rpt)

![OpenLane run reports directory view](submission/images/OpenLane%20run%20reports%20directory%20view.png)

---

## 4. Floorplan, Placement, CTS & Routing

All physical design steps completed with no congestion or routing violations.

![Reports directory structure](submission/images/reports_directory.png)  
![Signoff reports folder](submission/images/signoff_reports.png)

---

## 5. Final Layout Views in Magic VLSI

### Full Chip Layout
![Full Layout](submission/images/magic_layout_full.png)

### Zoomed-Out View
![Full Layout Zoomed Out](submission/images/magic_layout_full_zoom.png)

### Standard Cell Level Zoom
![Standard Cell Close-up](submission/images/magic_layout_zoom.png)

### Custom ALU Block (Zoomed-Out)
![Custom ALU layout zoomed-out view](submission/images/Custom%20ALU%20layout%20(zoomed-out%20view).png)

### Parasitic Extraction + ALU Layout (Side-by-Side in Magic)
![Extraction log and simple_alu layout side-by-side](submission/images/Extraction%20log%20+%20simple_alu%20layout%20(Magic%20side-by-side).png)

---

## 6. Signoff Verification

### 6.1 Design Rule Check (DRC) – Magic VLSI

**Result: 0 DRC violations**

![Magic DRC menu](submission/images/magic_drc_menu.png)  
![DRC Check in tkcon console – 0 errors](submission/images/tkcon_drc_check.png)  
![Final zero DRC confirmation](submission/images/zero_drc.png)

**DRC Report:** [drc.rpt](submission/OpenLane/reports/signoff/drc.rpt)

### 6.2 Static Timing Analysis (STA) – OpenSTA

**Result: Setup & Hold timing met (positive slack)**

![STA terminal output showing positive slack](submission/images/sta_summary_terminal-slack.png)  
![STA summary report file](submission/images/sta_summary_file.png)

**Key STA Reports:**
- [Summary: [31-rcx_sta.summary.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.summary.rpt)
- Setup: [31-rcx_sta.max.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.max.rpt)
- Hold: [31-rcx_sta.min.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.min.rpt)

### 6.3 Connectivity Verification Check (CVC)

**Result: Passed – No netlist mismatch**

![CVC Report – Passed successfully](submission/images/cvc_report.png)

**CVC Report:** [spm.rpt](submission/OpenLane/reports/signoff/spm.rpt)

---

## 7. Bonus: Complete LibreLane Full-Chip Scan

![Complete LibreLane scan of final GDS](submission/images/Complete_librelane_scan.jpg)

---

## 8. Final Tapeout-Ready Deliverables

| Deliverable         | File Path & Link                                                                 |
|---------------------|-----------------------------------------------------------------------------------|
| Final GDSII         | [submission/OpenLane/gds/spm.gds](submission/OpenLane/gds/spm.gds)                |
| Final DEF           | [submission/OpenLane/def/spm.def](submission/OpenLane/def/spm.def)                |
| RTL Source          | [submission/RTL/spm.v](submission/RTL/spm.v)                                      |

### All Signoff Reports (Direct Links)
| Report Type           | Link                                                                                   |
|-----------------------|----------------------------------------------------------------------------------------|
| DRC Report            | [drc.rpt](submission/OpenLane/reports/signoff/drc.rpt)                                 |
| STA Summary           | [31-rcx_sta.summary.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.summary.rpt)   |
| STA Setup             | [31-rcx_sta.max.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.max.rpt)           |
| STA Hold              | [31-rcx_sta.min.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.min.rpt)           |
| CVC Report            | [spm.rpt](submission/OpenLane/reports/signoff/spm.rpt)                                 |
| IR Drop (VPWR)        | [32-irdrop-VPWR.rpt](submission/OpenLane/reports/signoff/32-irdrop-VPWR.rpt)           |

---

## Folder Structure
