# Cross-Model Comparison
### 1. Fine-tuned BERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.85      | 0.85   | 0.85     |
| Neutral       | 0.90      | 0.90   | 0.90     |
| Positive      | 0.82      | 0.82   | 0.82     |
| Weighted Avg. | 0.87      | 0.87   | 0.87     |

![image](https://user-images.githubusercontent.com/92542287/220272940-be47e1f3-1f46-4561-bb99-2da716dc2c99.png)
![image](https://user-images.githubusercontent.com/92542287/220272972-79c80088-c7dc-4967-aa8d-a13b7fde3893.png)

### 2. Further Pre-trained BERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.79      | 0.86   | 0.82     |
| Neutral       | 0.89      | 0.91   | 0.90     |
| Positive      | 0.86      | 0.78   | 0.81     |
| Weighted Avg. | 0.87      | 0.87   | 0.87     |

![image](https://user-images.githubusercontent.com/92542287/220274697-31481627-f2d0-431e-b800-74b7f8af9314.png)
![image](https://user-images.githubusercontent.com/92542287/220274926-b08012ad-e34f-4f16-80e6-b1a97de1acec.png)

### 3. Untuned ProsusAI FinBERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.78      | 0.97   | 0.87     |
| Neutral       | 0.97      | 0.85   | 0.91     |
| Positive      | 0.82      | 0.93   | 0.87     |
| Weighted Avg. | 0.9       | 0.89   | 0.89     |

![image](https://user-images.githubusercontent.com/92542287/220276267-f47048c8-b51b-427d-b78d-81121a5ef221.png)
![image](https://user-images.githubusercontent.com/92542287/220276640-ad4914f4-4a09-4f18-91b8-3139e602eb01.png)

### 4. Fine-tuned ProsusAI FinBERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.95      | 1.00   | 0.97     |
| Neutral       | 0.99      | 0.97   | 0.98     |
| Positive      | 0.97      | 0.97   | 0.97     |
| Weighted Avg. | 0.98      | 0.98   | 0.98     |

![image](https://user-images.githubusercontent.com/92542287/220281033-667cca83-f9a7-4762-8e73-0a5e06a8123f.png)
![image](https://user-images.githubusercontent.com/92542287/220281082-c137c8b1-6b7a-489a-ad41-a43d6747b6e1.png)

### 5. Untuned HKUST FinBERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.80      | 0.69   | 0.74     |
| Neutral       | 0.79      | 0.92   | 0.85     |
| Positive      | 0.81      | 0.59   | 0.68     |
| Weighted Avg. | 0.80      | 0.80   | 0.79     |

![image](https://user-images.githubusercontent.com/92542287/220285617-06da5cd5-ec2f-4540-a745-644582292099.png)
![image](https://user-images.githubusercontent.com/92542287/220285846-14edb9f9-e785-43ec-9637-44f27481be0b.png)

### 6. Fine-tuned HKUST FinBERT

| Class         | Precision | Recall | F1-Score |
|---------------|-----------|--------|----------|
| Negative      | 0.76      | 0.88   | 0.81     |
| Neutral       | 0.89      | 0.88   | 0.88     |
| Positive      | 0.83      | 0.79   | 0.81     |
| Weighted Avg. | 0.85      | 0.85   | 0.85     |

![image](https://user-images.githubusercontent.com/92542287/220286595-16f9154e-25bd-4edf-b13e-4096b10652a3.png)
![image](https://user-images.githubusercontent.com/92542287/220286651-2badcb37-2d77-4244-bbb1-4333c331c9a8.png)
