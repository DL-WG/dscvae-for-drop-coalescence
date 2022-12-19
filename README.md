# Predicting drop coalescence in microfluidic device with a deep learning generative mode

## About the project
Machine learning methods can be used to predict drop coalescence, which is the process by which two or more droplets of a liquid merge to form a larger droplet. This process is important in a variety of applications, such as weather forecasting, water treatment, and pharmaceutical manufacturing. To predict drop coalescence using machine learning, one approach would be to first collect a large dataset of droplet pairs, along with corresponding labels indicating whether or not the droplets in each pair coalesced. This dataset could be created through experiments or simulations. Next, a machine learning model would be trained on this dataset to learn the relationship between the characteristics of the droplets (such as size, shape, and surface tension) and the likelihood of coalescence. Once the model has been trained, it can be used to make predictions on new droplet pairs, allowing researchers to understand the conditions under which coalescence is likely to occur. It's worth noting that predicting drop coalescence is a challenging problem, and achieving high accuracy may require using advanced machine learning techniques and large, high-quality datasets.

## Getting Started

### Hardware requirement

*   Programming language: Python (3.5 or higher)
*   Platform: Google Colab Pro
*   GPU: Tesla T4
*   Google Drive space: 200GB

### Software requirement

| Package Requirement                        |
|--------------------------------------------|
| os                                         |
| numpy                                      |
| pandas                                     |
| math                                       |
| seaborn                                    |
| matplotlib                                 |
| pytorch                                    |
| sklearn                                    |

## Dataset 
The experimental data can be available upon reasonable request to Dr. Nina Kovalchuk (n.kovalchuk@bham.ac.uk)

## Implementation
### Dataset processing
We use max-min normlazation to rescale the raw dataset, and split it into three for training, validation and test repectively. 
|                           |   Coalescence   | Non-coalescence | Total |
| --------------------------| --------------- | ----------------| ------------- |
| Total dataset             | 1162 | 369 | 1531  |
| Training dataset          | 1012 | 219 | 1231 |
| *Balanced training dataset* | 219 | 219 | 438 |
| Validation dataset        | 50 | 50 | 100 |
| Test dataset              | 100 | 100 | 200 |
*Balanced training dataset balances two labels of training dataset. 

### Generating synthetic data
We trains stardard CVAE, DSCVAE, LCVAE to generate efficient synthetic samples for predictive models. 

### Evaluating predictive models
We trains two tree-based predictive models ``dscvae-for-drop-coalescence/PredictiveModel``, random forest classifier and XGBoost classifier, to predict coalescence results. 

## Contact
Kewei Zhu - kz1018@york.com<br>
Sibo Cheng - sibo.cheng@imperial.ac.uk<br>
