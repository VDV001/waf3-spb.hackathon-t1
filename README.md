# waf3-spb.hackathon-t1
### Конфиг для блокировки атак
#### Основные моменты
-- Объяснение конфигурации
- Общие настройки
Включает режим защиты и устанавливает лимиты для PCRE.
Ограничивает размер тела запроса для предотвращения атак типа DoS.
Настраивает логирование всех заблокированных запросов.
- Правила для защиты
Правила для обнаружения сканеров безопасности на основе заголовка User-Agent.
Правила для защиты от SQL-инъекций и XSS.
Правила для предотвращения удаленного выполнения кода и CSRF.
Правила для защиты от Directory Traversal.
- Уровни паранойи
Уровни паранойи позволяют настраивать строгие проверки в зависимости от уровня угрозы.
Блокировка по умолчанию:
Все запросы без явного разрешения будут блокироваться.
#### Дополнительные правила
Защита от HTTP Response Splitting и HTTP Header Injection помогают предотвратить атаки через манипуляцию заголовками.
Блокировка запросов с подозрительными символами поможет предотвратить внедрение вредоносного кода через ввод пользователя.
Ограничение частоты запросов позволяет минимизировать риск DoS/DDoS атак.
Уровни паранойи:
Конфигурация использует уровни паранойи для настройки строгости правил.
Логирование:
Все действия по блокировке записываются в журнал для дальнейшего анализа.
Применение конфигурации
Создайте файл конфигурации:
Сохраните приведенный выше код в файл с именем policy.conf.
Поместите файл в директорию конфигурации вашего WAF:
Например, /etc/modsecurity/ или /etc/apache2/conf.d/.
Перезапустите WAF или веб-сервер, чтобы применить новые правила
