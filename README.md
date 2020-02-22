## Уровень back-end для ЛР № 4, основанный на Spring

Сервис построен по принципу REST API  
Собранный фронтенд для лабы надо закинуть в resources/static,
после чего для сборки всего проекта надо прописать или ./gradlew bootJar или ./mvnw clean package

- POST /api/users/register - запрос на создание нового пользователя.
В теле запроса должны присутсвовать данные пользователя в формате json.
- POST /api/users/login - запрос на аутентификацию пользователя.
В теле запроса должны присутсвовать данные пользователя в формате json.
В случае успешной аутентификации в теле ответа вернётся аутентификационный токен.
- GET /api/points - запрос на получение всех точек пользователя. 
Возвращается массив точек в формате json.
В запросе должен присутсвовать заголовок Authentication, содержащий аутентификационный токен.
- GET /api/points/recalculate?r=[r] - запрос на получение всех точек пользователя с учётом попадания/непопадания при изменившемся радиусе. 
Возвращается массив точек в формате json.
В запросе должен присутсвовать заголовок Authentication, содержащий аутентификационный токен.
- POST /api/points - запрос на добавление новой точки. 
В теле запроса должна присутсвовать точка в формате json.
В запросе должен присутсвовать заголовок Authentication, содержащий аутентификационный токен.
