# Улучшение процесса обогащения золота

[ipynb](https://github.com/NatalyaSe/portfolio/blob/master/Gold%20Recovery/gold_recovery.ipynb)

## Описание проекта

Требуется подготовить прототип модели машинного обучения, которая должна предсказать коэффициент восстановления золота из золотосодержащей руды. Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.


## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- **scipy**
- sklearn.model_selection.**cross_val_score**
- sklearn.metrics.**mean_squared_error**
- sklearn.metrics.**mean_absolute_error**
- sklearn.preprocessing.**StandardScaler**
- sklearn.linear_model.**LinearRegression**
- sklearn.tree.**DecisionTreeRegressor**
- sklearn.ensemble.**RandomForestRegressor**
- **matplotlib**

## 

## Вывод

* Итоговая модель построена на алгоритме RandomForest
* Ошибка на тестовой выборке: 9.23
* Параметры алгоритма: { max_depth: 10}
* Параметр recovery в тренировочной выборке был рассчитан верно
* Изначально, в тестовой выборке отсутствует 34 признака
