# Rearrange
A little python script for converting HGIS DualEM + GPS data files to a standard CSV format.

##  Rearrange.py
Usage:

```python
import Rearrange

Rearrange.dualem("~/path/to/input_file.csv","~/path/to/output_file.csv")
``` 
The data is arranged in the output file in the following format:
```
,Time,Lon,Lat,1mHCPcon,2mHCPcon,1mHCPmag,2mHCPmag,1mPRPcon,2mPRPcon,1mPRPmag,2mPRPmag
0,3,150.6638,-34.0222017,3.3,5.9,0.32,0.8,3.5,3.8,-0.72,-1.84
1,7,150.6638,-34.0222017,3.0,5.9,0.33,0.75,3.6,3.9,-0.72,-1.83
2,11,150.6638,-34.0222017,3.7,5.8,0.32,0.8,3.6,3.5,-0.73,-1.84
...
```

Where the readings (1mHCPcon) are translated in the following manner.
```
[1][m][HCP][con]
```
* The first character represents the intercoil spacing
* The second character represents the units for the intercoil spacing  
* Characters 3, 4 and 5 identifies the coil geometry. HCP for horizontal co-planar and PRP for perpendicular
* The last 3 characters identifies the attribute. con for the conductivity and mag for the magnetic susceptibility
