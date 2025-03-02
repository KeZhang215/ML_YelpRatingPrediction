# **Yelp Restaurant Ratings Prediction**  

Predicting Yelp star ratings for restaurants in **Las Vegas** using business attributes from their Yelp profiles. This project explores **regression and classification models** to understand factors influencing ratings and provides recommendations for businesses.  

## **Dataset**  
- **Source**: Yelp Dataset  
- **Training Data**: `yelp242a_train.csv` (6,272 entries)  
- **Test Data**: `yelp242a_test.csv` (2,688 entries)  
- **Features**: Includes **review count, GoodForKids, Alcohol, WiFi, BikeParking, Reservations, OutdoorSeating, etc.**  
- **Target Variables**:  
  - **Stars** (1-5 rating) for regression models.  
  - **FourOrAbove** (binary: 1 if stars ≥ 4, 0 otherwise) for classification models.  

## **Methodology**  
### **Data Preprocessing**  
- Missing values in categorical features are treated as a separate category `(Missing)`.  
- No feature selection is required as all features are used in modeling.  

### **Modeling Approaches**  
#### **Regression Models for Predicting Star Ratings**  
- **Linear Regression**  
- **Regression Tree (CART Algorithm with Cross-Validation for Complexity Parameter Selection)**  
- **Performance Metric**: **OSR²** on test data.  

#### **Classification Models for Predicting High Ratings (`FourOrAbove`)**  
- **Logistic Regression**  
- **Classification Tree (CART Algorithm with Cross-Validation)**  
- **Performance Metrics**:  
  - Accuracy (Primary Metric)  
  - True Positive Rate (TPR)  
  - False Positive Rate (FPR)  

## **Results & Business Insights**  
- **Comparison of Models:** Evaluating trade-offs between regression and classification models.  
- **Business Strategy:** Identifying **top three factors** that help restaurants increase ratings.  

## **Installation & Usage**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-repo/Yelp-Ratings-Prediction.git
   cd Yelp-Ratings-Prediction
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:  
   ```bash
   jupyter notebook Yelp_Prediction.ipynb
   ```

## **Future Work**  
- Further optimization of feature engineering and model tuning.  
- Exploring **sentiment analysis** on user reviews for additional insights.  
