# Pneumonia Image Classification

## Motivation
Pneumonia is most common cause of hospital admissions other than women giving birth. The goal of this project is to aid medical professionals with pneumonia diagnosis’ by using neural networks to classify pneumonia from a patient’s chest X-ray images. The hope is that our algorithm can help reduce error caused by misinterpretation of chest X-rays, streamline the diagnosis process and can help lighten the workoad of physicians.

## Data
Data was sourced from Kaggle and collected from Guangzhou Women and Children’s Medical Center. It contains a total of 5,856 images that are classified as either “Normal” [0] or “Pneumonia” [1]. The X-ray images are of pediatric patients, ranging from ages 1-5 years, and were scored by three different medical professionals. Images that were of low-quality or unreadable were removed from the dataset. 

## Methodology
Since the images were pre-screened prior to being uploaded, there was not a lot of data cleaning that needed to be preformed. All images and labels were reshaped and normalized to allow for training of the neural networks. A baseline model utilizing dense neural networks was created but abandoned in favor of convolutional neural networks. Two different CNN arcitectures were created, one consisting of three convolutional layers and the other utilizing a pre-trained network - InceptionV3. The pre-trained network outpreformed the other network architecture so we proceeded with this model for hyperpatameter tuning with the hopes of further increasing accuracy. 

## Results 
![Screen Shot 2021-09-19 at 11 06 41 PM](https://user-images.githubusercontent.com/81720110/133962303-e1ee65aa-f5fa-4846-b88b-19570f678ab6.png)

![Screen Shot 2021-09-19 at 11 06 57 PM](https://user-images.githubusercontent.com/81720110/133962308-fa5d572d-de4b-43be-ae68-404185cac3f9.png)

The images above show the most current model's preformance. The training accuracy score is at 75.9% with a loss of 0.366 while the testing accuracy is at 76.1% and a loss of 1.05. 

## Conclusion
This model is able to diagnose pneumonia, solely off a patient's chest X-ray image, with 76% accuracy. 

## Next Steps 
Future work can be done to further improve the models accuracy by increasing the number of epochs to allow for more learning to take place. Also adjusting other parameters to find the optimal learning rate would help increase accuracy and reduce overfitting. 
