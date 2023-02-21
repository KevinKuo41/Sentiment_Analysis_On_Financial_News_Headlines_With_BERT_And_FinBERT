# Fine-tuned ProsusAI FinBERT

### 1. Fine-tuning Process In This Work:
#### Here, we e used 3,924 samples to fine-tune ProsusAI’s FinBERT again. <br> * Params: learning rate = 2e-5, batch size = 32, with 5 epochs -> The model finishing 3 epochs produced the utmost F1-Score

### 2. Performance:
#### Compared to its untuned version, the fine-tuned model has the following performance: <br><br> (1) Accuracy: ProsusAI’s FinBERT model, after fine-tuning, has an incredibly high accuracy of 98%, the best score achieved in this work. <br><br> (2) F1-Score: The model’s weighted average F1-Score also increases to 98%, the highest score. Compared to the untuned version, the precision rate on Negative and Positive news and the recall rate on Neutral news all rise substantially. Only 22 out of 922 samples are misclassified.

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.95      | 1.00   | 0.97     |
| Neutral       | 0.99      | 0.97   | 0.98     |
| Positive      | 0.97      | 0.97   | 0.97     |
| Weighted Avg. | 0.98      | 0.98   | 0.98     |

![image](https://user-images.githubusercontent.com/92542287/220281033-667cca83-f9a7-4762-8e73-0a5e06a8123f.png)

#### (3) Prob. Distribution: The probability became much more concentrated in 0% and 100%, meaning the model is very sure of its predictions and, indeed, causes almost perfect results. <br><br> (4) ROC Curve: The AUCs for all classes are higher than 99%, with exceptionally high scores in all 3 kinds of News. <br><br> (5) Precision-Recall Curve: All APs are higher than 98%, with an exceptionally great conversion rate between precision and recall in Negative news.

![image](https://user-images.githubusercontent.com/92542287/220281082-c137c8b1-6b7a-489a-ad41-a43d6747b6e1.png)
