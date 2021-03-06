# Kibana-Grafana-QlikView

# Kibana
Поскольку Kibana работает только как часть стека ELK, кроме самой Kibana необходимо скачать также Elasticsearch и Logstash. Для этого (если вы пользуетесь ОС Windows) нужно скачать .zip-файлы с соответствующими программами с сайта Elastic:

https://www.elastic.co/downloads/elasticsearch

https://www.elastic.co/downloads/logstash

https://www.elastic.co/downloads/kibana

и распаковать их.

Далее нужно выполнить следующие действия:

1. В папке elasticsearch\bin запустить файл elasticsearch.bat

2. В PowerShell выполнить команду curl http://localhost:9200/ или Invoke-RestMethod http://localhost:9200

3. В папке logstash\bin создать файл logstash.conf и выполнить команду logstash -f logstash.conf

4. В файле настроек kibana.yml указать порт elasticsearch (по умолчанию 9200)

5. В папке kibana\bin запустить файл kibana.bat

После этого Kibana можно открыть в браузере по адресу https://localhost:5601/

Другой вариант - воспользоваться Docker. Для этого нужно ввести следующие команды в командную строку:

docker pull docker.elastic.co/elasticsearch/elasticsearch:7.9.2

docker pull docker.elastic.co/logstash/logstash:7.9.2

docker pull docker.elastic.co/kibana/kibana:7.9.2

# Grafana
Для того, чтобы установить программу Grafana, необходимо скачать программу установки с официального сайта. Для этого нужно перейти по адресу https://grafana.com/grafana/download и выбрать подходящую платформу. Для Windows можно либо скачать сам инсталлятор, либо .zip-файл с файлами программы.

После завершения установки можно изменить порт, используемый Grafana (по умолчанию 3000), а также внести другие изменения в настройки программы. Для этого необходимо в папке программы найти файл sample.ini, скопировать его под именем custom.ini, а затем отредактировать полученный файл.
После этого можно запустить Grafana. Проверить, работает ли программа, можно в приложении "Службы" Windows.

Если вы оставили порт по умолчанию, то для работы с Grafana нужно ввести в браузер адрес http://localhost:3000/ Здесь можно подключать источники данных, создавать и настраивать дашборды и уведомления, подключать плагины и т.д.

Также Grafana можно установить с помощью Docker:

docker run -d -p 3000:3000 grafana/grafana - последняя версия

docker run -d -p 3000:3000 --name grafana grafana/grafana:<version number> - самостоятельный выбор версии

# QlikView
Для установки QlikView необходимо зарегистрироваться на сайте https://www.qlik.com/us/

Сама ссылка на программу QlikView находится по адресу https://us-b.demo.qlik.com/download/

QlikView поддерживает только ОС Windows, вариант установки один - скачать инсталлятор. После установки программы её можно запустить, как и любую другую, через .exe-файл.
