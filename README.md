# ibm-applied-data-science-capstone
SpaceX Launch Success Prediction Using Machine Learning
# SpaceX Falcon 9 First Stage Landing Prediction

## Summary
SpaceX reuses boosters to cut costs. I built a pipeline using APIs/scraping to predict landing success, achieving 100% accuracy with KNN to optimize launch bidding and financial decisions.

---

## Solution
I developed an end-to-end Data Science solution to predict booster landings. Key features include interactive **Plotly Dash** dashboards for real-time filtering and **Folium** maps for geospatial analysis. By applying machine learning, I identified a "sweet spot" for success (3000-5000kg payloads) and confirmed the **Block 5** booster's superior reliability. This provides a clear business impact: more competitive bidding and high-precision cost forecasting for aerospace stakeholders.

---

## Approach
My process followed a rigorous analytical lifecycle:
1. **Data Ingestion:** Used BeautifulSoup and REST APIs for automated collection.
2. **EDA:** Cleaned and analyzed data via SQL/Pandas to identify success trends.
3. **Visualization:** Built interactive UI elements to explore site-specific performance.
4. **Model Tuning:** Implemented **GridSearchCV** with 10-fold cross-validation to optimize hyperparameters.
5. **Selection:** Evaluated models via Confusion Matrices, selecting **KNN** for its 1.0 accuracy score.

---

## Results & Key Findings

### 1. Predictive Performance
The model comparison showed that **K-Nearest Neighbors (KNN)** outperformed other algorithms.

| Classification Method | Test Accuracy |
| :--- | :--- |
| **KNN** | **1.0 (100%)** |
| Logistic Regression | 0.83 |
| SVM | 0.83 |
| Decision Tree | 0.83 |

```mermaid
graph LR
    A[Data Prep] --> B[Standardization]
    B --> C[GridSearchCV]
    C --> D[KNN Model]
    D --> E[100% Accuracy]
    style E fill:#2ecc71,stroke:#fff,color:#fff
