Mô tả tổng quan hoạt động

Chương trình này biến ESP32 thành một thiết bị BLE Server với các chức năng:

ESP32 khởi tạo BLE với tên "ESP_BLE".

Tạo 1 BLE Service với UUID cố định.

Trong Service tạo 2 đặc tính BLE (Characteristics):

LED Characteristic (Read + Write): nhận dữ liệu từ app → điều khiển LED.

Sensor Characteristic (Read): cho phép thiết bị khác đọc dữ liệu cảm biến (ở đây gán tạm "30.0").

Khi thiết bị BLE Client gửi "1" → ESP32 bật LED.
Khi gửi "0" → ESP32 tắt LED.

Serial Monitor sẽ in ra giá trị mới nhận được.
