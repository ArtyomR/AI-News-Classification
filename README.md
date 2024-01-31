# News classification with Logistic Regression, BERT and LLM/GPT

### Abstract
In this project I investigated several solutions for News classification.
A corpus of Russian-language news dedicated to Chines AI was
collected within ["Китайский Искусcтвенный Интеллект | 中国人工智能"](https://t.me/chinese_ai_news) news aggregation project. These news are divided on two classes: "Published" and "Not published". The problem was solved
using three natural language processing approaches: TF-IDF and Logistic
Regression, BERT and GPT. A comparative analysis of the results of
these approaches was carried out.
Repository of this project is located in https://github.com/ArtyomR/AI-News-Classification.

### Dataset
The Dataset was created within ["Китайский Искусcтвенный Интеллект | 中国人工智能"](https://t.me/chinese_ai_news) news aggregation project. It could be found in [ai_articles_prep_231124.xlsx](https://github.com/ArtyomR/AI-News-Classification/blob/main/ai_articles_prep_231124.xlsx "ai_articles_prep_231124.xlsx"). Data are combined from titles and first paragraphs of news dedicated
to Chinese high technologies. Originally these news were in English or
Chinese. Then they were translated into Russian by Google translation engine.
Example of Dataset records is on picture below.
![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/3cf6b5d7-9847-4daf-acaa-9f5077a02d9a)

After pre-processing and lematization dataset looks like on picture below.
![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/a6804a5d-0e77-4790-89e6-77892fbd5742)
There are 1711 (55.48%) 'Not published' news in this dataset and 'Published' news - 1373 (44.52%) in this dataset.
![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/e708e1b7-dddd-4cca-bbeb-39f1082ef560)

This dataset was divided on train dataset (2158 records - 70%) and test dataset (926 - 30%).

For Transformer (rubert-tiny2) model train dataset was divided on 2 subsets: train subset - 1726 records, validation subset - 432 records.

### Experiment Setup
- [01. Dataset preparation.ipynb](https://github.com/ArtyomR/AI-News-Classification/blob/main/01.%20Dataset%20preparation.ipynb) - It is Jupyter notebook for dataset pre-processing and exploration data analysis (EDA).
- [02_News_classification_with_TF_IDF_and_Logistic_Regression_v2.ipynb](https://github.com/ArtyomR/AI-News-Classification/blob/main/02_News_classification_with_TF_IDF_and_Logistic_Regression_v2.ipynb) - It is Jupyter notebook for News classification with TF-IDF and Logistic Regression.
- [03_News_classification_with_BERT_v6.ipynb](https://github.com/ArtyomR/AI-News-Classification/blob/main/03_News_classification_with_BERT_v6.ipynb) - It is Jupyter notebook for News classification with BERT (rubert-tiny2) model. I would like to recommend to use Google Colab because this code can use GPT processor and it is processed faster.
- [04_News_classification_with_LLM_and_RAG_v2.ipynb](https://github.com/ArtyomR/AI-News-Classification/blob/main/04_News_classification_with_LLM_and_RAG_v2.ipynb)) - It is Jupyter notebook for News classification with GPT (Saiga/Mistral) model. I would like to recommend to use Google Colab because this code can use GPT processor and it is processed faster.
  
### Results
Confusion matrix for Logistic Regression
![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/9951514d-0d3b-4474-b83a-fb625cefe9a9)

<br>
Confusion matrix for rubert-tiny2.

![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/26536e62-1392-48bb-96f6-bd9e893bb6e7)

Confusion matrix for GPT (Saiga/Mistral) model.
![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/4c2ab1b8-39b4-4f8b-aa99-6299221dfca1)

Best performance in terms of F1-score was shown by rubert-tiny2 model.

![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/220e3015-0c55-4355-97e9-af00767a9096)

Best performance in terms of Time of prediction was shown by Logistic Regression model.

![image](https://github.com/ArtyomR/AI-News-Classification/assets/10577827/d4b47f47-9884-478b-9464-17b85e79496a)

### Additional information
Please read [AI News Classification (LogReg, BERT, GPT) v4.pdf](https://github.com/ArtyomR/AI-News-Classification/blob/main/AI%20News%20Classification%20(LogReg%2C%20BERT%2C%20GPT)%20v4.pdf) for additional information.
