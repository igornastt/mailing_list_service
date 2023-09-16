Описание

Чтобы удержать текущих клиентов, они часто используют "разогревающие" 
рассылки для информирования и привлечения клиентов. 
Этот проект организует и систематизирует создание 
ваших информационных бюллетеней и управление ими.

Требования:

Django
psycopg2
pillow
django4-background-tasks
redis
python-dotenv

Настройте свои личные настройки

Создайте .env конфигурационный файл с вашими личными настройками 
в корневом каталоге проекта, согласно образцу, указанному в .env.sample. 
Заполните файл в соответствии с вашими личными данными.

Создайте базу данных в postgresql. Имя базы данных должно 
совпадать с именем, указанным в файле.

Предварительные настройки

Прежде всего, перенесите свою базу данных: python manage.py migrate.
Перед запуском проекта создайте суперпользователя, группы, менеджера и 
менеджера контента, выполнив следующие команды в терминале:

python manage.py csu
python manage.py create_groups
python manage.py create_manager
python manage.py create_content_manager
Заполните периоды рассылок с помощью команды:
python manage.py fill_periods Также, при желании, 
вы можете заполнить блог командой python manage.py loaddata blog.json 
или создать его самостоятельно!

Выполняется

Чтобы запустить проект, введите python manage.py runserver команду 
в терминале. Откройте второе окно терминала и 
введите python manage.py process_tasks (это необходимо для мониторинга и выполнения фоновых задач).
Перейдите по ссылке - проект готов к использованию!