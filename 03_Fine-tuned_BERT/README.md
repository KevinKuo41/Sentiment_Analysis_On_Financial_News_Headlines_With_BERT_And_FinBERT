# Fine-tuned BERT
### 1. Fine-tuning Process in This Work:
#### In this work, we aim to train the BERT model to conduct sentiment analysis on Financial News Headline dataset, so we used 80% of the dataset (3,924 samples) to fine-tune the BERT model and 10% of the dataset (485 samples) as the validation dataset. <br><br> In terms of the parameters we applied in the process, we used 2e-5 as the learning rate, as suggested by the ProsusAI team, and trained the BERT with 5 epochs and 32 as the batch size.  <br><br> With F1-Score as the metric, we compare the performances of models finishing different numbers of training epochs and only keep the best among them. Here, the model finishing 1 epoch performs the best, so we keep it and test its performance on the validation + test sets (total 922 samples).

### 2. Performance:
#### Considering the BERT model was only fine-tuned on 3,924 samples, the BERT’s power in the classification task is fabulous. <br><br> (1) Accuracy: The BERT model finishing 1 fine-tuning epoch performs the best among all only-fine-tuned BERT models with an accuracy of 87% on the validation and test dataset. <br><br> (2) F1-Score: The only-fine-tuned BERT model has a weighted average F1-Score of 87%. It does the best in recognising Neutral news but performs relatively worse in identifying Positive and Negative news.


| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.85      | 0.85   | 0.85     |
| Neutral       | 0.90      | 0.90   | 0.90     |
| Positive      | 0.82      | 0.82   | 0.82     |
| Weighted Avg. | 0.87      | 0.87   | 0.87     |

![image](https://user-images.githubusercontent.com/92542287/220272940-be47e1f3-1f46-4561-bb99-2da716dc2c99.png)

#### (3) Prob. Distribution: The predicting probability for all 3 classes is basically only concentrated in 0% and 100%. The model becomes a bit too confident in its classification. <br><br> (4) ROC Curve: All AUCs are greater than 94%, and the model’s AUC is higher in Negative News. <br><br> (5) Precision-Recall Curve: The APs for all 3 classes are higher than 89%, and the AP is higher in Neutral News. The conversion rate between precision and recall in Negative news is a bit worse.

![image](https://user-images.githubusercontent.com/92542287/220272972-79c80088-c7dc-4967-aa8d-a13b7fde3893.png)
