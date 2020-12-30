# Flipping Homes in a College Town

* Ames, Iowa dataset
  * 2049 home sales
  * 2006-2010
  * Ames had a population of ~60,000 in 2010 
    * https://worldpopulationreview.com/us-cities/ames-ia-population
  * Ames is home to Iowa State University
    * Any findings from this data will be more generalizeable to small college towns in the central US and midwest.
    * https://en.wikipedia.org/wiki/Ames,_Iowa 

* **Goal:** Build a linear regression model for inference.
    * Identify key unchangeable factors affecting home sale price in college towns.

    * Quantify renovation return on investment.
---
**Findings:**  
Most important set features:  
* Large Square footage  
* High quality  
* Low-density residential zoning  
* Single story  

Renovation ROI:  
* Our model can quantify this when trained on unscaled data.  

---
## Process
**1. Data Cleaning**  
 * Drop highly colinear features  
 * Clean missing values  
 * Remove outliers  
 * Map ordinal features to numeric scale  
 * One hot encode categorical features  
      
**2. EDA**  
 * Scatterplots  
 * Heatmap plots  
 * Check correlation and linearity of feature to target  
      
**3. Process new data in the same way**  
  
**4. Feature Engineering**  
 * Create interaction and polynomial terms  
  
**5. Evaluate baseline model**  
 * RMSE  
  
**6. Train-test split linear regression, ridge and lasso regression models**  
 * Check variance, bias, RMSE and R2 scores  
 * Select linear regression as production model  
  
**7. Tune production model for inference**  
 * Investigate scaled and unscaled coefficients  
  
**8. Packge predicitons for kaggle competition submission**  

---
## File Structure
root  
|__ code  
|　　|__ 01-EDA-cleaning.ipynb   
|　　|__ 02-new-data-cleaning.ipynb   
|　　|__ 03-feature-engineering.ipynb  
|　　|__ 04-model-benchmarks.ipynb  
|　　|__ 05-model-tuning.ipynb  
|　　|__ 06-production-model-and-insights.ipynb   
|　　|__ 07-kaggle-submissions.ipynb  
|__ datasets  
|　　|__ clean  
|　　|　　|__ test_clean.csv  
|　　|　　|__ test_engineered.csv  
|　　|　　|__ train_clean.csv  
|　　|　　|__ train_engineered.csv  
|　　|__ submissions  
|　　|　　|__ lasso.csv  
|　　|　　|__ mlr.csv  
|　　|　　|__ train.csv  
|　　|__ train.csv  
|　　|__ test.csv  
|__ plots  
|　　|__ renovation-features.png  
|　　|__ set-features.png  
|__ ames-ppt.pptx  
|__ README.md  

---

