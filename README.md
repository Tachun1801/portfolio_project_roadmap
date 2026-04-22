# portfolio_project_roadmap
## Giai đoạn 1: Thiết kế & Chuẩn bị Hạ tầng (Tuần 1-2)
*Mục tiêu: Định hình sản phẩm và thiết lập môi trường DevOps.*

- [ ] **Thiết kế UI/UX (Figma):**
    - Chọn 1 Template Portfolio tối giản trên Figma Community.
    - Vẽ 3 màn hình chính: Landing Page, Project Detail, Admin Dashboard.
    - Xác định các màu sắc chủ đạo (Brand Identity).
- [ ] **Môi trường Phát triển (Fedora):**
    - Cài đặt Docker để chạy MySQL local trong quá trình code.
    - Cấu hình Alias trong Bash/Zsh để thao tác Git nhanh hơn.
    - Thiết lập Project Spring Boot đầu tiên (Spring Initializr).
- [ ] **Khởi tạo Database (Aiven):**
    - Đăng ký tài khoản Aiven MySQL miễn phí.
    - Tạo bảng `profiles`, `projects`, `skills` (theo thiết kế đã thảo luận).

## Giai đoạn 2: Phát triển Frontend - Giao diện người dùng (Tuần 3-5)
*Mục tiêu: Biến bản vẽ Figma thành mã nguồn React.*

- [ ] **Nền tảng React:**
    - Khởi tạo project với Vite (nhanh và nhẹ hơn CRA).
    - Cài đặt Tailwind CSS để thiết kế giao diện nhanh.
- [ ] **Xây dựng Components:**
    - `Navbar`, `HeroSection`, `ProjectCard`, `SkillIcon`.
    - `ContactForm`: Xây dựng form validation cơ bản.
- [ ] **Quản lý dữ liệu:**
    - Sử dụng `useState` và `useEffect` để hiển thị dữ liệu giả (Mock Data).
    - Tích hợp AOS (Animate On Scroll) cho hiệu ứng chuyển động mượt mà.

## Giai đoạn 3: Phát triển Backend - Bộ não hệ thống (Tuần 6-8)
*Mục tiêu: Xây dựng RESTful API và quản lý dữ liệu thực.*

- [ ] **Cấu trúc Spring Boot:**
    - Thiết lập kết nối MySQL JPA.
    - Tạo các Entity, Repository và Service cho `Project` và `Profile`.
- [ ] **API Endpoints:**
    - `GET /api/projects`: Trả về danh sách dự án cho người ngoài xem.
    - `POST /api/contact`: Nhận dữ liệu từ form liên hệ.
- [ ] **Bảo mật (Spring Security):**
    - Cấu hình login đơn giản cho trang Admin.
    - Chặn các phương thức `POST/PUT/DELETE` đối với người dùng không có quyền.
- [ ] **Tích hợp Cloudinary:**
    - Viết Service upload ảnh từ Admin Dashboard lên Cloudinary.

## Giai đoạn 4: Tích hợp AI & Tính năng nâng cao (Tuần 9-10)
*Mục tiêu: Đưa "linh hồn" vào Portfolio.*

- [ ] **Telegram Bot Integration:**
    - Tạo bot với @BotFather.
    - Viết logic trong Spring Boot để tự động đẩy tin nhắn về điện thoại khi có người gửi form liên hệ.
- [ ] **AI Assistant (Gemini/OpenAI API):**
    - Viết System Prompt chuyên sâu về thông tin của Trung.
    - Tạo khung chat (hoặc Character) ở Frontend để tương tác với người dùng.
    - Xây dựng cơ chế RAG đơn giản: Backend đọc dữ liệu từ DB nạp vào context của AI.

## Giai đoạn 5: DevOps & Triển khai (Tuần 11-12)
*Mục tiêu: Đưa sản phẩm lên Internet và tối ưu hóa.*

- [ ] **Deploy Backend (Render):**
    - Dockerize ứng dụng (nếu cần) hoặc deploy trực tiếp từ GitHub.
    - Cấu hình Environment Variables (DB_URL, API_KEY...).
- [ ] **Deploy Frontend (Vercel):**
    - Kết nối GitHub, cấu hình build command.
    - Trỏ link API về server Render.
- [ ] **Tối ưu hóa (Monitoring):**
    - Cấu hình Cron-job để giữ cho Render luôn "thức".
    - Kiểm tra tốc độ load trang (Lighthouse score).

---

## Ghi chú Quan trọng cho Trung
1. **Học theo kiểu "Lego":** Đừng cố hiểu hết 100% code ngay lập tức. Hãy lắp ghép cho nó chạy được, sau đó mới soi kỹ từng dòng.
2. **Git thường xuyên:** Mỗi khi xong 1 tính năng nhỏ, hãy `git commit`. Đây là thói quen sống còn của dân Backend.
3. **Bảo mật:** Tuyệt đối không đẩy file `.env` chứa API Key của AI hay Telegram lên GitHub.
