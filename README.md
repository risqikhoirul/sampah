## /api/register
Endpoint ini digunakan untuk mendaftarkan pengguna baru.

**Request:**
```bash
curl -X POST \
-H "Content-Type: application/x-www-form-urlencoded" \
-d "username=farid&password=123" \
http://localhost:3000/api/register
```

**Response:**
```json
{
  "status": true,
  "message": "User registered successfully"
}
```

## /api/login
Endpoint ini digunakan untuk login pengguna.

**Request:**
```bash
curl -X POST \
-H "Content-Type: application/json" \
-d '{"username":"farid","password":"123"}' \
http://localhost:3000/api/login
```

**Response:**
```json
{
  "status": true,
  "user": {
    "id": 2,
    "username": "farid",
    "password": "123"
  }
}
```

## /api/reportTrash
Endpoint ini digunakan untuk melaporkan sampah.

**Request:**
```bash
curl -X POST \
-F "username=yulfi" \
-F "location=ngumpak" \
-F "type=plastik" \
-F "image=@bah.png" \
http://localhost:3000/api/reportTrash
```

**Response:**
```json
{
  "status": true,
  "message": "Report submitted successfully"
}
```

## /api/reports
Endpoint ini digunakan untuk mendapatkan laporan sampah.

**Request:**
```bash
curl -X GET \
http://localhost:3000/api/reports
```

**Response:**
```json
{
  "status": true,
  "reports": [
    {
      "id": 3,
      "username": "yulfi",
      "location": "ngumpak",
      "type": "plastik",
      "image": "1718200965110-bah.png",
      "created_at": "2024-06-12T14:02:45.000Z"
    },
    {
      "id": 2,
      "username": "yulfi",
      "location": "ngumpak",
      "type": "plastik",
      "image": "1718200775600-bah.png",
      "created_at": "2024-06-12T13:59:35.000Z"
    }
  ]
}
```
