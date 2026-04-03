# XAI Analysis: LIME and DiCE on the Adult Income Dataset

This project investigates implicit gender bias in income prediction models 
using two Explainable AI (XAI) methods: LIME and DiCE, applied to the 
Adult Income Dataset.

## Research Question
To what extent do counterfactual explanations (DiCE) provide more 
actionable and diagnostic insights into implicit gender bias within the 
Adult Income Dataset compared to feature attribution explanations (LIME)?

## Repo Structure
```
xai-lime-dice-adult-income/
│
├── adult.csv                  # Adult Income Dataset (UCI)
├── xai_notebook.ipynb         # Main notebook with all code
└── README.md                  # This file
```

## Requirements
Run this one cell in Google Colab to install all dependencies:

pip install lime dice-ml scikit-learn pandas numpy matplotlib

## How to Run
1. Clone the repository:
   git clone https://github.com/JoJmH/XAI-report.git
2. Install dependencies:
   pip install lime dice-ml scikit-learn pandas numpy matplotlib
3. Open the notebook:
   jupyter notebook xai_notebook.ipynb
4. Run all cells in order from top to bottom

## Dataset
- Name: Adult Income Dataset
- Source: https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data
- Instances: 48,842 (45,222 after cleaning)
- Target variable: income (<=50K = 0, >50K = 1)

## Key Results
- Model accuracy: 86% (Random Forest)
- Gender-only counterfactual flip rate: 5.31%
- DiCE actionable counterfactuals: 83%
- DiCE non-actionable counterfactuals: 17%

## References
Barocas, S., Hardt, M., & Narayanan, A. (2023). Fairness and machine 
learning: Limitations and opportunities. https://fairmlbook.org

Garreau, D., & von Luxburg, U. (2020). Explaining the explainer: A first 
theoretical analysis of LIME. AISTATS 2020. https://arxiv.org/abs/2001.03447

Goethals, S., Martens, D., & Calders, T. (2023). PreCoF: Counterfactual 
explanations for fairness. Machine Learning. 
https://doi.org/10.1007/s10994-023-06319-8

Mothilal, R. K., Sharma, A., & Tan, C. (2020). Explaining machine learning 
classifiers through diverse counterfactual explanations. FAT* 2020. 
https://arxiv.org/abs/1905.07697

Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). "Why should I trust you?": 
Explaining the predictions of any classifier. KDD 2016. 
https://arxiv.org/abs/1602.04938

Slack, D., Hilgard, S., Jia, E., Singh, S., & Lakkaraju, H. (2020). Fooling 
LIME and SHAP: Adversarial attacks on post hoc explanation methods. 
AIES 2020. https://arxiv.org/abs/1911.02508

Wachter, S., Mittelstadt, B., & Russell, C. (2017). Counterfactual 
explanations without opening the black box: Automated decisions and 
the GDPR. Harvard Journal of Law & Technology. 
https://arxiv.org/abs/1711.00399
