
# Golf Prediction Model

This project involves the development and training of a machine learning model to predict golf tournament outcomes, specifically focusing on top 5 and top 20 finishes for golfers. 
The model leverages various machine learning algorithms, including XGBoost, SVM, Logistic Regression, and Random Forest, to generate these predictions.


## Usage

1. **Prepare the Data:** The model expects cleaned and pre-processed data in a specific format. The data is read from an Excel file (`G.xlsx`) with the sheet name `RidgeTrain`.

2. **Train the Model:** Run the notebook to train the model. The data is split into training and testing sets (70/30 Split), and various machine learning models are trained and evaluated.

3. **Generate Predictions:** The model predicts the probability of each golfer finishing in the top 5 and top 20. The predictions are saved to a CSV file (`T5-T20.csv`).

### Running the Notebook

To run the notebook:

```bash
jupyter notebook Golf_Model_Train.ipynb
```

## Project Structure

```
├── Golf_Model_Train.ipynb    # Main Jupyter notebook containing the model training and prediction code
├── G.xlsx                    # Input data file (not included in the repository)
├── T5-T20.csv                # Output file containing the predictions
└── requirements.txt          # List of required Python packages
```

## Data

The data file (`G.xlsx`) contains historical performance data of golfers, which has been pre-processed and scaled. The sheet `RidgeTrain` is used to train and evaluate the models.

## Model Training

The following models are used in the training process:
- **XGBoost:** A gradient boosting model optimized for speed and performance.
- **SVM:** Support Vector Machine with RBF kernel for classification.
- **Logistic Regression:** A simple linear model for binary classification.
- **Random Forest:** An ensemble model that uses multiple decision trees.

### Hyperparameter Tuning

Hyperparameters for the Random Forest model are tuned using GridSearchCV to find the best parameters for the final model (Random Forest).

## Prediction Output

The final predictions are saved to `T5-T20.csv`, which contains:
- `Name`: The name of the golfer.
- `Top5`: Predicted probability of finishing in the top 5.
- `Top_20`: Predicted probability of finishing in the top 20.

