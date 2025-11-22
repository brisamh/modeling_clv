# Customer Lifetime Value: Modeling Customer Profile for Underwriting Optimization

---

## Project Overview

The aim of this study is to predict the Customer Lifetime Value (CLV) based on a customer’s profile to determine whether a prospective customer would represent a profitable policy to write. By building a model that can estimate CLV, we can help the insurance company decide whether a new customer would be profitable to write a policy for. This project also explores which features have the strongest impact on CLV, how accurately CLV can be predicted using the chosen models and how these predictions can support better decision making when evaluating prospective customers.



- **Objective:** Utilizing the available customer data to develop a prescriptive model that estimates the customer lifetime value.
- **Domain:** Insurance Business Analytics
- **Key Techniques:** Ordinary Least Squares model and Random Forest Model

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** https://www.kaggle.com/datasets/pankajjsh06/ibm-watson-marketing-customer-value-data/data . This is the link containing information on the dataset utilized.
- **Description:** The dataset consists of 9,134 customer records and 24 variables describing customer demographics, insurance policy details, vehicle characteristics, and financial information. It is a clean dataset with no missing values. The data includes both numerical and categorical features including: Income, Monthly Premium Auto, Total Claim Amount, Policy Type, Vehicle Class, and State.
- **License:** (if applicable)

---

## Analysis


The analysis began with an exploration of the dataset to understand how demographic, behavioral, and policy-related variables relate to Customer Lifetime Value (CLV). CLV was found to be heavily right-skewed with several extreme outliers, and categorical variables showed notable imbalance across states, coverage types, and policy counts. A key discovery was the unusual behavior of customers with exactly two policies, whose inconsistent and irregular patterns disrupted otherwise strong relationships, particularly the relationship between monthly premium and CLV. Because no feature in the dataset explained this instability, the two-policy group became a focal point of the methodological adjustments, leading to the development of multiple modeling strategies that treated this group differently.

---

## Results

The modeling results showed that standard OLS approaches performed poorly, with initial R² value of 0.169, but model performance improved significantly when accounting explicitly for the two policy customers. Introducing a two policy indicator and an interaction term raised the R² to 0.666, and building separate models by policy count produced extremely high accuracy for all groups except the two policy category. When two policy customers were excluded entirely, an OLS model achieved an R² of 0.796, while a Random Forest model reached a near perfect R² of 0.995. Overall, the results demonstrate that CLV is highly predictable for most customers, but meaningful prediction for two-policy customers remains unresolved due to unexplained variation in their monthly premiums.

---

## Authors

- Rashmi Kamath , Brisa Halviatti, Njenga Gakwa - [@brisamh](https://github.com/brisamh/modeling_clv/tree/main)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

This project used Jupyter Notebooks, NumPy, Pandas, Seaborn, Matplotlib, and sklearn.
Tutorials and guidance were provided by Dr. Fischer of Seattle University.

