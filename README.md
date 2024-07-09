# UsedCarPredictionModel
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
        <th>Unique Values</th>
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
