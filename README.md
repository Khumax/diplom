# Дипломный проект по профессии «Тестировщик»
Дипломный проект — автоматизация тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.

## Документация
- [План автоматизации](documents/Plan.md)
- [Отчётные документы по итогам тестирования](documents/Report.md)
- [Отчётные документы по итогам автоматизации](documents/Summary.md)

## Запуск SUT, авто-тестов и генерация отчетов

### Подключение SUT к MySQL

1. Запустить Docker Desktop
2. Открыть проект в IntelliJ IDEA
3. В терминале в корне проекта запустить контейнеры:

   ```
   docker-compose up -d
   ```
4. Запустить приложение:

   ```
   java -jar artifacts/aqa-shop.jar --spring.datasource.url=jdbc:mysql://localhost:3306/app
   ```


1. Открыть второй терминал
2. Запустить тесты:

   ```
   .\gradlew clean test -DdbUrl=jdbc:mysql://localhost:3306/app
   ```
3. Создать отчёт Allure и открыть в браузере

   ```
   .\gradlew allureServe
   ```
4. Закрыть отчёт:
   **CTRL + C -> Y -> Enter**

5. Перейти в первый терминал
6. Остановить приложение:
   **CTRL + C**

7. Остановить контейнеры:

   ```
   docker-compose down
   ```

## Запуск SUT, авто-тестов и генерация репорта

### Подключение SUT к PostgreSQL

 1. Запустить Docker Desktop
 2. Открыть проект в IntelliJ IDEA
 3. В терминале в корне проекта запустить контейнеры:

    ```
    docker-compose up -d
    ```
 4. Запустить приложение:

    ```
    java -jar artifacts/aqa-shop.jar --spring.datasource.url=jdbc:postgresql://localhost:5432/app
    ```
 5. Открыть второй терминал
 6. Запустить тесты:

    ```
    .\gradlew clean test -DdbUrl=jdbc:postgresql://localhost:5432/app
    ```
 7. Создать отчёт Allure и открыть в браузере

    ```
    .\gradlew allureServe
    ```
 8. Закрыть отчёт:
    **CTRL + C -> Y -> Enter**

 9. Перейти в первый терминал
10. Остановить приложение:
    **CTRL + C**
    
12. Остановить контейнеры:

    ```
    docker-compose down
    ```
