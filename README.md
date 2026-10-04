# [Bài tập] Nhúng CSS vào trang HTML

Dự án bài thực hành luyện tập nhúng CSS vào trang web bằng 3 phương pháp cơ bản: **Inline-style**, **Internal-style** và **External-style**.

## 📌 Mục đích bài tập
- Hiểu và vận dụng thành thạo 3 cách nhúng CSS vào trang HTML.
- Phân biệt sự khác nhau về cú pháp, vị trí khai báo, mức độ ưu tiên và phạm vi ảnh hưởng của từng phương pháp.

---

## 🛠 Cấu trúc thư mục dự án
- `index.html`: Cấu trúc tài liệu HTML5 bao gồm:
  - **Phần 1: Inline-style**: Thay đổi màu sắc của tiêu đề và đoạn văn sử dụng thuộc tính `style="..."` trực tiếp trên thẻ.
  - **Phần 2: Internal-style**: Thay đổi màu sắc của tiêu đề và đoạn văn sử dụng thẻ `<style>` đặt bên trong thẻ `<head>`.
  - **Phần 3: External-style**: Thay đổi màu sắc của tiêu đề và đoạn văn sử dụng tệp CSS ngoài (`style.css`) liên kết qua thẻ `<link>`.
  - **Bảng tổng hợp**: So sánh trực quan ưu nhược điểm và độ ưu tiên của 3 cách nhúng CSS.
- `style.css`: Tệp định kiểu CSS độc lập chứa quy tắc định dạng cho Phần 3 và giao diện chung.
- `README.md`: Tài liệu hướng dẫn bài thực hành.

---

## 📋 Chi tiết 3 phương pháp nhúng CSS

### 1. Inline-style (Định kiểu nội dòng)
- **Vị trí**: Viết trực tiếp trong thuộc tính `style` của thẻ HTML mở.
- **Ví dụ**:
  ```html
  <h2 style="color: #e11d48;">Tiêu đề</h2>
  <p style="color: #be123c;">Đoạn văn...</p>
  ```
- **Đặc điểm**: Mức độ ưu tiên cao nhất, chỉ ảnh hưởng đến đúng thẻ đó.

### 2. Internal-style (Định kiểu nội bộ)
- **Vị trí**: Viết trong thẻ `<style>` đặt trong phần `<head>` của trang HTML.
- **Ví dụ**:
  ```html
  <style>
      .internal-heading { color: #2563eb; }
      .internal-paragraph { color: #1e40af; }
  </style>
  ```
- **Đặc điểm**: Áp dụng chung cho toàn bộ các phần tử tương ứng trong trang hiện tại.

### 3. External-style (Định kiểu bên ngoài)
- **Vị trí**: Viết trong tệp `.css` riêng biệt và liên kết qua thẻ `<link>` trong `<head>`.
- **Ví dụ**:
  ```html
  <!-- Trong HTML -->
  <link rel="stylesheet" href="style.css">

  <!-- Trong file style.css -->
  .external-heading { color: #059669; }
  .external-paragraph { color: #065f46; }
  ```
- **Đặc điểm**: Tiêu chuẩn tốt nhất trong thực tế, dễ dàng tái sử dụng cho nhiều trang web khác nhau trong cùng hệ thống.
