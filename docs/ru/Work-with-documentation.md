### Руководство с использованием Python
1. [Установите Python и зависимости для MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
2. Активируйте виртуальное окружение Python

    ```bash
    source venv/Scripts/activate
    ```

3. [Предварительный просмотр при написании](https://squidfunk.github.io/mkdocs-material/creating-your-site/?h=serve#previewing-as-you-write)

    ```bash
    mkdocs serve
    ```

### или используйте Docker [образ](https://hub.docker.com/r/squidfunk/mkdocs-material/)

```bash
docker run --rm -it -p 8000:8000 -v /${PWD}:/docs squidfunk/mkdocs-material
```

Теперь вы можете открыть локальный сервер MkDocs: http://127.0.0.1:8000/