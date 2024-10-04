# Data-Analysis-on-E-commerce

This project performs customer segmentation using the **Brazilian E-Commerce Dataset** from Kaggle. The dataset contains approximately 100k orders placed between 2016 and 2018. The objective is to segment customers based on their purchasing behaviors and other relevant attributes to enable more targeted marketing strategies.

## Dataset Overview

The dataset consists of multiple files, each representing different aspects of the e-commerce transactions:

- **olist_customers_dataset.csv**: Contains customer information.
- **olist_order_items_dataset.csv**: Includes items purchased in each order.
- **olist_order_payments_dataset.csv**: Details the payment methods used.
- **olist_orders_dataset.csv**: The core dataset containing order information.
- **olist_products_dataset.csv**: Includes details of products sold.
- **olist_sellers_dataset.csv**: Information about sellers.
- **product_category_name_translation.csv**: Translates product category names from Portuguese to English.

You can download the dataset [here](https://www.kaggle.com/olistbr/brazilian-ecommerce).

## Project Structure

### 1. Data Loading
- All relevant CSV files are loaded into Pandas dataframes.
- Datasets are merged into a single dataframe for customer segmentation.

### 2. Data Preprocessing
- The dataset is cleaned and prepared for analysis.
- **OneHotEncoding** is used to convert categorical variables.
- **StandardScaler** is used to normalize numeric variables.
- **PCA (Principal Component Analysis)** is performed to reduce the dimensionality of the dataset, while retaining 95% of the variance.

### 3. Clustering (K-Means)
- **K-Means clustering** is applied to segment customers.
- The **Elbow method** and **Silhouette scores** are used to determine the optimal number of clusters.
- The final model is fitted, and customers are assigned to the identified clusters.

### 4. Data Visualization
- Clusters are visualized using **TSNE** to map the high-dimensional data into a two-dimensional space.
- Other visualizations include customer distributions by state, product categories, and order dates.

## Installation

1. Clone this repository.
    ```bash
    git clone https://github.com/yourusername/customer-segmentation.git
    cd customer-segmentation
    ```

2. Install the required dependencies.
    ```bash
    pip install module_name
    ```

## Usage

- The notebook (`customer_segmentation.ipynb`) walks through the entire process of loading, preprocessing, and clustering the data.
- To run the project, use the following steps:
    1. Download the dataset from Kaggle.
    2. Update the `root_path` in the notebook to point to the directory where your dataset is saved.
    3. Execute the cells in sequence.

## Requirements

- Python 3.x
- Pandas
- Numpy
- Matplotlib
- Scikit-learn

