# Service-AutoSendEmail
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Dùng để gửi Email đến người bệnh tự động khi đăng ký một lịch hẹn khám mới

Nền tảng công nghệ LCDP sử dụng: **N8N**

## Changelog

### v1.0
- **Node WebHook**:  
  - Node này sẽ lắng nghe sự kiện và nhận dữ liệu gửi về khi có 1 lịch hẹn khám được đăng ký. Dữ liệu gửi về ở đây sẽ là: email của bệnh nhân và nội dung email.

- **Node Send Email**:  
  -  Node này sẽ lấy thông tin từ node đầu tiên rồi sử dụng dịch vụ gửi email của Google để thực hiện việc gửi email lịch hẹn đến bệnh nhân.  

## Hướng dẫn cài đặt
### 1. Yêu cầu hệ thống
- **Tài khoản SMTP**: Là tài khoản gửi email đến các tài khoản khác  
- **N8N**: Phiên bản >=1.66.0

### 2. Cài đặt dữ án
#### Bước 1: Tải mã nguồn từ bản phát hành
1. Truy cập trang phát hành chính thức tại: [Releases](https://github.com/trungthanhcva2206/Service-AutoSendEmail/releases).
2. Chọn phiên bản phù hợp với nhu cầu của bạn.
3. Trong phần **Assets**, tải tệp:
   - `Source code (zip)` hoặc
   - `Source code (tar.gz)`.

#### Bước 2: Giải nén và truy cập thư mục
```bash
# Giải nén file đã tải
unzip Service-AutoSendEmail.zip
cd Service-AutoSendEmail
```
#### Bước 3: Import vô N8N 
1. Tạo 1 workflow trong N8N
2. Import file My-workflow.json, file này lấy được ở trong thư mục Service-AutoSendEmail

#### Bước 4: Chỉnh sửa các tài khoản dịch vụ
Ở trong node Send Email sẽ có phần **Credential to connect with**, hãy chỉnh sửa tài khoản SMTP của mình ở đây. 

## Tác giả
- Nguyễn Lê Trung Thành
- Trần Tuấn Anh
- Lê Văn Quang

# License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
