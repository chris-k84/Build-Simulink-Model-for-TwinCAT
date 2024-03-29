# Build your Simulink model for Deployment in TwinCAT RT

## Overview

It is possible to parameterise the build of a Simulink module using the Simulink coder tool options in MATLAB itself. Manually setting these can take a lot of time and requires effort, especially if you are building a number of models or changing the parameters regularly. This live script automates the process of setting a model up for building with the Simulink Coder and TE1400. It will also give you a base sample for how you would go about automating your build and deployment.

![Screenshot](LiveScript.png)

This script allows you to parameterise a given model, which you select in the first text box tool. Following that you simply set the features you want the deployment to have, creating PLC libraries, online changeable models etc

## Requirements

This demonstration was built and tested with R2022a. It will likely mostly run in R2021a and R2021b.

TE14xx 2.3.1.0
TC4024.20

## Instructions
* Open the Live Script, SetForTwinCATGrt.mlx file.
* Select the options required for the build 
* hit the Build button at the bottom

The build option function has been included that will allow you to run the build in parrallel to the MATLAB interface, thus allowing you to contiue working, or use the performance analysis tools to check build times etc.

<mark><span style="color:black">If you are building for a 64bit system make sure to specifiy your own driver signing certificate.</span></mark>

<mark><span style="color:black">Be aware that you will need to enable the TcCOM wrapper or PLC FB to create a PLC library.</span></mark>

## Contributing

If you would like to ontribute thats great, this is a developing project.
As a tip to find out what you have access to get the object params from your model:

get_param('YourModelName','ObjectParameters');

for example

get_param('MyTestModel','ObjectParameters');

replace 'MyTestModel' with your model name.

* fork the repo, 
* branch 
* make your changes
* submit a PR



