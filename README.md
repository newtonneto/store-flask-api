# STORE FLASK API

## How to build the Dockerfile

```
    docker build -t store-flask-api .
```

## How to run the Dockerfile locally

```
    docker run -dp 5000:5000 -w /app -v "$(pwd):/app" store-flask-api sh -c "flask run --host 0.0.0.0"
```