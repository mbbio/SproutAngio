# SproutAngio
A tool for quantitative analysis of sprouting angiogenesis and endothelial lumen space.

## Citation
If you use our scripts in a work contributing to a scientific publication, we ask that you cite our related publication:
##### "SproutAngio: An Open-Source Bioimage Informatics Tool for Quantitative Analysis of Sprouting Angiogenesis and Lumen Space"
##### https://www.nature.com/articles/s41598-023-33090-6 

## Features
- 3D segmentation of fibrin bead assay confocal microscopy images
- Automated analysis of endothelial lumen space:
  - Width measurement from different segments of the sprouts
  - Paired nuclei distance analysis
- Branch analysis for retina images

### Funding
This work was supported by Horizon 2020 Framework Programme (Marie Sklodowska Curie grant agreement 740264), Academy of Finland (321535, 328835, 353376), GeneCellNano Flagship Program 337431, wedish Research Council (Contract No. 2013-9279 and 2021-01919), European Research Council (project EC-ERC-VEPC, Contract No. 74292).

### Bugs
If you experience an error in the code while working, please report it under Issues.

## Step-by-step guide to install and use the tool for beginners:
A. INSTALLING
1. If you are new to Python, one of the best ways to install and use SproutAngio tool is by installing Anaconda Navigator. It simplifies the package management and installation process. Install Anaconda using their updated installation guide here: https://docs.anaconda.com/anaconda/install/ 
Note! After the installation of Anaconda update it to the current version if needed. 
2. Before installing SproutAngio and the necessary libraries, you need to create a new working environment using Anaconda. It always opens the base (root) environment as a default (marked by yellow rectangular in the figure below). 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/5ed275a4-98f8-4f15-8b93-30eae68a1439)
3. Click “Environments” and then “Create” (marked in yellow in the figure below) to create a new working environment for SproutAngio.
   Napari team recommends python=3.11 currently.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/1e344d76-8c0d-45e3-9617-b385af3c4f93)
5. After creating the working environment, you can now go back to the home tab of Anaconda Navigator. Then, you can install one of the interactive environment plugins, in this case we prefer using JupyterLab (marked with yellow rectangular to figure below) simply because we feel it is easier to use.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/4ffb2038-fc96-4f8c-b6d0-da8178882285)
6. Once JupyterLab is installed, you can launch it (marked in figure with yellow).
![image](https://github.com/mbbio/SproutAngio/assets/65368053/30075275-d112-48ed-bf87-b50ab9e0777c)
7. JupyterLab will simply open using your internet browser. Notice that Jupyterlab has multiple tabs in both left and right sides. Left tabs are file browser, terminals and kernels, table of contents, extension manager. On the right tab, you can create new launcher tabs by clicking the + icon. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/85083bb6-d554-41e4-99b7-6c2992e791a9)
8. Now select a file path for your working environment. As an example, here we double-click the Desktop in the browser (marked in yellow in the figure below). If you do not see your desktop, you can alternatively choose some other file path you know such as Documents or Downloads.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/87e138a7-db5b-42e7-b4a1-20377e724c9c)
9. Then, click the new folder icon to make a new folder on your desktop (see arrow in the figure below). We name it here as SproutAngio.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/a0d167fa-04fc-487f-b0e6-1739f2d5e2c0)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/03e36161-bb8a-4468-b9e7-6897b57bb2f9)
10. You can double click and get inside the newly created SproutAngio folder, which is empty right now. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/a2b7fcdd-2f2e-4600-873f-add8a3a08023)
11. Now, you will install the necessary dependencies to use the SproutAngio tool. By clicking on the Terminal, we will open a terminal (marked in yellow in the figure below).
![image](https://github.com/mbbio/SproutAngio/assets/65368053/c4760509-ad1f-4ccf-86bb-60ce9bab00d1)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/32ae3707-16b4-4a68-9def-f92337aaaa10)
12. Next part is the installation of the prerequisites to use SproutAngio. Before reading the next parts, just a reminder that installations might take couple of minutes especially for the first library (Napari) and when you run, it might seem that it is doing nothing in the beginning, but actually it is. So, be patient. 
Before you continue, to briefly explain the function of each library:
Napari is a multi-dimensional image viewer for Python environment. Czifile is a library to read confocal microscopy Carl Zeiss Image (CZI) files. Seaborn is a data visualization library. Fil-finder is a package to analyze filamentary structures in fibrin bead assay. Skan is a library to analyze skeleton structures in retina images. Openpyxl and XlsxWriter are libraries to handle and transfer data in excel files.
13. Now, copy (ctrl – C) paste (ctrl - V) the installation commends, one by one, for the prerequisites and press “enter” key on your keyboard. You can check when the installation of each package finishes, by seeing the same starting path for your new commend:
pip install "napari[all]"

14. Then press enter on your keyboard. Note that installation might take couple of minutes depending on the internet speed and processing time.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/97abe50d-1a5c-42a4-94f8-2ca222ec9966)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/c8f92ef7-1b82-4827-804b-667cf54f9205)
15. Once you see the Users\your username... line, it means the installation is finished for that library. You can do the same copy-paste with the next line, to install the other libraries:

