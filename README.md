# Проект парсинга документации Python и PEP
Парсинг информации:
https://docs.python.org/3/
https://peps.python.org/

## Описание
-Сбор ссылок на статьи о изменениях в версиях Python,
-Сбор информации о статусах версий Python.
-Скачивание архива с актуальной документацией Python.
-Сбор данных обо всех документах PEP и сравнение статуса
на странице каждого PEP и в общем списке.
-Собранная информация записывается в файл
-Управление парсером реализовано через аргументы командной строки.

## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке
Cоздать и активировать виртуальное окружение
Обновить PIP
Установить зависимости из файла requirements.txt
Запустить main.py

git clone https://github.com/AlexGriv/bs4_parser_pep.git
python3 -m venv env
source env/bin/activate
python -m pip install -U pip
pip install -r requirements.txt
python main.py [парсер] [аргумент]

Например:
python main.py whats-new -o pretty

## Встроенные парсеры
*whats-new*
*latest_versions*
*download*
*pep*

## Аргументы
Общая информация о командах: `-h, --help`
Очистка кеша: `-c, --clear-cache`
Вывода данных:
pretty - выводит данные в командной строке в таблице
file - сохраняет информацию в формате csv в папке ./results/

Например:
python main.py -с
python main.py [парсер] -o file
python main.py [парсер] -o pretty

## Автор
Гривцов А.С.
