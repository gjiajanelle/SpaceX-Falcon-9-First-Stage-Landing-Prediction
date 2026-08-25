# **🚀 SpaceX Falcon 9 First Stage Landing Prediction**

An end-to-end data science project predicting whether the SpaceX Falcon 9 first stage will land successfully. By determining landing outcomes, this framework estimates launch costs—since booster reuse cuts launch costs from ~$62M down to ~$16.5M. 💰✨

This repository contains all the notebooks and Python files used in my final project for the Applied Data Science Capstone Course

## 📌 Project Overview

This capstone project follows the complete Data Science lifecycle:

1. 🌐 Data Collection: REST API integration and Wikipedia web scraping.
2. 🧹 Data Wrangling: Outcome classification and binary label generation ($1 = \text{Success}, 0 = \text{Failure}$).
3. 🔍 Exploratory Data Analysis (EDA): SQL queries and Pandas data aggregation.
4. 🗺️ Geospatial & Interactive Visualizations: Folium maps for site proximities and Plotly Dash dashboards.
5. 🤖 Machine Learning Classification: Training, tuning, and evaluating predictive models.

## 💡 Key Findings 

- 🌊 Launch Sites & Geography: All launch facilities (KSC LC-39A, CCAFS LC-40, VAFB SLC-4E) are located adjacent to coastlines ($<1\text{ km}$) for over-water trajectories and within $5\text{ km}$ of rail/highway networks for booster transit.
- 🏆 Launch Site Success: KSC LC-39A achieved the highest overall success rate ($76.9\%$) and contributed over $41.7\%$ of total successful landings across all sites.
- 📦 Payload Correlations: High payload masses ($>8,000\text{ kg}$) showed improved landing success, largely driven by mature booster versions (Block 5).

## 📊 Machine Learning Results

Four classification algorithms were tuned using `GridSearchCV` on standardized feature matrices (`StandardScaler`):

| 🧠 Model | ⚙️ Hyperparameter Tuning (`GridSearchCV`) | 🎯 Test Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | `penalty: l2`, `C: 0.01`, `solver: lbfgs` | **83.33%** |
| **Support Vector Machine (SVM)** | `kernel: sigmoid`, `C: 1.0`, `gamma: auto` | **83.33%** |
| **Decision Tree** | `criterion: gini`, `splitter: best`, `max_depth: 4` | **83.33%** |
| **K-Nearest Neighbors (KNN)** | `n_neighbors: 10`, `p: 2`, `algorithm: auto` | **83.33%** |

## 🛠️ Tech Stack

* 💻 **Languages:** Python, SQL
* 🐼 **Data Manipulation:** `pandas`, `numpy`, `sqlite3` / `sqlalchemy`
* 🌐 **Data Extraction:** `requests`, `beautifulsoup4`
* 📈 **Visualization:** `matplotlib`, `seaborn`, `folium`, `plotly`, `dash`
* 🤖 **Machine Learning:** `scikit-learn`

## 📂 Project Structure

```text
├── README.md
├── SpaceX_Machine Learning Prediction.ipynb       # Model training & hyperparameter tuning 🤖
├── edadataviz_ipynb.ipynb                        # EDA and data visualization with Pandas & Seaborn 📊
├── jupyter-labs-eda-sql-coursera_sqllite.ipynb   # SQL queries and statistical analysis 🗄️
├── jupyter-labs-spacex-data-collection-api.ipynb  # Data extraction via SpaceX REST API 🚀
├── jupyter-labs-webscraping_ipynb.ipynb          # Wikipedia web scraping for Falcon 9 data 🌐
├── lab_jupyter_launch_site_location.ipynb        # Geospatial analysis & proximity mapping with Folium 🗺️
├── labs-jupyter-spacex-Data wrangling.ipynb      # Data preprocessing & binary outcome conversion 🧼
└── plotly dash.pdf                               # Interactive Plotly Dash dashboard records 🖥️
```


## ⚡ How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/gjiajanelle/Final-Project.git](https://github.com/gjiajanelle/SpaceX-Falcon-9-First-Stage-Landing-Prediction.git)
   cd Final-Project
   ```

2. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn folium plotly dash scikit-learn requests beautifulsoup4 sqlalchemy
   ```

3. **Launch the Plotly Dash application:**
   ```bash
   python 6_spacex_dash_app.py
   ```

4. **Run Jupyter Notebooks:**
   ```bash
   jupyter notebook
   ```
