# web-service-gin

## Overview
- Simple RESTful web service with Go and Gin Web Framework (Gin).
    - https://golang.org/doc/tutorial/web-service-gin

## How to run the code
### 1. Return all items
1. Run the code
```
$ go run .
```

2. Make a request to this running web service
```
$ curl http://localhost:8080/albums
```

### 2. Add a new item
1. Run the code
```
$ go run .
```

2. From a different command line window, use curl to make a request to this running web service.
```
$ curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
```

3. As in the previous section, use curl to retrieve the full list of albums, which you can use to confirm that the new album was added.
```
$ curl http://localhost:8080/albums \
    --header "Content-Type: application/json" \
    --request "GET"
```

### 3. Return a specific item
1. Run the code
```
$ go run .
```

2. From a different command line window, use curl to make a request to this running web service.
```
$ curl http://localhost:8080/albums/2
```