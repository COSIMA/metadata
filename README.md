# metadata
Metadata for published COSIMA data sets. Uses the [addmeta](https://github.com/coecms/addmeta) tool.

To add global metadata *and* ocean specific metadata to a number of ocean data files:

```
addmeta -l globals -m ocean.yaml <ocean_data_files> 
```

`globals` is a text file containing all the individual global metadata files for simplicity 