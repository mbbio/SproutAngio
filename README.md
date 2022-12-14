# SproutAngio
A tool for quantitative analysis of sprouting angiogenesis and endothelial lumen space.

## Citation
If you use our scripts in a work contributing to a scientific publication, we ask that you cite our related publication:
##### "SproutAngio: An Open-Source Bioimage Informatics Tool for Quantitative Analysis of Sprouting Angiogenesis and Lumen Space"

## Features
- 3D segmentation of fibrin bead assay confocal microscopy images
- Automated analysis of endothelial lumen space:
  - Width measurement from different segments of the sprouts
  - Paired nuclei distance analysis
- Branch analysis for retina images

## Gallery

![Gallery01](https://user-images.githubusercontent.com/65368053/196526490-f509905e-aeae-40e8-9a3e-34fbbfa5b48a.png)
![Gallery02](https://user-images.githubusercontent.com/65368053/196526495-eb822172-dcfd-4895-b6f3-62ef8789dbd4.png)
![Gallery03](https://user-images.githubusercontent.com/65368053/196526497-64f23187-efc2-45e0-bdc7-2503ce055dcf.png)
![Gallery04](https://user-images.githubusercontent.com/65368053/196526499-6f3f703c-ca0d-4ada-9f52-a2b8388f3517.png)
![Gallery05](https://user-images.githubusercontent.com/65368053/196533918-7a754f1e-d43a-47f8-b1df-af9ff565a95d.png)

## Details

The main tool for the in vitro fibrin bead assay analysis is: SproutAngio_main.

For volumetric measurement of the sprouts, you can view the 3D image using the napari viewer:
![Volume_segmentation github](https://user-images.githubusercontent.com/65368053/196514175-f43d1f0e-4d91-4799-8da6-ffa87d2bbabe.png)

For in vivo retina analysis you can use Retina_analysis tool. Before the section "creating a filled polygon to draw a central bead" in the retina analysis, do the following in the opened napari window to cover the retina area:
![SproutAngio github retina image](https://user-images.githubusercontent.com/65368053/196512628-3a50c525-9d02-4e7e-800e-6da2202ee8c0.png)

### Prerequisites for running the code: 

To install the necessary dependencies for fibrin bead assay analysis, statistical analysis and drawing graphs, run:
```
pip install "napari[all]"
pip install czifile
pip install openpyxl
pip install seaborn
pip install fil-finder
```

To install the necessary dependencies for retina analysis:
```
pip install skan
```

### Funding

This work was supported by Horizon 2020 Framework Programme (Marie Sklodowska Curie grant agreement 740264), Academy of Finland (321535, 328835, 353376), GeneCellNano Flagship Program 337431, wedish Research Council (Contract No. 2013-9279 and 2021-01919), European Research Council (project EC-ERC-VEPC, Contract No. 74292).

### Bugs
If you experience an error in the code while working, please report it under Issues/New issue
