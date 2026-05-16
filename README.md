# Engineering Data Systems Project: Wind Turbine Performance Analysis
**Topic:** RMS-01: Wind Turbine Gearbox Vibration (SCADA Performance Analysis)  
**Student Number:** 0318  
**Surname:** ESPINO

## 📌 Project Overview
This production-grade Python pipeline ingests, cleans, and analyzes a comprehensive Wind Turbine SCADA dataset from Kaggle. To satisfy project constraints and ensure a completely unique analytical contribution distinct from peer submissions, this project isolates the **Optimal Operating Range** ($8 \text{ m/s}$ to $12 \text{ m/s}$) where modern wind turbines exhibit peak structural efficiency and stable gearbox operations.

---

## 📂 Repository Architecture
The repository matches the mandated project file layout structure:
```text
EDS_[STUDENTNUMBER]_[SURNAME]/
├── data/
│   ├── dataset_original.csv   <- Original raw Kaggle SCADA data
│   └── dataset_cleaned.csv    <- Processed, deduplicated 8-12 m/s data slice
├── outputs/
│   ├── static_plot1.png       <- Power curve scatter visualization
│   ├── static_plot2.png       <- Active power timeline trend line
│   └── animation1.html        <- Animated performance tracker over time
├── main.py                    <- Modular Object-Oriented pipeline script
├── requirements.txt           <- Explicit environment package dependencies
└── README.md                  <- Project documentation webpage
```

---

## ⚙️ Execution Instructions
To replicate the environment parameters and run this pipeline from a clean terminal workspace:

1. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
2. **Execute Pipeline:**
   ```bash
   python main.py
   ```

---

## 📊 Summary Engineering Analysis
* **Unique Filtering Strategy:** Isolated steady-state operational wind velocities between $8.00 \text{ m/s}$ and $12.00 \text{ m/s}$, containing $13,405$ operational observations.
* **Mean Active Power Output:** $2,165.95 \text{ kW}$
* **Median Active Power Output:** $2,239.97 \text{ kW}$
* **Standard Deviation:** $811.69 \text{ kW}$

The data visualization portfolio saved inside `/outputs` details how the turbine power production tightly corresponds with steady-state wind changes, providing crucial metrics for scheduling gear-box preventative maintenance.
