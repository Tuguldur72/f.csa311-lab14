# f.csa311-lab14 — API Testing with Postman & Newman

F.CSM311 Программ хангамжийн бүтээлт — Integration & API Testing

## Ашигласан технологи

- **API:** JSONPlaceholder (`https://jsonplaceholder.typicode.com`)
- **Тест хэрэгсэл:** Postman, Newman
- **CI/CD:** GitHub Actions

## Шаардлага

Node.js 18+ суулгасан байх шаардлагатай.

```bash
node --version   # v18 буюу түүнээс дээш байх ёстой
```

## Суулгах

```bash
# Newman болон HTML тайлангийн нэмэлтийг суулгах
npm install -g newman newman-reporter-htmlextra
```

## Тестийг ажиллуулах

```bash
# Энгийн ажиллуулах (CLI тайлан)
newman run postman/collection.json -e postman/env.dev.json

# HTML тайлантай ажиллуулах
newman run postman/collection.json \
  -e postman/env.dev.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export reports/api.html
```

Тест дууссаны дараа `reports/api.html` файлыг хөтөч дээрээ нээж тайланг харна уу.

## Repository бүтэц

```
bie-daalt-14/
├── .github/workflows/api-tests.yml  # CI/CD тохиргоо
├── partA/
│   ├── SETUP.md                     # API сонголтын тайлбар
│   └── screenshot.png               # Эхний амжилттай request
├── postman/
│   ├── collection.json              # 8 request, 15+ тест
│   ├── env.dev.json                 # Локал орчин
│   └── env.ci.json                  # CI орчин
├── reports/
│   └── api.html                     # Newman HTML тайлан
├── README.md
└── REFLECTION.md
```

## CI/CD

GitHub дээр кодоо push хийхэд Actions tab-д автоматаар тестүүд ажиллана.
Ногоон дугуй тэмдэг = бүх тест амжилттай.