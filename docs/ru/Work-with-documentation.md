### Работа с использованием Python
1. [Установка Python и зависимостей для MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
2. Активируйте Python виртуальное окружение
```bash
source venv/Scripts/activate
```
3. [Предварительный просмотр при написании](https://squidfunk.github.io/mkdocs-material/creating-your-site/?h=serve#previewing-as-you-write)
```bash
mkdocs serve
```

### Использование Docker-образа [image use](https://hub.docker.com/r/squidfunk/mkdocs-material/)
```bash
docker run --rm -it -p 8000:8000 -v /${PWD}:/docs squidfunk/mkdocs-material
```

и откройте локальный сервер MkDocs: [http://127.0.0.1:8000/ReDeathmatch/](http://127.0.0.1:8000/ReDeathmatch/)