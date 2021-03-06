# mkosterin_microservices
mkosterin microservices repository
## kubernetes-5 homework
### obligatory part
- nginx-ingress has been installed
- prometheus has been installed and configured
- labels, endpoints and metrics have been added
- jobs post-endpoints, comment-endpoints, ui-endpoints have been made
- grafana has been installed
- kubernetes dashboard has been added
- previous dashboards have been added
- template and parameters have been added
- efk/kibana have been installed
## extra part
- 
## kubernetes-4 homework
### obligatory part
- helm has been installed/configured
- Charts structure with templates have been created for post, ui, comment
- helm install/delete/upgrade command have been tried
- requirements, variables, templates have been tried
- \_helpers.tpl mechanism was applied for ui, post, comment services
- requireents.yaml has been written
- helm dep update 
- GKE cluster was updated
- GitLab has been installed/configured
- test repos for ui, comment, post, reddit-deploy have been created and pushed into GitLab
- .gitlab-ci.yml with build, test and release has been implemented
- test environment by button has been implemented
- button for cleanup test environments has been added
- staging and production environments have been created
### extra part
-
## kubernetes-3 homework
### obligatory part
- some tests with kube-dns has been made
- LoadBalancer type has been used
- Ingress and IngressController with L7 have been tried
- SSL cert has been added
- NetworkPolicy has been enabled and tried for separate database from external network
- PersistentVolume has been created and applied for mongo
- PersistentVolumeClaim has been created and applied for mongo
- Dynamic PersistentVolume and StorageClasses have been studied
### extra part
- k8s manifest with Secret object has been written
## kubernetes-2 homework
### obligatory part
- kubectl utility has been installed
- minikube has been installed
- ~/.kube/config was checked
- ui-deployment.yml, post-deployment.yml, comment-deployment.yml, mongo-deployment.yml have been refactored
- \*-service.yml have been written
- ui-service.yml for external access has been written with NodePort option
- minikube dashboard was studied
- the namespace "dev" was created and studied
- the reddit application was started in "dev' namespace
- kubernetes cluster with two worker nodes has been created in GKE
- kubectl has been reconfigured for new cluster in GKE
- the dashboard has been configured in GKE
### extra part
-
## kubernetes-1 homework
### Обязательная часть
- написаны deployments для post, ui, comment, mongo
- пройден Kubernetes the hard way. В ходе работы столкнулся с ограничением триального режима на 4 хоста, поэтому нода воркер была только одна
- прогнал kubectl apply -f по deployments
- удалил кластер
- поместил все созданные файлы в каталог kubernetes/the_hard_way
### Задания со *

## logging-1 homework
### Обязательная часть
- написан код для создания инфраструктуры fluent, elasticsearch, kibana, zipkin
- настроены фильтры в fluentd
- настроен драйвер fluentd в контейнерах микросервисного приложения
- собраны структурированные и не структурированные логи
- подключен zipkin для распределенного трейсинга
###
## monitoring-2 home work
### обязательная часть
- настроен мониторинг docker контейнеров
- установлена-настроена grafana
- настроен сбор метрик с работы приложения и бизнес метрик
- настроен и проверен алертинг в слак
- https://cloud.docker.com/repository/docker/mkosterin/alertmanager
- https://cloud.docker.com/repository/docker/mkosterin/prometheus
- https://cloud.docker.com/repository/docker/mkosterin/post
- https://cloud.docker.com/repository/docker/mkosterin/comment
- https://cloud.docker.com/repository/docker/mkosterin/ui
- https://cloud.docker.com/repository/docker/mkosterin/otus-reddit
### Задания со *
- написан Makefile, который сбоирает образы, загружает их на докерхаб, делает деплой и андеплой
###
## monitoring-1 home work
### обязательная часть
- запущен prometheus
- написан Dockerfile для включения свего конфига в prometheus
- запущено reddit app с prometheus
- подключен node-exporter для сбора метрик с докер-хоста
- dockerhub https://cloud.docker.com/u/mkosterin/repository/docker/mkosterin/prometheus
- dockerhub https://cloud.docker.com/u/mkosterin/repository/docker/mkosterin/post
- dockerhub https://cloud.docker.com/u/mkosterin/repository/docker/mkosterin/comment
- dockerhub https://cloud.docker.com/u/mkosterin/repository/docker/mkosterin/ui
### задание со *
- подключен мониторинг mongodb с помощью xendera/mongodb-exporter
## gitlab-ci-2 home work
### обязательная часть
- настроил определение окружения dev с автовыкатыванием версий кода
- настроил окружение stage, prod с выкатыванием кнопкой
- добавил условия и ограничения на запуск job
- настроил динамическое окружение
### задание со *
- :-(
### задание со **
- :-(
## gitlab-ci-1 home work
### Обязательная часть
- развернул инсталляцию gitlab-ci, используя terraform, ansible, docker-compose
- настроил gitlab-ci
- создал группу/проект/репозиторий
- настроил pipeline
- создал, настроил runner
- попробовал тестирование приложения reddit в pipeline
### Задание со *
- продумал и написал скрипт автодеплоя runners в среде docker. Предусмотрена чистка окружения перед созданием раннеров, а также индивидуальные конфигурационные volume для раннеров
- настроил интеграцию pipeline со slack чатом, канал для проверки: https://devops-team-otus.slack.com/messages/CDC5R0RJ9
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

