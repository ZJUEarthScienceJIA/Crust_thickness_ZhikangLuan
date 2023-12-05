# Crust thickness XGBoost regression and Gangdese crust thickness evolution
---
# Overviews
This project provides a XGBoost Regression model to predict crust thickness based on their major and trace elements.
Version: Python 3.8 IDE: Jupyter We recommend the readers to download Anaconda (https://www.anaconda.com/download/). The install time is typically less than one hour.
# Requirements
All python library requirements are all in the ''Requirements.txt'' file and shows as below.

    matplotlib == 3.7.2
    numpy ==  1.22.3
    pandas ==   1.5.3
    scikit-learn  == 1.3.0
    seaborn ==   0.12.2
    scipy ==   1.8.1
    xgboost ==  1.7.3 

# Datasets
All training datasets, validation datasets and application datasets are all in the datasets files.

     Training_model_1.xlsx : Model 1 training and test datasets
     Training_model_2.xlsx : Model 2 training and test datasets
     Validation_Mexico.xlsx: Validation datasets of Trans-Mexican Volcanic Belt
     Validation_NorthChinaCraton.xlsx: Validation datasets of North China Craton
     Gangdese_Datasets.xlsx: Application datasets of Gangdese tarrane
     

# Code Functions

    CT_XGB_RF_ET_Final_Model 1.ipynb : Model 1 training and saving
    CT_XGB_RF_ET_Final_Model 2.ipynb : Model 2 training and saving
    XGBoost model1_ application.ipynb : Open Model 1 for applications
    XGBoost model2_ application.ipynb : Open Model 2 for applications

# Model Training 
This part is used for introducing the model training and saving. 
The model training use the major elements （SiO2 TiO2 Al2O3	FeOt CaO MgO MnO K2O Na2O P2O5) and trace elements (Cr Ni Rb Sr Y Zr Nb Ba La Ce Pr Nd Sm Eu Gd Tb Dy Er Yb Lu Hf Th Ln(La/Yb(n)) Sr/Y).

## Model 1
Model 1 uses global arc and orogenic magmatic whole rock geochemistry data including Gangdese with XGboost algorithm to build model to calculate the crust thickness (CT).

    CT_XGB_RF_ET_Final_Model 1.ipynb

    Parameters of XGBoost: 
                           base_score=0.3, boost_params='gbtree', booster=None,
                           callbacks=None, colsample_bylevel=None, colsample_bynode=None,
                           colsample_bytree=0.5, early_stopping_rounds=None,
                           enable_categorical=False, eval_metric=None, feature_types=None,
                           gamma=None, gpu_id=None, grow_policy=None, importance_type=None,
                           interaction_constraints=None, learning_rate=0.1, max_bin=None,
                           max_cat_threshold=None, max_cat_to_onehot=None,
                           max_delta_step=None, max_depth=10, max_leaves=None,
                           min_child_weight=100,  monotone_constraints=None,
                           n_estimators=250, n_jobs=None, num_parallel_tree=None,
                           

## Model 2
Model 1 uses global arc and orogenic magmatic whole rock geochemistry data barring Gangdese with XGboost algorithm to build model to calculate the crust thickness (CT).

    CT_XGB_RF_ET_Final_Model  2.ipynb

    Parameters of XGBoost:
                           base_score=0.3, boost_params='gbtree', booster=None,
                           callbacks=None, colsample_bylevel=None, colsample_bynode=None,
                           colsample_bytree=0.5, early_stopping_rounds=None,
                           enable_categorical=False, eval_metric=None, feature_types=None,
                           gamma=None, gpu_id=None, grow_policy=None, importance_type=None,
                           interaction_constraints=None, learning_rate=0.1, max_bin=None,
                           max_cat_threshold=None, max_cat_to_onehot=None,
                           max_delta_step=None, max_depth=5, max_leaves=None,
                           min_child_weight=100, monotone_constraints=None,
                           n_estimators=250, n_jobs=None, num_parallel_tree=None,
                           predictor=None,

# Data Predictions
This part is used to introduce how to apply our models. If you just  want to use our model, you can run the next two files.
Make sure your dataset has "SiO2 TiO2 Al2O3 FeOt CaO MgO MnO K2O Na2O P2O5 Cr Ni Rb Sr Y Zr Nb Ba La Ce Pr Nd Sm Eu Gd Tb Dy Er Yb Lu Hf Th Ln(La/Yb(n)) Sr/Y" those elements to use our model.
XGBoost Regression tolerates the null value. If dataset does not contain part of elements, just make it empty!
## Model 1

    XGBoost model1_ application.ipynb 

First input the datasets. Then drop other columns and run the cells.
Rename the output files. 
The calculated crust thickness will add to the last column.
## Model 2 

    XGBoost model2_ application.ipynb 

First input the datasets. Then drop other columns and run the cells.
Rename the output files. 
The calculated crust thickness will add to the last column.


Please run the CT_XGB_RF_ET_Final_Model 1.ipynb, CT_XGB_RF_ET_Final_Model 2.ipynb, XGBoost model1.0_ application.ipynb, XGBoost model2.0_ application.ipynb in turn. You can change the filenames and parameters as you need. 

# Contributors
Zhikang Luan；
Contant Email: zinkluan@zju.edu.cn
