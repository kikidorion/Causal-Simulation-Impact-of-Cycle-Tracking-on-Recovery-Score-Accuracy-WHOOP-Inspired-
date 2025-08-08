# 🧪 Causal Simulation: Impact of Cycle Tracking on Recovery Score Accuracy (WHOOP-Inspired)

## 👩🏽‍💻 Project Overview
This project simulates a **causal inference** problem inspired by WHOOP’s work at the intersection of **wearable technology**, **biometric signal processing**, and **women’s health**.  
It evaluates whether WHOOP users who log their menstrual cycles experience improved accuracy in recovery score estimates — after adjusting for behavioral confounders like **health engagement** and **sleep quality**.  

This scenario mirrors **real-world observability and data quality challenges** faced by WHOOP’s analytics and data science teams.

---

## 🎯 Objectives
- Simulate observational data with **treatment–confounding bias**
- Estimate the true causal effect of menstrual cycle tracking using **causal forests**
- Visualize the distribution of **confounders** and **propensity scores**
- Diagnose **overlap issues** and adjust estimation strategies accordingly

---

## 📊 Key Variables

| Variable | Description |
|----------|-------------|
| `Treat`  | Binary indicator: whether user logs menstrual cycles |
| `Y`      | Observed recovery score accuracy (inverse error proxy) |
| `HE`     | Health Engagement (journal use, app logins) |
| `SQ`     | Sleep Quality (aggregated nightly score) |

---

## 🧠 Why This Matters
**For WHOOP’s Senior Observability Analyst role:**
- Understands how user engagement impacts signal reliability
- Detects and visualizes bias in **observational biometric data**
- Applies causal methods to improve metric fidelity when logging gaps exist

**For WHOOP’s Data Scientist I – Women’s Health:**
- Models the interaction between behavioral and physiological inputs
- Uses **Generalized Random Forests** to isolate behavioral effects
- Shows sensitivity to **gender-specific signal variance** (e.g., cycle data quality)

---

## 💻 Methods
- `grf::causal_forest()` used to estimate treatment effects adjusting for confounders  
- `ggplot2` visualizations to illustrate **confounding** and **overlap**  
- **Propensity score modeling** to diagnose areas with poor identifiability  

---

## 📎 Files
- `simulation.Rmd` – Full annotated simulation and analysis
- `README.md` – Project summary (this file)
- `figures/` – Visual outputs (if saved)

---

## 🧪 Sample Output
```r
[1] "Estimated ATE (Causal Forest): 1.97"
[1] "True ATE: 2"
