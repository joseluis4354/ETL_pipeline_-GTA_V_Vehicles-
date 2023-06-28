
# GTA V Vehicles Analytics

ETL pipeline and data analytics using the data of all the present Vehicles in the videogame GTA V

## Dataset

The dataset is obtained from Kaggle and contains all the statistics of GTA V vehicles

[GTA V Dataset](https://www.kaggle.com/datasets/lucasokwudishu/gta-v-vehicle-dataset)


## Transformation process

#### Main_Extract_Transform_Load.ipynb
* Merge of all the files
* Cleaning of data
    * Removing the followings strings patters

       1. "GTA 5:" in title column
        2. "$ ," in price column
        3. "($* when fully upgraded)" in resale_price column
        4. var mph in column top_speed_game
        5. var mph in column top_speed_real
        6. "Speed" in speed column
        7. "Acceleration" in acceleration column
        8. "Braking" in braking column
        9. "Handling" in handling column
        10. "Overall" in overall column
        11. Remove the string pattern "/ found"
* Reorder of the table

#### Data_transform_ML_use.ipynb

In this file we apply standardization to the price column of our dataframe,
this technique is to re-scale features value with the distribution value between 0 and 1 is useful for the optimization algorithms, such as gradient descent, that are used within machine learning algorithms that weight inputs (e.g., regression and neural networks)

* Nonlinear transformation
* Linear transformation


#### EDA.ipynb

* Exploratory Data Analysis

    Using our output data to get basic insights with graphics through matplotlib and seaborn



## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the libraries

```python
pip install -r requirements.txt



