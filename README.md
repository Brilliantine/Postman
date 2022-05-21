# Postman
Демонстрация запросов в Postman осуществляется благодаря сервису [Dummy API](https://dummyapi.io/docs)</br>
![2022-05-21_12-16-59](https://user-images.githubusercontent.com/40222971/169644911-23dfaf52-dc2f-41a6-90cc-7f166374c616.png)</br>
[Документация](https://dummyapi.io/docs)</br>
При составлении запросов, будем работать с базовым URL https://dummyapi.io/data/v1/</br>
- [Предварительные действия](https://github.com/Brilliantine/Postman#предварительные-действия)
- [Запросы](https://github.com/Brilliantine/Postman#запросы)
    - [POST](https://github.com/Brilliantine/Postman#post)
    - [GET](https://github.com/Brilliantine/Postman#get)
    - [PUT](https://github.com/Brilliantine/Postman#put)
    - [DELETE](https://github.com/Brilliantine/Postman#delete)
## Предварительные действия
Прежде чем приступить к отправке запросов, необходиму пройти идентификацию. Для этого необходимо создать личный идентификатор app-id. Это можно сделать в [профиле](https://dummyapi.io/account), нажав на кнопку "Generate App ID"
![2022-05-21_12-19-48](https://user-images.githubusercontent.com/40222971/169645356-7bf3cf4d-9119-452c-869c-5a7f2503250b.png)</br>

В Headers делаем новую запись с ключом app-id и значением сгенерированного ключа
![2022-05-21_12-38-13](https://user-images.githubusercontent.com/40222971/169645680-be2e8ad1-900e-4e4e-b80a-ffbb784dc346.png)</br>
Теперь мы можем составлять запросы</br>
## Запросы
### POST
Создадим нового пользователя.</br>
Для этого выберем метод `POST`, добавим к базовому url `/user/create`. Затем перейдем во вкладку Body, выставим raw и выберем тип JSON</br>
***Тело запроса:***
```JSON
{
    "title": "mr",
    "firstName": "Eric",
    "lastName": "Cartman",
    "email": "ericcartwqfqfqgqgqgaman@gmail.com",
    "dateOfBirth": "1/1/1990",
    "phone": "+7(000)000-00-00",
    "picture": "https://dummyapi.io/",
    "location":
        {
            "street": "Green Street",
            "city": "Moscow",
            "state": "Moscow",
            "country": "Russia",
            "timezone": "+7:00"
        }
}
```
***Пользователь успешно создан***</br>
![2022-05-21_13-35-27](https://user-images.githubusercontent.com/40222971/169647783-3f703585-d1cf-4e72-9537-89391fc4c629.png)</br>
Копируем id из 2 строчки. Нам он ещё пригодиться.</br>
### GET
К базовому url добавляем `/user/6288bde93275fd10c6e7c72c`, выбераем метод `GET`.</br>
***Получаем созданного нами пользователя***
![2022-05-21_13-44-06](https://user-images.githubusercontent.com/40222971/169648143-b7a5a48e-0900-46b4-9344-cdbe4801ffb5.png)</br>
### PUT
Обновим данные нашего пользователя. Для скопируем предыдущий запрос `POST`, к базовому url добавим `/user/6288bde93275fd10c6e7c72c`, выберем метод `PUT`.</br>
***Поменяем тело запроса:***
```JSON
{
    "title": "mrs",
    "firstName": "Erica",
    "lastName": "Cartman",
    "email": "ericcartwqfqfqgqgqgaman@gmail.com",
    "dateOfBirth": "3/1/1990",
    "phone": "+7(111)111-11-11",
    "picture": "https://dummyapi.io/",
    "location":
        {
            "street": "Green Street",
            "city": "Moscow",
            "state": "Moscow",
            "country": "Russia",
            "timezone": "+7:00"
        }
}
```
***Данные успешно изменены***
![2022-05-21_14-03-01](https://user-images.githubusercontent.com/40222971/169648798-20d91a8c-8252-4faf-8f04-840bcc790697.png)</br>
### DELETE
Удалим нашего пользователя.</br>
Для этого выбераем метод `DELETE` к базовому url добавляем `/user/6288bde93275fd10c6e7c72c`.</br>
***Пользователь успешно удален***</br>
![2022-05-21_14-09-22](https://user-images.githubusercontent.com/40222971/169649009-2c41462f-9984-4e5f-ab2e-f68511cab210.png)

