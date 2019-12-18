## Classification and Image Segmentation with Deep Learning in Tensorflow 2.x

### Data Acquisition and GIS
The starting point is the [Data Acquisition notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/segmentation_load_from_weights.ipynb) In this notebook I import geojson data and use it, in conjunction with calls to the Google Streetview metadata API to generate coordinates including latitude, longitude, heading, and label (sidewalk vs no sidewalk). The label based on whether or not there is a sidewalk polygon object within specified distance of starting coordinate. Using this data, I downloaded streetview images from the Google StreetView static API. 

Images were obtained within the survey area for pontential sidewalks: 
![Dataset Extent](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/_resources/denver%20area.png "Sidewalk Data Region")

Final images were distributed as: 

![file](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/_resources/Sidewalk_images.png "Distribution of Images including Sidewalks") 

![file](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/_resources/Non-sidewalk_images.png "Distribution of Images without Sidewalks")

### Image Classification with TF
This data set is used in the [Image Classification notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/Image_classification.ipynb) to train tensorflow neural networks to identify if there is a sidewalk in a streetview image. This includes new and pretrained models.
The best model was built using the Xception pretrained model.  

![Xception results](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/_resources/xception_hist.png "Exception History")


### Image Segmentation
A second dataset, from [Cityscapes](https://www.cityscapes-dataset.com/) was used for training for image segmentation in [this notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/Unet_Model_for_Semantic_Segmentation.ipynb). I built a model with a UNet architecture to segment the sidewalks.
Example result: 
![example](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/_resources/mask2.png "Example")

Neither image dataset used are directly availible, but the first can be recreated using the code in the first notebook, and the second is publically availible upon approval at Cityscapes' website.

Final models with saved weights can be found [here](https://drive.google.com/open?id=1bNYCF0eH_ikBQkQlWz6BdXKez5IAgRqD).

Major technologies used: Python data ecosystem, Tensorflow 2, Google Streetview & Colabs, GIS (Geopandas, Shapely, Pyproj).
