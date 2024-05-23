## "Рекуррентные сети в NLP и приложениях"(AiEdu HSE)

### Задача: 
Классификация текстов с использованием рекуррентной нейронной сети
### Данные:
Используется датасет с соревнования kaggle VK CUP 2022 
[Russian Social Media Text Classification](https://www.kaggle.com/datasets/mikhailma/russian-social-media-text-classification/data)  
Датасет содержит тексты из спортивных сообществ социальной сети ВКонтакте.  
Всего 13 подкатегорий тем, со следующим распределением:  
<img width="925" alt="image" src="https://github.com/lteplova/rnn_in_nlp/assets/38242392/6d384fac-73e5-4284-8442-6c260ad5ba28">  
Данные сбалансированы по классам, можем использовать Accuracy как метрику для оценки качества.  
### Мое Решение:
Классификация была выполнена с использованием рекурентной нейронной сети (```LSTM```)
***Архитектура сети:***  
однослойный LSTM ```LSTM(hidden_dim = 256, num_layers = 2, bidirectional=True, dropout=0.2)```  
линейный слой ```Linear```  
нормализация ```BatchNorm1d```  
линейный слой для классификации ```Linear(hidden_dim, num_classes)```  
дропаут ```Dropout```  
функция активации ```Tanh()```  
в сеть подается - эмбединг, сформированный как результат конкатенации аггрегации всех токенов по максимуму и эмбединга последнего токена  
Файл обученной модели по [ссылке](https://drive.google.com/file/d/1SECK0p2jrfBuhSRl4_o_BmH5eLcsSGY3/view?usp=drive_link)  
### Используемые технологии
Cеть написана на PyTorch

### Применение модели в приложении:

Для применения модели используется FasAPI-сервис, описание и код доступны в следующем репозитории: 
<a href="https://github.com/lteplova/RNN_Classification_FasAPI">https://github.com/lteplova/RNN_Classification_FasAPI</a>



