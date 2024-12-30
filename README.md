# Predicting Research Funding Success from Grant Proposal Abstracts

**Course:** ECO482  
**Institution:** University of Toronto  
**Authors:** Unurjargal Batsuuri, Joyce Lin, Daniella Chung  
**Date:** November 2024  

## Project Overview

This research project investigates whether the textual features of grant proposal abstracts can predict funding outcomes in Canadian health research. Using machine learning and topic modeling, we aim to improve the efficiency and transparency of the grant allocation process by identifying key predictors of funding success.

## Objectives

1. **Prediction:** Analyze whether abstract features can predict the amount of funding received.  
2. **Optimization:** Develop machine learning models to reduce bias and improve the efficiency of the funding allocation process.  
3. **Insights:** Uncover trends in funding priorities and systemic biases in grant allocations.

## Data and Methods

### Data
- **Source:** Canadian Institutes of Health Research (CIHR) Funding Decision Database.  
- **Scope:** 7,011 proposals from the Social, Cultural, Environmental, and Population Health theme (1991–2018).  
- **Key Variables:**
  - Project Abstracts
  - CIHR Contribution (funding amount)
  - Project Duration
  - Institution Details  
- **Preprocessing:** 
  - Removed duplicates (1% of dataset).
  - Log-transformed skewed funding data.
  - Engineered features such as novelty scores and abstract length.

### Methodology
1. **Text Processing:** Cleaned abstracts by tokenizing, lemmatizing, and extracting bigrams using Gensim.  
2. **Topic Modeling:** Applied Latent Dirichlet Allocation (LDA) to identify five latent themes from abstracts.  
3. **Feature Engineering:** Added topic distributions, novelty scores, and abstract lengths as features.  
4. **Model Training:**
   - Algorithms: Gradient Boosting Trees, Random Forest, Linear Regression, Lasso, Ridge, KNN.
   - Tools: Python libraries (pandas, NumPy, scikit-learn, gensim).  
5. **Model Evaluation:** Evaluated models using \( R^2 \) and Mean Squared Error (MSE).

## Results

- **Best Model:** Gradient Boosting Trees  
  - \( R^2 = 0.5714 \), MSE = 1.4496  
  - Captured complex relationships within the data but explained only 57.14% of the variance in grant amounts.  
- **Topic Modeling:**
  - Identified five themes:
    1. Women’s Health in Canada  
    2. Youth-Centered Policy  
    3. Mental Health and Social Outcomes  
    4. Indigenous Community Health  
    5. HIV Risk and Canadian Population Health  
  - Topics like HIV Risk and Indigenous Health correlated positively with funding, while Women’s Health showed systemic underfunding.

## Key Findings

1. **Funding Priorities:** Significant disparities in funding allocation highlight systemic underfunding in Women’s and Mental Health initiatives.  
2. **Predictive Features:** Topic modeling and textual features provided critical insights into funding decisions, but additional unobserved factors likely influence allocations.  
3. **Model Performance:** Gradient Boosting performed best, but the unexplained variance suggests the need for more robust data and features.

## Limitations

- Dataset focuses solely on the Social, Cultural, Environmental, and Population Health theme.
- Missing data on unfunded proposals and grant review committee demographics.
- Monetary constraints prevented advanced sentiment analysis using premium tools like LIWC.

## Future Research

- Analyze other CIHR themes, such as Biomedical or Clinical research.  
- Investigate the role of applicant qualifications and demographics in funding decisions.  
- Study the long-term productivity of funded projects to optimize future grant allocations.

## Conclusion

This project highlights the potential of combining machine learning and topic modeling to improve the efficiency and fairness of grant allocations. By uncovering systemic biases and providing actionable insights, this research lays the groundwork for refining the funding process to better support impactful research initiatives.

## Citation

- Dataset: [CIHR Funding Decision Database](https://webapps.cihr-irsc.gc.ca/decisions/p/main.html?lang=en)
- Tools: Python (pandas, scikit-learn, gensim)

---
