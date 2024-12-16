Django установленный системой автоматической установки cms LTD BEGET
 
=> Действия описанные ниже необходимо выполнять в docker-окружении выполнив команду ниже <=
$ ssh localhost -p222
 
для установки дополнительных модулей используйте pip
сам джанго располагается в папке /home/t/tochkatbr/laserzlat.tochkatbr.beget.tech/public_html/venv/lib/python2.7/site-packages
 
для начала надо переключиться на текущий virtualenv
заходим в папку с проектом
 
$ cd /home/t/tochkatbr/laserzlat.tochkatbr.beget.tech/public_html
$ source venv/bin/activate
 
проверяем правильно ли определился путь до pip:
$ which pip
/home/t/tochkatbr/laserzlat.tochkatbr.beget.tech/public_html/venv/bin/pip
 
теперь мы можем пользоваться pip'ом для установки модулей не указывая полного пути до исполняемого файла:
 
$ pip install
 
где  имя модуля который мы хотим установить
 
Для перезапуска passenger в папке проекта достаточно выполнить команду touch на пустом файлике restart.txt
 
$ pwd
/home/t/tochkatbr/laserzlat.tochkatbr.beget.tech/public_html/HelloDjango/HelloDjango/tmp
$ touch restart.txt

!!! ВАЖНО !!!
laserzlat.tochkatbr.beget.tech адрес сейчас другой

Для локального запуска
1. Устанавливаем venv в корень проекта: lazer
2. ./venv/Scripts/activate.ps1 или ./venv/bin/activate (если linux)
3. pip install -r requirements.txt
4. Удаляем из папки HelloDjango\shop\migrations все файлы кроме __init__
5. Удаляем из папки HelloDjango\mypages\migrations все файлы кроме __init__
6. python .\HelloDjango\manage.py makemigrations
7. python .\HelloDjango\manage.py migrate
5. python .\HelloDjango\manage.py runserver
Файл sqlite таскаем с собой, иначе Welcome page не открывается