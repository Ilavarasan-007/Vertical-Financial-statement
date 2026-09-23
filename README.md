# Sample Financial Statements Template for Non-Corporate Entities (NCE)

A formula-driven financial reporting workbook designed in accordance with the **ICAI Technical Guidance Note on Financial Statements for Non-Corporate Entities**[span_0](start_span)[span_0](end_span).

Compatible with **Microsoft Excel** and **Google Sheets**[span_1](start_span)[span_1](end_span).

---

## 📌 Overview

This repository provides an automated, formula-linked financial reporting workbook (`.xlsx`) designed for non-corporate entities (Sole Proprietorships, Partnership Firms, and LLPs)[span_2](start_span)[span_2](end_span). All statements, ledgers, and cash flow calculations dynamically update using standard spreadsheet formulas—without requiring external scripts or macros[span_3](start_span)[span_3](end_span).

---

## 🗂️ Workbook Architecture & Sheet Sequence

The workbook consists of six sequentially organized worksheets[span_4](start_span)[span_4](end_span):

| Sheet # | Sheet Name | Format | Role & Linkage |
|:---:|---|---|---|
| **1** | `Setup_Control` | Control Panel | Business configuration, reporting dates, currency unit, and line-item visibility toggles[span_5](start_span)[span_5](end_span). |
| **2** | `Statement_of_P&L` | Vertical Statement | Dynamic Profit & Loss account pulling totals directly from expense and revenue registers[span_6](start_span)[span_6](end_span). |
| **3** | `Balance_Sheet` | Vertical Statement | Complete Balance Sheet linked to closing balances from ledger schedules with automatic balance check verification[span_7](start_span)[span_7](end_span). |
| **4** | `BS_Notes` | Horizontal T-Ledgers | Dual-sided Dr. / Cr. ledger schedules for all Balance Sheet items[span_8](start_span)[span_8](end_span). |
| **5** | `PL_Notes` | Vertical Registers | Itemized transaction registers for purchases, payroll, finance, and operating expenses[span_9](start_span)[span_9](end_span). |
| **6** | `Cash_Flow_Statement` | AS-3 Format | Automated cash flow report supporting both Direct and Indirect calculation methods[span_10](start_span)[span_10](end_span). |

---

## ✨ Key Features & Logic

* **Master Head Toggles:** Enable or disable individual balance sheet heads (PPE, Investments, Borrowings, Inventories, etc.) via **Yes/No** dropdowns in `Setup_Control`[span_11](start_span)[span_11](end_span). Excluded items cleanly collapse without formula errors[span_12](start_span)[span_12](end_span).
* **Horizontal Dr. / Cr. T-Ledgers (`BS_Notes`):** Formatted strictly as:
  * **Debit (Dr.):** `Date` | `Particulars (Debit)` | `Amount (₹)`[span_13](start_span)[span_13](end_span)
  * **Credit (Cr.):** `Date` | `Particulars (Credit)` | `Amount (₹)`[span_14](start_span)[span_14](end_span)
  * Automatic balancing lines (`To Balance c/d` / `By Balance c/d`) feed directly into the Balance Sheet[span_15](start_span)[span_15](end_span).
* **Vertical Expense Registers (`PL_Notes`):** 
  * Clean logs formatted as: `Entry #` | `Date` | `Particulars / Description` | `Amount (₹)`[span_16](start_span)[span_16](end_span).
  * Total rows use native `=SUM()` formulas that feed into the Statement of Profit & Loss[span_17](start_span)[span_17](end_span).
* **Zero Circular References:** Built along a strict linear calculation path to eliminate `#NAME?` and `#REF!` errors across desktop and mobile versions of Google Sheets and Excel[span_18](start_span)[span_18](end_span).
* **Adaptive AS-3 Cash Flow Statement:**
  * Displays the **Direct Method** when comparative figures are disabled[span_19](start_span)[span_19](end_span).
  * Automatically shifts to the **Indirect Method** when comparative previous year figures are included[span_20](start_span)[span_20](end_span).
* **Entity-Specific Logic:** Setting the constitution to **Proprietorship** automatically suppresses partner remuneration across all statements[span_21](start_span)[span_21](end_span).

---

## 📖 How to Use

1. Download the `NCE_Financial_Statements_Clean_Template.xlsx` file from this repository[span_22](start_span)[span_22](end_span).
2. Open the file in **Microsoft Excel** or upload it to **Google Drive / Google Sheets**[span_23](start_span)[span_23](end_span).
3. Go to the `Setup_Control` sheet[span_24](start_span)[span_24](end_span):
   * Enter the entity name, constitution type, and financial year dates[span_25](start_span)[span_25](end_span).
   * Choose whether to include previous year comparative figures (**Yes / No**)[span_26](start_span)[span_26](end_span).
   * Toggle the line items required for your business (**Yes / No**)[span_27](start_span)[span_27](end_span).
4. Enter opening balances and transactions in `BS_Notes` and `PL_Notes`[span_28](start_span)[span_28](end_span).
5. Review the automatically generated and reconciled statements in `Statement_of_P&L`, `Balance_Sheet`, and `Cash_Flow_Statement`[span_29](start_span)[span_29](end_span).

---

## 👨‍💻 Author

**Ilavarasan**

---

## 📄 License

This project is licensed under the [MIT License](LICENSE)[span_30](start_span)[span_30](end_span).
