### Ссылка на информацию
- https://vladilen.notion.site/Docker-2021-a72201ec8573461c8a2e62e2fcf33aa3

### DockerHub
- email - rusliksemp@gmail.com
- username - testdockerid123123jwada
- dockerId - testdockerid123123jwada

- docker push `image_name`- запушит в докерхаб
  - `image_name`:lates - тег опционален
  - docker tag `image_name` testdockerid123123jwada/`image_name` - переименовать образ
  - после этого можно пушить. Потому что без dockerId в названии докерхаба запушить не выйдет

### Info
- `Volumes`. Допустим, мы сохраняем какие-то данные в базу, которая находится в контейнере. Если контейнер снести, все данные будут утеряны.
Если немного упростить, то `Docker volume` — это просто папка хоста, примонтированная к файловой системе контейнера. Так как технически она больше не принадлежит контейнеру, то последний можно смело удалять, пересоздавать заново, снова прикручивать к нему хостовые папки, и ничего с данными внутри не случится.