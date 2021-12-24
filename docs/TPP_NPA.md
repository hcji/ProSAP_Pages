# TPP and NPA analysis

## Input
Data should be upload via *Data* menu, and click *Load proteomics*. You can upload
 multiple files in the same time. Then, please appoint each file as *case sample #1*, 
 *control sample #1*, *case sample #2*, *control sample #2*. The last two of them are 
 not compulsory. However, experimental replicates are highly recommended for reducing
 the false positive. 
 
After input, you can check and adjust the parameters with clicking the *Params* button.
 Then, select a statistical method for preprocessing the uploaded data with the *Analysis*
 menu. There are three methods for choosing: TPP method, NPARC method and Distance based
 method. 
 
## Parameters

### TPP method
The workflow of TPP analysis is implemented as described in the Savitski protocol. See the
 [reference](https://www.nature.com/articles/nprot.2015.101) for the details. The parameters
 includes:
 
- *Min R2*: The threshold of the goodness-of-fit of the melting culve fitting. Default: 0.8
- *H-Axis*: The threshold of how much protein is precipitated for calculating the Tm. Default: 0.5
- *Max Plateau*: Plateau (lower horizontal asymptote) of the fitted melting curve under the given condition. Default: 0.3
- *Replicate Check*: Whether to use the filtering criteria based on the replicates:  
 (1) One of the P values for the two replicate experiments < *p value threshold #1* and the other one *p value threshold #2*  
 (2) The coefficient of determination R2 are over the user-defined thresholds.  
 (3) The minimum slope in each of the control versus treatment experiments is lower than user-defined thresholds.  
 (4) The melting point shifts in the vehicle versus treatment experiments have the same direction.  
 (5) Both melting point differences in the two pairs of control versus treatment experiments are greater than the melting point difference between the two vehicle controls.  
- *Min Slope*: Slope threshold of the fitted melting curve at the inflection point under the given condition

<div align="center">
<img src="melting_curve.png" width="60%">
</div>

### NPARC method
The workflow of NPARC analysis is implemented as described in the Dorothee Childs's paper. See the
 [reference](https://linkinghub.elsevier.com/retrieve/pii/S1535947620316522) for the details. The parameters
 includes:

- *Min Null R2*: The threshold of the goodness-of-fit of the *Null model*. Default: 0.8
- *Min Alt R2*: The threshold of the goodness-of-fit of the *Alternative model*. Default: 0.8
- *Max Plateau*: Plateau (lower horizontal asymptote) of the fitted melting curve under the given condition. Default: 0.3

<div align="center">
<img src="nparc_curve.png" width="60%">
</div>

### Distance method
Distance based model is more straightforward. The relative fold changes of each protein of case and
 control groups are fitted into melting curves, respectively. The distance of the protein between
 case and control group is calculated for evaluating the changing of the thermal stability. The
 parameters includes:

- *Metrics*: Which function is used for calculating the distance.
- *Min R2*: The threshold of the goodness-of-fit of the melting culve fitting. Default: 0.8
- *Max Plateau*: Plateau (lower horizontal asymptote) of the fitted melting curve under the given condition. Default: 0.3

<div align="center">
<img src="distance_function.png" width="35%">
</div>
