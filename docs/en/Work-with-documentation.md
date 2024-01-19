### Manual with Python
1. [Install Python and deps for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
2. Activate python virtual env
```bash
source venv/Scripts/activate
```
2. [Previewing as you write](https://squidfunk.github.io/mkdocs-material/creating-your-site/?h=serve#previewing-as-you-write)
```bash
mkdocs serve
```

### Docker [image use](https://hub.docker.com/r/squidfunk/mkdocs-material/)
```bash
docker run --rm -it -p 8000:8000 -v /${PWD}:/docs squidfunk/mkdocs-material
```

and open local MkDocs server: [http://127.0.0.1:8000/ReDeathmatch/](http://127.0.0.1:8000/ReDeathmatch/)

