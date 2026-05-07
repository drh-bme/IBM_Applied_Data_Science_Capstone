# SpaceX Falcon 9 Landing Success Prediction
## IBM Data Science Professional Certificate Capstone Project
### Project Overview
The goal of this project is to predict whether the Falcon 9 first stage will land successfully. SpaceX reduces launch costs significantly (advertised at $62M vs. competitors' $165M+) by reusing the first stage. Determining landing success allows us to estimate launch costs, providing vital competitive intelligence for companies bidding against SpaceX.  

### Tech Stack

* Languages: Python   
* Data Collection: REST API, BeautifulSoup (Web Scraping)   
* Analysis: SQL (SQLite), Pandas, NumPy   
* Visualization: Matplotlib, Seaborn, Folium (Maps), Plotly Dash   
* Machine Learning: Scikit-Learn (Logistic Regression, SVM, Decision Tree, KNN)   

### Project Workflow
1. Data Collection & Wrangling:

    * SpaceX API: Utilized custom helper functions to request launch, booster, and core data from the SpaceX REST API.  
    * Web Scraping: Scraped historical launch records from Wikipedia using BeautifulSoup to supplement API data.  
    * Wrangling: Cleaned datasets by handling missing values (e.g., mean imputation for PayloadMass) and filtering for Falcon 9 launches.  

2. Exploratory Data Analysis (EDA):

    * SQL Analysis: Queried mission outcomes, payload statistics, and launch site trends using SQL magic commands.  
    * Visualization: Created scatter plots and line charts to identify success trends over time and the impact of payload mass and orbit type on landing success.  
    * Finding: Success rates remained near 0% until 2013, peaking at ~90% in 2019 as technology matured.  

3. Interactive Analytics:

    * Launch Site Mapping: Developed interactive maps using Folium to visualize launch site locations.  
    * Proximity Analysis: Added MarkerCluster for launch outcomes and calculated distances to coastlines and infrastructure using MousePosition.  

4. Machine Learning Prediction:
    * Standardized feature data using StandardScaler.  
    * Tuned hyperparameters for four classification models using GridSearchCV with 10-fold cross-validation:  
        * Logistic Regression
        * Support Vector Machine (SVM)
        * Decision Tree
        * K-Nearest Neighbors (KNN)

### Results
All models achieved a test accuracy of approximately 83.33%. Due to the small test sample size (18 samples), the models showed identical performance metrics. Logistic Regression's confusion matrix identified that the primary challenge for the models was minimizing False Positives.  

### Repository Structure

* Master_Notebook.ipynb: The complete end-to-end technical implementation.  
* Spacex.csv: CSV datasets used for training and testing.
* requirements.txt: The complete list of libraries used in this project.
* README.md: Project summary and presentation.

### Installation & Setup
To run this project locally, clone the repository using [Git](https://git-scm.com/install/windows) and install the required dependencies. For the Windows command prompt:

```bash
# bash code
git clone [https://github.com/drh-bme/IBM_APPLIED_DATA_SCIENCE_CAPSTONE.git](https://github.com/drh-bme/IBM_APPLIED_DATA_SCIENCE_CAPSTONE.git)
cd IBM_APPLIED_DATA_SCIENCE_CAPSTONE
pip install -r requirements.txt
```

### External References
[SpaceX API](https://docs.spacexdata.com/#5fc4c846-c373-43df-a10a-e9faf80a8b0a) 
__________________________________________________________________________________________________________
_This project was completed as the final requirement for the IBM Data Science Professional Certificate._