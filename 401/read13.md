# Linear Regression

## Linear regression is probably one of the most important and widely used regression techniques. Itβs among the simplest regression methods. One of its main advantages is the ease of interpreting results.

## Problem Formulation
When implementing linear regression of some dependent variable π¦ on the set of independent variables π± = (π₯β, β¦, π₯α΅£), where π is the number of predictors, you assume a linear relationship between π¦ and π±: π¦ = π½β + π½βπ₯β + β― + π½α΅£π₯α΅£ + π. This equation is the regression equation. π½β, π½β, β¦, π½α΅£ are the regression coefficients, and π is the random error.

## What is Scikit-Learn?
Scikit-learn (or sklearn for short) is a free open-source machine learning library for Python. It is designed to cooperate with SciPy and NumPy libraries and simplifies data science techniques in Python with built-in support for popular classification, regression, and clustering machine learning algorithms.

Sklearn serves as a unifying point for many ML tools to work seamlessly together. It also gives data scientists a one-stop-shop toolkit to import, preprocess, plot, and predict data.

The project was started by David Cournapeau during the 2007 Google Summer of Code, and this library has grown over the last decade in both popularity and features. Scikit-learn is now the most popular machine learning library on Github.

### Scikit-learn provides tools for:

Regression, including Linear and Logistic Regression
Classification, including K-Nearest Neighbors
Model selection
Clustering, including K-Means and K-Means++
Preprocessing, including Min-Max Normalization

## Advantages of Scikit-Learn
Developers and machine learning engineers use Sklearn because:

Itβs easy to learn and use.
Itβs free and open-source.
It helps in all aspects and algorithms of Machine Learning, even Deep Learning.
Itβs very versatile and powerful.
Detailed documentation and active community.
It is the most widely used Machine Learning toolkit.


To install Scikit-learn enter the following line into your Python 3.
```
 pip install -U scikit-learn
 ```
Then to verify the installation, enter:
```
python -m pip show scikit-learn # displays which version and where sklearn is installed
python -m pip freeze # displays all packages installed in virtualenv
python -c "import sklearn; sklearn.show_versions()"
Linux users: add 3 after pip and python in the above lines β pip3, python3.
```

Now to install NumPy, SciPy and, matplotlib, enter:
```
pip install -U numpy
pip install -U scipy
pip install -U matplotlib
```
As we did before, weβll confirm the installation of each with:
```
python -m pip show numpy
python -m pip show scipy
python -m pip show matplotlib
```
Now youβre ready to start using Scikit-learn! Letβs jump into our tutorial by importing a dataset.

## Standard
If your data instead follows standard deviation, you can use the StandardScaler instead. This scaler fits a passed data set to be a standard scale along with the standard deviation.

```
import sklearn.preprocessing as preprocessing

std = preprocessing.StandardScaler()
# X is a matrix
std.fit(X)
X_std = std.transform(X)
```