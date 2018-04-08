# Objectives

[MF]
> waar we naar toe willen is het volgende:
> - presenteren van dit als een atlas van de early onset van AD
> - bescrhijven van globale veranderingen - welke gelijk moeten zijn aan al gekende modellen
> - kunnen we regiospecifieke veranderingen vinden??
> - kunnen we plaque-gerelateerde veranderingen binden??

# Observations

## strong batch effect
* may detrimentally influence feature selection, e.g. by statistical leverage
* cause: logcpm -> z-score

# Considerations
* Compensate batch effect by mean-centering per batch?

# Wild ideas (possibly total BS)
* transform the problem into a synthetic multitask learning problem:
    * for every KI batch: make a variable YEN_batch1, YEN_batch2 
    * NaN for all other batches for this variable
    * 0 for all WT for all of the synthetic variables
* binarize the outputs to turn it into a multilabel classification problem
    * needs a cutoff value to binarize output
    
    ```
    KI      WT      Young       Old     PlaqueClose
    
    
    ```
    
