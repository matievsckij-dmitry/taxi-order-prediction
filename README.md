# Прогнозирование заказов такси

**Цель проекта**

Основная цель проекта - разработать модель машинного обучения, способную прогнозировать количество заказов такси на следующий час, основываясь на исторических данных. Это поможет компании "Чётенькое такси" более эффективно управлять ресурсами, в частности, привлекать больше водителей в периоды пиковой нагрузки. Ключевой показатель успеха проекта - достижение значения метрики RMSE (Root Mean Squared Error) не более 48 на тестовой выборке.

**Описание задачи**

1.  Анализ временных рядов: Данные о заказах такси представляют собой временной ряд, поскольку они упорядочены во времени. Необходимо проанализировать структуру этого ряда, выявить тренды, сезонность и другие закономерности, которые могут повлиять на прогнозы.

2.  Прогнозирование: На основе анализа данных нужно построить модель, которая сможет предсказывать количество заказов такси на следующий час. Это задача прогнозирования временных рядов.

**Вывод**

 LGBMRegressor признана лучшей моделью благодаря наименьшему RMSE (27.60) на валидационной выборке и хорошему балансу между скоростью и точностью. DecisionTreeRegressor, несмотря на высокую скорость, показала сопоставимую с более сложными моделями точность. Переобучение не наблюдается. Все модели показали RMSE на тестовой выборке менее 48. Распределение остатков близко к нормальному с небольшим смещением. Модели занижают прогнозы для высоких значений тестовой выборки (более 150 заказов), но улавливают временные паттерны.
