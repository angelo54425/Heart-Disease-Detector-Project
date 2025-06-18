# Heart-Disease-Detector-Project
## Problem Statement

Heart disease remains a leading global cause of death, especially in low-resource regions lacking early diagnostic tools. Existing clinical methods are often manual, subjective, and inaccessible. This project develops a machine learning model to predict heart disease using patient clinical data. It aims to support early detection and improve diagnostic efficiency in underserved healthcare systems.

## Objectives

- **Improve Diagnosis Accuracy**: Utilize AI algorithms to analyze patient data and identify potential heart disease indicators with higher precision than traditional methods.
- **Speed Up Diagnosis Process**: Reduce the time required for diagnosis by automating data analysis, allowing healthcare professionals to focus on patient care.

- **Data-Driven Insights**: Generate actionable insights from large datasets, helping to inform treatment decisions and preventive measures.

### Model Training Results Table

The table below summarizes the performance of various neural network configurations tested for heart disease prediction. Each row represents a different experiment, detailing the optimizer, regularization method, learning rate, and other hyperparameters used, along with the resulting accuracy, F1 score, recall, precision, and loss. This comparison helps identify which model setup yields the best predictive performance for the dataset.

| Instance | Model          | Optimizer | Regularization | Epochs | Early Stopping | Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision | Loss   |
|----------|----------------|-----------|----------------|--------|----------------|--------|----------------|----------|----------|--------|-----------|--------|
| 1        | Neural Network | SGD       | None           | 100    | No             | 3      | 0.001          | 0.783    | 0.780    | 0.783  | 0.785     | 7.836  |
| 2        | Neural Network | Adam      | L2             | 200    | No             | 3      | 0.001          | 0.761    | 0.760    | 0.761  | 0.789     | 8.619  |
| 3        | Neural Network | Adam      | L1             | 200    | Yes            | 3      | 0.001          | 0.790    | 0.791    | 0.790  | 0.795     | 7.574  |
| 4        | Neural Network | RMSprop   | L2             | 200    | Yes            | 3      | 0.0005         | 0.710    | 0.684    | 0.710  | 0.755     | 10.447 |
| 5        | Neural Network | Adam      | L2             | 200    | Yes            | 3      | 0.0004         | 0.804    | 0.805    | 0.804  | 0.808     | 7.052  |

## Results Summary

**Instance 1:**  
Used SGD optimizer without regularization or early stopping. Achieved moderate accuracy (0.783) and F1 score (0.780). The lack of regularization and early stopping may have limited its ability to generalize, resulting in higher loss.

**Instance 2:**  
Switched to Adam optimizer with L2 regularization but no early stopping. Accuracy (0.761) and F1 score (0.760) slightly decreased compared to Instance 1, possibly due to overfitting from the absence of early stopping, despite regularization.

**Instance 3:**  
Used Adam optimizer with L1 regularization and early stopping. Accuracy (0.790) and F1 score (0.791) improved, and loss decreased. Early stopping likely helped prevent overfitting, while L1 regularization promoted sparsity in the model.

**Instance 4:**  
Tested RMSprop optimizer with L2 regularization and early stopping, but with a lower learning rate (0.0005). This configuration resulted in the lowest accuracy (0.710) and highest loss (10.447), suggesting that the optimizer and learning rate combination was less effective for this dataset.

**Instance 5:**  
Adam optimizer with L2 regularization, early stopping, and the lowest learning rate (0.0004). This model achieved the best accuracy (0.804) and F1 score (0.805), and the lowest loss (7.052). The combination of Adam, L2 regularization, early stopping, and careful learning rate tuning contributed to optimal generalization and performance.

**Instance 5 performed the best among all configurations.**  
It achieved the highest accuracy (0.804), F1 score (0.805), and the lowest loss (7.052). This superior performance is attributed to the use of the Adam optimizer, L2 regularization, early stopping, and a carefully tuned low learning rate (0.0004). These factors together helped the model generalize well, avoid overfitting, and optimize learning efficiency, making Instance 5 the most effective setup for heart disease prediction in this project.

Overall, models with early stopping and regularization performed better, highlighting the importance of preventing overfitting. The Adam optimizer, especially with L2 regularization and a well-chosen learning rate, yielded the best results for heart disease prediction in this study.


## How to Run the Notebook

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Required Python packages (install with `pip install -r requirements.txt`)

### Running the Notebook

1. Clone the repository:
    ```bash
    git clone https://github.com/angelo54425/Heart-Disease-Detector-Project.git
    cd Heart-Disease-Detector-Project
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Launch Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
    Open the main notebook (e.g., `Heart_Disease_Detector.ipynb`) in your browser.

4. Run all cells in the notebook to train and evaluate the models.


# Video
**Watch:** [Presentation Video](https://youtu.be/FBgzpOTOVbk))