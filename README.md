## Installation
```bash
Install MatLab and load demo.m into workspace.
```
## Running the project
open demo.m in the python and tap 'RUN' in the ToolBar
## 
```python
Function MTLF will be resulting the output showed below.

# hyps  and combination of data sets would print the accuracy in each iteration
For example:
>> demo(PIE)
Load data...
1 2
Init parameters...
Running MTLF...
0.100000 0.213014
0.010000 0.421731
0.001000 0.503990
0.000100 0.492327
0.000010 0.490485
0.000001 0.489871
0.000000 0.489871

These are the acuracy for the 1,2 dataset{'PIE05','PIE07','PIE09','PIE27','PIE29'}.ie, "PIE05,PIE07" for each combination of the data set and hyps mentioned and 
the results will be printed for all possible combination of the datasets with the hyps mentioned.


```

simillarly open demo1.m in the python and tap 'RUN' in the ToolBar
## 
```python
Function MTLF will be resulting the output showed below.

# hyps  and combination of data sets would print the accuracy in each iteration
For example:
>> demo_1(Caltech)
Load data...
1 2
Init parameters...
Running MTLF...
0.001000 0.395370
0.010000 0.395370
0.100000 0.395370
1.000000 0.395370

These are the acuracy for the 1,2 dataset{'amazon_SURF_L10','Caltech10_SURF_L10','dslr_SURF_L10','webcam_SURF_L10'}.ie, "amazon_SURF_L10','Caltech10_SURF_L10" for each combination of the data set and hyps mentioned 

```

## Optimization Function
Based on the type of output needed we have to change the optimization function.
```python
For MMD:
At = At-gamma*(1*sumA+1*sumA_targ+ 2*A0+h*MMD+0.00*sub1+0.00*sub2+0.00*XL);
For L1Norm:
At = At-gamma*(1*sumA+1*sumA_targ+ 2*A0+0.00*MMD+h*sub1+0.00*sub2+0.00*XL);
For L2Norm:
At = At-gamma*(1*sumA+1*sumA_targ+ 2*A0+0.00*MMD+0.00*sub1+h*sub2+0.00*XL);
For Laplacian:
At = At-gamma*(1*sumA+1*sumA_targ+ 2*A0+0.00*MMD+0.00*sub1+0.00*sub2+0.h*XL);

```




