# README.md : tutorial for Rubin-LSST commissioning and early science

- author : Sylvie Dagoret-Campagne
- creation date : 2025-05-02
- last update : 2025-05-05

Note if you want to run and save these notebook, install the pre-commit hook to clean the notebooks before commit as follow (see https://pre-commit.com/).

     pip install pre-commit
     pre-commit install
            


## 01) Consolidated database : Easy access to telescope parameters through the database called ConstDB
Note it is not through the butler.
- **01_ConstDB.ipynb** : Find main visit parameters for LSSTCam, LSSTComCam and LATISS

## 02) Finding the information 
Another method to access to the information using the butler.
- **02_FindObservationsInButlerRegistry.ipynb** : visit parameters from butler registry     
- **03_QueryCollectionsAndDatasetsInButler.ipynb** : Dump from butler which collections and datasettypes to use. 

## 04) Plotting DeepCoadds for LSSTComCam
- **04_LSSTComCamDeepCoadds.ipynb**	: show a DeepCoadds of a single tract and patch in the 6 bands	     
- **04_LSSTComCamDeepCoaddsMosaicMatplotlib.ipynb** : show a centra DeepCoadds patch surrouned by its 8 neighboring patches in a given band. Use matplotlib as the plotting backend. (Must clean memory by shutting all notebooks and kernels before running this notebook).
- **04_LSSTComCamDeepCoaddsMosaicFirefly.ipynb** : show a centra DeepCoadds patch surrouned by its 8 neighboring patches in a given band. Use Firefly as the plotting backend. (Must clean memory by shutting all notebooks and kernels before running this notebook).

## 05) Work on Objects extracted from ObjectTable
- **05a_SearchForObjects.ipynb** : Make a list of Objects extracted by the DRP pipeline from Coadds, including magnitude plots.
- **05b_SearchForObjetcsCutouts.ipynb** : Show cutout images from the Objects found in ObjectTable.
- **05c_SearchForObjectsInDeepCoadds.ipynb** : Show where the object has been found in the Coadds images in the 6 bands.


## 06) Searching sources in the SourcesTable 
Extract all the sources detected in single-visit processed images in order to associate them later to an Object detected in a Coadds image.
The goal is to be able to make Light Curves from DRP sources.
- **06a_SearchForSourcesAndObjectsVisits_WriteSources.ipynb**: Extract source visit by visit.
- **06b_SearchForSourcesAndObjectsVisits_ReadSources.ipynb**: For each object in Object table find the sources associated and make the Light Curve. 



## 09) DIA Objects
Work using DIA analysis.
- **09_SearchForDIAObjectsLightCurves.ipynb** : Light curve from DIA source.



                            