pip install czifile seaborn fil-finder skan==0.10.0 openpyxl XlsxWriter opencv-python

Then press enter

15. After the packages are installed, you can close the terminal:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/c80a8e26-432f-4020-a189-17926446e250)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/3a8fda1b-125f-4542-8791-481d3586ae29)
16. Now you can download SproutAngio files from GitHub, i.e., a website and cloud-based service used for storage and management of codes. If you do not have experience with using GitHub, we recommend using GitHub desktop application. To install it: https://desktop.github.com/ 

17. After installing GitHub, you can clone SproutAngio repository following the next steps (steps 1,2,4,5). 
Manual Uniform Resource Locator (URL) for SproutAngio, for step 2 cloning steps below is: https://github.com/mbbio/SproutAngio 

![image](https://github.com/mbbio/SproutAngio/assets/65368053/da477572-66fa-421f-8554-86a80447926f)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/1e2bd048-50b1-49df-bb11-2e17b460205a)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/cd3718ef-2ac1-457d-918d-33eac1386b1a)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/9bc05d73-561d-4181-af19-c083f666da6c)
Note: Alternatively, you can download the SproutAngio-main files here: 
https://github.com/mbbio/SproutAngio/archive/refs/heads/main.zip
However, if you download the files from the link directly, you need to unzip the “SproutAngio-main" zipped folder. Then you need to copy paste the files into the SproutAngio folder you created previously in JupyterLab.

18. After you downloaded the SproutAngio-main files, you still need to re-download the test samples. Normally, test data are uploaded in GitHub but, currently GitHub protocol does not let the downloading of large sized files unless it is from a direct link or Git Large File Storage (Git LFS). So, if you are not familiar with using Git LFS, you can click download the data here:   
https://github.com/mbbio/SproutAngio/raw/main/test_data/VEGFA_1ng.czi 
https://github.com/mbbio/SproutAngio/raw/main/test_data/VEGFA_10ng.czi 
https://github.com/mbbio/SproutAngio/raw/main/test_data/VEGFA_20ng.czi 

19. After your download is complete, copy paste these test samples inside the test_data folder inside your SproutAngio folder. (Notice that SproutAngio folder is the one you created using Jupyterlab, while SproutAngio-main folder is the one you downloaded from GitHub.)
Note! When you open the test_data folder for the copy-paste, you can see that there are already files with the same name in test_data folder but their size is 1kb, so they are not the actual image files. You can delete them.

20. Turn off the GitHub application and be sure to copy paste all 6 files below from GitHub downloaded files and test samples into the “SproutAngio” folder which you created with Jupyterlab. After all these files are in your Jupyterlab created folder, when you open the Jupyterlab tab in your internet browser, you can see the files in your folder there.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/d253d24d-d52f-4813-8c4f-ebd42449c374)

