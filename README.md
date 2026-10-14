# Urban Water Leakage & Consumption Analytics

**Level:** Intermediate  
**Tools:** Python, Pandas, NumPy, MySQL, Power BI  
**Dataset:** 25,000 synthetic records (500 houses × 50 days)

> The data is simulated for learning. A high-consumption alert indicates a record for investigation; it does not prove that a physical leak exists.

## Project question
Can we summarize water usage by house, date, and area, and flag unusually high readings for further inspection?

## Folder structure
- `data/water_consumption.csv` — ready-to-use synthetic dataset
- `src/generate_data.py` — regenerate the dataset (fixed random seed)
- `src/analyze_data.py` — clean data, calculate rolling-median alerts, export summaries
- `sql/analysis_queries.sql` — MySQL table definition and analysis queries
- `docs/power_bi_guide.md` — dashboard build steps and DAX measures
- `docs/interview_prep.md` — project explanation and interview questions
- `requirements.txt` — Python dependencies

## Run it
1. Install Python 3.10+.
2. Open a terminal in this folder.
3. Install packages: `python -m pip install -r requirements.txt`
4. Generate data: `python src/generate_data.py`
5. Analyze data: `python src/analyze_data.py`
6. Review the CSV files in `outputs/`.

The ready-to-use dataset is already in `data/`, so you can skip step 4 if you don't want to regenerate it.

## SQL
1. Open MySQL Workbench and connect to your local MySQL server.
2. Open `sql/analysis_queries.sql`.
3. Run the database/table creation statements.
4. Import `data/water_consumption.csv` into `water_analytics.water_consumption` with Table Data Import Wizard.
5. Run the analysis queries. If the import wizard detects a type incorrectly, map the columns to the types in the CREATE TABLE statement.

## Power BI
Follow `docs/power_bi_guide.md`. You can import the CSV directly using **Home > Get data > Text/CSV** or connect Power BI Desktop to MySQL if the MySQL connector/driver is configured.

## Suggested portfolio description
Built an end-to-end water consumption analytics project using Python, Pandas, MySQL, and Power BI. Generated 25,000 synthetic daily readings across 500 houses, cleaned and summarized consumption data, compared usage by date and area, and implemented a rolling-median anomaly rule to flag unusual readings for investigation. Designed an interactive dashboard to monitor consumption patterns and high-risk readings.

Only claim tasks you have actually run and understood.
