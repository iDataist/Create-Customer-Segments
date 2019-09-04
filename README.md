# Create Customer Segments 

## Project Overview
A company that performs mail-order sales in Germany is interested in identifying facets of the population that are most likely to be purchasers of their products for a mailout campaign. The goal of the project is to use unsupervised learning techniques to organize the general population into clusters, then use those clusters to see which of them comprise the main user base for the company. The project is documented in [Identify_Customer_Segments.ipynb](https://github.com/iDataist/Create-Customer-Segments/blob/master/Identify_Customer_Segments.ipynb).

## Key Skills Demonstrated:
- Data cleaning
- Dimensionality reduction with PCA
- Unsupervised clustering

## Data
Udacity_AZDIAS_Subset.csv: Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).

Udacity_CUSTOMERS_Subset.csv: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).

Data_Dictionary.md: Information file about the features in the provided datasets.

AZDIAS_Feature_Summary.csv: Summary of feature attributes for demographic data.

## Project steps
**Step 1: Preprocessing**

In this step, I assessed and cleaned the data in order to convert it into a usable form. Below are the key considerations in this step:

How are missing or unknown values encoded in the data? Are there certain features (columns) that should be removed from the analysis because of missing data? Are there certain data points (rows) that should be treated separately from the rest?
Consider the level of measurement for each feature in the dataset (e.g. categorical, ordinal, numeric). What assumptions must be made in order to use each feature in the final analysis? Are there features that need to be re-encoded before they can be used? Are there additional features that can be dropped at this stage?

**Step 2: Feature Transformation**

After the data is cleaned, I applied dimensionality reduction techniques to identify relationships between variables in the dataset, resulting in the creation of a new set of variables that account for those correlations. Below are the key considerations in this step:

What might happen if I don’t perform feature scaling before applying later techniques?
How much variability in the data does each principal component capture? How to interpret associations between original features in the dataset based on the weights given on the strongest components? How many components to keep as part of the dimensionality reduction process?

**Step 3: Clustering**

Finally, on the transformed data, I applied clustering techniques to identify groups in the general demographic data. I then applied the same clustering model to the customers dataset to see how market segments differ between the general population and the mail-order sales company. Below are the key considerations in this step:

How to make a decision on how many clusters to use?
Which types of people are likely consumers for the mail-order sales company?

## About Unsupervised Learning
The unsupervised learning branch of machine learning is key in the organization of large and complex datasets. While unsupervised learning lies in contrast to supervised learning in the fact that unsupervised learning lacks objective output classes or values, it can still be important in converting the data into a form that can be used in a supervised learning task. Dimensionality reduction techniques can help surface the main signals and associations in your data, providing supervised learning techniques a more focused set of features upon which to apply their work. Clustering techniques are useful for understanding how the data points themselves are organized. These clusters might themselves be a useful feature in a directed supervised learning task.
