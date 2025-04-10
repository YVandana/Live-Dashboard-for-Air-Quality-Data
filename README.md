# Live Air Quality Dashboard

**A real-time and historical air quality monitoring dashboard built with Python, Dash, Plotly, and DuckDB.**

## 📌 Overview
This project is a **live-updating dashboard** that visualizes air quality data from **OpenAQ** (or other sources). It processes both **real-time and historical** air pollution data, stores it efficiently using **DuckDB**, and presents it in an interactive **Dash (Plotly) dashboard**.

Key features:
✅ **Real-time data updates** (pollutant levels, AQI, trends)
✅ **Historical data analysis** (time-series trends, comparisons)
✅ **Scalable data pipeline** (easily add new locations without downtime)
✅ **Efficient storage** with **DuckDB** (fast querying, low overhead)
✅ **Interactive visualizations** with **Plotly & Dash**

## 🛠️ Technologies Used
| Category       | Tools/Libraries |
|---------------|----------------|
| **Backend**   | Python, DuckDB (for lightweight SQL-based storage) |
| **Dashboard** | Plotly, Dash (for interactive web visualizations) |
| **Data Tools**| Pandas (data processing), DBeaver (DB management) |
| **Data Source**| OpenAQ API (or other air quality APIs) |

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/YVandana/Live-Dashboard-for-Air-Quality-Data.git
cd Live-Dashboard-for-Air-Quality-Data
```

### 2. Set Up a Virtual Environment (Recommended)
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
.\venv\Scripts\activate   # Windows
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Data Sources
- Rename `config.example.py` to `config.py` and add your **OpenAQ API key** (if required)
- Modify `data_pipeline.py` to adjust data fetching intervals or locations

### 5. Run the Dashboard
```bash
python app.py
```
Visit **http://127.0.0.1:8050/** in your browser

## 🔧 How It Works

### 📂 Data Pipeline
1. **Fetching Data**
   - The app pulls **real-time air quality data** from OpenAQ (or another source)
   - Historical data is stored in **DuckDB** for fast querying

2. **Processing & Storing**
   - Data is cleaned and structured using **Pandas**
   - DuckDB provides **lightweight, SQL-based storage** (no need for a full DB server)

3. **Dashboard Updates**
   - The **Dash app** refreshes at a set interval (e.g., every 10 minutes)
   - Users can filter by:
     - **Location** (city, country)
     - **Time range** (last 24h, 7 days, custom range)
     - **Pollutants** (PM2.5, PM10, O₃, NO₂, etc.)

### 📊 Dashboard Features
✔ **Live AQI (Air Quality Index) gauge**
✔ **Time-series trends** for pollutants
✔ **Geographical heatmap** (if location data is available)
✔ **Comparison between multiple stations**
✔ **Export data** (CSV/JSON)

## 📈 Adding New Locations
The pipeline is designed to **dynamically include new air quality stations** without restarting.

1. **Edit `config.py`** to include new city/station IDs
2. The **data fetcher** will automatically incorporate them in the next update cycle
3. The dashboard will show them in the **location dropdown**

## 🤝 Contributing
Want to improve this project? Contributions are welcome!
1. **Fork** the repository
2. Create a **new branch** (`git checkout -b feature/new-location-support`)
3. **Commit** your changes (`git commit -m "Add support for new data source"`)
4. **Push** to the branch (`git push origin feature/new-location-support`)
5. Open a **Pull Request**

## 📬 Contact
For questions or feedback:
📧 Email: [vandanayalla321@gmail.com]

## 🔗 Reference Tools
- [OpenAQ](https://openaq.org/) – Open air quality data
- [DuckDB](https://duckdb.org/) – Lightweight analytical database
- [Plotly Dash](https://plotly.com/dash/) – Dashboard framework

---

**Enjoy monitoring air quality in real-time! 🌍💨**
