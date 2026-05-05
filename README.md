# 📊 HR Analytics Dashboard — AtliQ Hardware

<img width="999" height="400" alt="Image" src="https://github.com/user-attachments/assets/68f3d668-189f-48a7-b5a4-15d81373ae77" />

## 🔍 Project Overview

An interactive **HR Analytics Dashboard** built in Power BI to help AtliQ Hardware's HR team monitor employee attendance trends across **April–June 2022**. The dashboard tracks three core workforce metrics — **Presence %, Work From Home (WFH) %, and Sick Leave (SL) %** — with day-of-week breakdowns and time-series trend lines.

---

## 🎯 Business Problem

The HR team needed a single-view solution to:
- Monitor overall employee attendance and identify attendance dips
- Understand WFH patterns and how they vary across the week
- Track sick leave usage to flag potential burnout or wellness concerns
- Make data-driven decisions around hybrid work policies

---

## 📁 Dataset

| File | Description |
|------|-------------|
| `Attendance-Sheet-2022-2023.xlsx` | Raw attendance data across Apr, May & Jun 2022 |
| `Attendance Key` (sheet) | Legend for attendance codes (P, WFH, SL, PL, HO, ML, etc.) |

- **~80–86 employees** per month across 3 monthly sheets
- **45 columns** per sheet covering daily attendance codes per employee
- Attendance codes include: `P` (Present), `WFH` (Work From Home), `SL` (Sick Leave), `PL` (Paid Leave), `HO` (Holiday Off), `ML` (Menstrual Leave)

---

## 📐 Key Metrics

| Metric | Value |
|--------|-------|
| **Overall Presence %** | 91.83% |
| **Overall WFH %** | 10.00% |
| **Overall SL %** | 1.10% |

---

## 📈 Dashboard Features

- **KPI Cards** — Snapshot of Presence %, WFH %, and SL % at a glance
- **Line + Area Charts** — Time-series of each metric with moving average overlay
- **Day-of-Week Breakdown** — Table showing which weekdays have highest/lowest presence
- **Employee-Level Table** — Individual Presence %, WFH %, and SL % per employee
- **Attendance Detail Grid** — Daily attendance codes per employee per date
- **Month Filter** — Toggle between Apr 22, May 22, Jun 22

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|------|-------|
| **Power BI** | Dashboard design, DAX measures, visualizations |
| **Microsoft Excel** | Source data — raw attendance sheets |
| **DAX** | Calculated columns and measures (Presence %, WFH %, SL %) |
| **Power Query** | Data cleaning, unpivoting date columns, merging sheets |

---

## 🔄 Data Transformation Steps (Power Query)

1. Loaded all 3 monthly sheets and appended into a single fact table
2. Unpivoted date columns to create a long-format `Date | Employee | Status` table
3. Mapped attendance codes to categories using the `Attendance Key` reference table
4. Created calculated columns for `Is_Present`, `Is_WFH`, `Is_SL`
5. Built DAX measures for % calculations with DIVIDE to handle zero denominators

---

## 📊 Key Insights

- **Monday has the highest presence** (93.21%) while **Friday is lowest** (90.19%)
- **Friday has the highest WFH rate** (13.01%), suggesting employees prefer remote Fridays
- **Sick leave peaks on Mondays** (1.62%), potentially indicating weekend-to-weekday fatigue
- Presence % dipped to **~77–78% in mid-May**, warranting further HR investigation
- WFH trended upward through June, reaching **16.31%** — a growing hybrid work pattern

---

## 🚀 How to Use

1. Clone the repo
   ```bash
   git clone https://github.com/yourusername/hr-analytics-dashboard.git
   ```
2. Open `Attendance-Sheet-2022-2023.xlsx` to explore the raw data
3. Open the `.pbix` file in **Power BI Desktop**
4. Use the **month filter buttons** (Apr 22 / May 22 / Jun 22) to explore trends by period

---

## 📌 Future Improvements

- [ ] Extend dataset to full FY 2022–23
- [ ] Add department-level segmentation
- [ ] Alert system for employees with presence below 75%
- [ ] Forecast attendance trends using Power BI's built-in analytics

---

## 📄 License

This project is for educational and portfolio purposes only.
