# Прогнозирование заказов такси на следующий час

[ipynb](https://github.com/NatalyaSe/portfolio/blob/master/Taxi%20Service/taxi_prediction.ipynb)

## Описание проекта

Требуется спрогнозировать количество заказов такси на следующий час, чтобы привлекать больше водителей в период пиковой нагрузки.

## Навыки и инструменты

- **python**
- **pandas**
- **numpy**
- statsmodels.tsa.seasonal.**seasonal_decompose**
- sklearn.model_selection.**TimeSeriesSplit**
- sklearn.model_selection.**GridSearchCV**
- sklearn.metrics.**mean_squared_error**
- sklearn.metrics.**make_scorer**
- sklearn.linear_model.**LinearRegression**
- sklearn.ensemble.**RandomForestRegressor**
- catboost.**CatBoostRegressor**
- **matplotlib**

## 

## Вывод

* Ресемплировали исходные данные по одному часу и рассмотрели тренд, сезонность и остатки: в общем тренд растет, также количество заказов значительно больше в вечернее время
* Перешли к разностям нашего ряд - такой ряд является стационарным, что подходит для прогнозирования
* Создали признаки для прогноза: max_lag = 24 и rolling_mean_size = 48
* Разделили выборку в соотношении 9:1
* Даллее рассмотрели модели LineralRegressor,RandomForestRegressor, CatBoostRegressor и LightGBM
  
Все модели удовлетворяют требованию задания RMSE < 48, но по итогам качества и скорости обучения лучшей я считаю модель СatBoostRegressor. RMSE на тестовых данных = 42, скорость обучения = 13.5s, скорость предсказания = 0.06s
