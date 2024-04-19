# 기능 명세
- 방탈출 예약을 관리할 수 있는 웹 애플리케이션의 어드민 페이지를 만든다.
- `/admin` 요청 시 어드민 페이지를 응답한다.
- `/admin/reservation` 요청 시 예약 관리 페이지를 응답한다.
- 어드민은 예약을 추가, 조회, 삭제할 수 있다.

# API 명세
## 예약 조회 API
### Request
```
GET /reservations HTTP/1.1
```

### Response
```
HTTP/1.1 200 
Content-Type: application/json

[
    {
        "id": 1,
        "name": "브라운",
        "date": "2023-01-01",
        "time": "10:00"
    },
    {
        "id": 2,
        "name": "브라운",
        "date": "2023-01-02",
        "time": "11:00"
    }
]
```

## 예약 추가 API
### Request
```
POST /reservations HTTP/1.1
content-type: application/json

{
    "date": "2023-08-05",
    "name": "브라운",
    "time": "15:40"
}
```

### Response
```
HTTP/1.1 200 
Content-Type: application/json

{
    "id": 1,
    "name": "브라운",
    "date": "2023-08-05",
    "time": "15:40"
}
```

## 예약 취소 API
### Request
```
DELETE /reservations/1 HTTP/1.1
```
### Response
```
HTTP/1.1 200
```
