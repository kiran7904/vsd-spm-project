# Digital VLSI SoC Design and Planning – Final Project Report

**Design:** `spm` (Small Processing Module)  
**Author:** Kiran Kumar Siripurapu  
**PDK:** Skywater 130nm (sky130A)  
**Flow:** OpenLane 2 – Full RTL → GDSII  
**Environment:** GitHub Codespaces  

**Final Result → 0 DRC | Timing Met | CVC Passed | Tapeout-Ready GDSII**

---

### Project Overview & Achievements

> Successfully completed **full open-source ASIC flow** from RTL to signoff-clean GDSII  
> All tools: Yosys → OpenROAD → Magic → OpenSTA → CVC  
> Entire flow executed inside GitHub Codespaces  

**All Signoff Checks Passed**

---

### 1. RTL Source

> File: `submission/RTL/spm.v`  
> → [View spm.v](submission/RTL/spm.v)

---

### 2. Synthesis Reports Directory

> ![OpenLane run reports directory view](submission/images/OpenLane%20run%20reports%20directory%20view.png)

> Key Reports:  
> → [Area Report](submission/Synthesis/1-synthesis.AREA_0.stat.rpt)  
> → [Timing Summary](submission/Synthesis/2-syn_sta.summary.rpt)

---

### 3. Reports Folder Structure

> ![Reports directory](submission/images/reports_directory.png)

> ![Signoff reports folder](submission/images/signoff_reports.png)

---

### 4. Final Layout Views – Magic VLSI

> **Full Chip Layout**  
> ![magic_layout_full.png](submission/images/magic_layout_full.png)

> **Zoomed-Out View**  
> ![magic_layout_full_zoom.png](submission/images/magic_layout_full_zoom.png)

> **Standard Cell Close-Up**  
> ![magic_layout_zoom.png](submission/images/magic_layout_zoom.png)

> **Custom ALU Block (Zoomed-Out)**  
> ![Custom ALU layout (zoomed-out view)](submission/images/Custom%20ALU%20layout%20(zoomed-out%20view).png)

> **Extraction Log + ALU Layout Side-by-Side**  
> ![Extraction log + simple_alu layout](submission/images/Extraction%20log%20+%20simple_alu%20layout%20(Magic%20side-by-side).png)

---

### 5. Design Rule Check (DRC) – Magic

> **Result: 0 DRC Violations**

> ![Magic DRC menu](submission/images/magic_drc_menu.png)

> ![DRC Check – 0 Errors](submission/images/tkcon_drc_check.png)

> ![Final Zero DRC](submission/images/zero_drc.png)

> **DRC Report** → [drc.rpt](submission/OpenLane/reports/signoff/drc.rpt)

---

### 6. Static Timing Analysis (STA) – OpenSTA

> **Result: Setup & Hold Met – Positive Slack**

> ![STA Terminal – Positive Slack](submission/images/sta_summary_terminal-slack.png)

> ![STA Summary File](submission/images/sta_summary_file.png)

> **Key STA Reports**  
> → [Summary](submission/OpenLane/reports/signoff/31-rcx_sta.summary.rpt)  
> → [Setup](submission/OpenLane/reports/signoff/31-rcx_sta.max.rpt)  
> → [Hold](submission/images/31-rcx_sta.min.rpt)

---

### 7. Connectivity Verification Check (CVC)

> **Result: Passed – Layout matches netlist**

> ![CVC Report – Passed](submission/images/cvc_report.png)

> **CVC Report** → [spm.rpt](submission/OpenLane/reports/signoff/spm.rpt)

---

### 8. Bonus: Complete LibreLane Full-Chip Scan

> ![Complete_librelane_scan.jpg](submission/images/Complete_librelane_scan.jpg)

---

### 9. Final Tapeout Deliverables

> **GDSII File**  
> → [spm.gds](submission/OpenLane/gds/spm.gds)

> **DEF File**  
> → [spm.def](submission/OpenLane/def/spm.def)

> **RTL**  
> → [spm.v](submission/RTL/spm.v)

---

### All Important Signoff Reports

> | Report Type      | Link |
> |----------------------|----------------------------------------------------------------|
> | DRC Report          | [drc.rpt](submission/OpenLane/reports/signoff/drc.rpt) |
> | STA Summary      | [31-rcx_sta.summary.rpt](submission/OpenLane/reports/signoff/31-rcx_sta.summary.rpt) |
> | STA Setup            | [31-rcx_sta.max.rpt](submission/images/OpenLane/reports/signoff/31-rcx_sta.max.rpt) |
> | STA Hold             | [31-rcx_sta.min.rpt](submission/images/OpenLane/reports/signoff/31-rcx_sta.min.rpt) |
> | CVC Report           | [spm.rpt](submission/OpenLane/reports/signoff/spm.rpt) |
> | IR Drop (VPWR)       | [32-irdrop-VPWR.rpt](submission/images/OpenLane/reports/signoff/32-irdrop-VPWR.rpt) |

---

**Conclusion**

> The `spm` design is **fully verified, timing-clean, and ready for tapeout** using **100% open-source flow on Sky130A PDK.  
> **DRC = 0** | **Timing Closed** | **CVC Passed** | **GDSII Generated**

**Thank you VSD Team & Open-Source EDA Community!**

**Submitted by Kiran Kumar Siripurapu**  
**November 29, 29, 2025**
