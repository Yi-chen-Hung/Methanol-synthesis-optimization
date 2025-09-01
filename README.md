# Methanol-syntehsis-optimization

Using artificial neural network to optimize the methanol synthesis process.<br>

First of all, I have calculated the target parameter (Methanol selectivity, CO2 conversion rate, CO selectivity) 
based on the mole-flow fraction from reactor's input and output in a real methanol synthesis reactor.

According to the methanol reaction equation and related formula
<br>1.  x1 CO2 + 3H2 <--> CH3OH +H2O (main reaction)
<br>2.  x2 CO + 2H2 <--> CH3OH
<br>3.  x3 CO2 + H2 <--> CO + H2O (side reaction)

⚠️ Confirm the calculation steps and logistic with professor

Example code:<br>
[Target parameter calculation.py](Target%20parameter%20calculation.py)<br>
Dataframe Output:<br>
![Target_parameter](images/Target_parameter_calculation.png)<br>


# Feature selection and correlation
Since there are too many potential columns in the raw data that could be used as the input of an artificial neuron network model, so the feature selection is inevitable <br>
I have ran over the correlation analysis between target parameter and all the 74 columns (Non-stream) and filter the one whose |r|>0.5.
There are 14 potential columns that could be used as ANN model input parameters.

⚠️ Principal component analysis (PCA) could be added

Example code:<br>
[Feature selection and correlation](Feature%20selection%20and%20correaltion.py)<br>
Correlation Output:<br>
![Target_correlation](images/Feature%20selection%20and%20correlation.png)

# Simple ANN establishment
ANN hyperparameters:<br>
Algorithms : Multi-Layer Perceptron for regression<br>
Number of hiddden layers : 3<br>
Neuron numbers: (64, 32, 16)<br>
Activation function : ReLU <br>

⚠️ Try to adjust the hyperparameters of the ANN model so as to improve model's performance

Example code:<br>
[](ANN%20establish.py).<br>
First Training Output:<br>
![Accuracy](images/ANN%20first%20run%20accuracy.png)
![Methanol selectivity](images/Methanol%20selectivity%20ANN%20parity.png)
![CO2 conversion rate](images/CO2%20conversion%20rate%20ANN%20parity.png)
![CO selectivity](images/CO%20selectivity%20ANN%20parity.png)

