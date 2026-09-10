# GHI CHÚ CẤU HÌNH VÀ THIẾT LẬP DỰ ÁN TRÊN ATLASSIAN JIRA

**Người thực hiện:** Phạm Nam Khánh
**Giai đoạn:** Tuần 1 - Khởi tạo môi trường quản lý tiến độ
**Công cụ áp dụng:** Atlassian Jira Software

---

## 1. Mục tiêu thiết lập
Để đảm bảo quá trình tự triển khai dự án đi đúng hướng theo phương pháp luận Agile/Scrum, em đã lựa chọn sử dụng **Atlassian Jira** - công cụ quản lý dự án phổ biến nhất hiện nay trong các doanh nghiệp IT. 

Mục tiêu của tuần 1 là khởi tạo thành công không gian làm việc (Workspace), cấu hình luồng công việc (Workflow) và chuẩn bị sẵn sàng bảng Backlog để nhập yêu cầu bài toán vào Tuần 2.

---

## 2. Các bước khởi tạo dự án (Project Creation)
Dựa trên kiến thức đã nghiên cứu, em đã thực hiện thiết lập dự án theo các thông số sau:
1. **Loại dự án (Project Type):** Chọn mẫu *Software Development* (Phát triển phần mềm).
2. **Khung làm việc (Template):** Chọn **Scrum** thay vì *Kanban*. Quyết định này giúp em có thể chia nhỏ quá trình code thành các vòng lặp Sprint (dự kiến 2 tuần/Sprint) và có tính năng Backlog để lên kế hoạch.
3. **Mô hình quản lý:** Chọn *Team-managed project* (Dự án do nhóm tự quản lý) để tối ưu hóa sự linh hoạt trong việc tự tùy chỉnh các luồng trạng thái mà không cần can thiệp quá sâu vào cấu hình hệ thống (Company-managed).

---

## 3. Tùy chỉnh Luồng công việc (Workflow & Board)
Mặc định của Jira chỉ có 3 cột trạng thái (To Do, In Progress, Done). Để phù hợp với quy trình phát triển phần mềm độc lập, em đã tự tinh chỉnh lại Workflow trên Scrum Board thành 4 cột (Columns) như sau:

* **Cột 1 - TO DO:** Chứa các User Story / Task đã được kéo từ Backlog vào Sprint hiện tại nhưng chưa bắt đầu làm.
* **Cột 2 - IN PROGRESS:** Các task đang tiến hành viết code.
* **Cột 3 - IN REVIEW (Mới thêm):** Các task đã code xong nhưng đang trong giai đoạn kiểm thử lại (Testing) hoặc review lại kiến trúc code để đảm bảo không có bug trước khi đóng gói.
* **Cột 4 - DONE:** Các task đã hoàn thiện 100% (đáp ứng tiêu chuẩn Definition of Done) và đã được đẩy code lên GitHub.

---

## 4. Cấu hình Product Backlog và Sprint
Trước khi có đề tài chi tiết để tạo Ticket, em đã thiết lập sẵn các cấu hình khung trên hệ thống:

* **Bật tính năng Epic Panel:** Cho phép nhóm các task nhỏ lẻ vào các Epic lớn (Ví dụ Epic: *Quản lý người dùng*, Epic: *Thanh toán*), giúp dễ dàng theo dõi tiến độ tổng thể.
* **Cấu hình độ dài Sprint:** Thiết lập độ dài mặc định cho mỗi Sprint là **2 tuần (2 weeks)**.
* **Bật tính năng Story Point Estimation:** Cấu hình sử dụng dãy số Fibonacci (1, 2, 3, 5, 8...) để đánh giá mức độ phức tạp của từng User Story thay vì dùng giờ (Hours), đúng với tư duy chuẩn của Agile.

---

## 5. Minh chứng thực hành (Screenshots)
Dưới đây là một số hình ảnh minh chứng giao diện Jira đã được em khởi tạo và thiết lập thành công trong Tuần 1, sẵn sàng cho việc nạp dữ liệu (Log task) vào Tuần 2:

*(Thầy xem ảnh giao diện bảng Scrum Board và Backlog em đã chụp bên dưới)*

![Giao diện Backlog trên Jira](link_anh_chup_man_hinh_backlog_cua_ban_o_day.png)

![Giao diện Scrum Board trên Jira](link_anh_chup_man_hinh_board_cua_ban_o_day.png)

---
**Kết luận:** Hệ thống Jira đã sẵn sàng. Ngay sau khi chốt xong đề tài và vẽ xong sơ đồ Use Case ở đầu tuần 2, toàn bộ yêu cầu phần mềm sẽ được chuyển hóa thành dạng Issue trên hệ thống này.
