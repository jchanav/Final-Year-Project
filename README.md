# 📦 Inventory Allocation Optimisation at Towngas Hong Kong

> Final Year Project — Department of Industrial Engineering and Decision Analytics  
> The Hong Kong University of Science and Technology (HKUST) · May 2026

---

## 👥 Team

| Name | Student ID |
|------|-----------|
| CHAN, Jannis | 20900000 |
| WONG, Cheng Loong | 20916293 |
| YUEN, Yu Yung | 20965749 |

**Supervisor:** Professor ZHANG, Jiheng  
**Teaching Assistant:** NG, Cho Yin

---

## 🏢 Industry Partner

This project was developed in collaboration with **Towngas Hong Kong** (The Hong Kong and China Gas Company Limited), one of Hong Kong's oldest utility companies founded in 1862. Towngas operates a multi-echelon physical distribution network for thousands of appliance SKUs across Hong Kong Island, Kowloon, and the New Territories.

---

## 📌 Project Overview

Towngas's logistics team makes daily decisions on how to move appliance goods through a four-node distribution network:

Cargo Terminal (CT) → NP / TM Warehouses ⇄ External Warehouse (EX) → Customer

These decisions — container collection timing, internal warehouse transfers, and external warehouse management — are currently handled through experience and manual judgment, leading to suboptimal costs and operational inefficiencies.

---

## 🎯 Objective

Design and implement a **7-Day Rolling Horizon Mixed-Integer Linear Programme (MILP)** that jointly optimises all daily logistics decisions to minimise total operational cost, including:

- External warehouse holding, retrieval, and offloading costs
- CT transport and overstay penalties
- Backlog and lost-sales costs

---

## 🔬 Methodology

- **Model:** Mixed-Integer Linear Programme (MILP) solved via Gurobi
- **Horizon:** 7-day rolling window; only Day-1 decisions are executed daily
- **Scope:** APPL (appliance) goods category · January 2026 backtest · 511 SKUs
- **Baselines:** Greedy Heuristic, Rule-Based Policy, Actual Towngas Operations

---

## 📊 Key Results

| Model | Total Cost (HKD) |
|-------|-----------------|
| **MILP (Ours)** | **632,617** |
| Greedy Heuristic | 747,902 |
| Actual Operations | 867,653 |
| Rule-Based Policy | 969,305 |

> The MILP achieves **27% cost reduction** vs actual operations and **15% vs greedy heuristic**.

---

## 🖥️ Prototype

A decision-support web application prototype was developed to allow logistics managers to review and approve daily MILP recommendations, integrating with Towngas's existing SAP system.

---

## 📁 Repository Structure
├── index.html # Main presentation (open in browser)
├── Towngas_dist.png # Distribution network diagram
├── Prototype.mp4 # Prototype demo video
├── Towngas202401.png # Towngas logo
├── IEDAbrm.png # HKUST IEDA logo
└── README.md

---

## 🚀 How to View the Presentation

1. Clone or download this repository
2. Place all assets in the **same folder**
3. Open `index.html` in any modern browser (Chrome, Edge, Safari)
4. Navigate using **Arrow Keys** or **Spacebar**
5. Press **`O`** to open the slide overview grid

---

## 📄 License

This project is submitted as a Final Year Project at HKUST. All rights reserved by the authors and Towngas Hong Kong. Not for commercial use.

