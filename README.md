# Book Recommendation System

This repository contains a complete workflow for building a **book
recommendation engine** using collaborative filtering techniques
implemented with the **Surprise** library.\
It includes preprocessing, exploratory analysis, model comparison,
evaluation, and final conclusions.

------------------------------------------------------------------------

## 📚 Dataset Overview

The project uses three main files:

-   **Books.csv** -- book metadata (title, author, year, publisher,
    cover URLs)
-   **Ratings.csv** -- user ratings for books
-   **Users.csv** (if present) -- demographic metadata (not used in
    modeling)

### Key Stats After Cleaning

-   **1,149,780** original ratings\
-   **271,360** books\
-   **105,283** users\
-   After removing invalid ISBNs and all **0‑ratings**: **\~433,671**
    usable rating rows remain.

------------------------------------------------------------------------

## 🧼 Data Preparation

Main preprocessing steps:

-   Merged book metadata with the ratings file.
-   Detected that **0 ratings dominated the distribution**, so they were
    removed to avoid bias.
-   Identified missing or invalid ISBNs that didn't match any book in
    the catalog.
-   Ensured consistent dtypes and indexing for Surprise models.
-   Computed rating distributions and user/book activity.

### Key Observations

-   The dataset is **highly sparse**, with most users rating very few
    books.
-   Most books receive **0--1 ratings**, indicating long‑tail behavior.
-   The most common rating (after filtering) is **8**.
-   Removing 0 ratings greatly improved the meaningfulness of the
    training set.

------------------------------------------------------------------------

## 🤖 Models Used & Comparison

Several collaborative filtering algorithms were trained and evaluated.\
All models were assessed using **RMSE, Precision, Recall, and F1
score**.

  ------------------------------------------------------------------------------------
  Model             Description       RMSE         Precision       Recall     F1
  ----------------- ----------------- ------------ --------------- ---------- --------
  **KNNBasic**      User--item        **1.8455**   1.0             0.941      0.97
                    similarity                                                
                    (default KNN)                                             

  **KNN (cosine     Custom similarity **1.6866**   1.0             0.941      0.97
  similarity)**     matrix                                                    

  **KNN (tuned)**   Improved          **1.6210**   1.0             0.941      0.97
                    similarity +                                              
                    parameters                                                

  **KNNBaseline**   Includes          **1.5882**   1.0             0.941      0.97
                    user/item biases                                          

  **SVD             Matrix            **1.5106**   1.0             0.941      0.97
  (baseline)**      factorization                                             

  **SVD (tuned)**   Final optimized   **1.5026**   1.0             0.941      0.97
                    model                                                     
  ------------------------------------------------------------------------------------

### Model Comparison Summary

-   **KNNBasic performed the worst** (highest RMSE), likely due to
    sparse user--item matrices.
-   **Similarity‑based KNN models improved with tuning**, especially
    when adjusting the similarity metric.
-   **Bias‑adjusted KNNBaseline** performed substantially better than
    raw KNN.
-   **SVD significantly outperformed all KNN variants**, as matrix
    factorization handles sparsity more effectively.
-   **Tuned SVD achieved the best overall results**, making it the
    chosen model for generating recommendations.

------------------------------------------------------------------------

## 🏆 Final Model: Tuned SVD

The final model was selected based on best‑in‑class RMSE while
maintaining perfect precision and high recall.

    RMSE: 1.5026  
    Precision: 1.0  
    Recall: 0.941  
    F1: 0.97

### Why SVD Won

-   Handles sparse rating matrices better than neighborhood‑based
    models.
-   Learns latent factors representing user/book preferences.
-   More robust against users with very few ratings.
-   Hyperparameter tuning further reduced prediction error.

------------------------------------------------------------------------

## 📌 Conclusions

From the notebook's final conclusions:

-   **Rating cleanup (removing 0‑ratings) dramatically improves model
    performance.**
-   **SVD is the most effective model for this dataset**, outperforming
    all KNN variants in RMSE.
-   **Precision is consistently perfect across models**, but RMSE
    distinguishes quality.
-   The dataset remains extremely sparse; hybrid or content‑based
    features could help future improvements.
-   Additional hyperparameter exploration may reduce RMSE even further.

------------------------------------------------------------------------

## 🚀 How to Run

1.  Install dependencies:

    ``` bash
    pip install surprise numpy pandas matplotlib
    ```

2.  Open the notebook:

        Book_rec_final_Patricio.ipynb

3.  Ensure dataset CSVs are placed in the correct folder structure shown
    in the notebook.

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Add **content-based filtering** for hybrid recommendations.
-   Introduce **implicit feedback models** (e.g., ALS).
-   Deploy a **web API** for real‑time recommendations.
-   Build a **UI dashboard** for interactive book discovery.

------------------------------------------------------------------------

## 📄 Repository Structure

    📁 Book-Recommendation
    │── Book_rec_final_Patricio.ipynb
    │── README.md
    │── Books.csv
    │── Ratings.csv
    └── Users.csv  (optional)

------------------------------------------------------------------------
