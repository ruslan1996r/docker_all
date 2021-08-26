# Перед тем как запустить эти команды, нужно убедиться, что с помощью docker build создан нужный образ. logsapp:env, logsapp:volumes, etc
# Чтобы воспользоваться, просто нужно написать make stop (make + command). Должен быть установлен make
# Чтобы наш Volume был именован, нужно добавить такую приставку: "logs:". Название + :

run_with_envs:
	docker run -d -p 4200:4200 --env-file ./config/.env --rm --name logsapp logsapp:env
run:
	docker run -d -p 4200:4200 -v logs:/app/data --rm --name logsapp logsapp:volumes
# RUN-DEV сделает папку с проектом VOLUME из-за чего любые изменения теперь будут доступны
# Также node_modules были сделаны в качестве VOLUME (анонимного)
run-dev:
		docker run -d -p 4200:4200 -v "/home/ruslan/Рабочий стол/MyProjects/DockerMinin/logs-app:/app" -v /app/node_modules -v logs:/app/data --rm --name logsapp logsapp:volumes
stop:
	docker stop logsapp

