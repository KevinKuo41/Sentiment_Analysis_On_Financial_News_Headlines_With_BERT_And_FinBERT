# Source
#### The dataset used in this work was downloaded from the Kaggle Database – [Financial News Headline](https://www.kaggle.com/datasets/keitazoumana/financialnewsheadline). The dataset has 4,846 financial news headlines, each with a tag to label its sentiment as either Neutral, Negative, or Positive. They were published by CNBC, Guardian or Reuters from 2017 to 2020. The average length of the headlines is 30.6 tokens (mostly short sentences), and the max length among them is 150 tokens. No headline’s token length is greater than the maximum token length, 512, that the BERT model can take. Regarding the dataset’s sentiment distribution, 59.4% is labelled as Neutral, 28.1% as Positive, and 12.5% as Negative. We randomly sort 81% of the samples into the training set, 9% into the validation set, and 10% into the test set.

# Sentiment Distribution of the Dataset

![image](https://user-images.githubusercontent.com/92542287/219822919-e8e01bc6-650d-4ce2-808a-2be7273755cd.png)


# Data Structure & Content

| #    | Label    | Financial News Headline                            |
|------|----------|----------------------------------------------------|
| 0    | Neutral  | According to Gran , the company has no plans t...  |
| 1    | Neutral  | Technopolis plans to develop in stages an area...  |
| 2    | Negative | The international electronic industry company ...  |
| 3    | Positive | With the new production plant the company would... |
| 4    | Positive | According to the company 's updated strategy f...  |
| ...  | ...      | ...                                                |
| 4841 | Negative | LONDON MarketWatch -- Share prices ended lower...  |
| 4842 | Neutral  | Rinkuskiai 's beer sales fell by 6.5 per cent ...  |
| 4843 | Negative | Operating profit fell to EUR 35.4 mn from EUR ...  |
| 4844 | Negative | Net sales of the Paper segment decreased to EU...  |
| 4845 | Negative | Sales in Finland decreased by 10.5 % in January... |
