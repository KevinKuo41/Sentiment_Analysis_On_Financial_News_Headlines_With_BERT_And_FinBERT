# Fine-tuned HKUST FinBERT

### 1. Fine-tuning Process In This Work:
#### Here, we e used 3,924 samples to fine-tune HKUST’s FinBERT again. <br> * Params: learning rate = 2e-5, batch size = 32, with 5 epochs -> The model finishing 3 epochs produced the utmost F1-Score

### 2. Performance:
#### Compared to its untuned version, the fine-tuned model has the following performance: <br><br> (1) Accuracy: After our fine-tuning again, the HKUST FinBERT model’s accuracy increased by 5% to 85% compared to its untuned version. <br><br> (2) F1-Score: Compared to the untuned version, the model’s weighted average F1-Score also rose to 85%. The recall rates for Negative and Positive news are drastically improved. Moreover, the precision rate for Neutral news also substantially rises with an exchange of a bit lower recall rate.

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.76      | 0.88   | 0.81     |
| Neutral       | 0.89      | 0.88   | 0.88     |
| Positive      | 0.83      | 0.79   | 0.81     |
| Weighted Avg. | 0.85      | 0.85   | 0.85     |

![image](https://user-images.githubusercontent.com/92542287/220286595-16f9154e-25bd-4edf-b13e-4096b10652a3.png)

#### (3) Prob. Distribution: Its probability became less concentrated in 0% and 100% as its untuned version did, meaning it has become more flexible. <br><br> (4) ROC Curve: The AUC for all 3 classes is greater than 93%, especially a significant improvement on Neutral and Positive news. <br><br> (5) Precision-Recall Curve: The APs for all 3 classes ameliorate to higher than 89%. The Precision-Recall conversion curves also get a bit better.

![image](https://user-images.githubusercontent.com/92542287/220286651-2badcb37-2d77-4244-bbb1-4333c331c9a8.png)
