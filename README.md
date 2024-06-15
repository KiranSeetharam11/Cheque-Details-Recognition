
# Cheque Details Recogintion

Cheques are yet used in large amount transactions around the world, since each cheque is handwritten we need to go through each of them to update the transactions database which keeps record of all cheque transactions.

# Project Overview

This project develops a CNN Model that recognizes the numbers in the format image given, and update the account number and amount as a transaction in the dataset.

It uses 2 datasets - one has all transactions details and another has user details







## Data Background
The dataset to train the model is MNIST Dataset
[MNSIT DATASET](http://yann.lecun.com/exdb/mnist/)

It has 60,000 train images with labels and 10,000 test images.

For the transactions dataset, we used Chat-GPT to generate random list of 10 Account numbers and names, with this we had a total of 50 transactions according to the columns that need to be filled.



## Run Locally

To run this project locally, ensure you have the following libraries installed:

```bash
  pip install pandas
  pip install numpy
  pip install scikit-learn
  pip install keras
  pip install matplotlib
  pip install cv2
  pip install pillow
  
```
    
## Structure of the project


### Data Cleaning
- Check and handle Null values, the dataset had none

### Feature Engineering
- Get the data in the required shape
- Use one-hot Encoding by using to_categorical()

### Model Training
- A sequentional Nueral Network was added with multiple layers.
- The model was fit with epochs set to 10

### Performance
-  The accuracy obtained was 0.9843 

### Cheque Image Usage
- The input image has all 3 inputs - From A/c, To A/c, Amount
- They are cropped and sent to the model as 3 seperate units and stored later
- Contours are sorted based on centroid to obtain the numbers in the correct order

### Updating Transaction file
- Functions are defined to calculate all the required columns
- Necessary warnings are produced when there is unknown A/c Number
- Warning is generated in case of possibility of cheque bounce due to insufficient balance
- If none of the warnings are triggered, the new record is updated in the main file



## Acknowledgements

 - [Multiple Number Recognition Model](https://yash-kukreja-98.medium.com/recognizing-handwritten-digits-in-real-life-images-using-cnn-3b48a9ae5e3)
 - [Re-organize Conoturs](https://www.youtube.com/watch?v=7FPD_UmFqqU&t=625s)



## ER Diagram

![ER Diagram](https://github.com/KiranSeetharam11/Cheque-Details-Recognition/blob/main/Cheque%20ER.png)

