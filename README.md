# SupplyProphet™: AI-Powered Sales Forecasting & Supply Chain Insights for Laitinelle Dairies™

## 🏭 Project Overview

**SupplyProphet™** is a machine learning masterpiece crafted for **Laitinelle Dairies™**, a fictional Algerian yogurt company, as part of a Gomycode Data Scientist certification. It delivers a sales forecasting pipeline using **Prophet** and a supply chain insight (reorder alerts) to keep inventory tighter than a glass jar’s lid. This project fuses technicality, business, and a narrative. 

### 🎯 Objectives

- **Sales Forecasting**: Predict daily yogurt sales (`units_sold`, `sales_dzd`) with time-series magic, nailing seasonality, promotions, and temperature vibes.
- **Supply Chain Insight**: Flag reorder alerts to dodge stockouts and cut waste, keeping Laitinelle’s shelves stocked with fresh *Yaourt Fraîcheur D’Eté*.
- **Narrative & Visuals**: Spin a story about Laitinelle’s quest for data-driven glory, backed by Plotly visuals that pop like a mint yogurt swirl.

### 📍 Why This Matters

In Algeria’s dairy game, yogurt’s 14-day shelf life is a ticking bomb. Overstock, and you’re tossing spoiled jars; understock, and customers ditch you for competitors. **SupplyProphet™** tackles these pain points with AI, simulating real-world challenges to save Laitinelle millions. It’s not just yogurt—it’s a blueprint for any business juggling perishables, from Algiers to the multiverse.

### 🕒 Project Constraints

- **Data**: Synthetic, mimicking 6 months of daily sales (Jan 1–June 30, 2024).
- **Tools**: Beginner-friendly (Python, Prophet, Plotly) for max impact in minimal time.
- **Audience**: Gomycode jury—technical evaluators and virtual non-technical stakeholders expecting clarity and wow-factor.

---

## 🧃 About Laitinelle Dairies™

Founded in 2018, **Laitinelle Dairies™** is a fictional Algerian brand slinging premium probiotic yogurts under the *Yaourt Fraîcheur D’Eté* line. Operating in Algiers, Oran, Constantine, and Blida.

### 🎯 Business Challenges

- **Demand Chaos**: Sales swing wildly with promotions, hot weather, and holidays (Eid, Ramadan, summer vacations).
- **Perishability**: Yogurt spoils in 14 days, demanding ninja-level inventory precision.
- **Logistics Headaches**: Supplier lead times (2–7 days) mess with restocking plans.
- **Profit Squeeze**: Balancing production costs, waste, and sales in a competitive market.

### 🧑‍💼 CEO: Madame Zineb Belkacem

- **Background**: Algerian-French food scientist, Sorbonne-trained, obsessed with probiotics and Algerian dairy heritage.
- **Personality**: Visionary, warm, quotes *Dune* like a boss (“The spice must flow!”). Sips mint tea while plotting data revolutions.
- **Role**: A Junior Data Scientist, building SupplyProphet™ and save this issue.

### 🧁 Brand Essence

| Ingredient | Description |
|------------|-------------|
| 🧬 **Name DNA** | “Latinelle” fuses “lait” (milk) and “élégance,” screaming Euro-chic for Algiers’ trendiest cafes. |
| 🧴 **Product Identity** | Probiotic yogurts in glass jars, infused with Mediterranean herbs (mint, basil, thyme). |
| 🌍 **Mission** | “To bring warmth to your gut, and elegance to your spoon.” |
| 🧠 **Storytelling** | Born from Madame Zineb’s dream to blend Algerian tradition with modern science. |
| 💋 **Visual Signature** | Handwritten logo, mint-green and lavender hues, golden jar accents. |
| 💰 **Marketing Hook** | “Not just yogurt. **Latinelle™**.” |
| 🌞 **Core Values** | Freshness, sustainability, community (partners with local dairy farmers). |

### 🏪 Competitors (Fictional)

- **Yoghurto**: Mass-market brand, cheap but bland, dominates supermarkets.
- **MédinaMilk**: Artisanal rival, focuses on rural markets, less tech-savvy.
- **SupplyProphet™** gives Laitinelle an edge over Yoghurto’s volume-driven model and MédinaMilk’s outdated logistics.”

---

## 📊 Dataset Description

The project runs on a **synthetic dataset** (`latinelle_yogurt_data.csv`), simulating daily sales and inventory for Laitinelle from January 1 to June 30, 2024 (181 days). Crafted with Python, it mirrors Algerian market dynamics—seasonality, promotions, weather—while keeping things beginner-friendly.

### 📁 Dataset Columns

| Column | Type | Description | Business Logic |
|--------|------|-------------|----------------|
| `ds` | Date | Date of sales entry (YYYY-MM-DD) | Drives time-series analysis. |
| `units_sold` | Integer | Number of yogurt units sold | Target for forecasting. |
| `price_per_unit_dzd` | Integer | Price per unit (100 DZD) | Fixed; computes `sales_dzd`. |
| `sales_dzd` | Float | Revenue (`units_sold × price_per_unit_dzd`) | Tracks financial impact. |
| `promotion` | Binary | 1 if promotion active, 0 otherwise | Every 15th day, adds 30–70 units. |
| `temperature_c` | Float | Daily average temperature (°C) | Hot days (>25°C) boost sales by ~1.5 units/°C. |
| `inventory_level` | Integer | Stock on hand (units) | Triggers reorder alerts if low. |

### 🧠 Dataset Generation Logic

- **Sales**: Base sales (300 units) + seasonality (sine wave for weekly/monthly cycles) + promotion effects (30–70 units every 15 days) + temperature impact (1.5 units/°C above 25°C) + noise (±15 units).
- **Promotions**: Mimic marketing campaigns (discounts, Instagram ads) every 15 days.
- **Temperature**: Cyclic pattern (20–30°C) with noise, reflecting Algeria’s climate.
- **Inventory**: Simulated as 500 units ± normal noise (50 units), representing warehouse stock.
