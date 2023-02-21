# Further Pre-trained BERT
### 1. Further Pre-training Process in This Work:
#### In this work, we aim to train the BERT model to conduct sentiment analysis on Financial News Headline dataset, so we use 81% of the dataset (3,924 samples) to further pre-train the BERT model and test its performance on the validation and test dataset (922 samples). <br><br> To simultaneously implement the 3 mentioned techniques to avoid catastrophic forgetting, we applied the transformer (4.25.1) and fast.ai (1.0.58) packages together to further pre-train the BERT model. <br><br> For the Discriminative Layer Training, we applied 2e-5 as the learning rate cap for the last layer and 1.7e-5 as the learning rate cap for the first layer. For the layers between the first and last layer, their learning rate caps are proportionally increasing from 1.7e-5 to 2e-5. We mention “cap” here because we applied the Slanted Triangular Learning Rates simultaneously, so the learning rates kept changing dynamically through the training process. <br><br> For the Gradual Unfreezing, we unfroze 1 layer by 1 layer, starting from the last layer, with each training epoch. Since the BERT has 12 layers, we need at least 12 epochs to unfreeze all layers. We noticed that starting from the 5th epoch, the model began overfitting, and the model further pre-trained on the last 4 layers outperforms all others, so we keep and test it only.

### 2. Performance:
#### We used 3,924 samples to further pre-train the BERT. Compared to the only-fine-tuned BERT, the further pre-trained BERT has the following performance: <br><br> (1) Accuracy: The model further pre-trained only on the last 4 layers has an accuracy of 87%. <br><br> (2) F1-Score: The model has a weighted average F1-Score of 87%. However, compared to the only-fine-tuned BERT, its performance in identifying Negative and Positive news is slightly worse, which is not good since we care more about Negative and Positive news than Neutral news in the financial market.

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.79      | 0.86   | 0.82     |
| Neutral       | 0.89      | 0.91   | 0.90     |
| Positive      | 0.86      | 0.78   | 0.81     |
| Weighted Avg. | 0.87      | 0.87   | 0.87     |

![image](https://user-images.githubusercontent.com/92542287/220274697-31481627-f2d0-431e-b800-74b7f8af9314.png)

#### (3) Prob. Distribution: The predicting probability for all 3 classes is continuously distributed better. <br><br> (4) ROC Curve: The AUCs for all 3 classes are greater than 94%, and the model’s AUC is relatively higher in recognising Negative News. <br><br> (5) Precision-Recall Curve: The APs for all 3 classes are higher than 89%, but the conversion rate between precision and recall in Negative news is worse.

![image](https://user-images.githubusercontent.com/92542287/220274926-b08012ad-e34f-4f16-80e6-b1a97de1acec.png)
