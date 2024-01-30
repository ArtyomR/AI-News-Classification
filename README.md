# News classification with Logistic Regression, BERT and GPT

#### Abstract
In this project I investigated several solutions for News classification.
A corpus of Russian-language news dedicated to Chines AI was
collected within "Китайский Искусcтвенный Интеллект | 中国人工智能" (https://t.me/chinese_ai_news) news aggregation project. These news are divided on two classes: "Published" and "Not published". The problem was solved
using three natural language processing approaches: TF-IDF and Logistic
Regression, BERT and GPT. A comparative analysis of the results of
these approaches was carried out.
Repository of this project is located in https://github.com/ArtyomR/AI-News-Classification.

#### Dataset
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

For Transformer (rubert-tiny2) model train dataset was divided on 2 subsets:train subset - 1726 records, validation subset - 432 records.
