## 📂 Repository Architecture
The repository has been updated to match the strict project requirements:
```text
EDS_[STUDENTNUMBER]_[SURNAME]/
├── data/
│   ├── dataset_original.csv   <- Original raw Kaggle SCADA data
│   └── dataset_cleaned.csv    <- Processed, deduplicated 8-12 m/s data slice
├── outputs/
│   ├── static_plot1.png       <- Power curve scatter visualization
│   ├── static_plot2.png       <- Active power timeline trend line
│   ├── static_plot3.png       <- Power output distribution histogram
│   ├── animation1.html        <- Animated power output tracker over time
│   └── animation2.html        <- Animated wind velocity direction tracking
├── main.py                    <- Modular Object-Oriented pipeline script
├── requirements.txt           <- Explicit environment package dependencies
└── README.md                  <- Project documentation webpage
```

Save, commit, and push this change using your terminal:
```bash
git add README.md
git commit -m "docs: sync readme directory map with final 5-plot submission parameters"
git push origin main
```

---

### 📄 Step 2: Submission Report / Paper Template

To save you time on your project documentation paper, here is a highly technical, structured report template based on your actual data outputs and the curriculum mapping framework outlined in your reference paper. 

Copy this text into your word processor (like Google Docs or MS Word) and fill in your details:

***

# ENGINEERING PROJECT REPORT
**Project Title:** Modular Data Pipeline for Wind Turbine SCADA Performance and Analytics  
**Course Code:** Engineering Data Systems (EDS)  
**Topic Reference:** RMS-01: Wind Turbine Gearbox Vibration  
**Academic Framework Reference:** Madrigal & Cabatuan (2026) OBE Automation Guidelines  

---

### I. INTRODUCTION & PROBLEM FRAMEWORK
Industrial data pipelines in renewable energy systems face critical bottlenecks due to data noise, sensor anomalies, and subjective analysis slices. In professional environments, manual data extraction impedes continuous engineering evaluations. This project develops a completely automated, object-oriented software engine written in Python to ingest, parse, filter, and structurally evaluate a year-long Wind Turbine SCADA dataset consisting of 50,530 technical records.

To enforce algorithmic uniqueness and simulate specialized engineering conditions, a distinct operational envelope filter was designed. While standard evaluations look exclusively at peak storm thresholds, this investigation targets the **Optimal Operating Range** ($8.00 \text{ m/s}$ to $12.00 \text{ m/s}$). This boundary isolates steady-state torque environments where gearbox component stresses are highly predictive for preventative maintenance cycles.

---

### II. METHODOLOGICAL IMPLEMENTATION
Following the multi-stage pipelines found in production data engineering, a four-stage execution architecture was deployed inside a compiled execution block (`main.py`):

1. **Ingestion Engine:** Employs a defensive programming framework checking file system path constraints using the `os` and `pandas` libraries before committing raw binary allocations to system memory.
2. **Data Sanitation & Filter Realization:** Resolves missing entries (`.dropna()`) and multi-sensor collisions (`.drop_duplicates()`). Converts scalar date strings into real datetime objects and slices the operational envelope using a strict numerical conditional bitwise mask ($8.00 \le V \le 12.00 \text{ m/s}$).
3. **NumPy Mathematical Pipeline:** Extracts data vectors into memory-optimized NumPy matrices. It calculates key statistics without higher-level abstraction layers to maintain low execution latencies.
4. **Visualization Core:** Auto-generates three high-fidelity static image arrays and compiles two production-grade multi-temporal HTML web animations to visualize multi-variable shifts over time.

---

### III. EMPIRICAL RESULTS & MATHEMATICAL METRICS
The data pipeline was executed over the full raw dataset, isolating **13,405 rows** of steady-state operational data. The mathematical computations on the active power vector (`LV ActivePower (kW)`) yielded the following definitive engineering parameters:

$$\text{Minimum Operational Wind Speed} = 8.00 \text{ m/s}$$
$$\text{Maximum Operational Wind Speed} = 12.00 \text{ m/s}$$
$$\text{Mean Active Power Output } (\mu) = 2,165.95 \text{ kW}$$
$$\text{Median Active Power Output } (\tilde{x}) = 2,239.97 \text{ kW}$$
$$\text{Standard Deviation } (\sigma) = 811.69 \text{ kW}$$

The minor left-skewness between the mean and the median indicates that within the $8\text{–}12 \text{ m/s}$ wind window, the turbine is running efficiently and consistently approaching its optimal operational yield capacity.

---

### IV. VISUALIZATION PORTFOLIO BREAKDOWN
The portfolio saved within the `/outputs` folder includes:
* **`static_plot1.png`:** A scatter plot mapping the relationship between wind velocity and power generation within our target filter window.
* **`static_plot2.png`:** A continuous line tracking turbine power outputs over time.
* **`static_plot3.png`:** A frequency histogram confirming that power production trends heavily toward the maximum bounds of its capacity.
* **`animation1.html`:** An interactive, animated scatter tracking window that maps active power generation changes alongside directional wind shifts.
* **`animation2.html`:** A temporal animation showing wind direction shifts across the operational wind speed domain.
