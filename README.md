# open-data-battle

Репозиторий содержит решение задач соревнования [Open data battle](https://open-data-battle.geecko.com/issues)  
## Результат  
15 место (top 6%), финальный скор mae 0.05853  
## Структура репозитория
- airport - содержит решение задачи отборочного тура [Airport](https://open-data-battle.geecko.com/issues/airport)  
- gender - содержит решение задачи отборочного тура [Gender](https://open-data-battle.geecko.com/issues/gender)  
- mpp - содержит решение основной задачи соревнования [MPP](https://open-data-battle.geecko.com/issues/mpp)
## Идея решения основной задачи
MPP - pадача по прогнозированию ошибки модели оценки вероятности дефолта.  
Решалась задача регрессии для целевой переменной |PD - flg_90_12_add|.  
Алгоритм - catboost.  
Функция ошибки - MAE.  
Использовалось логарифмирование целевой переменной, чтобы сделать ее распределение более похожим на нормальное.  
Для категориальных переменных пропуски заполнены модой, а для числовых - средним.
