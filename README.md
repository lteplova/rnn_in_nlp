# rnn_in_nlp
Проект курса "Рекуррентные сети в NLP и приложениях"(AiEdu HSE)

## Задача: Классификация текстов с использованием рекуррентной нейронной сети

Классификация была выполнена с использованием рекурентной нейронной сети (LSTM) на PyTorch

Используются данные с соревнования VK CUP 2022 ссылка на kaggle
[Russian Social Media Text Classification](https://www.kaggle.com/datasets/mikhailma/russian-social-media-text-classification/data)

Датасет содержит тексты из спортивных сообществ социальной сети ВКонтакте.
Содержит 13 подкатегорий тем:
* athletics
* autosport
* basketball
* boardgames
* esport
* extreme
* football
* hockey
* martial_arts
* motosport
* tennis
* volleyball
* winter_sport

<img width="925" alt="image" src="https://github.com/lteplova/rnn_in_nlp/assets/38242392/6d384fac-73e5-4284-8442-6c260ad5ba28">

Данные сбалансированы по классам, можем использовать Accuracy как метрику для оценки качества.

Для применения модели в дальнейшем используется FasAPI-сервис, описание и код доступен в следующем репозитории: 
<a href="https://github.com/lteplova/RNN_Classification_FasAPI">https://github.com/lteplova/RNN_Classification_FasAPI</a>



