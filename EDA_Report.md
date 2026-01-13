# B2B Business Analysis & Optimization Report

## 1. Project Overview

The primary objective of this project was to analyze B2B sales data to assess the health of the wholesale channel, identify inefficiencies in inventory management, and propose data-driven strategies for revenue growth. The analysis focused on distinguishing genuine bulk purchasing behavior from lower-value transactions (likely dropshipping) and pinpointing capital trapped in non-performing stock.

By merging sales data with inventory reports, the project aimed to:

- Evaluate the true nature of B2B demand (**Volume vs. Value**)
- Quantify potential financial uplift from strategic shifts such as **Minimum Order Quantities (MOQs)**
- Identify **"Dead Stock"** specific to the B2B channel to free up capital


---

## 2. Data Overview & Integrity

The analysis was performed using two primary datasets:

1. **Sales Data (`cleaned_data_1.csv`)**  
   Contains transaction-level details including Order IDs, SKUs, Quantities, and Revenue. A B2B filter was applied to isolate wholesale transactions.

2. **Inventory Data (`Sale Report.csv`)**  
   Provides a snapshot of current stock levels for each SKU.

### Data Integrity Steps & Checks

- **SKU Standardization:**  
  Harmonized SKU formats across both datasets (trimmed whitespace, uppercase conversion) to ensure accurate joins.

- **B2B Classification:**  
  Applied a custom classification function based on sales channel identifiers (e.g., *Wholesale*, *Bulk*) to separate B2B from B2C data.

- **Missing Values:**  
  Filled `NaN` values in sales and inventory columns with `0` to prevent aggregation errors.

- **Data Types:**  
  Explicitly cast Revenue and Quantity fields to numeric types to maintain calculation integrity.

---

## 3. Key Performance Indicators (KPIs)

The following KPIs summarize the current performance of the B2B channel:

| KPI | Value | Insight |
|----|------|--------|
| **Total B2B Revenue** | **₹6,17,180.00** | Total revenue generated from wholesale transactions |
| **Total B2B Orders** | **794** | Total number of B2B transactions |
| **Average Order Value (AOV)** | **₹777.30** | **Critically low for B2B**, indicating retail-like purchasing behavior |
| **Hero Category** | **Sets** | Contributes **52.3%** of total B2B revenue |

---

## 4. Strategic Insights & Diagnosis

### A. The "Fake Wholesale" Phenomenon

- **Observation:**  
  **86%** of B2B orders (683 out of 794) consist of just **one unit**. Only **8.9%** qualify as true bulk orders (>1 unit).

- **Diagnosis:**  
  The B2B channel is currently subsidizing retail-like resellers who benefit from wholesale pricing without delivering volume. This increases operational overhead without proportional revenue gain.

---

### B. "Dead Stock" Capital Trap

- **Observation:**  
  Significant inventory is locked in SKUs with **zero B2B demand**.

  **Examples:**
  - `JNE3405-KR-XXL`: **1,234 units in stock**, **0 B2B sales**
  - `JNE1525-KR-UDF19BLACK-M`: **1,082 units in stock**, **0 B2B sales**

- **Diagnosis:**  
  This dead stock ties up working capital, increases storage costs, and limits reinvestment into high-performing SKUs.

---

### C. Supply Chain Risk: Demand–Supply Mismatch

- **Observation:**  
  Identified **14 SKUs** where B2B demand is exceeding allocated inventory levels.

- **Diagnosis:**  
  High-velocity B2B items face stockout risk. Without inventory ring-fencing or faster replenishment, B2B demand may cannibalize stock needed for higher-margin B2C sales.

---

## 5. Recommended Action Plan

### Step 1: Restructure B2B Pricing & Policy (The MOQ Fix)

- **Action:**  
  Enforce a **Minimum Order Quantity (MOQ)** of **3–5 units per SKU** to eliminate inefficient single-unit B2B orders.

- **Projected Impact:**  
  Converting just **20%** of single-unit buyers into 3-unit buyers increases:
  - **AOV by 16%** (₹777 → ₹904)
  - **Revenue uplift of ~₹1,00,000**

---

### Step 2: Strategic Inventory Focus

- **Action:**  
  Prioritize procurement and replenishment for the **Hero Category (Sets)**.

- **Implementation:**  
  Deploy **automated low-stock alerts** for the top 20 B2B-performing Set SKUs.

- **Rationale:**  
  With over **52%** of B2B revenue coming from this category, stock availability is critical to revenue stability.

---

### Step 3: Active B2B Sales Management

- **Action:**  
  Actively review **Zero-Sales SKUs** with the sales team.

- **Tactic:**  
  - Verify presence in B2B catalogs and line sheets  
  - Present physical samples to key buyers  
  - Collect feedback to decide between promotion or discontinuation

---
