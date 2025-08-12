# ⚽ Football Match Outcome & Scoreline Prediction

This project predicts the **winner/loser** and **scoreline** of English Premier League (EPL) matches using historical match data from **football-data.org** and **Understat** (xG statistics).

## 📂 Project Structure

├── data                              # Merged dataset (Football-Data + Understat)
- data_scrapper.ipynb  
├── model                              # Main Jupyter Notebook with model training
- model.ipynb                       
├── README.md                                              # Project documentation


## 🚀 Features

* Predicts **match outcome**: Home Win, Away Win, or Draw.
* Predicts **exact scoreline** (home and away goals).
* Uses **Expected Goals (xG)** and other team statistics for better accuracy.
* Trained on **last two seasons** of EPL data.

## 📊 Data Sources

1. **[Football-Data.org](https://www.football-data.org/)** – Official match results & metadata.
2. **[Understat](https://understat.com/)** – Advanced metrics like Expected Goals (xG) & Expected Goals Against (xGA).


## 🛠 Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/football-prediction.git
cd football-prediction

# Install dependencies
pip install -r requirements.txt
```

**requirements.txt**

```
pandas
numpy
scikit-learn
```

## 📖 Usage

1. Open the **Jupyter Notebook**:

   jupyter notebook model.ipynb
   

2. Train the model:

   * The notebook will load and preprocess the dataset.
   * A **MultiOutput Random Forest Regressor** will be trained to predict both home and away goals.

3. Predict a match:

   python:

   result = predict_match("Manchester United FC", "Liverpool FC")
   print(result)
   # Example Output:
   # {'Predicted Outcome': 'Draw', 'Predicted Scoreline': 'Manchester United FC 1 - 1 Liverpool FC'}
   


## 🔮 How It Works

* **Model Type**: MultiOutput Random Forest Regressor
* **Inputs**: Encoded team names, xG, xGA stats from past matches.
* **Outputs**: Predicted Home Goals & Away Goals.
* **Outcome Decision**: Based on predicted scores.

## 📌 Notes

* The model is trained only on **last two seasons** – predictions may be less accurate for teams with major changes (e.g., transfers, new managers).
* Can be improved by **weighting recent head-to-head matches** more heavily.

