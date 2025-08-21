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
- **Cloudinary** → lưu trữ ảnh  
- **Tailwind CSS** → UI  

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

### 🖼️ Upload ảnh (Image Attachments)
- Chọn file để upload ảnh trước khi gửi
- Ảnh được tải lên Cloudinary, lưu metadata (URL, kích thước, dung lượng, định dạng) vào DB
- Tin nhắn có thể gồm text + ảnh hoặc chỉ ảnh
- Giới hạn mặc định: JPG/PNG/WebP, tối đa ~5MB/ảnh (có thể chỉnh)
- Hiển thị thumbnail trong khung chat, bấm để phóng to (lightbox)

### 🎨 UI/UX
- **Sidebar**: danh sách conversation  
- **Chat panel**: hiển thị message stream, realtime update  
- **Input box**: gõ & gửi tin nhắn  

---


