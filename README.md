# fertilizer_recommendation
Help farmers better care for their plants nutritional needs

#### CROPS FOCUSSED:
* Rice
* Wheat
* Maize

#### NUTRIENTS FOCUSSED:
* Potassium
* Magnesium
* Zinc
* Iron
* Manganese
* Copper
* Boron
* Sulphur
* Nitrogen deficiency levels - only for rice

### FLOW:
* User can upload an image of the leaf (that begins to show some symptoms like loss of color(chlorosis), drying(necrosis)
* The model runs on the image and classifies it into 1 of 5 symptoms (includes a healthy/normal class).
* Uses user input on age of leaf (new/old/middle) and presence of 4 additional symptoms (not capture in leaf image), like stunted growth of entire plant.
* Using this infomation and the research on identifying nutrient deficiencies (done by Montana State University, U.S. Department of Agriculture), the following rules are developed.
* These results are further used to recommend appropriate fertilizers to the farmer, helping in **avoiding overfertilization** by adding standard fertilizers recommended to crop grown and **control costs**

### FILES:
* fertilizer.xls - Excel file containing the data on fertilizers. It has 2 pages which needs to be updated with the info collected
* first_app.py - The web application that is viewed by users
* 200_epoch_97_87_soft.h5 - Neural network model for classifying leaf image into 1 of 5 classes ['interveinal', 'margin', 'normal', 'spotty', 'tip']
* plain2model.tflite - Neural network model for classifying rice leaf image into 1 of 4 classes based on LCC
* nn_model_basic.ipynb - Jupyter notebook containing code used to train the Neural Network model
* SessionState.py - Library to allow use of session in application
