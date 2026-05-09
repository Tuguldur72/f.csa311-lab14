# API Setup

## Сонгосон API

| Талбар | Мэдээлэл |
|--------|----------|
| **API нэр** | JSONPlaceholder |
| **Base URL** | https://jsonplaceholder.typicode.com |
| **Auth** | No Auth (шаардахгүй) |
| **Документац** | https://jsonplaceholder.typicode.com |

## Товч тайлбар

JSONPlaceholder нь хуурамч онлайн REST API бөгөөд бодит back-end сервер шаардахгүйгээр
CRUD үйлдлүүдийг тестлэхэд зориулагдсан нийтэд нээлттэй үйлчилгээ юм.
Энэ лабораторийн ажилд `/posts` endpoint-ийг ашиглан GET, POST, PUT, DELETE болон
Error case тестүүдийг бичлээ.

## Ашигласан Endpoint-үүд

| Endpoint | Тайлбар |
|----------|---------|
| `GET /posts` | Бүх постуудыг авах |
| `GET /posts/:id` | Тодорхой нэг постыг авах |
| `POST /posts` | Шинэ пост үүсгэх |
| `PUT /posts/:id` | Пост шинэчлэх |
| `DELETE /posts/:id` | Пост устгах |
| `GET /posts/:id/comments` | Постын сэтгэгдлүүд |
| `GET /posts?userId=1` | Хэрэглэгчээр шүүх |
| `GET /posts/999999` | Байхгүй пост (404 алдаа) |

## Rate Limit

Байхгүй — JSONPlaceholder нийтэд нээлттэй, хязгааргүй.