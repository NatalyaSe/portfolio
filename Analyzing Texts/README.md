# Анализ текстов

[ipynb](https://github.com/NatalyaSe/portfolio/blob/master/Analyzing%20Texts/text_classif.ipynb)

## Описание проекта

Требуется анализировать комментарии пользователей на английском языке и выделять токсичные, чтобы отправить на модерацию.


## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- nltk.stem.**WordNetLemmatizer**
- sklearn.feature_extraction.text.**TfidfVectorizer**
- sklearn.linear_model.**LogisticRegression**
- sklearn.ensemble.**RandomForestClassifier**
- catboost.**CatBoostClassifier**



## Вывод

Проделаны следующие шаги:
* Загрузили данные и провели их предобработку - очистили текст, провели лемматизацию
* Обучилм 4 модели LogisticRegression, DecisionTreeClassifier, CatBoostClassifier, RandomForestClassifier с разными гиперпараметрами и выборками, посмотрели результаты на валидационной выборке
* По показателю F1 лучшей выбрали LogisticRegression, провели тестирование и результатом оказалось 0.774, что удовлетворяет требованию задания
* Аутсайдером среди моделей стали RandomForestClassifier и DecisionTreeClassifier, так как дали наименьшее F1.

Итак, наилучшей моделью стала LogisticRegression, которая на тестировании показала F1 = 0.774
