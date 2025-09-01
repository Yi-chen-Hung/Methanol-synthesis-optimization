# Methanol-synthesis-optimization
Using artificial neural network to optimize the methanol synthesis process.<br>

First of all, I have calculated the target parameter (Methanol selectivity, CO2 conversion rate, CO selectivity) 
based on the mole-flow fraction from reactor's input and output in a real methanol synthesis reactor.

According to the methanol reaction equation and related formula
<br>1.  x1 CO2 + 3H2 <--> CH3OH +H2O (main reaction)
<br>2.  x2 CO + 2H2 <--> CH3OH
<br>3.  x3 CO2 + H2 <--> CO + H2O (side reaction)

Example:<br>
[Target parameter calculation.py](Targetparametercalculation.py)<br>
Outcome:<br>
![Target_parameter](images/Target_parameter_calculation.png)

