# Aviation_Accident_Analysis
In the project we have built intractive dashboard to analyze civil aviation accidents and selected incidents. The data includes accidents from the United States, its territories and possessions, and in international waters.

Group members:
1. Tejal Kotkar
2. Savita Hirilall
3. Hibo Dahir
4. Tana Larson

#### Tools:

This project is achieved by using:
HTML, CSS, JavaScript combined with D3, Python Flask API, Jupyter Notebook, Plotly, Leaflet with mapbox.

#### Additional Libraries used:
Additional JS Library : [flickity carousel](https://unpkg.com/flickity@2/dist/flickity.pkgd.min.js)

Additional CSS Styling: [Grid and Flex](https://medium.com/youstart-labs/beginners-guide-to-choose-between-css-grid-and-flexbox-783005dd2412)

### Dataset:
Datasets is in form on CSV file taken from Kaggle link:
[https://www.kaggle.com/khsamaha/aviation-accident-database-synopses](https://www.kaggle.com/khsamaha/aviation-accident-database-synopses)

### Data Cleanup:
Below is the data cleaning process outlined in sequence where we used data only from United States:
1. Read CSV file as pandas DF
2. Dropped unnecessary columns 
3. Renamed remaining columns
4. Saved DF to another DF to prepare for Perfect data set
5. Checked for missing values & removed it & wrote in CSV (Which gave us perfect data set)
6. From orig DF, added Unknown is column except lat & long
7. checked for missing values & removed those rows (which gave us not so perfect data set)

### Machine Learning:
Flying has been the go-to mode of travel for years now; it is time-saving, affordable, and extremely convenient. According to the FAA, 2,781,971 passengers fly every day in the US, as in June 2019. Passengers reckon that flying is very safe, considering strict inspections are conducted and security measures are taken to avoid and/or mitigate any mishappenings. However, there remain a few chances of unfortunate incidents.
So we have used machine learning to predict some of the aspects of an accident. 

#### Machine learning & prediction details:
Process followed starts with data cleanup. When was in cleanup process, we realised there are some of the things which are unknows regarding the accidents.
Hence decided to go with two data sets where one is the perfect data set and other data set with some unknowns. Idea behind was to see how much unknowns affect the models.

To start with we picked up the two Machine Learning Algorithms, named Logistic Regression and Random Forest Regreesion to predict below 3 aspects:
1. Type of Investigation - Whether the event happend will be categorized as Incident or Accident.
2. Aircraft Damage - How severe the Aircraft damage will be. Will it be Minor, Substancial or Destroyed.
3. Severity of Incident - How much severe the event will be from Fatal , Non-Fatal or Incident.

For each of these predictions we ran both Logistic and Random Forest Regreesion on both the data sets. We could see from results that the data set with perfect data has much more better model.
Now from using perfect data set, we chose the model which gave us better Accuracy and finally used that best model for predictions. Models with accuracy below:
1. Type of Investigation: 
    * Algorithm - Random Forest 
    * Accuracy - 93.54%

2. Aircraft Damage: 
    * Algorithm - Random Forest 
    * Accuracy - 83.87%

3. Severity of Incident:
    * Algorithm - Logistic Regression
    * Accuracy - 93.54%

### Visualization Questions:
1. Distribution of Accidents in the United States.
    * Graph demonstrates accidents distribution by states. 
    * New york tops the chart with highest number of accidents. San Juan, Kauai, Oahu & Kauai islands have least number of accidents.
![Distribution](Accident_Analysis/static/Bkg_images/distribution_img.PNG)

2. Top 10  Accidents by Highest Number of Injuries.
    * Graph demonstrates the top accidents by highest number of injuries and date, location & State of an accident.
    * San Fransisco's 2013 accident tops the chart reporting 190 injuries and 117 uninjured.
    * Knoxville's 2020 accident is at the bottom with 23 injured and 50 uninjured.
    * Accident happened in Jamaika in 2002 had reported highest number on uninjured which is 349
![Injuries](Accident_Analysis/static/Bkg_images/injuries_img.PNG)

3. Aircraft Make & Model With Highest Number of Accidents.
    * More than 85% of accidents happend with an Airplane.
    * From Airplane manufactures Cessna tops with 45% accidents followed by Piper with 29% accidents.
    * To be specific on Cessna its a model 172 which is at the top with 43.4% accidents.
![Injuries](Accident_Analysis/static/Bkg_images/Aircraft_make_model_img.PNG)

4. Accident Count by Purpose of Flight.
    * Highest serious injuries occurred were due to 'Air Race/Shows'.
    * The investigation type was an accident.
![Purpose](Accident_Analysis/static/Bkg_images/purpose_img.PNG)

5. Accident Count with Respect to Aircraft Damage & Phase of Flight.
    * Aircraft had Substantial damages in around 24K accidents.
    * Maximum accidents are reported during the Landing phase of the flight approximately 8K.
![Damage](Accident_Analysis/static/Bkg_images/damage_img.PNG)
![Phase of Flight](Accident_Analysis/static/Bkg_images/damage_phase_img.PNG)