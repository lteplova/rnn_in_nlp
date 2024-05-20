## "Рекуррентные сети в NLP и приложениях"(AiEdu HSE)

### Задача: 

Классификация текстов с использованием рекуррентной нейронной сети

### Данные:

Используется датасет с соревнования VK CUP 2022 ссылка на kaggle
[Russian Social Media Text Classification](https://www.kaggle.com/datasets/mikhailma/russian-social-media-text-classification/data)

Датасет содержит тексты из спортивных сообществ социальной сети ВКонтакте.

Всего 13 подкатегорий тем, со следующим распределением:

<img width="925" alt="image" src="https://github.com/lteplova/rnn_in_nlp/assets/38242392/6d384fac-73e5-4284-8442-6c260ad5ba28">

Данные сбалансированы по классам, можем использовать Accuracy как метрику для оценки качества.

### Мое Решение

Классификация была выполнена с использованием рекурентной нейронной сети (```LSTM```) на PyTorch
Архитектура сети 

Для применения модели в дальнейшем используется FasAPI-сервис, описание и код доступен в следующем репозитории: 
<a href="https://github.com/lteplova/RNN_Classification_FasAPI">https://github.com/lteplova/RNN_Classification_FasAPI</a>



