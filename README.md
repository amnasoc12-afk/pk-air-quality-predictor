AI-Based Air Quality Predictor for Pakistani Cities
Predicting Air Quality Index (AQI) across major Pakistani cities using Machine Learning
This project connects to my earlier work on the 3D Air Purifier (UCP Science Fest 2023).
While the purifier was a physical solution to indoor air pollution, this project tackles
the same problem from a data-driven perspective — predicting when and where air quality
becomes dangerous, so cities can act before it's too late.
 Project Overview
Air pollution is one of Pakistan's most serious environmental challenges. Cities like Lahore consistently rank among the most polluted in the world, particularly during the November–February smog season. This project builds a machine learning model that predicts the Air Quality Index (AQI) for 6 major Pakistani cities based on weather and traffic data.
Project Structure
ai-air-quality-predictor

├── air_quality_predictor.py     
├── air_quality_data.csv         
├── eda_analysis.png            
├── model_comparison.png         
├── requirements.txt         
└── README.md                   
            
How to Run
Step 1 — Install Dependencies
pip install -r requirements.txt
Step 2 — Run the Project
python air_quality_predictor.py
That's it. The script will:
Generate the dataset and save it as CSV
Run Exploratory Data Analysis and save plots
Train and compare all 3 models
Show live AQI predictions for sample cities
Requirements
numpy
pandas
matplotlib
seaborn
scikit-learn
Or install via:
pip install -r requirements.txt

Live Prediction Example
The script includes a prediction function you can call directly:
predict_aqi(
    model=best_model,
    scaler=scaler,
    le=le,
    city="Lahore",
    month=12,           # December — smog season
    temperature=15,
    humidity=75,
    wind_speed=5,
    traffic_index=9     # Heavy traffic
)
Output:
─────────────────────────────────────────────
  🏙️  City          : Lahore
  📅 Month         : 12
  🌡️  Temperature   : 15.0°C
  💧 Humidity      : 75.0%
  💨 Wind Speed    : 5.0 km/h
  🚗 Traffic Index : 9.0/10
─────────────────────────────────────────────
  📊 Predicted AQI : 142.3
  📋 Category      : 🔴 Unhealthy
─────────────────────────────────────────────
Future Improvements
[ ] Use real-time data from Pakistan Meteorological Department (met.gov.pk)
[ ] Add more cities (Multan, Hyderabad, Quetta)
[ ] Integrate PM2.5 and PM10 as additional features
[ ] Build a simple web dashboard using Flask or Streamlit
[ ] Add time-series forecasting (predict next 7 days)
 Related Work
3D Air Purifier Project — UCP Science & Technology Fest 2023
(Physical solution → this project is the AI/data-driven follow-up)
 About the Author
Amna Shahid
ICS Physics | Punjab College, Lahore
Aspiring AI Researcher & Engineer
LinkedIn: linkedin.com/in/amna-shahid-6113b1372
Email: amnasoc.12@gmail.com
License
This project is open source — feel free to use, modify, and build upon
