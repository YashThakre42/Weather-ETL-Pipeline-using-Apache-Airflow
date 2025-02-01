# Weather-ETL-Pipeline-using-Apache-Airflow
How to Set Up & Run

1️⃣ Clone the Repository
sh
Copy
Edit
git clone https://github.com/yourusername/weather-etl-pipeline.git
cd weather-etl-pipeline

2️⃣ Install Dependencies
sh
Copy
Edit
pip install -r requirements.txt

3️⃣ Set Up Airflow
sh
Copy
Edit
export AIRFLOW_HOME=~/airflow
airflow db init
airflow webserver --port 8080
airflow scheduler

4️⃣ Add Airflow Connections
PostgreSQL Connection
Go to Airflow UI (localhost:8080)
Navigate to Admin > Connections
Add a new connection:
Connection ID: postgres_default
Connection Type: Postgres
Host: localhost
Schema: weather_db
Login: your_username
Password: your_password
Port: 5432
API Connection (Open-Meteo)
Add a new HTTP connection:
Connection ID: open_meteo_api
Connection Type: HTTP
Host: https://api.open-meteo.com

5️⃣ Trigger DAG in Airflow
Open Airflow UI (localhost:8080)
Search for "weather_etl_pipeline"
Click Trigger DAG 🚀
