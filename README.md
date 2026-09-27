
# HOU6 Tote Command Center

An Excel-based tote inventory management tool for tracking, balancing, and prescribing tote movements across all 5 floors of the HOU6 fulfillment center. Automates demand calculations, surplus/deficit analysis, and generates actionable pallet movement prescriptions.

> Built by Hayden Gruppi — PA at HOU6

---

## 🚀 Features

- **Floor-by-floor tote tracking** across all 5 floors (1st–5th)
- **Automated demand calculations** based on picker count, pick rate, units per tote, and shift length
- **Surplus/deficit analysis** per floor with auto-generated prescriptions
- **Pallet movement recommendations** — tells you exactly how many pallets to ADD or REMOVE per floor
- **Quick View dashboard** — leadership-friendly summary with actionable steps
- **Historical data tracking** — daily snapshots for trend analysis

---

## 📊 Workbook Structure

| Sheet | Purpose | Input Required? |
|---|---|---|
| **Instructions** | How to use the tool, daily workflow | No |
| **Tote Count Entry** | Enter tote counts by floor and area (Stacks & Pallets) | ✅ Yes |
| **Building Overview** | Auto-generated floor summaries with surplus/deficit and prescriptions | No — auto-calculates |
| **Demand Calculator** | Calculates tote demand from staffing inputs | ✅ Yes (if staffing changes) |
| **Historical Data** | Daily tote count snapshots for trend analysis | ✅ Yes (paste as values) |
| **Quick View** | Simplified read-only dashboard for leadership | No — auto-generates |

---

## 🔢 Key Calculations

| Metric | Formula |
|---|---|
| **Totes per Pallet** | 66 (11 totes × 6 stacks) |
| **Floor Demand** | Picker Count × Pick Rate × Shift Length ÷ Units per Tote |
| **Surplus/Deficit** | Available Totes − Floor Demand |
| **Pallet Prescription** | Surplus ÷ 66 = pallets to REMOVE; Deficit ÷ 66 = pallets to ADD |

> **1st Floor** has no pick demand — its totes redistribute to deficit floors (3rd and 4th).

---

## 📋 Daily Workflow

1. **Update demand inputs** if staffing has changed (Demand Calculator sheet)
2. **Save previous day's data** as values in Historical Data ⚠️ *Critical — prevents data loss*
3. **Enter current tote counts** in Tote Count Entry
4. **Review Building Overview** for floor-by-floor prescriptions
5. **Consult Quick View** for actionable steps to share with leadership

---

## ⚠️ Important Notes

- Only the **Tote Count Entry** sheet requires manual data entry — all other sheets auto-calculate
- Historical data **must be pasted as values** before entering new counts
- Input data must be **manually cleared** before resetting
- Quick View provides **leadership-friendly summaries** without detailed breakdowns

---

## 🔧 Usage

1. Clone the repo:
   ```bash
   git clone https://github.com/hggruppi94/HOU6-tote-command-center.git
