# MID TERM GABRYELLA APRIANI SINAGA TOKOPEDIA PLAY CLONE

## API Documentation

### 1) GET /video-thumbnails

Mengembalikan semua video thumbnail

- url params (none)
- headers
  - Content-Type: application/json
- success response
  - content
    ```json
    {
    "status": "success",
    "data": {
        "videoThumbnailList": []
    }
    ```

### 2) POST /video-thumbnails
Membuat video thumbnail baru

- url params (none)
- headers
  - Content-Type: application/json
- body
  - content
    ```json
    {
      "urlVideoThumbnail": "test",
      "urlImageThumbnail": "test"
    }
    ```

- success response
  - content
    ```json
    {
    "status": "success",
    "data": {
        "videoThumbnail": {
            "urlVideoThumbnail": "test",
            "urlImageThumbnail": "test",
            "_id": "64c33c5d27368397e4ce1307",
            "__v": 0
        }
    }
    ```
    
### 3) GET /products/{video-id}

Mengembalikan semua product berdasarkan id video thumbnail

- url params 
  - /{video-id}
- headers
  - Content-Type: application/json
- success response
  - content
    ```json
    {
      "status": "success",
      "data": {
          "products": []
      }
    }
    ```

### 4) POST /products/{video-id}
Membuat video produk baru berdasarkan id video thumbnail

- url params
  - /{video-id}
- headers
  - Content-Type: application/json
- body
  - content
    ```json
    {
      "title": "product",
      "price": 100,
      "linkProduct": "product"
    }
    ```
- success response
  - content
    ```json
    {
      "status": "success",
      "data": {
          "product": {
              "title": "product",
              "price": 100,
              "linkProduct": "product",
              "videoThumbnailId": "64c3277268a7ec27e67c554d",
              "_id": "64c33dea27368397e4ce130a",
              "__v": 0
          }
      }
    }
    ```

### 5) GET /comments/{video-id}

Mengembalikan semua comment berdasarkan id video thumbnail

- url params
  - /{video-id}
- headers
  - Content-Type: application/json
- success response
  - content
    ```json
    {
      "status": "success",
      "data": {
          "comments": []
      }
    }
    ```

### 6) POST /comments/{video-id}
Membuat video comment baru berdasarkan id video thumbnail

- url params
  - /{video-id}
- headers
  - Content-Type: application/json
- body
  - content
    ```json
    {
      "username": "username",
      "comment": "lorem ipsum"
    }
    ```
- success response
  - content
    ```json
    {
      "status": "success",
      "data": {
          "comment": {
              "username": "username",
              "comment": "lorem ipsum",
              "timestamp": "2023-07-28T04:05:40.064Z",
              "videoThumbnailId": "64c3277268a7ec27e67c554d",
              "_id": "64c33e9427368397e4ce130d",
              "__v": 0
          }
      }
    }
    ```
