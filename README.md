# mkosterin_microservices
mkosterin microservices repository
## gitlab-ci-1 home work
### Обязательная часть
### Задание со *
## docker-4 home work
### Обязательная часть
- изучена работа драйвером сети docker - none, bridge, host
- при работе с драйвером host важно следить за отсутствием пересечения портов как между контейнерами так и между хостовой машиной
- изучено присвоение DNS имен контейнерам при помощи --name, --network-alias
- изучена возможность работы контейнеров в разных сетях
- изучены настройки сетевого стека хостовой машины 
- установлен docker-compose
- написан docker-compose.yml для приложения
- добавлена настройка docker-compose.yml для работы в нескольких сетях
- часть значений в файле docker-compose.yml параметризована: порт UI, ыерсии севисов, адреса сетей
- параметры записаны в файл .env
- в качестве префикса проекта в docker-compose берется имя рабочей директории. Для изменения можно использовать ключ -P или переменную окружения COMPOSE_PROJECT_NAME
### Задание со *
- создал файл docker-compose.override.yml с подменой волюма (с костыльным копированием на хостовой машине), дебаггингом puma
## docker-3 home work
### Обязательная часть
- установлен linter
- используем docker-machine и gce для экспериментов
- написаны Dockerfile для трех компонентов приложения
- собраны образы, сборка некоторых идет не с первого шага, так как в кеше уже находятсидентичные слои файловой системы
- для работы приложения создали свой бридж
- оптимизированы размеры образов ui, comment за счет использования alpine и оптимизации порядка команд в Dockerfile
- создан и подключен Docker volume для хранения файлов базы данных
### Задание со *
- запустил контейнеры с дургими сетевыми алиасами без модификации Dockerfile, через установку переменных окружения в командной строке
- оптимизирован образ comment

## docker-2 home work
### Обязательная часть
- настроен docker-machine
- создан новые проект в GCE
- сравнен запуск контейнеров с ключом\без ключа --pid host. В первом случае внутри контейнера видно все процессы хостовой машины с реальными pidами. Во втором случае htop выполняется с pid=1
- написан Dockerfile и файлы docker-space
- собран образ
- запущен контейнер с приложением
- настроен брэндмауэр
- пройдена регистрация на docker hub, залит образ mkosterin/otus-reddit:1.0
- образ скачен и запущен в локальном окружении docker. Все работает
- весь код валидирован, проверен линтерами и проч.
### Задание со *
- создана инфраструктура в GCE с параметризованным количеством инстансов
- настроено динамическое инвентори для ansible. Использовался terraform-inventory
- написана роль Docker и другие плей буки для установки и настройки docker и деплоя приложения
- написан плей бук и напсан код для packer, который генерирует образ с установленным docker

## docker-1 home work
### Обязательная часть
- клонирован новый репозиторий;
- настроена интеграция с travis-ci
- настроена интеграция с slack
- установлено окружение: docker-ce, docker-compose, docker-machine
- потренировался с запуском контейнеров, созданием образов
- изучены базовые команды docker CLI
- удалил скачанные\созданные образы и контейнеры
### Задание со *
- проанализировал вывод двух комманд, описал различия в файле docker-1.log

