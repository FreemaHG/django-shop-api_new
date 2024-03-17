


#### Pre-commit

В проекте используются Git-хуки для автоматической проверки и форматирования кода перед созданием коммита.

**ВАЖНО**: на локальной машине разработчика должен быть установлен пакет **pre-commit**:
   ```
   pip install pre-commit
   ```

Применяемые хуки описаны в корне проекта в файле .pre-commit-config.yaml

Для активации хуков вводим:
   ```
   pre-commit install
   ```
Предварительная проверка и форматирование кода:
   ```
   pre-commit run --all-files
   ```

#### Тестирование

**Теги**:
* anonymous - тесты, проверяющие ответ при обращении неавторизованным пользователем
* get - тесты, проверяющие корректность возвращаемых данных
* profile - тесты, проверяющие возврат и обновление профиля
* password - тесты, проверяющие обновление пароля
* update - тесты, проверяющие обновление данных приложения
* not_found - тесты, проверяющие сообщение при отсутствии данных для вывода или обновления
* invalid_data - тесты, проверяющие обработку при передаче невалидных данных
* error - тесты, проверяющие сообщения в случае возникновения ошибок
* cache - тесты, проверяющие корректность сохранения и очистки кэша

Запуск тестов:
   ```
   python3 -m backend.manage test
   ```

Запуск тестов с тегом "profile":
   ```
   python3 -m backend.manage test --tag=profile
   ```
