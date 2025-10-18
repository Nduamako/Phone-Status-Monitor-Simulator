# 📱 Phone Status Monitor Simulator

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Notebook](https://img.shields.io/badge/notebook-Jupyter-orange.svg)](#)

A friendly, beginner-focused Python OOP simulator of a mobile phone that tracks **battery**, **balance**, and **data** — with actions like charging, topping up, buying data, calling, and browsing.

---

## 🔑 Features

- **Battery Monitoring** — charge by minutes or percent, with a visual battery bar  
- **Balance Tracking** — top up in dollars and spend on calls or data  
- **Data Management** — buy data bundles using balance ($1 → 2 MB by default)  
- **Call Simulation** — make calls that deduct balance and battery  
- **Browsing Simulation** — simulate browsing intensity: _light_, _normal_, _heavy_  
- **Status Display** — concise phone status with progress bar

---

## 🎯 Learning Goals

This project demonstrates Object-Oriented Programming (OOP) fundamentals:

- Classes as blueprints  
- Objects representing real-world things (a phone)  
- Attributes holding state (battery, balance, data)  
- Methods modeling actions (charge, call, browse)

---

## ▶️ Quick Start (example)

```python
from phone import Phone   # or the name of your module / notebook cell

# Create a phone for "Alex"
p = Phone(owner="Alex", battery=45, balance=5.0, data_mb=10)

p.status()                 # show current state
p.top_up(10)               # add $10
p.buy_data(3)              # spend $3 -> gains MB (based on DATA_MB_PER_DOLLAR)
p.call(4)                  # call for 4 minutes
p.browse(5, profile="light")  # browse for 5 minutes on light profile
p.charge(minutes=20)       # charge for 20 minutes
p.status()
