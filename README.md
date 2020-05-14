# openseadragon_project
Modification of OpenSeadragon viewer with several overlays and annotation control 

openseadragon.min.js from https://github.com/openseadragon/openseadragon  
openseadragon-fabricjs-overlay.js from https://github.com/altert/OpenseadragonFabricjsOverlay  
osd_fabric_annotation based on https://github.com/WilliamCarlos/OpenSeadragonAnnotationPlugin

__HOW TO RUN__

1.	Prerequisites: IIPIMAGE server https://iipimage.sourceforge.io/documentation/server/ 
    - server will provide DZI files from existing TIF files via DEEPZOOM protocol      (https://iipimage.sourceforge.io/documentation/protocol/)

2.	Download openseadragon_project (https://github.com/cesekova/openseadragon_project)

3.	Unzip and save demo_images folder on IIPIMAGE server

4.	Run openseadragon_project/index.html

  - make sure that your path to iipsrv.fcgi is the same as in line 266, or adjust it accordingly (e.g,  "/fcgi-bin/iipsrv.fcgi")

5.	To load images, fill out url parameters:  
  .../openseadragon_project/index.html?image=""&annotation =demo_images/ TP-2019_2824-01-1-annot.tif&probabilities= demo_images/TP- 2019_2824-01-1-vis.tif&decision=demo_images/ TP-2019_2824-01-1-sal.tif&log_thresh=0.001 

  - image attribute stays empty as the original source image contains real patient tissue and cannot be published
  -in case decision layer has multiple images, decision argument can be repeated  (...&decision=path/to/decision1.tif&decision=path/to/decision2.tif&decision=path/to/decision3.tif...)
  - log_thresh attribute is used to enhanced color intesity distribution by log scaling

