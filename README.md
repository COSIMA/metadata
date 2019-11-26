# metadata
Metadata for published COSIMA data sets. Uses the [addmeta](https://github.com/coecms/addmeta) tool.

To add global metadata *and* ocean specific metadata to a number of ocean data files:

```
addmeta -l global/globals -l ocean/oceanlist -m global/model_1deg.yaml <ice_data_files>
```

`globals` is a text file containing all the individual global metadata files for simplicity. 
`oceanlist` is a list of all the metadata files common to all ocean models. Metadata for individual
variables are included in this list for simplicity. They have no effect if the variable does not
exist in the file that is being operated on.

The command for the ice data files is similar
```
addmeta -l global/globals -l ice/icelist -m global/model_1deg.yaml <ice_data_files>
```

There are resolution specific global metadata files that are common across the ice and ocean models.
To process the quarter and one tenth degree models run the same commands but substitute `global/model_025de.yaml`
and `global/model_01deg.yaml` respectively.
