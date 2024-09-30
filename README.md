##  Отборочное задание на смену по машинному обучению в Сириус

### Задача

Требуется реализовать свою русскоязычную QA систему. Для простоты будем полагать, что ответ уже есть в заданном вопросе.

### Пререквизиты

Для обучения / тьюнинга / построения базы знаний можно взять аннотированный датасет [sberquad](https://huggingface.co/datasets/kuznetsoffandrey/sberquad) или что-то на своё усмотрение :)

### Подходы к решению

1. Information retrieval (+ ranking)
   - можно построить RAG
2. Encoder-decoder models (T5)
3. Поиск start/end токенов ответа в вопросе
4. Всё что угодно (кроме банального вызова генеративной llm-ки с вопросом в промпте)

### Ожидаемый формат решения

Чтобы нам было проще валидировать ваши модели, желательно поднять телеграм-бота. Либо написать простенький фласк-сервис и обернуть его в докер.

Модельные эксперименты можно проводить в коллабе.

В качестве решения нужно прислать ссылку на гитхаб-репозиторий с кодом сервиса и экспериментов (можно закоммитить в отдельную директорию юпитер-ноубук, либо отправить ссылку на коллаб).

**Мы будем оценивать:**
- качество кода
- описание решения (чем подробнее, тем лучше)
- сложность выбранного метода
- его работоспособность

### FAQ

**Вопросы по формату запроса/ответа:**
- Если вы положили весь контекст из sberquad в свою базу знаний, это хорошее решение! Тогда для валидации мы будем отправлять вопросы, похожие на те, что были в этом датасете (но не обязательно их же точь-в-точь)
- Если ваше решение подразумевает предварительное написание контекста, тогда, пожалуйста, опишите предполагаемый формат запроса в readme

**Вопросы по поднятию бота:**
- Я искренне верю, что смогу проверить все задания в первые две недели октября. Поэтому хочется, чтобы бот был доступен в течении этого времени
- Если вам не хочется поднимать телеграм-бота, можете запушить образ со своим сервисом на [докерхаб](https://hub.docker.com). Тогда при проверке мы сами развернём у себя приложение.
