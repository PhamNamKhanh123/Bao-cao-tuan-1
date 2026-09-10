# PHƯƠNG PHÁP ĐẶC TẢ YÊU CẦU BÀI TOÁN THEO CHUẨN AGILE

**Người thực hiện:** Phạm Nam Khánh
**Giai đoạn:** Tuần 1 - Chuẩn bị phân tích hệ thống

---

## 1. Quy trình phân rã yêu cầu trên Jira
Trong mô hình Agile, yêu cầu bài toán không được viết dưới dạng một tài liệu text dài hàng trăm trang mà được bóc tách và quản lý trên các công cụ như Jira theo cấu trúc phân cấp:

1. **Theme/Initiative:** Mục tiêu lớn của dự án.
2. **Epic:** Một cụm tính năng lớn, không thể hoàn thành trong 1 Sprint. *(VD: Quản lý tài khoản người dùng).*
3. **Story / Task:** Chức năng cụ thể, có thể hoàn thành trong 1 Sprint. *(VD: Đăng nhập bằng Google).*
4. **Sub-task:** Các đầu việc kỹ thuật nhỏ để hoàn thành Story. *(VD: Thiết kế UI nút đăng nhập, Viết API xử lý token).*

---

## 2. Viết User Story (Câu chuyện người dùng)
Để đảm bảo phần mềm giải quyết đúng nhu cầu thực tế, các yêu cầu tính năng sẽ được viết dưới góc nhìn của người dùng (End-user) thay vì góc nhìn kỹ thuật.

**Cấu trúc tiêu chuẩn:**
> **As a** [Loại người dùng/Actor], **I want to** [Hành động/Tính năng] **so that** [Mục đích/Giá trị mang lại].

*Ví dụ minh họa:*
* *As a* khách hàng, *I want to* khôi phục mật khẩu qua email *so that* tôi có thể đăng nhập lại khi quên mật khẩu cũ.
* *As an* admin, *I want to* xem biểu đồ doanh thu theo tháng *so that* tôi có thể đánh giá hiệu quả kinh doanh.

---

## 3. Tiêu chí nghiệm thu (Acceptance Criteria & Definition of Done)

Một User Story chỉ được chuyển sang trạng thái "Done" khi thỏa mãn các điều kiện rõ ràng để tránh việc dev báo "xong rồi" nhưng hệ thống vẫn lỗi.

### 3.1. Acceptance Criteria (AC - Tiêu chí chấp nhận)
Là các điều kiện cụ thể áp dụng cho riêng một User Story đó.
*Ví dụ cho tính năng Đăng nhập:*
* AC1: Người dùng nhập đúng email và password sẽ được chuyển hướng vào Dashboard.
* AC2: Nhập sai password quá 5 lần sẽ bị khóa tài khoản 15 phút.
* AC3: Phải có thông báo lỗi hiển thị bằng tiếng Việt nếu để trống trường email.

### 3.2. Definition of Done (DoD - Định nghĩa Hoàn thành)
Là bộ quy tắc chung áp dụng cho MỌI User Story trong dự án. Một task được coi là "Done" khi:
* [x] Code đã chạy không có lỗi (Zero bugs).
* [x] Giao diện hiển thị tốt trên cả Desktop và Mobile (Responsive).
* [x] Đã đẩy code lên GitHub.
* [x] Đã kiểm thử các luồng cơ bản (Happy path).

---

## 4. Phương pháp đánh giá mức độ ưu tiên (MoSCoW)
Vì thời gian làm dự án có hạn, các chức năng trong Product Backlog sẽ được phân loại độ ưu tiên theo kỹ thuật **MoSCoW**:
* **M - Must have:** Các tính năng bắt buộc phải có, nếu thiếu phần mềm sẽ không hoạt động (VD: Đăng nhập, Thêm giỏ hàng).
* **S - Should have:** Các tính năng quan trọng nhưng không khẩn cấp, hệ thống vẫn chạy được nếu thiếu (VD: Quên mật khẩu).
* **C - Could have:** Tính năng "nice to have", có thì tốt nhưng không ảnh hưởng lớn (VD: Chế độ Dark mode).
* **W - Won't have (this time):** Các tính năng chưa cần thiết trong phạm vi đồ án hiện tại.

**Kết luận:** Dựa trên phương pháp này, vào đầu tuần 2 (sau khi chốt đề tài cụ thể), toàn bộ chức năng của hệ thống sẽ được bóc tách thành các User Story và nhập liệu vào Product Backlog trên Jira.
