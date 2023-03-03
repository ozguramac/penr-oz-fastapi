# penr-oz-fastapi
In this example, we create a new instance of the FastAPI class, and define two endpoint functions using the @app.get() decorator.

The first function, read_root(), handles GET requests to the root URL ("/"), and simply returns a dictionary with a "Hello" key and "World" value.

The second function, read_item(item_id: int, q: str = None), handles GET requests to a URL with an integer item_id parameter (e.g. "/items/42"), and an optional string q parameter. It returns a dictionary with the item_id and q values.

## run
```shell
$ uvicorn main:app --reload
```

## test
```
$ curl http://localhost:8000/
{"Hello": "World"}

$ curl http://localhost:8000/items/42?q=testing
{"item_id": 42, "q": "testing"}
```
