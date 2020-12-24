# Лабораторная работа 6 по Highload

## Установка и запуск
```bash
git clone https://github.com/assisken/highload-hw-6.git
cd highload-hw-6
docker ps -a | tr -s ' ' | tail -n +2 | cut -d' ' -f1 | xargs docker rm --force
docker-compose up
```

[Ссылка на графану](http://localhost:3000/d/ijTVtdxGk/app-dashboard)

Пользователь: `user`

Пароль: `qwerty`

## Как насрать запросами
```bash
for i in $(seq 1 100); do
    curl "http://127.0.0.1:80/v1/forecast/?city=Moscow&dt=2020-12-23T18:00:00Z"
done
```
