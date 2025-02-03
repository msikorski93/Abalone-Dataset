# Abalone-Dataset
![ alt text ](https://img.shields.io/badge/license-MIT-green?style=&logo=)
![ alt text ](https://img.shields.io/badge/-Jupyter-F37626?logo=Jupyter&logoColor=white)
![ alt text ](https://img.shields.io/badge/-NumPy-013243?logo=Numpy&logoColor=white)
![ alt text ](https://img.shields.io/badge/-TensorFlow-FF6F00?logo=TensorFlow&logoColor=white)
![ alt text ](https://img.shields.io/badge/-Keras-D00000?logo=Keras&logoColor=white)
![ alt text ](https://img.shields.io/badge/-pandas-150458?logo=pandas&logoColor=white)
![ alt text ](https://img.shields.io/badge/-scikit--learn-F7931E?logo=scikitlearn&logoColor=white)

The age of an abalone can be estimated by cutting its shell, staining it, and counting the number of rings in the shell through a microscope. However, this process is time-consuming, boring, and can cause death to the creature. Therefore, it is necessary to find another non-collision method for age estimation. Other physical measurements, which are easier to collect, can be used to determine the age.  The subject of this notebook was to estimate the number of rings based on other independent features: either as a continuous value or as a classification problem.

**Achieved test metrics for regression task:**

|         | MSE      | RMSE     | R²       | MAE      |
|---------|----------|----------|----------|----------|
| **MLP** | 4.307223 | 2.071724 | 0.561825 | 1.463248 |
| **CBR** | 4.589306 | 2.139295 | 0.533128 | 1.572072 |
| **ANN** | 4.421819 | 2.097471 | 0.599223 | 1.519808 |
| **GPR** | 4.340534 | 2.083136 | 0.606591 | 1.487793 |

The best model overall was GPR (Gaussian process regression). While its MSE and RMSE were slightly higher than MLP (multilayer perceptron) model, it had the highest R² and a competitive MAE. This suggests that GPR was doing the best job in terms of explaining the variance in the data, with relatively low error rates. It balanced error rates and variance explanation well. The key to achieve very good performance with GPR depends greatly on kernel choice and is one of the most important components. This determines the structure of the function we are modeling and controls how points are related in the input space.
