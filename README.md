---

# 📘 คู่มือติดตั้งและใช้งานโปรเจกต์ Term Project (แบบละเอียด)

---

## 🧩 สารบัญ

1. [ติดตั้งโปรแกรมที่จำเป็น](#1-ติดตั้งโปรแกรมที่จำเป็น)
2. [การติดตั้ง Frontend (React)](#2-การติดตั้ง-frontend-react)
3. [การติดตั้ง Backend (Node.js/Express)](#3-การติดตั้ง-backend-nodejsexpress)
4. [การติดตั้งระบบ Machine Learning (Python)](#4-การติดตั้งระบบ-machine-learning-python)
5. [การติดตั้งฐานข้อมูล (MySQL)](#5-การติดตั้งฐานข้อมูล-mysql)
6. [ทดสอบการทำงาน](#6-ทดสอบการทำงาน)

---

## 🔧 1. ติดตั้งโปรแกรมที่จำเป็น

### ✅ Node.js และ npm

1. ดาวน์โหลด Node.js จาก [https://nodejs.org/](https://nodejs.org/) (แนะนำเวอร์ชัน LTS)
2. เมื่อติดตั้งเสร็จแล้ว ตรวจสอบด้วยคำสั่ง:

```bash
node -v
npm -v
```

### ✅ Yarn

1. ติดตั้ง Yarn ผ่าน npm:

```bash
npm install -g yarn
```

2. ตรวจสอบเวอร์ชัน:

```bash
yarn -v
```

---

### ✅ Python 3.10

1. ดาวน์โหลดได้จาก [https://www.python.org/downloads/release/python-3100/](https://www.python.org/downloads/release/python-3100/)
2. ระหว่างติดตั้ง ให้ติ๊ก ✅ “Add Python to PATH”
3. ตรวจสอบเวอร์ชัน:

```bash
python --version
```

> 🔁 หาก `python` ยังไม่ใช่ 3.10 ให้ลองใช้ `python3.10`

---

### ✅ XAMPP (MySQL + phpMyAdmin)

1. ดาวน์โหลด XAMPP จาก [https://www.apachefriends.org/index.html](https://www.apachefriends.org/index.html)
2. ติดตั้งให้เรียบร้อย แล้วเปิดโปรแกรม
3. กด Start ที่ **MySQL**

---

## 🖥️ 2. การติดตั้ง Frontend (React)

1. เปิดเทอร์มินัล หรือ CMD
2. เข้าไปยังโฟลเดอร์โปรเจกต์ frontend:

```bash
cd path/to/project/frontend
```

3. ติดตั้ง dependencies ด้วย yarn:

```bash
yarn install
```

4. เริ่มรันโปรเจกต์:

```bash
yarn dev
```

> 🔗 ระบบจะรันที่ [http://localhost:5173](http://localhost:5173)

---

## 🛠️ 3. การติดตั้ง Backend (Node.js/Express)

1. เปิดเทอร์มินัลใหม่
2. เข้าโฟลเดอร์ `backend`:

```bash
cd path/to/project/backend
```

3. ติดตั้ง dependencies:

```bash
yarn install
```

4. รัน backend:

```bash
yarn dev
```

> 🔗 ปกติ backend จะรันที่ [http://localhost\:8888](http://localhost:8888) แล้วแต่ที่กำหนดไว้ในโปรเจกต์

---

## 🤖 4. การติดตั้งระบบ Machine Learning (Python)

1. เปิดเทอร์มินัล
2. เข้าไปที่โฟลเดอร์ `ml` (หรือชื่อโฟลเดอร์ machine learning):

```bash
cd path/to/project/ml
```

3. สร้าง Virtual Environment ด้วย Python 3.10: (หากมี venv ลบอันเก่าออกก่อน)

```bash
python3.10 -m venv venv
```

4. เปิดใช้งาน virtual environment:

   * Windows:

     ```bash
     venv\Scripts\activate
     ```

5. ติดตั้งไลบรารีจาก `requirements.txt`:

```bash
pip install -r requirements.txt
```

6. รันแอป ML:

```bash
python app.py
```

> 🔗 API ของ ML จะรันที่ [http://localhost:8877](http://localhost:8877) หรือพอร์ตอื่นตามโค้ด

---

## 🗃️ 5. การติดตั้งฐานข้อมูล (MySQL)

### 1. สร้างฐานข้อมูลใหม่ชื่อ `termproject`

1. เปิด `XAMPP Control Panel`
2. Start `MySQL`
3. เปิดเบราว์เซอร์ไปที่ [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
4. กด “ฐานข้อมูล” ➜ ตั้งชื่อว่า `termproject` ➜ กด “สร้าง”

---

### 2. นำเข้าไฟล์ `.sql`

1. คลิกที่ฐานข้อมูล `termproject`
2. ไปที่แท็บ **นำเข้า (Import)**
3. เลือกไฟล์ `.sql` ที่อยู่ในโฟลเดอร์ `database` แล้วกด "ดำเนินการ"

---

## ✅ 6. ทดสอบการทำงาน

### 🔎 ตรวจสอบว่าแต่ละระบบทำงานแล้ว:

| ส่วน        | URL                                                        | คำอธิบาย                     |
| ----------- | ---------------------------------------------------------- | ---------------------------- |
| Frontend    | [http://localhost:5173](http://localhost:5173)             | เว็บไซต์หลัก                 |
| Backend API | [http://localhost\:8888](http://localhost:8888)            | REST API                     |
| ML API      | [http://localhost:8877](http://localhost:8877)             | ทำนายผล (เช่น POST /predict) |
| phpMyAdmin  | [http://localhost/phpmyadmin](http://localhost/phpmyadmin) | ตรวจสอบฐานข้อมูล             |

---
