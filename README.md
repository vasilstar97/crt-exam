1. git clone https://git.crtweb.ru/creative-packages/docker-lesson в репозитории
2. git remote set-url origin https://github.com/vasilstar97/crt-exam
затем git push и всё стянется в удаленный репозиторий в master
(при создании репозитория гит вроде как дает возможность сразу инициализировать его с другого репозитория, но не проверял)
3. git branch dev - создаем новую ветку, с помощью switch переключаемся на нее
4. в /docker/php есть Dockerfile, в него добавляем переменную окружения со своим именем фамилией, пересобираем проект с помощью docker-compose up --build. У меня ругалось на версию, поэтому в yml файле поменял на 3.3. winpty docker-compose exec app composer install для установки пакетов внутри контейнера. Всё будет доступно по адресу docker-machine ip default и 8008 порту
