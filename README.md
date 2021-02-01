# mssc-beer-service

## Curls

GET

```bash
curl -v 'http://localhost:8080/api/v1/beer/188cdbcc-c0b4-49ce-bc7b-398d28684e8b'
```

POST

```bash
curl --location --request POST 'localhost:8080/api/v1/beer' \
--header 'Content-Type: application/json' \
--data-raw '{
    "beerName": "White Pale Ale",
    "beerStyle": "PALE_ALE",
    "price": "12.79",
    "upc": "123"
}'
```

```bash
curl -v --request POST 'localhost:8080/api/v1/beer' --header 'Content-Type: application/json' --data-raw '{"beerName": "White Pale Ale","beerStyle": "PALE_ALE","price":"12.79","upc": "123"}'

Note: Unnecessary use of -X or --request, POST is already inferred.
*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
> POST /api/v1/beer HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.64.1
> Accept: */*
> Content-Type: application/json
> Content-Length: 79
> 
* upload completely sent off: 79 out of 79 bytes
< HTTP/1.1 201 
< Content-Length: 0
< Date: Mon, 01 Feb 2021 13:25:31 GMT
< 
* Connection #0 to host localhost left intact
* Closing connection 0
```

```bash
curl --request POST 'localhost:8080/api/v1/beer' --header 'Content-Type: application/json' --data-raw '{"beerName": "Berliner Weisse","beerStyle": "Weisse","upc": "123"}'
```

PUT

```bash
curl --location --request PUT 'localhost:8080/api/v1/beer/188cdbcc-c0b4-49ce-bc7b-398d28684e8b' \
--header 'Content-Type: application/json' \
--data-raw '{
    "beerName": "White Pale Ale",
    "beerStyle": "PALE_ALE",
    "price": "12.79",
    "upc": "123"
}'


```bash
curl -v --request PUT 'http://localhost:8080/api/v1/beer/188cdbcc-c0b4-49ce-bc7b-398d28684e8b' --header 'Content-Type: application/json' --data-raw '{"beerName": "White Pale Ale","beerStyle": "PALE_ALE","price":"12.79","upc": "123"}'
```