21. After you downloaded all, open the terminal again and run the following code, in case numpy is conflicting with skan:

pip install -r requirements.txt
<img width="1277" height="447" alt="image" src="https://github.com/user-attachments/assets/551fe42e-938b-4720-ab3c-470f37de479a" />

22. Well done! Now, everything is ready to start using the SproutAngio tool.


B. USING THE TOOL:         
1. To start using the SproutAngio, double click the SproutAngio_main file on the left (yellow rectangular in the figure below).
![image](https://github.com/mbbio/SproutAngio/assets/65368053/2af351d5-6d10-416f-8b70-7d9bd461ad70)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/eddf0598-1b23-4694-a10c-733be25a9834)
2. In this test run, we are using one of the images from our VEGFA dataset. So, if you cloned the github repository using github application and downloaded the test_data files seperately as instructed so far, then you do not need to change the path: 'test_data/VEGFA_10ng.czi'
However, if you downloaded the image samples from zenodo or if you are testing any other image file, then change the path. For example, if you have an image file named “FILENAME.czi”, inside test_data folder, then you need to change the image_path into: 
'test_data/FILENAME.czi'
![image](https://github.com/mbbio/SproutAngio/assets/65368053/9f4d0e33-67b8-4f93-9df9-3ed493863c64)
3. If you are not familiar with using Python, the code on the right is separated into different sections. Every section has a name referring to its function. When you click inside each section, you can run the code for only that section by clicking the “run” button. You need to run the first section first. This section includes the user defined basic parameters.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/c8cd64fc-92b7-4e60-b44d-bd1618b5dc32)
4. Then, you can click inside anywhere the second section and run it (see below the yellow rectangular). This section includes: importing the necessary libraries, channel separation, filtering, thresholding, skeletonization, bead removal and sprout segmentation.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/b819f172-a071-47b9-9047-5935e86025da)
Note! Running of this section will take some time depending on your computer’s power and you can observe this from the bottom of the panel which says “Busy” during the run. When the run finishes, it writes “Idle”.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/adb10336-5d2a-4aed-8585-cb7652d4674e)
5. Once it finishes, a Napari user interface window opens.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/37adf24b-177e-4509-8177-f1c27680b75d)
6. Now you have two application screens:
i) a SproutAngio Jupyterlab tab which is working on your browser
ii) a Napari viewer screen (not on your browser but as independent screen). Click on the Napari symbol to switch to Napari viewer screen.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/8fd8cd70-6dd8-475b-85a5-5a6c1f288c53)
7. Now continue in SproutAngio.   
The next section is nuclei segmentation part (marked with yellow rectangular in the image below). It includes importing the libraries and initial 3D nuclei segmentation. 

Reminder: Run finishes when you see “Busy” turn into “Idle” and it might take couple of minutes or more depending on your computer. After you run this section, you can click and see initial nuclei segmentation on the Napari screen if wanted. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/516889cf-5331-4140-9b8f-a7a3c506987b)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/be682976-2c4c-4f6c-93aa-cb3d6795a223)
8. Now run the next two parts one by one. Lumen analysis and results section includes segmentation of under-segmented nuclei, lumen space analysis (regional width and paired nuclei distance analyses) and printing the results in the Jupyter notebook. The volumetric analysis section includes 3D sprout segmentation and volume measurements.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/97441c59-cb6e-4cad-9e28-55827f4dabd6)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/d800957a-c4d8-49f1-8acf-9691cf21044f)
9. After both runs are finished, you can go to the Napari screen to see the result.

