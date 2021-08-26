## Commands
* docker ps -a - вывести все контейнеры, даже незапущенные
* docker images - выведет **образы** (на основе которых создаются контейнеры), например, ноды
* docker build -t `name` . - создать образ с конкретным именем
* docker run node - запустить `image`
* docker run -it node - запустит `контейнер`. Можно будет работать с ним в консоли
* docker rm `id` - удалит контейнер по его id. ID можно получить через docker ps
  * docker rm `container_id_1` `container_id_2`... - удалит сразу несколько контейнеров
* docker container prune - удалить все контейнеры
* docker stop `container_id` - остановить контейнер
* docker rmi `image_name_1` `image_name_2` - удалить образы по айди
* docker image prune - удалить все неиспользованные образы
* docker tag `image_name` testdockerid123123jwada/`image_name` - переименовать образ (создаст новый на его основе)

* docker volume rm `volume_name` - удалить выбранный
* docker volume prune - удалить все
* docker volume create `volume_name` - создать новый 

## Make smt
* docker rmi -f $(docker images -a -q) - удалить все images
* docker run -p 3000:3000 2b736f008696 - запустить контейнер на порту 3000(порт машины, который надо использовать):3000(порт контейнера, где будет приложение)
  * -d - при запуске контейнера не откроет его консоль
  * --name `name` - задаст контейнеру какое-то имя. В будущем можно использовать его вместо `container_id`
  * --rm - удали контейнер сразу после того как он будет остановлен
  * -e PORT=4200 - так можно передавать какие-то environments в контейнер. Чтобы передать больше, перед каждой пиши -e
  * --env-file ./config/.env - передаёт место, где лежит .env-файл со всеми переменными