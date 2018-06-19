# IEEE-39-bus-power-system
A full-replica MATLAB/Simulink dynamic model of the IEEE 39-bus power system, including dynamic models of conventional generation and dynamic load profiles. 
## Simulink model
### Transmission line parameters
The IEEE 39-bus does not specify any line lengths; therefore, we choose them to obtain a propagation speed just below the speed of light. 
### Loads profiles
We include two types of load profiles: constant and realistic. The constant load profiles are the original data of the IEEE 39-bus system. The realistic load profiles are active and reactive components inferred by time series data, adapted from a monitoring system based on Phasor Measurement Units (PMUs) installed in the 125-kV grid of the city of Lausanne, Switzerland. The resolution of the time series is 20 milliseconds and the profiles are voltage and frequency independent. 
## The real-time simulator 
We use the Opal-RT real-time digital simulator OP5600, coupled with the eMEGAsim PowerGrid running on the RT-LAB real-time simulation platform. For installation, user guide and more information of the real-time simulator go [here](https://www.opal-rt.com/).
## Software 
The following software is required to run the model:
* MATLAB Version 8.5.1 (R2015aSP1)   
* Simulink Version 8.5.1 (R2015aSP1)   
* ARTEMIS Blockset Version 7.2.2.1206 (R2015a)   
* RT-LAB Version v11.2.2.108 (R2015a.x), available [here](https://www.opal-rt.com/)
### Note
Before building the model, you need to add an S-function file (sfun_discreteVariableDelay.c) in the files section of your model. This file can be found under the following path C:\Program Files (x86)\MATLAB\R2015aSP1\toolbox\physmod\powersys\powersys. Add the file and choose ascii in Mode, S-Function in Category, and Before Compilation in the Transfer Time.
## References 
For a more detailed description of this full-replica IEEE 39-bus system model, refer to the following references:
* Yihui Zuo, Fabrizio Sossan, Mokhtar Bozorg, Mario Paolone, “Dispatch and Primary Frequency Control with Electrochemical Storage: a System-wise Verification,” Accepted for presentation at 2018 IEEE PES Innovative Smart Grid Technologies Conference Europe (ISGT-Europe), 2018. Available [here](https://arxiv.org/abs/1806.05825).
* Asja Derviškadić, Yihui Zuo, Guglielmo Frigo, Mario Paolone, “Under Frequency Load Shedding based on PMU Estimates of Frequency and ROCOF,” Accepted for presentation at 2018 IEEE PES Innovative Smart Grid Technologies Conference Europe (ISGT-Europe), 2018. Available [here](https://arxiv.org/abs/1805.00744).
