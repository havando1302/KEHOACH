# 🚀 TaskFlow - Ứng Dụng Quản Lý Kế Hoạch & Công Việc Thông Minh

<p align="center">
  <a href="https://taskflow-kehoach.onrender.com/">
    <img src="https://img.shields.io/badge/Live_Demo-taskflow--kehoach.onrender.com-blue?style=for-the-badge&logo=render&logoColor=white" alt="Live Demo" />
  </a>
  <img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React 19" />
  <img src="https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-v4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS 4" />
</p>

---

## 🌐 Trải Nghiệm Ứng Dụng (Live Demo)

👉 **Đường dẫn ứng dụng:** [https://taskflow-kehoach.onrender.com/](https://taskflow-kehoach.onrender.com/)

---

## 📖 Giới Thiệu Tổng Quan

**TaskFlow** là ứng dụng web Fullstack hiện đại hỗ trợ người dùng lập kế hoạch, theo dõi tiến độ công việc hằng ngày một cách trực quan, mượt mà và khoa học. Ứng dụng được xây dựng theo kiến trúc Monorepo, tối ưu hóa tốc độ tải trang và phản hồi API tức thì.

---

## ✨ Tính Năng Nổi Bật

- 📝 **Quản lý công việc toàn diện (CRUD):** Thêm mới, chỉnh sửa nội dung, đánh dấu hoàn thành hoặc xóa nhiệm vụ nhanh chóng.
- 📅 **Bộ lọc thời gian thông minh:** Xem danh sách công việc theo *Hôm nay (Today)*, *Tuần này (This Week)*, *Tháng này (This Month)* hoặc *Tất cả (All)*.
- 📊 **Thống kê tiến độ trực quan:** Tự động đếm và cập nhật số lượng công việc đang xử lý (*Active*) và công việc đã hoàn thành (*Completed*).
- 📄 **Phân trang tiện lợi (Pagination):** Giúp giao diện gọn gàng, tải mượt mà ngay cả khi có số lượng lớn nhiệm vụ.
- 🎨 **Giao diện người dùng hiện đại (UI/UX):**
  - Tích hợp **Tailwind CSS 4** và bộ component cao cấp **Shadcn UI**.
  - Tương thích 100% trên mọi thiết bị (Responsive: Mobile, Tablet, Desktop).
  - Thông báo hành động tương tác thời gian thực bằng toast notification (**Sonner**).

---

## 🛠️ Công Nghệ Sử Dụng (Tech Stack)

### Frontend
- **Framework & Thư viện:** [React 19](https://react.dev/), [Vite 7](https://vitejs.dev/)
- **Styling:** [Tailwind CSS 4](https://tailwindcss.com/), [Shadcn UI](https://ui.shadcn.com/) (Radix UI)
- **Icons & UI Extras:** [Lucide React](https://lucide.dev/), `tw-animate-css`
- **Networking & Routing:** [Axios](https://axios-http.com/), [React Router](https://reactrouter.com/)
- **Thông báo:** [Sonner](https://sonner.emilkowal.ski/)

### Backend
- **Nền tảng:** [Node.js](https://nodejs.org/) (ES Modules)
- **Framework:** [Express.js](https://expressjs.com/)
- **Cơ sở dữ liệu:** [MongoDB Atlas](https://www.mongodb.com/atlas) (Cloud NoSQL)
- **ODM:** [Mongoose](https://mongoosejs.com/)
- **Công cụ hỗ trợ:** Dotenv, CORS, Nodemon

---

## 📁 Cấu Trúc Dự Án (Project Structure)

```text
KEHOACH/
├── backend/                  # Mã nguồn Server (Node.js & Express)
│   ├── src/
│   │   ├── config/           # Cấu hình kết nối MongoDB
│   │   ├── controllers/      # Bộ điều hướng xử lý logic tác vụ
│   │   ├── models/           # Mongoose Schema (Task model)
│   │   ├── routes/           # RESTful API Endpoints (/api/tasks)
│   │   └── server.js         # Entrypoint server & cấu hình static hosting
│   └── package.json
├── frontend/                 # Mã nguồn Giao diện (React & Vite)
│   ├── src/
│   │   ├── components/       # Các component chức năng (Header, Footer, TaskList, TaskCard...)
│   │   │   └── ui/           # Bộ thành phần giao diện Shadcn UI
│   │   ├── pages/            # Trang chính (HomePage, NotFound)
│   │   └── lib/              # Cấu hình Axios instance & tiện ích
│   └── package.json
├── package.json              # Script gốc điều phối build và start
└── README.md
```

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Cục Bộ (Local Setup)

### 1. Yêu cầu hệ thống
- Đã cài đặt [Node.js](https://nodejs.org/) (phiên bản 18+ trở lên).
- Có tài khoản và chuỗi kết nối [MongoDB Atlas](https://www.mongodb.com/atlas).

### 2. Cài đặt thư viện
Mở terminal tại thư mục gốc của dự án:
```bash
npm install --prefix backend
npm install --prefix frontend
```

### 3. Cấu hình biến môi trường
Tạo file `.env` bên trong thư mục `backend/` (`backend/.env`):
```env
PORT=5001
MONGODB_CONNECTIONSTRING=mongodb+srv://<username>:<password>@cluster0.mongodb.net/taskflow?retryWrites=true&w=majority
```
*(Thay `<username>`, `<password>` bằng thông tin tài khoản MongoDB Atlas của bạn)*.

### 4. Khởi chạy ứng dụng
Mở 2 cửa sổ terminal:

- **Terminal 1 - Khởi chạy Backend:**
  ```bash
  cd backend
  npm run dev
  ```
  *(API chạy tại: `http://localhost:5001`)*

- **Terminal 2 - Khởi chạy Frontend:**
  ```bash
  cd frontend
  npm run dev
  ```
  *(Giao diện chạy tại: `http://localhost:5173`)*

---

## 🚢 Hướng Dẫn Triển Khai (Deployment on Render)

Dự án đã được cấu hình monorepo trọn gói phục vụ cả Backend và Frontend trên **Render**:

1. Đăng nhập vào [Render Dashboard](https://dashboard.render.com/) -> Chọn **New Web Service**.
2. Kết nối tới Repository GitHub: `https://github.com/havando1302/KEHOACH`.
3. Điền các tham số cấu hình:
   - **Environment:** `Node`
   - **Build Command:** `npm run build`
   - **Start Command:** `npm start`
4. Cấu hình biến môi trường (**Environment Variables**):
   - `MONGODB_CONNECTIONSTRING`: Điền chuỗi kết nối MongoDB Atlas của bạn.
   - `NODE_ENV`: `production`
5. Bấm **Deploy Web Service**. Render sẽ tự động build frontend và chạy ứng dụng tại liên kết:  
   👉 **https://taskflow-kehoach.onrender.com/**
---

## 👨‍💻 Tác Giả

- **Hà Văn Đô**
- **GitHub:** [@havando1302](https://github.com/havando1302)
- **Repository:** [https://github.com/havando1302/KEHOACH](https://github.com/havando1302/KEHOACH)

---

