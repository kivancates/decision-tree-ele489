
# Banknote Authentication using Decision Tree Classifier

This project aims to classify banknotes as **authentic** or **fake banknotes** using the **variance**, **skewness**, **kurtosis** and **entropy** features used in the classification of images. This classification is done using the **Decision Tree** model.

## Dataset Overview

Using wavelet transforms, features were taken from images of real and counterfeit banknotes to create the dataset utilized in this project.  The following columns are included in it:

- **Variance**
- **Skewness**
- **Kurtosis**
- **Entropy**
- **Class** (0 = Fake, 1 = Real)

Dataset: [`data_banknote_authentication.txt`](https://archive.ics.uci.edu/dataset/267/banknote+authentication)

---

## Objective

The aim of this project is to try to create the most optimum model by using different parameters (such as **max_depth**, **min_samples_split**, and **criterion**) and to observe the different trees created. Also, one of the aims of the project is to observe which feature is important in creating the model.

---

## Key Steps

1. **Data Loading & Exploration**:
   - Visualized pairwise relationships using `seaborn.pairplot()`.
   - Identified clear separability between classes in some feature pairs.

2. **Preprocessing**:
   - Split data into training (80%) and testing (20%) sets.

3. **Model Training**:
   - To train model we used `DecisionTreeClassifier` from `sklearn.tree`.
   - The model was trained by giving different values ​​to the **max_depth**, **min_samples_split**, and **criterion** parameters.

4. **Evaluation**:
   - Accuracy score, Classification report (Precision, Recall, F1-score) and Confusion matrix were observed for different models.

5. **Visualization**:
   - `plot_tree()` is used to observe the Full Decision Tree.
   - `feature_importances_` is used to observe the Feature Importance plot.
---

## Results

- **Accuracy**: ~`0.9927` (The highest value observed) 
- Most important features:
  - Variance (the most important) 
  - Skewness
  - Kurtosis
  *(These are based on `feature_importances_` results)*


## Key Takeaways

- Decision Trees work well on small-to-medium-sized tabular datasets.
- Controlling `max_depth` and `min_samples_split` helps prevent overfitting.
- Visual tools like `plot_tree()` and feature importance plots greatly aid interpretability.

---


## Requirements
The code 'tree.ipynb' must be imported into the Google Collab environment and the file [`data_banknote_authentication.txt`] must be uploaded to the Google Collab environment via Google Drive.
```
