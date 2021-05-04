## myXception
The habitats of native species of plants are threatened in many areas of the world. Presently, scientists who have been trained in this field visit these locations to better understand the challenges. The use of such professionals is expensive and time-consuming.
The project uses deep learning to identify images of invasive and non-invasive species in Virginia. Our data set consists of 405 images of five types of plants: Duckweed, Watercress, Arrowhead, Grassy Mud Plantain , and Hydrilla . Using deep learning, we achieved an accuracy 96% from Xception on a held-out test set.
## Motivation
According to some, Hydrilla poses an ecological threat. It has the ability to grow in various conditions and this gives it an advantage over native plants. Infestations of hydrilla can be harmful to fish populations as well. They can cause oxygen depletion zones which can be harmful to fish.

## Experiments
Model Deployment: We deployed the model to the Google Cloud Platform. The procedure includes uploading the model to Google Storage, hosting the model on AI Platform, and creating a service account to access it. Since we want to enhance end-to-end user collaboration, we built an app in Streamlite linked to our Google AI Platform so the users can upload the images and generate and verify model predictions based on the images.

## Results 
Xception Model
Xception merges the ideas of GoogLeNet and ResNet, claiming the usage of fewer parameters, less memory, and fewer computations than a regular convolution layer, yet with better performance. Xception has a total 14 blocks with multiple layers in each block. We experimented with two configurations to solve our image classification question. The first approach adopted an Adam optimizer with a learning rate of 0.01. BatchNormalization was adopted and served as an inference mode. The model accuracy from the training data was 99% compared to 85% for the testing dataset. The second configuration included a stochastic gradient descent (SGD) optimizer, a momentum of 0.9, a learning rate of 0.01, and a decay rate of 0.001. BatchNormalization was also adopted and served as inference mode. The model accuracy from the training data was 99%, while the testing dataset accuracy was 95.56%. The model accuracy improved with the SGD optimizer when compared to Adam. 
We built an app in Streamlite linked to our Google AI platform, so that users are able to upload  images and generate and verify model predictions based on the image. The prediction had an accuracy for the identification of  Hydrilla with a  confidence level of 94%, while the other plant species  in the study were identified with 100% confidence. The model is therefore able to identify the relevant plant species in the image correctly, which is consistent with the obtained model accuracy of 95.56%. 

## Conclusions
Our models are able to distinguish 5 classes of plants, including Hydrilla. Our purpose is to accurately classify plants in Virginia, specifically Hydrilla, which is an invasive plant. This means our models are beneficial to Virginia’s natural environment and its residents, leveraging machine learning to accurately and rapidly identify invasive plants. We could also collaborate with the public and as well as non-governmental and government organizations, such as the Virginia Department of Conservation and Recreation, to control the spread of invasive plant species in Virginia. 
Given more time, because our dataset currently includes five classes, in the future, we could also be able to add a non-plant class (such as animals) so when users upload non-plant images, our model will be able to label them as such. This model could theoretically be adapted with more classes and datasets to identify a variety of plant and animal species, including invasive ones.


## Streamlit -app for model prediction
<br>
<img height = "700" src="https://github.com/gladieschanggoodluck/myXception/blob/main/image/VAplantPrediction.JPG"/>
<br>
