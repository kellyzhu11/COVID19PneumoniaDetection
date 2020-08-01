
# COVID-19 Pneumonia Detection in Chest X-Ray Images Using Deep Learning

The purpose of this project is to leverage deep learning techniques to automatically detect COVID-19 pneumonia in chest X-ray images.

First, two classifiers are built based on ResNet-152: 
1. A binary classifier that aims to separate COVID-19 pneumonia and non-COVID-19 cases
2. A four-class classifier that aims to distinguish COVID-19 pneumonia, viral pneumonia, bacterial pneumonia and normal cases

Second, Grad-CAM method is applied to evaluate the four-class classifier.

## Results
### Model Performance
#### Binary Classifier 
The binary classifier is able to separate COVID-19 pneumonia and non-COVID-19 cases with 100% testing accuracy.

Confusion matrix of the binary classifier:
<p align="center">
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/confusion_matrix_2class.png" height=250/>
</p>

#### Four-class Classifier 
The four-class classifier is able to distinguish COVID-19 pneumonia, viral pneumonia, bacterial pneumonia and normal cases with an average accuracy, precision, sensitivity, specificity, and F1-score of 93%, 93%, 93%, 97%, and 93%, respectively.

Confusion matrix and ROC curve of the four-class classifier:
<p align="center">
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/confusion_matrix_2class.png" height=250/>
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/roc_4class.png" height=230 />
</p>

### Grad-CAM
The localization maps generated by Grad-CAM show that the four-class classifier is able to focus on the patchy areas in chest X-ray images and has high consistency with radiologists’ diagnoses. Please note that the left and right side are reversed in chest X-ray images.

Case 5: Radiologist’s comment: Mutifocal consolidation in right mid zone and left mid/lower zones.
<p align="center">
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/case05.png" width=500 />
</p>

Case 9: Radiologist’s comment: Patchy areas of air space opacification bilaterally with a lower zone predominance.
<p align="center">
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/case09.png" width=500/>
</p>

Case 17: Radiologist’s comment: There is peripheral patchy air space opacification seen in both lung lower zones with diffuse ground-glass haze bilaterally.
<p align="center">
  <img src="https://raw.githubusercontent.com/kellyzhu11/COVID19-Pneumonia-Detection/master/pics/case17.png" width=500/>
</p>


## Usage
### Clone the repositories
 
 `git clone https://github.com/kellyzhu11/COVID19-Pneumonia-Detection.git`
 
### Generate dataset
run data.ipynb
### Train model
run train.ipynb
### Evaluate model
run evaluate.ipynb
