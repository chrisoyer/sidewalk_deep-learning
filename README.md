# sidewalks_deep-learning
Image processing with tensorflow
Starting point is sidewalks #TODO update & rename notebook. Imports geojson data and uses it to generate coordinates including latitude, longitude, heading, and label (sidewalk vs no sidewalk). Label based on whether there is a sidewalk polygon object within specified distance of starting coordinate. Using this data, the class downloads streetview images from the Google StreetView static api. 

This data set is used in the second notebook to train a tensorflow neural network to identify if there is a sidewalk in a streetview image.
