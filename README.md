# SproutAngio
A tool for quantitative analysis of sprouting angiogenesis and endothelial lumen space.
If you use our scripts in a work contributing to a scientific publication, we ask that you cite our related publication:
### SproutAngio: An Open-Source Bioimage Informatics Tool for Quantitative Analysis of Sprouting Angiogenesis and Lumen Space

The main tool for the in vitro fibrin bead assay analysis is: SproutAngio_main.

For volumetric measurement of the sprouts, you can view the 3D image using the napari viewer:
![Volume_segmentation github](https://user-images.githubusercontent.com/65368053/196514175-f43d1f0e-4d91-4799-8da6-ffa87d2bbabe.png)

For in vivo retina analysis you can use Retina_analysis tool. Before the section "creating a filled polygon to draw a central bead" in the retina analysis, do the following in the opened napari window to cover the retina area:
![SproutAngio github retina image](https://user-images.githubusercontent.com/65368053/196512628-3a50c525-9d02-4e7e-800e-6da2202ee8c0.png)

### Prerequisites for running the scripts: 
(Requirement libraries can be installed using pip install)
It is advised to start with installing napari.
```
astropy 4.3, 
czifile 2019.7.2, 
fil-finder 1.7, 
matplotlib 3.3.4, 
napari 0.4.12, 
numpy 1.21.5, 
scikit-image44 0.18.1, 
scipy 1.6.2, 
seaborn 0.11.2, 
skan 0.10.0. 
```
### Bugs
If you experience an error in the code while working, please report it under Issues/New issue
