# CarMax 

This iPython notebook explores the CarMax dataset, consisting of cars listing from 2015 to 2017 on CarMax, the largest retailer of used vehicles in the
United States. Apart from having a section on Exploratory Data Analysis, this notebook attempts to forecast sales for CarMax.

## Getting Started

Some libraries have been used for this task, especially the `fast.ai` library for forecasting sales.

### Prerequisites

```
pip install numpy
pip install pandas
pip install -U feather-format
pip install fastai
pip install -U seaborn
pip install fbprophet
```

## Background

The main reason `fast.ai` was used is cars listed on CarMax have too many makes and models (categorical variables with too many categories!) 

This would create a large sparse matrix if one-hot encoding is performed on the dataset.

To overcome this, [Entity Embedding](https://towardsdatascience.com/decoded-entity-embeddings-of-categorical-variables-in-neural-networks-1d2468311635) was applied instead. 

Essentially, Entity Embedding will map categorical variables in a function approximation problem into Euclidean spaces, which are the entity embeddings of the categorical variables

## Acknowledgments

* `fast.ai` for their library
* Georgios Drakos for his article on Entity Embedding
