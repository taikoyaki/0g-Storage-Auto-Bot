## 🇻🇳 **Tiếng Việt**

# 0G Storage Auto Bot

Bot tự động tương tác với mạng lưu trữ 0G nhằm tối đa hóa cơ hội nhận airdrop.

## Tổng Quan

Công cụ này tự động hóa quá trình tải lên các tệp ngẫu nhiên lên mạng lưu trữ 0G trên Galileo Testnet. Nó giúp người dùng tham gia các hoạt động testnet, từ đó có thể có cơ hội nhận airdrop trong tương lai.

## Tính Năng

* **Hỗ trợ nhiều ví**: Thực hiện tác vụ tuần tự với nhiều khóa cá nhân
* **Tích hợp proxy**: Sử dụng proxy xoay vòng để tránh bị giới hạn
* **Xoay vòng User-Agent**: Thay đổi user-agent tự động cho mỗi yêu cầu
* **Thống kê chi tiết**: Theo dõi các thao tác thành công và thất bại
* **Lịch sử giao dịch**: Lưu tất cả chi tiết giao dịch để tham khảo sau

## Cài Đặt

```bash
# Clone repository
git clone https://github.com/taikoyaki/0g-Storage-Auto-Bot.git

# Di chuyển vào thư mục
cd 0g-Storage-Auto-Bot

# Cài đặt các phụ thuộc
npm install
```

## Cấu Hình

1. Tạo file `.env` trong thư mục gốc với các khóa cá nhân:

```
# Một ví duy nhất
PRIVATE_KEY=your_private_key_here

# Hoặc nhiều ví
PRIVATE_KEY_1=your_first_private_key
PRIVATE_KEY_2=your_second_private_key
PRIVATE_KEY_3=your_third_private_key
```

2. (Tùy chọn) Tạo file `proxies.txt` với mỗi proxy trên một dòng:

```
http://username:password@ip:port
http://ip:port
socks5://username:password@ip:port
```

## Sử Dụng

Chạy bot với:

```bash
node index.js
```

Khi được hỏi, nhập số lượng tệp bạn muốn tải lên cho mỗi ví.

## Cách Hoạt Động

1. Bot tải các khóa cá nhân và proxy
2. Với mỗi ví:

   * Tải hình ảnh ngẫu nhiên
   * Tính hash và chuẩn bị dữ liệu
   * Tải các phần của tệp lên indexer 0G
   * Gửi giao dịch lên blockchain để đăng ký tải lên
   * Chờ xác nhận trước khi tiếp tục
3. Kết quả được lưu trong thư mục `results`

## Khắc Phục Sự Cố

* **Lỗi phí gas**: Đảm bảo ví có đủ token testnet 0G
* **Sự cố mạng**: Kiểm tra kết nối internet hoặc sử dụng proxy
* **Lỗi RPC**: RPC testnet có thể đang quá tải, thử lại sau

## Cảnh Báo

Công cụ này chỉ dành cho mục đích giáo dục và tham gia testnet. Sử dụng bot không đảm bảo đủ điều kiện nhận airdrop. Hãy sử dụng testnet một cách có trách nhiệm.

## Giấy Phép

MIT

