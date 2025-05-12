# SupplyCast-A-Dual-Pipeline-AI-System-for-Demand-Forecasting-Supply-Chain-Optimization
# 📦 SupplyCast™: A Dual-Pipeline AI System for Sales Forecasting & Supply Chain Prediction

**By Empress Ruler of All Kingdoms 👑 | Powered by Shams ☀️, Samaa 🌌, and Dune 🌵**

---

## 🧠 Overview

SupplyCast™ is a modular machine learning framework built to predict **product demand** and **optimize supply chains** — across any industry.

Originally developed for a fictional Algerian yogurt brand (*Laitinelle Dairies™*), this system can adapt to different products like shoes, makeup, cleaning products, and more.

> Forecast demand like a prophet. Optimize stock like a supply chain oracle. 🔮

---

## 🔍 What This Project Does

### ✅ **Sales Forecasting Pipeline**
- Predicts **future product demand** (e.g., yogurt units sold).
- Uses features like:
  - `date`
  - `promotion`
  - `temperature` (optional, product-specific)
  - `units_sold`

### ✅ **Supply Chain Prediction Pipeline**
- Uses predicted sales + inventory + delivery delays to optimize stock.
- Answers questions like:
  - How much to reorder?
  - When will stock run out?
  - Are we at risk of overstock or stockout?

> These two pipelines are separate but interlinked. Sales forecast is **fed** into the supply chain model to guide smart inventory decisions.

---

## 🏗️ Architecture

             +---------------------------+
             |   Raw Dataset (Yogurt)    |
             +------------+--------------+
                          |
                          v
   +------------------- Sales Forecasting Pipeline --------------------+
   |  Select sales features (date, temp, promo)                        |
   |  Train model (Prophet, XGBoost, etc.)                             |
   |  Predict future `units_sold`                                      |
   +----------------------------+--------------------------------------+
                                |
                                v
   +--------------- Add predicted sales to dataset --------------------+
                                |
                                v
+---------------------- Supply Chain Prediction Pipeline ----------------------+
| Use inventory, lead_time, delivery_delay, and predicted demand |
| Train regression/classification models |
| Predict reorder quantity, timing, and risks |
+------------------------------------------------------------------------------+


---

## 📊 Features Used

### Sales Forecasting

| Feature         | Description                                  |
|-----------------|----------------------------------------------|
| `ds`            | Date of sale                                 |
| `units_sold`    | Number of units sold                         |
| `promotion`     | Binary flag if promo was active              |
| `temperature_c` | Daily avg temperature (for perishables only) |
| `price`         | Price per unit (optional if fixed)           |

### Supply Chain Prediction

| Feature            | Description                                |
|--------------------|--------------------------------------------|
| `inventory_level`  | Stock on hand                              |
| `lead_time`        | Days until new stock arrives               |
| `reorder_point`    | Stock threshold to trigger reorder         |
| `supplier_delay`   | Delays in delivery (simulated or real)     |
| `predicted_demand` | Output from sales forecast pipeline        |

---

## 🛠 How to Run This Project

### 1. Clone the repo:
```bash
git clone https://github.com/your-username/SupplyCast
cd SupplyCast
