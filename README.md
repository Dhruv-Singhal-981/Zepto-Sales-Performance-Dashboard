# Zepto Quick-Commerce Sales Performance Dashboard (Tableau)

## 📌 Project Overview
This project features an interactive executive-level BI dashboard designed to analyze transaction velocities, regional revenue performance, and operational efficiencies for **Zepto**, a leading instant grocery delivery service. 

The dashboard synthesizes complex transactional datasets to provide senior leadership with a 360-degree view of core revenue drivers, operational metrics (delivery times), marketing impact (promotions), and consumer financial behavior (payment modes).

*🎯 **Live Dashboard Link:** [Insert your Tableau Public Link Here]*

---

## 🛠️ Dashboard Visual Analytics & Features
*   **Executive KPI Block (BANs):** Direct high-level tracking of macro business health: Active Customers (650K), Total Revenue (₹1.31B), Average Order Value (₹2,014), and Avg Discount per Order (287.5).
*   **Operational Telemetry:** Tracking delivery efficiency with an "Avg Delivery Minutes" tracker (21.01 mins) anchored alongside key segment filters.
*   **Dual-Axis Trend Analysis:** A sophisticated monthly combo-chart overlaying Total Revenue against Monthly Discount Outlays to track margin dilution across the financial year.
*   **Regional Demand Matrix:** Clean horizontal bar visualization isolating geographical revenue distribution across 9 core metropolitan markets.
*   **Marketing & Promo Attribution:** Multi-slice proportional analysis mapping customer engagement across distinct campaign archetypes (BOGO, Flat, Free Delivery, Percentage).

---

## 🔄 Design Evolution & Refactoring Log (The Learning Curve)
A key highlight of this project is its iteration lifecycle. The dashboard was refactored across multiple stages to move it from an exploratory draft into a clean, client-ready production asset:

### 1. Spatial Structure & Container Organization
*   **Before:** Early drafts (v1/v2) suffered from vast empty spaces on the canvas, floating slicers with clipped text boxes, and disjointed visual weight.
*   **After:** Refactored using a strict horizontal/vertical **Layout Container Grid**. Added a dedicated left-hand action sidebar for global context metrics (Month, City, Customer Segment) to anchor user interaction.

### 2. Tableau Pane Granularity Correction
*   **Before:** In the city revenue chart, a database dimensionality mismatch occurred by accidentally dropping the `City` dimension onto the Marks Card while leaving the Rows shelf completely empty. This compressed the visual field into unreadable squares.
*   **After:** Relocated `City` onto the **Rows Shelf**, instantly generating structural horizontal bars that scale properly across the financial axis for clean comparative analysis.

### 3. Localization & Enterprise Formatting
*   **Before:** Metrics were initially represented as raw, unformatted integers, forcing the user to manually count numerical digits to ascertain scale.
*   **After:** Implemented strict formatting protocols—applying the localized **Indian Rupee symbol (₹)** and truncating deep millions/billions structures into human-readable shorthand (`₹1.31B`, `₹783.47M`).

---

## 🗂️ Integrated Data Relational Sources
The dashboard actively blends and maps relationships across three separate relational data modules:
1.  `Sales_Data.csv` (Core transaction engine, pricing models, timelines)
2.  `Stores_Information.csv` (Geographical indexing, localized branch tags)
3.  `Promotions_Information.csv` (Marketing campaign definitions, offer scopes)

---

### 🎨 Preview & Layout Blueprint
<img width="1920" height="1043" alt="image" src="https://github.com/user-attachments/assets/be2020fc-573d-42c0-a5c2-0dfe96625ace" />

