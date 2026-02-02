# Power BI Learning Path


## 🎯 Progress Tracker

- [x] [**White Belt**](#white-belt) - Automation basics
- [ ] [**Yellow Belt**](#yellow-belt) - Data modeling
- [ ] [**Green Belt**](#green-belt) - Business logic & analysis
- [ ] [**Red Belt**](#red-belt) - Advanced visualization
- [ ] [**Black Belt**](#black-belt) - Performance & scale

---
#### 👆Click on each level to expand and view the detailed sessions.
---

<details open>
<summary><strong>
🥋⚪ Level 1: The Automator (White Belt)</strong></summary>

> **Focus:** Killing the manual copy-paste cycle and building your first automated report.

## White belt

### 📍 You are here if:
You manually export CSVs/Excel files from the ERP system every morning, clean them up (remove rows, fix headers) by hand, and email a static spreadsheet to your manager.

### 🚀 Increasing Benefit: 
**Save Time.** You perform data cleaning once, and it runs automatically forever. You move from "reporting history" to "monitoring now".

---

### Actionable Sessions (30-min each):

#### **Session 1: Connect & Combine**
- Connect Power BI to a folder containing daily production logs (Excel/CSV). Use Power Query to combine them into one continuous table automatically.
- **Goal:** Stop opening individual daily files.

#### **Session 2: The "One-Time" Clean**
- Use Power Query to remove top rows (headers), promote first rows as headers, and filter out empty null rows.
- **Goal:** Automate the "morning clean-up" routine.

#### **Session 3: Basic Categorization**
- Create a calculated column using simple logic (e.g., Volume = Length × Width × Height) to classify items. Example: If Volume > 20,000, classify as "Large," otherwise "Standard".
- **Goal:** Create new data points that don't exist in the raw ERP dump.

</details>

---

<details>
<summary><strong>🥋🟡 Level 2: The Modeler (Yellow Belt)</strong></summary>

> **Focus:** Connecting different data silos to create a "Single Source of Truth."

## Yellow belt

### 📍 You are here if:
You have a clean table, but you are struggling to compare Production Data against a separate Budget spreadsheet, or your VLOOKUPs are slowing down your report.

### 🚀 Increasing Benefit:
**Single Truth.** You stop debating which number is correct. You create a robust structure (Star Schema) that allows for fast, accurate reporting across different business perspectives.

---

### Actionable Sessions (30-min each):

#### **Session 1: The Star Schema**
- Split your big "flat" table into a Fact Table (transactions/production output) and Dimension Tables (Machines, Shifts, Products).
- **Goal:** Organize data so Power BI runs efficiently.

#### **Session 2: The Date Table**
- Create a dedicated Date Dimension (Calendar) and mark it as a Date Table. Connect it to your Production Date column.
- **Goal:** Enable drill-down from Year to Quarter to Month without writing complex formulas.

#### **Session 3: Implicit vs. Explicit Measures**
- Stop dragging columns to visuals to sum them. Create explicit DAX measures (e.g., Total Output = SUM(Production[Qty])).
- **Goal:** Create reusable formulas that can be used in any chart without recreating logic.

</details>

---

<details>
<summary><strong>🥋🟢 Level 3: The Analyst (Green Belt)</strong></summary>

> **Focus:** Adding business logic, time intelligence, and comparisons.

## Green belt

### 📍 You are here if:
You have a working model, but you are manually calculating "Year-to-Date" in Excel or struggling to highlight "High Priority" items dynamically.

### 🚀 Increasing Benefit:
**Deep Dive.** You enable extended analysis. You can answer "How are we doing compared to last year?" or "Which machines are underperforming?" instantly.

---

### Actionable Sessions (30-min each):

#### **Session 1: Priority Logic (The SWITCH)**
- Use DAX to create a dynamic priority system. Example: Use the SWITCH function to label production orders: If Price > 200 = "High", > 100 = "Medium", else "Low".
- **Goal:** Automate business decision logic directly in the report.

#### **Session 2: Time Intelligence**
- Create measures for Production YTD (Year-to-Date) and Production Last Year using CALCULATE and SAMEPERIODLASTYEAR.
- **Goal:** Instant context on whether production is trending up or down.

#### **Session 3: Visual Indicators (KPIs)**
- Use Matrix visuals with Conditional Formatting (Icons). Set rules to show a Red Diamond if Scrap Rate is High, or a Green Circle if Low.
- **Goal:** Allow managers to spot problems in 5 seconds or less.

</details>

---

<details>
<summary><strong>🥋🔴Level 4: The Architect (Red Belt)</strong></summary>

> **Focus:** Advanced data shaping and visual storytelling.

## Red belt

### 📍 You are here if:
Your data sources are complex (e.g., nested folders, messy APIs), or users complain they "can't understand" the charts.

### 🚀 Increasing Benefit:
**User Adoption.** You move from "reporting data" to "explaining why." You use advanced visuals to show root causes (e.g., why did we miss the target?).

---

### Actionable Sessions (30-min each):

#### **Session 1: The Waterfall Chart**
- Build a Waterfall chart to visualize the variance between Target and Actual production. Break it down by "Machine Breakdown," "Material Shortage," or "Staffing".
- **Goal:** Visually explain why the target was missed.

#### **Session 2: Parameterization**
- Create Power Query parameters (e.g., RangeStart and RangeEnd) to filter data loading or manage file paths dynamically.
- **Goal:** Make your reports flexible and easy to update if file locations or date targets change.

#### **Session 3: Drill-Through & Tooltips**
- Create a "Drill-through" page. Allow a user to right-click a specific Machine ID on the main dashboard and jump to a detailed page showing that machine's maintenance history.
- **Goal:** Provide summary first, details on demand (Ben Shneiderman's mantra).

</details>

---

<details>
<summary><strong>🥋⚫ Level 5: The Wizard (Black Belt)</strong></summary>

> **Focus:** Performance tuning, scale, and enterprise constraints.

## Black belt

### 📍 You are here if:
Your report is slow (taking >10 seconds to load), you are dealing with millions of rows, or you need near-real-time data.

### 🚀 Increasing Benefit:
**Scalability & Speed.** Your reports load instantly even with massive data. You handle "Big Data" scenarios using hybrid models.

---

### Actionable Sessions (30-min each):

#### **Session 1: Performance Analyzer**
- Use the "Performance Analyzer" tool in Power BI to record how long visuals take to load. Identify which DAX measure is the bottleneck.
- **Goal:** Scientifically diagnose slow reports.

#### **Session 2: Storage Modes (DirectQuery vs. Import)**
- Convert a large historical table to DirectQuery mode (leaving data in the SQL server) while keeping small dimension tables in Import mode (Composite Model).
- **Goal:** Analyze massive datasets without running out of memory.

#### **Session 3: DAX Optimization with Variables**
- Refactor a slow measure by using Variables (VAR) to calculate a value once and reuse it, preventing the engine from recalculating it multiple times.
- **Goal:** Reduce query time by up to 50%.

</details>

---
