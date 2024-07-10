# Used Car Prediction Model
## Overview
Automobiles offering convenience, freedom, and mobility, are an essential and irreplaceable part of everyday life.  The significance of cars extends beyond mere transportation; they also symbolize personal status and identity. However, with the myriad of manufacturers, car models, and features available, it can be challenging for customers to make informed decisions. The sheer variety of options can be overwhelming, leading to difficulty in choosing the right vehicle that suits their needs and preferences.

Fom the business perspective, the profitability of the used car business hinges on acquiring well-maintained vehicles, precisely evaluating their worth, and providing competitive prices. Additionally, regional fashion and preferences play a crucial role in the regional automotive market. Different areas may have varying demands based on climate, terrain, and local trends, further complicating the purchasing process for consumers. Understanding and catering to these regional preferences can help dealerships optimize their pricing strategies and inventory, ensuring they meet the unique needs of their customer base.  

From the consumer perspective, especially for those typically lacking the car domain-specific expertise, the ability to make an inform purchase resulting in an positive and happy outcome is of great importance for future purchases.  A crucial aspect is identify the key features that determine the price of a used car. Factors such as the vehicle's wear and tear measured using its age, mileage, condition, and service history play a significant role in its valuation. The make and model of the car, its popularity, and regional market demand also influence the price.


## DataSet
The dataset is a tabular, comma delimited, excel (.csv) file, where each row represents a specific used car listing, and each columns represents the specific feature or attribute for the car.

### Data Source:

<table>
    <tr>
        <th>Filename</th>
        <th>Type</th>
        <th>Number of Rows</th>
        <th>Number of Features</th>
        <th>Delimiter</th>
    </tr>
    <tr>
        <td>'data/vehicle.csv'</td>
        <td>Excel csv</td>
        <td>426,880</td>
        <td>18</td>
        <td>,</td>
    </tr>
</table>

### Features:

<table>
    <tr>
        <th>Feature</th>
        <th>Type</th>
        <th>Description</th>
        <th>Sample Values</th>
        <th>Good Values</th>
    </tr>
    <tr>
        <td>id</td>
        <td>Numeric</td>
        <td>assigned vehicle ID</td>
        <td>7222695916, ...</td>
        <td>426880</td>
    </tr>
    <tr>
        <td>region</td>
        <td>String</td>
        <td>Vehicle roaming area</td>
        <td>hudson valley, el passo, ...</td>
        <td>426880</td>
    </tr>
    <tr>
        <td>price</td>
        <td>Numeric</td>
        <td>Vehicle Listed Price
        <td>21000, 15,995, ...</td>
        <td>426880</td>
    </tr>
    <tr>
        <td>year</td>
        <td>Numeric</td>
        <td>Manufacture year of the vehicle
        <td>2014, 2018, ...</td>
        <td>425675</td>
    </tr>
    <tr>
        <td>manufacturer</td>
        <td>String</td>
        <td>Vehicle manufacturer</td>
        <td>gmc, chevrolet, toyota, ...</td>
        <td>409234</td>
    </tr>
    <tr>
        <td>model</td>
        <td>String</td>
        <td>Vehicle model
        <td>f-150 xlt, tacoma, cherokee</td>
        <td>421603</td>
    </tr>
    <tr>
        <td>condition</td>
        <td>String</td>
        <td>Vehicle condition</td>
        <td>good, excellent, ...</td>
        <td>252776</td>
    </tr>
    <tr>
        <td>cylinders</td>
        <td>String</td>
        <td>Number of engine cylinders</td>
        <td>8 cylinders, 6 cylinders, ...</td>
        <td>249202</td>
    </tr>
    <tr>
        <td>fuel</td>
        <td>String</td>
        <td>Vehicle fuel type</td>
        <td>gas, diesel, ...</td>
        <td>423867</td>
    </tr>
    <tr>
        <td>odometer</td>
        <td>Numeric</td>
        <td>Milage driven in miles</td>
        <td>12102, 80328, ...</td>
        <td>422480</td>
    </tr>
    <tr>
        <td>title_status</td>
        <td>String</td>
        <td>Vehicle title status</td>
        <td>clean, rebuilt, ...</td>
        <td>418638</td>
    </tr>
    <tr>
        <td>transmission</td>
        <td>String</td>
        <td>Vehicle transmission type</td>
        <td>automatic, manual, ...</td>
        <td>424324</td>
    </tr>
    <tr>
        <td>VIN</td>
        <td>String</td>
        <td>Vehicle Identification Number</td>
        <td>5TFTX4CN6CX015282, ...</td>
        <td>265838</td>
    </tr>
    <tr>
        <td>drive</td>
        <td>String</td>
        <td>Vehicle Drive type</td>
        <td>fwd, rwd, ...</td>
        <td>296313</td>
    </tr>
    <tr>
        <td>size</td>
        <td>String</td>
        <td>Vehicle Size Classification
        <td>mid-size, full-size, ...</td>
        <td>120519</td>
    </tr>
    <tr>
        <td>type</td>
        <td>String</td>
        <td>Vehicle type classification</td>
        <td>pickup, SUV, truck, ...</td>
        <td>334022</td>
    </tr>
    <tr>
        <td>paint_color</td>
        <td>String</td>
        <td>Vehicle Color</td>
        <td>white, red, blue, ...</td>
        <td>296677</td>
    </tr>
    <tr>
        <td>state</td>
        <td>String</td>
        <td>Abbreviated lower case of each state where the vehicle is registered
        <td>ma, ca, or, ...</td>
        <td>426880</td>
    </tr>
