# Untuned ProsusAI FinBERT
### 1. Introduction:
#### FinBERT by Dogu Araci (ProsusAI Team): <br> The ProsusAI version of the FinBERT model is first further pre-trained on the TRC2 dataset with 1.8M news articles published by Reuters from 2008 to 2010. <br> Then, the model is fine-tuned on the Financial PhraseBank dataset from Malo et al. (2014). <br> *** Here, we just use the version created by ProsusAI team and don't do any further adjustment on the FinBERT.

### 2. Performance:
#### Compared to other models in this work, the Untuned ProsusAI’s FinBERT has the following performance: <br><br> (1) Accuracy: ProsusAI’s FinBERT model without fine-tuning has an accuracy of 89%, which is the 2nd best score we achieved in this work. <br><br> (2) F1-Score: The model has a weighted average F1-Score of 89% (also the 2nd best) and performs well on the recall rate in recognising Negative and Positive news with a sacrifice on the precision rate. By contrast, its performance in Neutral news is the opposite.

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.78      | 0.97   | 0.87     |
| Neutral       | 0.97      | 0.85   | 0.91     |
| Positive      | 0.82      | 0.93   | 0.87     |
| Weighted Avg. | 0.9       | 0.89   | 0.89     |

![image](https://user-images.githubusercontent.com/92542287/220276267-f47048c8-b51b-427d-b78d-81121a5ef221.png)

#### (3) Prob. Distribution: Its predicting probability is continuously distributed though its predictions on Neutral and Positive news are less assured than the 2 BERTs, but it has a better result. <br><br> (4) ROC Curve: The AUCs for all 3 classes are greater than 96%, and the model’s AUC is exceptionally high in Negative News. <br><br> (5) Precision-Recall Curve: All APs are higher than 95%, and it has a slightly better conversion rate between precision and recall in Negative news.

![image](https://user-images.githubusercontent.com/92542287/220276640-ad4914f4-4a09-4f18-91b8-3139e602eb01.png)
