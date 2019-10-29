# metadata
Metadata for published COSIMA data sets. Uses the [addmeta](https://github.com/coecms/addmeta) tool.

To add global metadata *and* ocean specific metadata to a number of ocean data files:

```
addmeta -l globals -m ocean.yaml <ocean_data_files> 
```

`globals` is a text file containing all the individual global metadata files for simplicity 

The same works for the ice data files
```
addmeta -l globals -m ice.yaml <ice_data_files>
```

Some of the ice variables which have standard names don't have that attribute defined, so
they have variable specific attribute files. These can be processed in a separate step
```
addmeta -m aice_m.yaml <aice_m_data_files>
```

Or do the ice variables one by one but all attributes at once (probably not a bad idea)
```
addmeta -l globals -m ice.yaml addmeta -m aice_m.yaml <aice_m_data_files>
```