# Food Retail Backend

Backend API cho ứng dụng Food Retail sử dụng Node.js, Express, MySQL và Docker.

## 📋 Yêu cầu

- Docker >= 20.x
- Docker Compose >= 1.29.x

## 🚀 Cài đặt

### 1. Clone và di chuyển vào thư mục

```bash
git clone https://github.com/tnphat203/food-retail-project.git
cd food-retail-project/backend
```

### 2. Tạo file `.env`

```env
# Node.js app
PORT=10000
NODE_ENV=development

# Database connection
DB_HOST=food_retail_db
DB_PORT=3306
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_NAME=your_database_name

# MySQL container
MYSQL_ROOT_PASSWORD=your_root_password
MYSQL_DATABASE=your_database_name
MYSQL_USER=your_db_user
MYSQL_PASSWORD=your_db_password
```

> ⚠️ **Lưu ý:** Thay đổi các giá trị `your_*` thành thông tin thực tế của bạn

### 3. Chạy ứng dụng

```bash
docker-compose up -d --force-recreate
```

Ứng dụng chạy tại: http://localhost:10000

## 🐳 Lệnh Docker

```bash
# Xem log
docker-compose logs -f

# Dừng container
docker-compose down

# Rebuild và chạy lại
docker-compose up -d --build --force-recreate

# Truy cập container
docker exec -it food_retail_app /bin/bash

# Truy cập MySQL
docker exec -it food_retail_db mysql -u user -ppass123 food_retail
```

## 📁 Cấu trúc

```
backend/
├── src/
│   ├── config/         # Database, environment config
│   ├── controllers/    # Request handlers
│   ├── models/         # Sequelize models
│   ├── routes/         # API routes
│   └── services/       # Business logic
├── docker-compose.yml
├── Dockerfile
└── package.json
```

## 📞 Liên hệ

**Trần Ngọc Phát** - tnphat203@gmail.com

---

MIT License
