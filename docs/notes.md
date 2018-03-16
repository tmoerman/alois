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
    