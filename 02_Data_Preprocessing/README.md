# Data Preprocessing
## 1. Replacing the labels
#### (1) For BERT and HKUST FinBERT, we replace the labels as follows: {'Neutral':0, 'Positive':1, 'Negative':2}. <br><br> (2) For ProsusAI FinBERT, we replace the labels as follows: {'Neutral':2, 'Positive':0, 'Negative':1}.

## 2. Sorting smaples into training, validation and test dataset
#### (1) Training Dataset: 3924 samples <br><br> (2) Validation Dataset: 437 samples <br><br> (3) Test Dataset: 485 samples (4) Final Test Dataset = Validation set + Test set: 922 samples

## 3. Exploratory Data Analytics
#### (1) Frequency & Length: Facts: <br> 1. Number of Sequences With Greater Than 512 Tokens: 0 <br> 2. Maximum Sequence Length: 150 Tokens <br> 3. Average Sequence Length: 30.6 Tokens

![image](https://user-images.githubusercontent.com/92542287/220123650-7a13eaeb-d465-4da6-b4ed-874074db06ad.png)

#### (2) Percentage & Distribution

![image](https://user-images.githubusercontent.com/92542287/220123749-81bff115-0ba7-4317-8cac-cc74676d9c96.png)
![image](https://user-images.githubusercontent.com/92542287/220123767-9a585974-704f-43c3-93ae-e87861f08859.png)
