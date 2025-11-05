# **Module-5 RETAKE**
## **Singer & Album API Documentation**

---

### **retake.jar file ni run qilib tashqi server sifatida foydalaning va unga bog‘lanib quyidagi tasklarni bajaring.**

---

## **1. Singer entity si uchun 1.1-1.5 API lar va 1.6 task ni bajaruvchi menu yarating**

### **Base URL:** `http://localhost:5050/api/singers`

---

### **1.1 POST http://localhost:5050/api/singers**
**Yangi qo‘shiqchi qo‘shish**

**Request Body:**
```json
{
  "name": "Ariana Grande",
  "birthYear": 1993,
  "country": "USA"
}
```

**Response Body (201 Created):**
```json
{
  "id": 1,
  "name": "Ariana Grande",
  "birthYear": 1993,
  "country": "USA"
}
```

---

### **1.2 GET http://localhost:5050/api/singers**
**Barcha qo‘shiqchilarni olish**

**Response Body (200 OK):**
```json
[
  {
    "id": 1,
    "name": "Ariana Grande",
    "birthYear": 1993,
    "country": "USA"
  },
  {
    "id": 2,
    "name": "Ed Sheeran",
    "birthYear": 1991,
    "country": "UK"
  }
]
```

---

### **1.3 GET http://localhost:5050/api/singers/{id}**
**Qo‘shiqchini ID bo‘yicha olish**

**Response Body (200 OK):**
```json
{
  "id": 1,
  "name": "Ariana Grande",
  "birthYear": 1993,
  "country": "USA"
}
```

**Response Body (404 Not Found):**
```json
{
  "error": "Singer not found"
}
```

---

### **1.4 PUT http://localhost:5050/api/singers/{id}**
**Qo‘shiqchini yangilash**

**Request Body:**
```json
{
  "name": "Ed Sheeran",
  "birthYear": 1991,
  "country": "United Kingdom"
}
```

**Response Body (200 OK):**
```json
{
  "id": 2,
  "name": "Ed Sheeran",
  "birthYear": 1991,
  "country": "United Kingdom"
}
```

---

### **1.5 DELETE http://localhost:5050/api/singers/{id}**
**Qo‘shiqchini o‘chirish**

**Response Body (204 No Content):**  
*Hech qanday body qaytmaydi.*

---

### **1.6 Country kesimida singerlarni chiqaruvchi method yarating**
User country ni kiritishi kerak → unga shu davlatdagi barcha qo‘shiqchilar qaytadi.

---

## **2. Album entity si uchun 2.1-2.5 API larni va 2.6 taskni bajaruvchi menu yarating**

### **Base URL:** `http://localhost:5050/api/albums`

---

### **2.1 POST http://localhost:5050/api/albums**
**Yangi albom qo‘shish**

**Request Body:**
```json
{
  "title": "Thank U, Next",
  "releaseYear": 2019,
  "price": 12.99,
  "singerId": 1
}
```

**Response Body (201 Created):**
```json
{
  "id": 1,
  "title": "Thank U, Next",
  "releaseYear": 2019,
  "price": 12.99,
  "singer": {
    "id": 1,
    "name": "Ariana Grande",
    "birthYear": 1993,
    "country": "USA"
  }
}
```

---

### **2.2 GET http://localhost:5050/api/albums**
**Barcha albomlarni olish**

**Response Body (200 OK):**
```json
[
  {
    "id": 1,
    "title": "Thank U, Next",
    "releaseYear": 2019,
    "price": 12.99,
    "singer": {
      "id": 1,
      "name": "Ariana Grande",
      "birthYear": 1993,
      "country": "USA"
    }
  },
  {
    "id": 2,
    "title": "Divide",
    "releaseYear": 2017,
    "price": 10.99,
    "singer": {
      "id": 2,
      "name": "Ed Sheeran",
      "birthYear": 1991,
      "country": "UK"
    }
  }
]
```

---

### **2.3 GET http://localhost:5050/api/albums/{id}**
**ID bo‘yicha albom olish**

**Response Body (200 OK):**
```json
{
  "id": 1,
  "title": "Thank U, Next",
  "releaseYear": 2019,
  "price": 12.99,
  "singer": {
    "id": 1,
    "name": "Ariana Grande",
    "birthYear": 1993,
    "country": "USA"
  }
}
```

**Response Body (404 Not Found):**
```json
{
  "error": "Album not found"
}
```

---

### **2.4 PUT http://localhost:5050/api/albums/{id}**
**Albomni yangilash**

**Request Body:**
```json
{
  "title": "Divide (Deluxe)",
  "releaseYear": 2017,
  "price": 14.99,
  "singerId": 2
}
```

**Response Body (200 OK):**
```json
{
  "id": 2,
  "title": "Divide (Deluxe)",
  "releaseYear": 2017,
  "price": 14.99,
  "singer": {
    "id": 2,
    "name": "Ed Sheeran",
    "birthYear": 1991,
    "country": "UK"
  }
}
```

---

### **2.5 DELETE http://localhost:5050/api/albums/{id}**
**Albomni o‘chirish**

**Response Body (204 No Content):**  
*Hech qanday body qaytmaydi.*

---

### **2.6 Singer kesimida albomlarni chiqaruvchi method yarating**
User singer nomini kiritadi → unga shu qo‘shiqchining barcha albomlari qaytadi.


---

## **Project ni yakunlagandan so‘ng**

> **Bajargan ishingizni GitHub da `module_5_retake_familiya_ism` nomli repositoryga joylang**  
> **Repository URL ni adminlarga topshiring.**

---

**OMAD YOR BO‘LSIN**
