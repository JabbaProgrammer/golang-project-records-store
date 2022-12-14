
# Records store
## Summary
The first step in learning about the Go programming language is to write a simple Go project. This project is a REST API project template that made me understand how to work with Go and Gin framework on the go.

Unfortunately, in this project you will not see the structural distribution of files according to their business logic, since this is the first project on Go and it is more important for me to first understand the mechanisms and learn how to use these tools.

## In a nutshell about the API.
GET /albums - get a list of all albums.
```
# get albums request
curl http://localhost:8080/albums/ 
```
GET /albums/:id - Get an album by index
```
# example: get album by id
curl http://localhost:8080/albums/1
```
POST /albums - add an album to the list
```
curl http://localhost:8080/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "Another brick in the wall","artist": "Pink Floyd","price": 49.99}'
```

## Album structure
ID - identifier
Title - album name
Artist - the name of the artist
Price - album price
### Go album struct  
```
type album struct {
    ID     string  `json:"id"`
    Title  string  `json:"title"`
    Artist string  `json:"artist"`
    Price  float64 `json:"price"`
}
```
