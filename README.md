# PostgreSQL_python

PostgreSQL + python + psycopg2

Перед запуском потребуется установить библиотеку psycopg2, команда для установки:

<code> pip install psycopg2 </code>

<a href="https://pypi.org/project/psycopg2/" target="blank"> Подробнее о билиотеке psycopg2 </a>

Для отображения ответа базы данных используется библиотека prettytable, 
её так же потребуется установить перед запуском, команда для установки:

<code>pip install PrettyTable</code>

<a href="https://pypi.org/project/PrettyTable/" target="_blank"> Подробнее о билиотеке PrettyTable</a>

Скрипт для подключения и работы с БД postgresql, для запуска потребуется создать файл 
connection-data.txt указать параметры подключения:

<pre>
Название_базы
Имя_пользователя
Пароль
IP адрес хоста
Порт хоста
</pre>

Важно! Параметры указываются без использования дополнительных символов, каждый параметр записывается с новой строки.

После подключения покажет существующие таблицы в базе и предложит ввести команду, доступные команды:

1. select - select * from <Input table name>
Обычный select запрос, возвращает все поля в таблице.  

2. create - Create new table
Создаёт новую таблицу, название вводится после выбора этой функции.

3. his - Your query
Введите ваш запрос.

4. exist - Вернёт названия существующих таблиц.

5. drop - Drop exist table
Запросит ввод названия таблицы, далее удалит её из базы, если таблицы нет в базе вернёт соответствующие сообщение.

6. q - Exit.
Выход.

Что бы использовать функцию нужно ввести её номер или название.


<h2>Логирование.</h2>

<p> Функция log отвечаеть за запись файла лога, в лог сохраняется время, в которое был выполнен запрос(сейчас это время записи в файл),
сам запрос, ответ от БД, если он есть. По умолчанию файл лога создаётся в директории со скриптом, название состоит из log{date}.log,
где date это дата в формате год-месяц-день, можно указать нужный путь до файла, он определяется в переменной file_with_log.</p>