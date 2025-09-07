**🏀 NBA MVP Predictor**

This project predicts the NBA Most Valuable Player (MVP) award using historical player statistics and machine learning. By leveraging player-level data from 1982 to 2025, the model identifies patterns in performance that best correlate with MVP outcomes.

**📊 Dataset**

Seasons: 1982–2022

Source: https://www.kaggle.com/datasets/robertsunderhaft/nba-player-season-statistics-with-mvp-win-share

Data includes:

Player statistics (points, rebounds, assists, advanced stats, etc.)

Team performance (win-loss records)

MVP award shares (for supervised training)

**⚙️ Feature Engineering**

To improve prediction accuracy, several custom features and preprocessing steps were introduced:

  **🧹 Data Cleaning**

    - Player names were standardized (e.g., fixing encoding issues like "Luka Don?i?" → "Luka Doncic").
  
    - Missing values handled through imputation or dropping when necessary.
  
    - Train/test splits aligned to avoid data leakage.

  **📐 Feature Construction**

    - Positional Encoding
    
    - Players’ positions were converted into categorical encodings.
    
    - One-hot encoding or numerical mapping was used to incorporate positional effects (point guards dont need to rebound,          centers dont need to assist, etc)
    
    - A season column added to account for temporal trends (pace changes, 3-point era, etc.).

**🧠 Model Training**

  - Training Set: 1982–2018

  - Testing Set: 2019–2022

**📈 Results**

  - Strong correlation between predicted award shares and actual MVP shares.

  - Model successfully identifies top MVP candidates in most seasons.

  **- Key predictive features:**

    - Player efficiency metrics (PER, WS, BPM)

    -Team win percentage