10. You can switch between the results by clicking on the eye symbol on the left. 
Also, as the top image is 3Dsprout segmentation result, you can move in the z-dimension using the bottom tool.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/af85bbba-592c-47cc-b376-0ca3275d6aca)
11. Since some of the results are in 3D such as “sprout_3D” and “Chan-Vese nuclei segmentation”, to see the 3D results, you can click “Toggle display” icon on the bottom left part. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/24025f14-c2dd-4e20-9aba-3d641806eec4)
12. To simplify the view, you can make only a couple of selected results visible by clicking the eye icons. In 3D image such as this you can use your mouse to move the orientation. Also, in 3D view if you press “shift” in your keyboard then you can move the 3D image using your mouse without changing its orientation. 

13. For more detailed information related to Napari viewer, you can check its tutorials: https://napari.org/stable/tutorials/fundamentals/viewer.html 

14. When you switch to the SproutAngio JupyterLab tab, you can see that the results are written on the right side after section 4 run and the paired nuclei distance result image was saved as “analyzed_image.png” on the left in the SproutAngio folder.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/e82e790a-127a-4b64-a699-17a68c86ed95)
15. You can easily change the parameters if needed for the filtering and % radius of the detected bead from the first section you ran. 
As examples: 
i)	When you increase/decrease the rad_ it will increase/decrease the detected bead area. Therefore, it will change the sprout segmentation. E.g., test by changing median_filtering = (6,6,6) and rad_ = 1.1. 

ii)	If you think the sprouts are not separated well enough, you can increase the radius and improve the sprout segmentation.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/7baf7067-c269-4842-9128-4e9761976f1e)
16. Another important section which you can easily change is the nuclei segmentation part (section #3). Depending on your image, if you are not satisfied with the nuclei segmentation, you can change the num_iter. 
As examples: 
i)	You have nuclei that are not included in the segmentation, decrease the iterations (num_iter), as this changes the number of repetition steps for the algorithm to get a better segmentation.
ii)	You have parts included in the nuclei segmentation which are not true nuclei, improve the analysis by increasing the num_iter value. Note that for num_iter values you can only use integers.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/25a061a5-23f9-44c9-a8fa-96b1eecf17f9)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/071cf588-1c73-48b5-857f-9502177a9be4)
17. For the segmentation of under-segmented nuclei and following calculations, you can change the area threshold values if needed (section #4 Lumen analysis and results). After you run the previous section (section #3), you will get a histogram for the area of the segmented nuclei. Area_threshold value in section #4 defines the threshold for the correct nuclei area. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/4104d053-e803-433d-bfec-01e79408a92f)
Note! Depending on your data, you can check the histogram and decide the correct area threshold for individual nucleus. For example, cell size might be different between your cell lines. 

18. For the sprout width measurement (section #4), you can change the part of the sprout from which the width is measured. By default, SproutAngio tool measures the width of 25%, 50%, 75% parts of the segmented sprouts. However, you can change this if you want to get measurements from different parts of the sprouts depending on your experiment.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/da8da165-d5e9-4a18-9d0f-cd2e65f2f358)
19. For the volume measurement, similar to the nuclei segmentation part, you can change the num_iter value to get better segmentation. 
As examples:
i)	If you have areas missing in the segmentation, you can decrease the num_iter integer value. 
ii)	If you have regions which are not sprouts but still segmented as sprout volume, then you can increase the num_iter to improve the segmentation.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/1284c208-1601-4f8a-9d44-e91337e4ab0c)
Note! In this user’s guide, we cover the most useful parameters that you can modify. However, you can also play with different parts of the sections to familiarize yourself with the code. There are more explanations related to the sections on the code itself.

