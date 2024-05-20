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
Классификация была выполнена с использованием рекурентной нейронной сети (```LSTM```) на PyTorch  
Архитектура сети:
однослойный LSTM ```nn.LSTM(hidden_dim = 256, num_layers = 2, bidirectional=True, dropout=0.2)```  
линейный слой ```nn.Linear```  
нормализация ```nn.BatchNorm1d```  
линейный слой для классификации ```nn.Linear(hidden_dim, num_classes)```  
дропаут ```nn.Dropout```  
функция активации ```nn.Tanh()```  
входной эмбеддинг формируется путем  аггрегации по максимуму и конкатенации результата с эмбедингом последнего токена  

### Используемые технологии
Cеть написана на PyTorch

### Применение модели в приложении:

Для применения модели используется FasAPI-сервис, описание и код доступны в следующем репозитории: 
<a href="https://github.com/lteplova/RNN_Classification_FasAPI">https://github.com/lteplova/RNN_Classification_FasAPI</a>



