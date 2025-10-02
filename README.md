# 🚀 Spaceship Titanic - Kaggle Competition

This repository contains my solution for the **[Kaggle Spaceship Titanic competition](https://www.kaggle.com/competitions/spaceship-titanic)**.  
The goal of this challenge is to predict whether a passenger was transported to an alternate dimension during the Spaceship Titanic disaster, based on various features such as demographics, spending patterns, and cabin information.  

---

## 📊 Results

- **Kaggle Public Leaderboard Rank:** 🏅 **635**  
- **Best Score (Accuracy):** `0.79845`  
- **Submissions:** `2`  
- **Time Spent:** `~3 months`  

---

## 👤 Author

- **Name:** Gagan Patel  

---

## 🛠️ Approach

### 1. Data Cleaning
- Handled missing values using median (for numerical features) and mode (for categorical features).  
- Filled missing expenses (RoomService, FoodCourt, ShoppingMall, Spa, VRDeck) with `0`.  
- Engineered missing `Cabin` values by splitting into **Deck, CabinNum, Side**.  
- Dropped irrelevant columns: `PassengerId`, `Name`, `Cabin`.  

### 2. Feature Engineering
- Created `GroupId` and `GroupSize` from `PassengerId`.  
- Created `TotalSpend` feature as the sum of all expenses.  
- Encoded categorical variables (`HomePlanet`, `Destination`, `Deck`, `Side`) using **Label Encoding**.  
- Converted boolean features (`CryoSleep`, `VIP`, `Transported`) into `0/1` format.  

### 3. Model Training
- **Baseline Model:** RandomForestClassifier → `0.8021` validation accuracy.  
- **Hyperparameter Tuning:** RandomizedSearchCV → Best CV Score ≈ `0.8003`.  
- **Final Model for Submission:** RandomForestClassifier with tuned parameters.  

### 4. Future Work
- Experiment with boosting models: **LightGBM, XGBoost, CatBoost**.  
- Try ensembling (stacking/blending multiple models).  
- Perform feature importance analysis and advanced feature engineering.  

---

## 📂 File Structure
├── spaceship_titanic.ipynb # Main notebook with code and analysis

├── submission.csv # Final Kaggle submission file

├── README.md # Project documentation


---

## 🚀 How to Run
1. Clone this repository.  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Run the notebook:
     jupyter notebook spaceship_titanic.ipynb
4. Generate predictions:
     python generate_submission.py
---

🏆 Acknowledgements

Kaggle & the Titanic Spaceship dataset.

Inspiration from classic Titanic survival prediction.

Kaggle community for EDA and baseline model insights.
