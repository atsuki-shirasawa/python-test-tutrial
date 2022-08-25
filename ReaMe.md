# python-test-tutrial

## Package and Tools

### Web API

- Web framework: [FastAPI](https://fastapi.tiangolo.com/ja/)
- Web Server: [Uvicorn](https://www.uvicorn.org/)
- Data validation: [pydantic](https://pydantic-docs.helpmanual.io/)

### Development

- Python package management: [poetry](https://python-poetry.org/)
- Test framework: [pytest](https://docs.pytest.org/en/)
- Formatter: [black](https://black.readthedocs.io/en/stable/), [isort](https://pycqa.github.io/isort/)
- Linter: [flake8](https://flake8.pycqa.org/en/latest/), [pydocstyle](https://www.pydocstyle.org/en/stable/)
- Test automation: [tox](https://tox.wiki/en/latest/)

## Install

```shell
$ poetry install
```

## Run Web API

### local

```shell
$ poetry run uvicorn src.main:app --host 0.0.0.0 --port 3000
```

## Request API

### Request Command

```shell
$ curl -X 'POST' \
  'http://0.0.0.0:3000/tax_price' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "name": "beer",
  "price": 200,
  "is_reduce_tax": false
}'
```

### Result

```shell
{"price_with_tax":220}
```

## Web API documentation

### Swagger UI

```shell
http://0.0.0.0:3000/docs
```

## Run Tests and Linter

```shell
$ poetry run tox
```
