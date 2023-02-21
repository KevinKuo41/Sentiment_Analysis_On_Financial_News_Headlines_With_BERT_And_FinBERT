# Untuned HKUST FinBERT
### 1. Introduction:
#### FinBERT by Yi Yang et al. (HKUST Team): <br> The HKUST version of the FinBERT model is first further pre-trained on the dataset comprised of (1) Corporate Reports 10-K & 10-Q with 2.5B tokens, (2) Earnings Call Transcripts with 1.3B tokens and (3) Analyst Reports with 1.1B tokens. <br> Then, the model is fine-tuned on 10,000 manually annotated (positive, negative, neutral) sentences from S&P500 firms’ Analyst Reports. <br> *** Here, we just use the version created by HKUST team and don't do any further adjustment on the FinBERT.

### 2. Performance:
#### Compared to other models in this work, the Untuned HKUST’s FinBERT has the following performance: <br><br> (1) Accuracy: HKUST’s FinBERT model without fine-tuning has an accuracy of 80%, which is the lowest score among the models created. <br><br> (2) F1-Score: The model has a weighted average F1-Score of 79% (also the lowest). Compared to other models, it performs extremely badly on the recall rate & F1-Score in recognising Negative and Positive news. Besides, it also performs poorly on Neutral news’s precision rate.

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.80      | 0.69   | 0.74     |
| Neutral       | 0.79      | 0.92   | 0.85     |
| Positive      | 0.81      | 0.59   | 0.68     |
| Weighted Avg. | 0.80      | 0.80   | 0.79     |

![image](https://user-images.githubusercontent.com/92542287/220285617-06da5cd5-ec2f-4540-a745-644582292099.png)

#### (3) Prob. Distribution: The predicting probability is too concentrated in 0% and 100%. Considering it misclassifies many samples, the model is a bit too confident in its predictions. <br><br> (4) ROC Curve: The AUCs for Neutral and Positive news are slightly higher than 87%. The performance is transparently worse than other models. <br><br> (5) Precision-Recall Curve: The Positive news’s AP is just 75%. Overall, the 3 Precision-Recall conversion curves are all worse than other models.

![image](https://user-images.githubusercontent.com/92542287/220285846-14edb9f9-e785-43ec-9637-44f27481be0b.png)
