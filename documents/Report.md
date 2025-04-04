# Отчет по итогам тестирования

## Краткое описание

- ​	Было проведено автоматизированное тестирование комплексного сервиса покупки тура, взаимодействующего с СУБД и API Банка.
- ​	В процессе проведения тестирования были реализованы позитивные и негативные сценарии.
- ​	Для работы с БД и симулятором банковских сервисов использовался Docker.
- ​	Результаты тестов не зависят от типа подключенной базы данных, поэтому представлен единый отчёт по тестам.

## Количество тест-кейсов

###### Всего было проведено 60 автотестов:

- ​	API тестирование - 12;
- ​	UI тестирование - 48;

###### Общий процент успешных тестов равен 55%.

По результатам авто-тестов составлены баг-репорты, описанные в [issue](https://github.com/Khumax/diplom/issues).

###### Результаты автоматизированного тестирования (в отчетах Allure)

### SQL
<details>
  <summary>Посмотреть</summary>
  
![](/img/sql/1.png)![](/img/sql/2.png)![](/img/sql/3.png)![](/img/sql/4.png)![](/img/sql/5.png)

</details>

### Postgre
<details>
  <summary>Посмотреть</summary>

![](/img/pgre/1.png)![](/img/pgre/2.png)![](/img/pgre/3.png)![](/img/pgre/4.png)![](/img/pgre/5.png)

</details>

### Общие рекомендации:

Сервис не готов к релизу, так как найденные баги критичны и негативно скажутся на бизнесе, необходима доработка сервиса и устранение багов.
