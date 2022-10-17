# SproutAngio
A tool for quantitative analysis of sprouting angiogenesis and lumen space.
If you use our scripts in a work contributing to a scientific publication, we ask that you cite our related publication:
### SproutAngio: An Open-Source Bioimage Informatics Tool for Quantitative Analysis of Sprouting Angiogenesis and Lumen Space

<img src="https://user-images.githubusercontent.com/65368053/159856802-00f8b357-3b63-4545-a16e-eadf49d53ab8.gif" width="200" height="200">
<img src="https://user-images.githubusercontent.com/65368053/159856808-172a5a02-a893-42fa-9c66-73cbc7dceccf.gif" width="200" height="200">

The main scripts, which are linked to the in vitro fibrin bead assay analysis are: Py_Angio_01 and Py_Angio_02. 
Other than these, there are several independent scripts which are linked to the article including Py_branch_analysis that we used for in vivo retina analysis. 

### Prerequisites for running the scripts: 
(Requirement libraries can be installed using pip install)
```
Python 3.8
astropy41 4.3, 
czifile 2019.7.2, 
fil-finder 1.7, 
matplotlib42 3.3.4, 
napari 0.4.12, 
numpy43 1.21.5, 
pickle 4.0, 
scikit-image44 0.18.1, 
scipy 1.6.2, 
seaborn 0.11.2, 
skan 0.10.0, 
stardist 0.7.3. 
```
### Bugs
If you experience an error in the code while working, please report it under Issues/New issue

### Manual_distance_measurement script:
We used this for manual measurement. On napari viewer, you can put points by clicking and the order you put them
would be important. The measurement will be done between first point and second point and then third and fourth etc. 
Here are the helper images
![Manual distance measurement 01](https://user-images.githubusercontent.com/65368053/159269140-2bdea4d7-04dc-421e-928b-b9f4d0015efb.JPG)
![Manual distance measurement 02](https://user-images.githubusercontent.com/65368053/159269154-db81dd1d-3488-4d6d-aabf-0e06831be38a.JPG)

### Stardist_nuclei_segmentation:
We added necessary functions for bead assay usage of stardist2D nuclei prediction.

### Sprout_volume_measurement:
We modified the segmentation part, more specifically changed the mask for segmentation 
to do 3D sprout segmentation and volume measurement.

### Graph_and_statistics:
We prepared a script to create graphs and statistics from your data in excel. 
We had our excel data prepared like this before running the script:
![Graphs and statistics](https://user-images.githubusercontent.com/65368053/159269242-29f25aaa-b687-4fd3-8457-56b83cdb7ea0.JPG)
