# sidewalks_deep-learning
Image processing with TensorFlow 2.0. 
The starting point is the [Data Acquisition notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/segmentation_load_from_weights.ipynb) In this notebook I import geojson data and use it, in conjunction with calls to the Google Streetview metadata API to generate coordinates including latitude, longitude, heading, and label (sidewalk vs no sidewalk). The label based on whether or not there is a sidewalk polygon object within specified distance of starting coordinate. Using this data, I downloaded streetview images from the Google StreetView static API. 

This data set is used in the [Image Classification notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/Image_classification.ipynb) to train tensorflow neural networks to identify if there is a sidewalk in a streetview image. This includes new and pretrained models.

A second dataset, from [Cityscapes](https://www.cityscapes-dataset.com/) was used for training for image segmentation in [this notebook](https://github.com/chrisoyer/sidewalks_deep-learning/blob/master/Unet_Model_for_Semantic_Segmentation.ipynb).
