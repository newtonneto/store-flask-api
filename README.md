# STORE FLASK API

## How to build the Dockerfile

```
    docker build -t store-flask-api .
```

## How to run the Dockerfile locally

```
    docker run -dp 5000:5000 -w /app -v "$(pwd):/app" store-flask-api sh -c "flask run --host 0.0.0.0"
```

## How to build the Dockerfile [With Redis]

```
    docker build -t store-flask-email-queue .
```

## How to run the Dockerfile locally [With Redis]

```
    docker run -w /app store-flask-email-queue sh -c "rq worker -u rediss://red-cg18ou7dvk4ronss1fu0:wUvdmRAqpn23rASihnFqRF5KWHcBwTTe@ohio-redis.render.com:6379 emails"
```

- on another terminal:

```
    docker run -p 5005:80 store-flask-email-queue
```