20. The last part of SproutAngio_main is for writing the data into excel file. After you run this part (section #6), there will be an excel file created in the SproutAngio folder you created in the beginning on your desktop. Also, an image of the paired nuclei distance analysis used for studying lumens is automatically saved in the same folder as “analyzed_image.png”. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/964cc4c0-1816-4195-8910-dd2466380882)
21. Now, to turn off the analysis platform and the SproutAngio Jupyter tab, you need to close both the Jupyter notebook tab and the kernel (marked in the figure below in yellow). First, select on the left the “running terminals and kernels” and “shut down all”.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/57cf3405-0957-46a2-bc33-a9aae179341e)
22. Close the SproutAngio_main tab.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/20d68cad-1a61-4e46-adc0-3a88920713e3)
23. When you work on your dataset, first optimize your analysis using SproutAngio_main tool as demonstrated in this guide. After you finish optimizing your parameters, if you want to run multiple files at once, then launch the “SproutAngio_multiple_run.ipynb” by double click opening it instead of “SproutAngio_main.ipynb”. Change the parameters you optimized previously, here. Note that there is only one section here and after you run it, it will take a while for the run to be completed depending on the number of images you analyze.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/680456c2-ee39-4d1f-ad41-02029ace3f01)

C. RETINA ANALYSIS:     
1. To start using the SproutAngio_retina, double click the SproutAngio_retina file on the left (yellow rectangular in the figure below). Then, run the first section which imports the necessary libraries such as Skan Skeleton Analysi library and define necessary functions to exclude the central part during image processing.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/cef0c293-45e2-478f-8a5f-d6ffa9f9d29e)
2. Next, run the second section. This section first reads all the files in defined “retina_sample” folder. If you create another folder in this file, simply change the file_path to open the new folder. 
In our retina_sample folder there is only 1 retina image file. However, if you have multiple files, you can change to the next image file by simply changing the “folder_names[0]” into “folder_names[1]”. Read the instructions above the code for more information.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/34190476-41de-47d9-b482-87d875dbe299)
3. After running the previous section, Napari viewer tab should open in your computer. Open the Napari viewer.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/ba50a38e-96da-4f28-837a-c93796a2294f)
Now click the “new shapes layer” as shown below image to create a new shape layer to draw the region of interest.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/7f97fd96-79e5-4e22-bb0a-d5f0d52c16e9)
4. When “Shapes layer” is selected, change the color into something you can easily see/ differentiate during drawing on this black and white image. After that choose “add polygon” to start drawing the region of interest.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/4bae7d9d-b4ec-42c7-8f54-b57229e9be91)
5. Now draw around the retina area by clicking one by one, on your last click you either use double clicking or “space” key on your keyboard to stop drawing. If you make a mistake you have multiple options shown in below figures.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/76ad3532-0c6a-4978-9dd9-1e360a3f7a4e)
If you make a mistake, you can click to the selection tool and move each individual dot you have put so far.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/533a3478-b68a-4ebb-bb71-ae982a400c56)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/6342adb4-d36f-4928-aa9a-1c06cf37b9dc)
Or you can delete the whole shape and draw a new one:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/cf22d2b0-15e7-4e06-941c-44c4aaf2c5fa)
6. After you finish drawing your region of interest, in our case it is the whole retina, you can return to Jupyter notebook and run the next section. This section’s purpose here is to get the drawn points into an array to use in the pipeline.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/6bea84f1-83c3-417e-9579-38c0da32e7a3)
7. After the last section’s run finishes, run the next section. This part is all about the exclusion of user defined central part. You can easily change the radius you want to remove. Here, we will use 0.3 R, 0.5 R and 0.7 R radius exclusion.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/463b57ae-f81f-4537-b6a3-3e03ac3cbaa0)
After the run ends (when you see Idle instead of Busy on the left bottom part of the notebook), you can open Napari viewer to check the images. Remember to switch between the images by clicking the eye symbol as shown below.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/f5f87ba3-e7ac-4784-b9b6-f0d09ecb9bdd)
8. Next section is branch length analysis. Run this section. You will get total skeleton length (pixels), total branch number and long branch number results printed. Also, you will see three histograms of branch lengths for 0.3R, 0.5R, 0.7R radius selections. At the end of the run, you can also check the napari viewer to see the skeletonization of the branches. We will explain these steps in detail below. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/ac9c6cf2-df92-4996-bfbf-31d59767e2ed)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/14a20049-e6ed-48fe-9711-fb4c2f8f057a)
9. On histograms, x-axis shows the branch length (pixels) and y-axis shows the number of branches. Long branch number results give here the branch number which are longer than 40 pixels. However you can easily change this in the code. For example looking at the histogram, if you think you want to use 50 pixel length as threshold here, to get the number of branches longer than 50 px:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/eac66d28-32e6-4737-990f-30b4da467db6)
Simply change these “40” values into “50”:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/8df76b19-22e8-42c1-8e82-2ad649837e2c)
10. You can look at the Napari viewer to check the skeletonizations. You can open the same branch and skeleton to look at them together. Here we will choose 0.3 R branch and its skeleton together:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/a81b0539-fe71-46d1-9778-489a38af60ef)
First, only select these two from the eye symbol:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/a27214c2-0717-4ce3-afbf-4d2008c6f113)
Then select the skeleton channel by simply clicking on it, and change the color of skeleton something visible and reduce the opacity. We used 0,60 for opacity here. Then zoom in using your mouse scroll to see in detail.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/6b687751-b76d-4e92-8818-35987d8fdd02)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/56e4a7b8-aee6-418b-bfa3-6f15bd544f57)
11. Now run the last part of the code. Output of this section gives you vessel density % area measurements and radial expansion result. 
![image](https://github.com/mbbio/SproutAngio/assets/65368053/ec8591ff-a267-4a9c-b130-d7338934a1f4)
12. Remember to turn off JupyterLab!
![image](https://github.com/mbbio/SproutAngio/assets/65368053/e33d3aa1-6e24-4e00-a27b-4ff265d80a4a)

D. RESULT GRAPHS AND STATISTICAL ANALYSIS:     
1. The purpose of this part is to help you do statistical analysis and draw graphs in the same platform easily. Open “Result_graphs” file by double clicking on it.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/1fdf6741-7eab-4b5f-b4cf-e0f0b8d8b536)
2. If you followed the guide so far, you already created multi_analysis_results excel document during part B Using the tool, step 23. We will not work on it as an example. 
Run the first section to define the file path, which is the excel document we created previously here:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/a3cc3a43-8a4d-4c40-9a78-caf4aa6cf536)
3. Run the next section. It will print the results in the excel file for you to check.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/d58881f9-d76b-43f1-9f09-3881a525b0e7)
4. Run the next section. The purpose of this part is to check your data to see if it is normally distributed or not.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/2c77e298-2ed9-4973-858e-641b4601656b)
5. Run the next section. It draws a correlation heatmap. You can delete or add the parameters you want to include by changing inside the part shown in yellow rectangular below:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/f9d9965c-a33b-4f9e-a0dc-057dfcc60a95)
6. Run the next section. This section draws individual correlation graphs between two parameter results you choose. Here it shows a graph correlation of nuclei number and total skeleton length. Also, this part, removes the “0” data points, not including them in the correlation calculation.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/0720b99d-ac64-4615-997e-13272ca73216)
7. Next section draws bar graphs. One way of using this part is grouping your data in your excel file. For example, below we show a sample excel document and we added a column to group our data into untreated, 1ng and 10ng. So, we have three groups.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/ae2f1e2a-fe3e-4bcc-9daa-3a12e69e7f77)
If we had used this excel for defining the path in step 2, then, running the section would give a bar graph with statistics:
![image](https://github.com/mbbio/SproutAngio/assets/65368053/7c7aec93-3f96-4d75-9f95-c84f6d1b4e5b)
![image](https://github.com/mbbio/SproutAngio/assets/65368053/e67a441e-2af5-49a1-b793-e580a995fb2c)
8. The last section is an example of Kruskal Wallis test. Here we tested sprout length in our grouped excel data shown above in step 7.
![image](https://github.com/mbbio/SproutAngio/assets/65368053/4a7594dc-239d-4c74-a214-9a1f5c78bfb1)
You can use other statistical tests: https://docs.scipy.org/doc/scipy/reference/stats.html

