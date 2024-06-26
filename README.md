# Домашнее задание к занятию «`11.02 Микросервисы: принципы`» - `Живарев Игорь`

Вы работаете в крупной компании, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps-специалисту необходимо выдвинуть предложение по организации инфраструктуры для разработки и эксплуатации.

## Задача 1: API Gateway 

Предложите решение для обеспечения реализации API Gateway. Составьте сравнительную таблицу возможностей различных программных решений. На основе таблицы сделайте выбор решения.

Решение должно соответствовать следующим требованиям:
- маршрутизация запросов к нужному сервису на основе конфигурации,
- возможность проверки аутентификационной информации в запросах,
- обеспечение терминации HTTPS.

Обоснуйте свой выбор.

## Задача 2: Брокер сообщений

Составьте таблицу возможностей различных брокеров сообщений. На основе таблицы сделайте обоснованный выбор решения.

Решение должно соответствовать следующим требованиям:
- поддержка кластеризации для обеспечения надёжности,
- хранение сообщений на диске в процессе доставки,
- высокая скорость работы,
- поддержка различных форматов сообщений,
- разделение прав доступа к различным потокам сообщений,
- простота эксплуатации.

Обоснуйте свой выбор.

### Как оформить ДЗ?

Выполненное домашнее задание пришлите ссылкой на .md-файл в вашем репозитории.

---


## Ответ


| Решение | Маршрутизация запросов | Аутентификация при запросах | Терминация HTTPS | Модель распространения |
|:---:|:---:|:---:|:---:|:---:|
| APIGee | ✔ | ✔ | ✔ | Платная |
| Apache APISIX | ✔ | ✔ | ✔ | Опенсоурс |
| Axway | ✔ | ✔ | ✔ | Платная  |
| Kong | ✔ | ✔ | ✔ | Опенсоурс |
| Tyk | ✔ | ✔ | ✔ | Опенсоурс |
| NGINX Plus | ✔ | ✔ | ✔ | Платная |
| Gravitee.io | ✔ | ✔ | ✔ | Опенсоурс |

 - Можно использовать любое из указанных решений, но всё зависит от финансовой стороны вопроса.

 - Так же у больших облачных платформ присутствуют свои API Gateway решения, начиная с Амазона заканчивая Яндексом соответственно при использовании того или иного облака можно рассмотреть предложенные ими варианты.

 - Как я заметил в большинстве статей видимо из за популярности предлагают использовать API Gateway Kong. А чем популярнее решение тем легче его использовать.


### Ответ 2


| Возможности | Apache Kafka | RabbitMQ | Redis | ActiveMQ |
|:---:|:---:|:---:|:---:|:---:
| Поддержка кластеризации для обеспечения надежности | ✔ | ✔ | ✔ | ✔ |
| Хранение сообщений на диске в процессе доставки | ✔ | ✔ | ✔ | ✔ |
| Высокая скорость работы | ✔ | ✔ | ✔ | ✖ |
| Поддержка различных форматов сообщений | BINARY on TCP | STOMP/AMQP/MQTT |  RESP | AMQP//MQTT/RESP и пр. |
| Разделение прав доступа к различным потокам сообщений | ✔ | ✔ | ✔ | ✔ |
| Простота эксплуатации | ✖ | ✔ | ✔ | ✔ |


 - Как и в предыдущем задании, из за распространённости и частоты использования можно выбрать брокер сообщений RabbitMQ, он менее сложен в эксплуатации чем Apache Kafka и поддерживает несколько форматов сообщений.

---
 
