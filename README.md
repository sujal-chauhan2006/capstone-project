
# Clinic Appointment No-Show Prediction

## About the Project

This project is about predicting whether a patient will miss their clinic appointment. It uses Python, SQL, Machine Learning, and Gemini API to analyse appointment data and understand the reasons behind missed appointments.

## Tools Used

- Python
- Google Colab
- Pandas, NumPy, Matplotlib, Seaborn
- MySQL Workbench
- Scikit-learn
- Google Gemini API

## Project Files

- `01_ingest_clean.ipynb` – Clean the data and prepare clinic information.
- `02_queries.sql` – Create database tables and perform SQL queries.
- `03_model.ipynb` – Train and evaluate Machine Learning models.
- `04_genai.ipynb` – Analyse patient notes using Gemini API.
- `Datasets/` – Contains the original CSV files.
- `appointments_clean.csv` – Cleaned appointment data.
- `clinics_enriched.csv` – Clinic data with weather information.
- `load_data.sql` – SQL commands to load the prepared data.
- `test_risk_scores.csv` – Final prediction results.
- `notes_analysed.csv` – Results of patient note analysis.

## How to Run the Project

Follow the steps in the same order.

### Step 1: Data Cleaning

1. Open Google Colab.
2. Upload and open `01_ingest_clean.ipynb`.
3. Upload the required CSV files from the `Datasets` folder.
4. Make sure the file names and paths match the notebook.

   Use these names in Colab:
   - `Datasets/followup_notes.csv` → `appointment_records.csv`
   - `Datasets/clinics.csv` → `clinic_records.csv`
   - `Datasets/appointments.csv` → `followup_notes.csv`

5. Run the notebook cells from top to bottom.
6. This step creates `appointments_clean.csv`, `clinics_enriched.csv`, and `load_data.sql`.

### Step 2: SQL Analysis

1. Open MySQL Workbench.
2. Open `02_queries.sql`.
3. Execute the SQL script on a fresh database.
4. Run the queries in order to see the appointment analysis.
5. Check the results of each query.

**Note:** Avoid running the duplicate appointment INSERT statement near the end of the SQL file. Also, do not execute the same INSERT statements repeatedly, as they can create duplicate-key errors.

### Step 3: Machine Learning

1. Open Google Colab.
2. Upload and open `03_model.ipynb`.
3. Upload `appointments_clean.csv`.
4. Run all cells from top to bottom.
5. The notebook trains and compares different Machine Learning models.
6. It also generates `test_risk_scores.csv`.

### Step 4: Generative AI Analysis

1. Open Google Colab.
2. Upload and open `04_genai.ipynb`.
3. Upload the follow-up notes CSV as `followup_notes.csv`.
4. Add your Gemini API key when requested.
5. Run the notebook cells in order.
6. The notebook analyses patient notes and generates `notes_analysed.csv`.

**Note:** Gemini API has usage limits. If you get a quota error (429), wait until the quota resets. A 503 error usually means the service is temporarily unavailable.

## Final Output

After completing all four steps, the project provides:

- Cleaned appointment and clinic data.
- SQL-based appointment analysis.
- Machine Learning models for predicting appointment no-shows.
- Risk scores for test appointments.
- AI-generated analysis of patient follow-up notes.

## Important

- Run the notebooks in the given order.
- Make sure all required CSV files are uploaded before running the notebooks.
- Run SQL scripts only when the required database and tables are ready.
- Keep your Gemini API key private.
