**MATLAB to HDF5 Converter for CLIMADA v6.0.1**

In CLIMADA v3, it was possible to convert matlab `.mat` files to HDF5. However, this feature was deprecated in newer CLIMADA releases (v6). This notebook documents a replacement approach to perform that same conversion **without** needing to downgrade or maintain older versions of CLIMADA.

### Approach

1. I studied the HDF5 structure produced by CLIMADA v3  
2. Reconstructed the expected HDF5 schema (groups, datasets, dimensions)  
3. Wrote a custom script to convert the MATLAB `.mat` hazard data into this HDF5 structure
4. Downloaded the file as a hdf5 format into the application folder 
5. Tested 4 in the example script in the application folder.

### How to use
The **custom folder** in this repo contains the notebook for the converstion
Download and add it into the 'script' folder in the climada V6 codebase from github. 
You can either **A**. create a subfolder named 'custom' and add the notebook: {'script/custom/notebook'}  or **B**. add it directly into the 'script' folder: {'script/notebook'}.

if you do A, you don't have to change the file path when using the function but make sure to use the correct file path with B

### Example File 

The application folder in the repo contains the example data and test files

The hdf5 data downloaded into the applications/eca_san_salvador are: 'Salvador_hazard_FL_2015.hdf5 and 
'Salvador_hazard_FL_2040_extreme_cc.hdf5'.
They have been tested and works with all the .ipynb file in the same folder