</table>

## Data Preprocessing
The data is preprocessed to prepare it for modeling.
1.  Remove missing, null.
2.  Remove bad data, where price = 0
3.  Standardize the entire dataset to 'lower case'
4.  Remove unusable features

<table>
    <th>Usable Rows</th>
    <th>32,496</th>
    <th>Features</th>
    <th>18</th>
</table>

## Features Analysis - Mutual Importance Score
* target feature: price
* id, VIN features are independent and unique for each vehicle and have no influence on its price, and therefore removed from the dataset

The remaining features of the dataset are analyzed with the objective to reduce the number of features to use for regression, a <b>Mutual Information Score</b> is performed for every feature vs the target feature: price, and shown in the following diagram.  A odometer reading cluster breakdown vs car price is also shown.

![mi_scores](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/21785032-02f0-49e6-8744-2bc84171e705)

![odometer_range_price](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/800d4e74-0086-4d35-847c-5b5bd3199dcc)

All none numeric fields are label encoded.  The odometer feature is range encoded for group computation.
From the Mutual Importance score, and not surprising, the odometer, the model, and the year of the vehicle are the top features that influences the price of the car. 
Vehicle with lower odometer milages tend to have higher prices.

## Price Prediction Model
Create pipeline to transform each features:

    a. Odometer: RangeEncode, assign numerical values for the various ranges
    
    b. All remaining non-numeric features: OrdinalEncode, with numerical values assigned on first-come-first-serve bases for each unique values in the feature

Perfrom run_model() function to find the best model estimator, where:
    
    a. Dataset is split up X_train: 80%, X_dev: 19%, X_test: 1%
    
    b. setup grid search parameters:
        
        1. PolynomialFeatures, with features_degree=[1,2,3]
        
        2. SequentialFeatures, with features_to_select=[3,5,9], selector_direction=['forward']
        
        3. alpha = [0.01,0.1,1.0,5.0,10.0]
    
    c. Setup Process Pipeline:
        
        1. PolynomialFeatures(), expand features
        
        2. SequentialFeatureSelector(), to select the best features
        
        3. Lasso(), or Ridge() regularization, 
    
    d. Perform GridSearchCV() to find best estimator
        
        1. cv = 5 fold for validation
        
        2. scoring = 'r2', variance scoring
        
        3. error_score = 'raise'
    
    e. List best model's feature selected, and r2 score

## Model Results
The model results are tabulated in the following tables. For the selected top feature selected, due to the PolynomialFeatures of cross-multiplcation between polynomial degrees and with other features, for brevity, only the dataset's captured features are listed.  Note that these features only listed that they are important features influencing the price of the car, and not necessary in the order of importance.  This is again due to the PolynomialFeatures.

![model_results](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/72ac40e1-5367-4dd2-b722-f4512f89d245)
![model_results (1)](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/cf594e06-0b62-43cd-8b93-e323ba62bd04)
![model_results (2)](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/17c81a38-03f6-42f1-8347-3ecbea397a0e)
![model_results (3)](https://github.com/fkao37/UsedCarPredictionModel/assets/391381/fd84a304-9177-4756-a10d-1b739f33b601)

## Result Analysis
Two models are created using different regularization model, Ridge, and Lasso and their model performace result used for comparsion. The first run results uses the entire data set and generates the model on a National level, and model performance data listed in the first row.  Both Ridge and Lasso end up selecting the same key features with Ridge regularization having a better performance of variance score r2 of 63.2% vs 57.9%, both well above the 50% common acceptable variance level.

Deeper analysis of the dataset discovered the imbalance dataset source from different regions.  For example for the state of california there are more data samples than that from Hawaii.  A second run is performed first by isolating the data for the state, and then execute the model against the filtered data set.  The model variance score, and top features selected are listed in the results table.

Not surprisingly, variance score varies highly between each state.  This can be explained due to the lack of sufficient traning and test data for the state.  For each state, same as in the National run, the Lasso regression result lags slightly behind the Ridge model in terms of model performance.

# Conclusion

The Ridge based regularization model performs slightly better than that of the Lasso regularization.  The crucial features in predicting used cars are: 
Year, fuel type, tranmission type, odometer reading, type of drive (fwd, rwd, ...), and the number of cylinders.  Based on the dataset, the model is able to account for 63% (Ridge) for the entire data, or at the National level.
However, on a regional and state level, the model variance score vary drastically between states.  This is mainly due to the lack of data, and diversity of the data for each state.  However, important key features important for predicting price can be used as reference for further data acquistion needs.  Therefore, for states with r2 score lower than the National r2 score, use the National model, otherwise, use the state specific model for more accurate prediction.






