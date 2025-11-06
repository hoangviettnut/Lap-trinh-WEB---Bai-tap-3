# LẬP TRÌNH WEB BÀI TẬP 3
# SINH VIÊN: LƯƠNG HOÀNG VIỆT - MSSV:K225480106073
## 1. Cài đặt môi trường linux
### a) Cài đặt WSL: <img width="1103" height="639" alt="image" src="https://github.com/user-attachments/assets/e6700709-ca99-4719-bf06-efbd7c6fbd6d" /><br>
### b) Cài đặt Ubuntu: <img width="1483" height="762" alt="image" src="https://github.com/user-attachments/assets/8190f6af-bde3-4cbf-9e60-508da9eb0ef7" /><br>
## 2. Cài đặt Docker Desktop
Cài đặt Docker Desktop: <img width="1588" height="900" alt="image" src="https://github.com/user-attachments/assets/6ad3ec2e-94ae-4178-99c8-3c6b789227db" /><br>
## 3. Cài đặt Docker Container, sử dụng docker-compose.yml<br>
<img width="1483" height="762" alt="image" src="https://github.com/user-attachments/assets/f2c10364-052a-41ab-bd9d-0b4949df805f" /><br>
Nhớ Enable integration with additional distros Ubuntu 24-04: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/0dd4b871-3e89-47bb-af81-b357a6d3b233" /><br>
## 4. Tạo Web IoT
### a) Giao diện FE ban đầu (Tại phần này đã đăng nhập được với mật khẩu plain text, mã hóa bằng BASE64 rồi so sánh với DB): <img width="1915" height="1035" alt="image" src="https://github.com/user-attachments/assets/343f64b0-5664-476d-86cf-8f283f24210a" /> <br>
### b) Tạo CSDL ban đầu trên mariadb: <img width="1353" height="480" alt="image" src="https://github.com/user-attachments/assets/070eab90-ba4e-46b1-b5c7-5411781344d6" /><br>
### c) Kết InfluxDB để nhận nhiệt độ, cường độ ánh sáng: <img width="558" height="101" alt="image" src="https://github.com/user-attachments/assets/6a4393a9-85b5-4688-bdac-816c6cc44e82" /><br>
Lúc này các dữ liệu ảo được sinh ra sẽ lưu vào trong InfluxDB.
InfluxDb 1.8 ko có giao diện nên ko thể truy cập từ Localhost
### d) Tạo Flow dùng để kiểm tra kết quả đã được nhận hay chưa: <img width="1629" height="236" alt="image" src="https://github.com/user-attachments/assets/ec375913-6c21-427c-b5f0-014581acd608" /><br>
Khi truy cập: http://localhost:1880/api/latest nếu đúng sẽ nhận được dữ liệu trả về(nếu có thì là đúng): <img width="1916" height="1078" alt="image" src="https://github.com/user-attachments/assets/c46d88db-65a6-4feb-b638-644a08002aea"/> <br>
### e) Dùng Grafana kết nối với InfluxDB: <br>
Nhập URL:
<img width="1919" height="1085" alt="image" src="https://github.com/user-attachments/assets/adad27c1-5ae7-4add-9d4e-89c255195d9d" /><br>
Nhập DB và user kèm Password, sau đó Save & test:
<img width="1473" height="875" alt="image" src="https://github.com/user-attachments/assets/3f8a3232-9701-4a53-a09e-4c5e763c657c" /><br>
Hiển thị nhiệt độ: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/d7fe644c-bd81-4e8d-bd35-dc8bd0fb7efc" /><br>
Hiển thị cường độ ánh sáng: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/8eadb07b-7e1e-4603-b0f8-4bdddb50e634" /><br>
Nhiệt độ hiển thị theo dạng biểu đồ: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/a803a236-7469-4bd9-94a8-cb8dd90c0990" /><br>
Ánh sáng hiển thị theo dạng biểu đồ: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/67c82d8f-cc2f-4446-802f-a5848bcd88a1" /><br>
## 5. Cấu hình nginx:
### Phải tắt tường lửa để tiện cấu hình
### a) Cấu hình file nginx và host để thêm luonghoangviet.com và đăng nhập: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/d4dc0490-7e88-47ba-aab8-3cb7ec28532f" /><br>
### b) Cấu hình nginx để http://luonghoangviet.com/nodered truy cập vào nodered qua cổng 80: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/426864b1-c829-4d73-b5fa-3461a8807ae7" /><br>
### c) Cấu hình nginx để http://luonghoangviet.com/grafana truy cập vào grafana qua cổng 80: <img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/514338c1-e364-4f53-965c-c4a91d88050c" /><br>
# TOÀN BỘ DB VÀ SOURCE CODE ĐƯỢC UPLOAD KÈM THEO GITHUB (BAO GỒM FILE CẤU HÌNH)<br>
## 6. Giải thích các công cụ sử dụng trong bài<br>
a) MariaDB: Hệ quản trị cơ sở dữ liệu quan hệ (Relational Database Management System - RDBMS).<br>
b) phpMyAdminL: Công cụ quản trị cơ sở dữ liệu qua giao diện web.<br>
c) Node-RED: Công cụ lập trình trực quan (Visual Programming Tool) dựa trên luồng (flow-based). Thường dùng làm BE<br>
d) InfluxDB: Cơ sở dữ liệu chuỗi thời gian (Time-Series Database - TSDB).<br>
e) Grafana: Công cụ trực quan hóa (Visualization) và giám sát.<br>
f) Nginx: Máy chủ web và Proxy ngược (Reverse Proxy).<br>
# KẾT LUẬN: ĐÂY LÀ BÀI TOÁN SỬ DỤNG NODERED LÀM BACKEND KẾT NỐI VỚI DATABASE RỒI DÙNG FRONTEND ĐỂ THỰC HIỆN CÁC YÊU CẦU, FE LÀM NHIỆM VỤ MÃ HÓA PLAIN TEXT RỒI GỬI VỀ NODERED, NODERED SO SÁNH HASHPASSWORD VỚI DB VÀ TRẢ VỀ KẾT QUẢ. GRANFANA ĐỌC DỮ LIỆU ĐƯỢC LƯU TRONG INFLUXDB RỒI XUẤT RA DƯỚI DẠNG CÁC BIỂU ĐỒ TÙY CHỈNH => DỄ ÁM SÁT


