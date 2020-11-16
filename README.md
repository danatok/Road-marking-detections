# Road marking condition monitoring and classification using deep learning for City of Helsinki
This project is the part of a master thesis for Data Science Degree at Aalto University.
## Table of Contents
* [Project Motivation and Description](#motivation)
* [Installation](#Installation)
* [File Description](#description)
* [Results](#Results)
* [Limitations](#Limitations)
* [Licensing, Authors, Acknowledgements](#licensing)
## Project Motivation and Description <a name="motivation"></a>
The thesis explores application of deep learning on detection and classification of road markings in the city of Helsinki. The need for maintaining the infrastructure is the essential part for smart cities. City of Helsinki is thriving towards the digitization of the city, providing geo spatial information on one of their open geoinformatics service, [Helsingin karttapalvelu](https://kartta.hel.fi). That was utilized as the main data source. Based on the satellite images obtained from kartta.hel, the road markings were extracted.


## Installation
The code requires Python versions of 2.x or 3.x and general libraries available through the Anaconda package. In addition, [geopandas](http://geopython.github.io/OWSLib/installation) for working with OWS.
## File Description <a name="description"></a>
This project includes notebook for data extraction made by Alex Jung et al.
The .ipynb file titled 'dataset_creation.ipynb' contains the code that creates the csv file 'bike_sharing_dataset.csv' that is used by the file 'bike_sharing_demand.ipynb' to implement the ML algorithms. The three different .sav files include the best saved ML models.
## Results
Further, previous work on zebra crossings was studied, both using traditional ways and deep learning (DL) based ones. Deep Learning were favoured over traditional due to ability to capture deeper abstract concepts and hierarchical features. Several recent DL based object detection algorithms, their training process, hyperparameter tuning, results are described in depth. In addition history of computer vision, especially object detectors, their benchmarks, disadvantages, and advantages are studied extensively. Taking into account the specifics of the dataset such as low resolution, small size and noise, data augmentation and transfer learning were applied. After the comparison between various object detection algorithms and also taking into account requirements for the performance as accuracy, robustness to noise, shadows, state of the art algorithms were chosen, such as Retina Net and YOLO5. YOLO5 outperformed in all desired metrics. It achieved mAP_0.5 of 0.68, inference time of 0.017 seconds with relatively low (compared to RetineNet) time for training. However Retina Net took twice less time for training.

## Licensing, Authors, Acknowledgements <a name="licensing"></a>
The data used for the analysis comes from:
* [Helsingin karttapalvelu](https://kartta.hel.fi/) `Data Preparation.ipynb`
The loading of the data was done using the below code:
* [Alex Jung ResearchPublic](https://github.com/alexjungaalto/ResearchPublic/blob/master/RoadMarkingHelsinki/RoadMarkingMonitoring.ipynb): this includes the code for getting the data from geoinformation server kartta.hel.fi. Implemented by Alex Jung, Jyoti Prasad Bartaula, Sangam Deuja.
Data was trained using Retine Net and YOLO5
* [Retina-Net](https://github.com/fizyr/keras-retinanet): this includes the implementation of the Retina-Net by Fizyr.
* [YOLO5](https://colab.research.google.com/drive/1gDZ2xcTOgR39tGGs-EZ6i3RTs16wmzZQ) 
* [Roboflow](https://roboflow.com) as data augmentation tool. Moroever with Roboflow the data was converted to the appropriate for YOLO5 format.

