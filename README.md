# Тестирование API
Демонстрация запросов в Postman осуществляется благодаря сервису [Dummy API](https://dummyapi.io/docs)</br>
![2022-05-21_12-16-59](https://user-images.githubusercontent.com/40222971/169644911-23dfaf52-dc2f-41a6-90cc-7f166374c616.png)</br>
[Документация](https://dummyapi.io/docs)</br>
При составлении запросов, будем работать с базовым URL https://dummyapi.io/data/v1/</br>
## Предварительные действия
Прежде чем приступить к отправке запросов, необходиму пройти идентификацию. Для этого необходимо создать личный идентификатор app-id. Это можно сделать в [профиле](https://dummyapi.io/account), нажав на кнопку "Generate App ID"
![2022-05-21_12-19-48](https://user-images.githubusercontent.com/40222971/169645356-7bf3cf4d-9119-452c-869c-5a7f2503250b.png)</br>

В Headers делаем новую запись с ключом app-id
![2022-05-21_12-38-13](https://user-images.githubusercontent.com/40222971/169645680-be2e8ad1-900e-4e4e-b80a-ffbb784dc346.png)
## Запросы
Теперь мы можем оставлять запросы
### POST
Создадим нового пользователя. Для этого добавим к базовому url `/user/create`. Затем перейдем во вкладку Body, выставим raw и выберем тип JSON</br>
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
