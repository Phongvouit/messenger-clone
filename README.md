# 💬 Real-time Chat App

## 📌 Mô tả dự án
Ứng dụng chat real-time cho phép người dùng đăng ký, đăng nhập, trò chuyện 1-1 hoặc theo nhóm.

---

## ⚙️ Công nghệ
- **Next.js (App Router)** → frontend + backend routes  
- **Prisma ORM** → quản lý database schema  
- **MongoDB** → lưu user, conversation, message  
- **NextAuth** → xác thực người dùng  
- **Pusher** → realtime messaging (publish/subscribe events)  
- **Tailwind CSS + Shadcn UI** → UI  

---

## 🏗️ Chức năng chính

### 🔑 Authentication
- Đăng ký/đăng nhập (NextAuth + Prisma)  
- Quản lý session người dùng  

### 💬 Chat 1-1 & Chat nhóm
- Tạo conversation mới (có thể là **private** hoặc **group**)  
- Gửi/nhận tin nhắn **real-time** qua Pusher  

### ⚡ Realtime messaging
Mỗi khi gửi tin nhắn, API sẽ:  
1. Lưu tin nhắn vào **MongoDB** (qua Prisma)  
2. Gửi sự kiện **Pusher (`pusher.trigger`)** đến channel của conversation  
3. Client đang subscribe channel sẽ nhận tin nhắn mới ngay lập tức  

### 🎨 UI/UX
- **Sidebar**: danh sách conversation  
- **Chat panel**: hiển thị message stream, realtime update  
- **Input box**: gõ & gửi tin nhắn  

---


