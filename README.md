# ** Project Report: Predicting User Satisfaction in a Dating App**

## **1. Introduction**
The goal of this project was to analyze user behavior on a Gen Z dating app and build a predictive model to classify user satisfaction. We explored data through cleaning, visualization, feature engineering, and machine learning techniques to optimize model accuracy.

## **2. Data Analysis & Cleaning**
- The dataset contained **500 entries** with **16 features** such as age, gender, occupation, app usage frequency, and satisfaction scores.
- **Missing Data Handling:**
  - `Secondary_Apps` and `Challenges` had missing values, which were imputed or handled appropriately.
- **Data Encoding:**
  - Categorical features like `Primary_App`, `Education`, and `Occupation` were encoded into numerical values.

## **3. Feature Engineering & Data Visualization**
### **Feature Engineering Highlights:**
- Encoded categorical variables (Gender, Location, Education, etc.) using Label Encoding.
- Converted Usage_Frequency into numerical format (1 = Monthly, 2 = Weekly, 3 = Daily).
- Transformed Daily_Usage_Time into Daily_Usage_Minutes (numerical values).
- Extracted priority rankings from Partner_Priorities (Appearance, Personality, Interests, Values).
- One-hot encoded Challenges and Desired_Features to handle multi-category fields.
- Dropped redundant text columns after encoding.

### **Key Insights from Visualizations:**
- Age vs. Satisfaction: No strong trend, but younger users (18-24) show diverse satisfaction levels.
- Daily Usage vs. Satisfaction: More time spent on the app does not guarantee higher satisfaction.
- Top Challenges: The most common issues include matching problems, safety concerns, and ghosting.
- Most Desired Features: Users want better matchmaking algorithms, improved safety, and video chat options.
- Usage Frequency: Most users engage daily or weekly, with fewer using the app monthly.

## **4. Machine Learning Models & Results**
We tested multiple models to predict user satisfaction:

| Model | Accuracy |
|--------|----------|
| Random Forest | 23% |
| Logistic Regression | 17% |
| XGBoost | 24% |
| k-Nearest Neighbors (k-NN) | 77% |
| Neural Network (MLPClassifier) | **80%** |

### **Final Model: Optimized Neural Network**
- **Best Parameters:**
  - Activation Function: `ReLU`
  - Hidden Layers: `(64, 32, 16)`
  - Learning Rate: `0.01`
  - Iterations: `500`
- **Final Accuracy:** **80%** (Best among all models)

## **5. Business Implications**
- **User Engagement:** Features affecting satisfaction can help improve user experience.
- **Personalized Recommendations:** Insights can enhance matchmaking algorithms.
- **Retention Strategies:** Identifying dissatisfied users early can help reduce churn.

## **6. Conclusion**
- **Binary classification improved performance**, leading to an **80% accuracy rate**.
- **Neural Networks performed the best**, capturing hidden behavioral patterns.
- **Future work:** Further feature engineering or gathering more data could boost accuracy beyond 80%.

This model can be implemented to analyze real-time user feedback and improve dating app satisfaction strategies.

---
