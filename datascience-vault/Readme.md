# 🌑 Data Science Library Guide

<div align="center">

### *Minimal • Dark • Professional*

**Created by: Arun VK**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=flat-square)](https://www.python.org/)
[![Data Science](https://img.shields.io/badge/Data-Science-blueviolet.svg?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg?style=flat-square)]()

</div>

---

## 🖤 Overview

Data Science is the art and science of extracting insights from data through statistical analysis, visualization, and computational methods. The right libraries can transform raw data into actionable intelligence, making complex analyses simple and efficient.

This guide provides a curated collection of essential **Data Science libraries** — from data manipulation and statistical analysis to advanced visualization and big data processing. Each tool is chosen for its power, reliability, and real-world utility.

Dark-themed. Minimal. Data-driven.

---

## 📚 Library Categories

### 1️⃣ Data Handling & Manipulation

| Library | Description | Install |
|---------|-------------|---------|
| **NumPy** | Array computing | `pip install numpy` |
| **Pandas** | DataFrames & cleaning | `pip install pandas` |
| **Polars** | Faster alternative to Pandas | `pip install polars` |
| **Dask** | Distributed data processing | `pip install dask` |
| **PyArrow** | Columnar memory format | `pip install pyarrow` |

---

### 2️⃣ Statistical Analysis

| Library | Description | Install |
|---------|-------------|---------|
| **SciPy** | Stats, optimization | `pip install scipy` |
| **Statsmodels** | Stats, time-series | `pip install statsmodels` |

---

### 3️⃣ Visualization

| Library | Description | Install |
|---------|-------------|---------|
| **Matplotlib** | Basic plotting | `pip install matplotlib` |
| **Seaborn** | Statistical plotting | `pip install seaborn` |
| **Plotly** | Interactive charts | `pip install plotly` |
| **Bokeh** | Web-based visualization | `pip install bokeh` |

---

### 4️⃣ Data Engineering / Processing

| Library | Description | Install |
|---------|-------------|---------|
| **PySpark** | Big data handling | `pip install pyspark` |
| **Vaex** | Out-of-core DataFrames | `pip install vaex` |

---

## 🚀 Install All at Once

```bash
pip install numpy pandas polars dask pyarrow scipy statsmodels matplotlib seaborn plotly bokeh pyspark vaex
```

---

## 💡 Quick Start

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load data
df = pd.read_csv('data.csv')

# Analyze
print(df.describe())

# Visualize
sns.histplot(df['column'])
plt.show()
```

---

## 📋 Requirements

- Python 3.8 or higher
- pip (Python package installer)
- Virtual environment recommended

---

## 🎯 Use Cases

- **Data Analysis**: Pandas, NumPy, SciPy
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Big Data**: PySpark, Dask, Vaex
- **Statistical Modeling**: Statsmodels, SciPy

---

## 🔗 Resources

- [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/)
- [Kaggle Learn](https://www.kaggle.com/learn)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/)

---

## 📄 License

MIT License - Free to use and modify.

---

<div align="center">

**Made with 🖤 by Arun VK**

*"In data we trust, in code we execute."*

---

🌑 **Dark theme. Clean code. Better insights.**

</div>