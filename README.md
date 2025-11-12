# Smartphone Usage Analytics 📱  
**PSTAT 131 Final Project — University of California, Santa Barbara**  
**Author:** Isaiah Singer  
**Date:** May 2025  

## Overview  
This study investigates whether age and gender significantly influence the amount of time people spend on their smartphones.  
Using a dataset containing variables such as **Daily_Screen_Time_Hours**, **Age**, **Gender**, **Location**, **Total_App_Usage_Hours**, and **Number_of_Apps_Used**, I modeled and visualized patterns in smartphone engagement across demographics.  

The central hypothesis was that **younger generations are not necessarily more glued to their phones than older ones**, contrary to popular belief.  

## Objectives  
- Test whether **age** and **gender** are significant predictors of daily screen time.  
- Visualize trends across age ranges, genders, and cities.  
- Fit and compare multiple predictive models to evaluate which best explains variance in smartphone use.  

## Tools & Techniques  
- **R packages:** tidymodels, ggplot2, dplyr, ggcorrplot, xgboost, ranger  
- **Models Tested:** Linear Regression, Pruned Decision Tree, Random Forest, Gradient Boosted Tree  
- **Validation:** 5-fold cross-validation using RMSE and R² metrics  
- **Feature Engineering:** dummy encoding, correlation filtering (0.9 threshold), normalization  

## Exploratory Findings  
- Average daily screen time was **roughly consistent across age groups**, with a mild peak around ages 20–30.  
- **Gender** showed almost no difference in daily screen time.  
- **Location** had minor effects — for example, users in **Houston** had slightly higher variance than those in **Los Angeles**.  
- **Correlation heatmap** confirmed **no strong correlation** between age and screen time or app usage hours.  

## Model Performance  
| Model | RMSE | R² (approx.) | Notes |
|--------|------|--------------|-------|
| Linear Regression | ~3.7 | 0.0002 | Best performing overall, though variance explained was minimal. |
| Gradient Boosted Tree | ~3.8 | 0.00018 | Slightly worse after tuning; not significant improvement. |
| Random Forest | ~3.74 | 0.006 | Marginally better RMSE, still poor explanatory power. |
| Pruned Decision Tree | ~3.79 | 0.00 | No discernible structure found. |

Despite model tuning, **no model could explain even 1.5% of variance** — reinforcing the finding that **age is not a meaningful predictor of smartphone screen time**.

## Key Takeaways  
- **Age and gender are not statistically significant factors** in predicting daily screen time.  
- The popular narrative that “younger people are always on their phones” is **not supported by the data**.  
- The best-fitting model was a **linear regression**, though its predictive power was very weak — a result consistent with the study’s original hypothesis.  

## Reflection  
This project demonstrated practical application of:  
- Building full machine learning workflows with `tidymodels`  
- Cross-validation and model tuning  
- Translating quantitative results into clear conclusions  

Ultimately, the study suggests that **smartphone overuse is a universal behavior**, not limited by age or gender — a finding that emphasizes collective digital awareness rather than generational blame.  

---

*Created by Isaiah Singer — Data Analyst/Scientist | R, Python, SQL | UCSB Statistics & Data Science*
