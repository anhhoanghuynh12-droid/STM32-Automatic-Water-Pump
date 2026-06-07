# Hệ Thống Điều Khiển Máy Bơm Tự Động Sử Dụng STM32

## Giới thiệu

Đây là project xây dựng hệ thống điều khiển máy bơm nước tự động sử dụng vi điều khiển STM32 và cảm biến mực nước. Hệ thống có khả năng giám sát mực nước theo thời gian thực và tự động bật/tắt máy bơm khi đạt các ngưỡng được thiết lập.

Project được triển khai trên kit STM32 thực tế nhằm phục vụ mục đích học tập và nghiên cứu hệ thống nhúng.

## Chức năng chính

* Đọc giá trị cảm biến mực nước thông qua bộ ADC của STM32.
* Giám sát mực nước liên tục.
* Tự động bật máy bơm khi mực nước thấp.
* Tự động tắt máy bơm khi mực nước đạt ngưỡng cho phép.
* Sử dụng ngắt ngoài (External Interrupt) để xử lý các sự kiện điều khiển.
* Điều khiển relay đóng/ngắt nguồn cho máy bơm.

## Phần cứng sử dụng

* Kit STM32
* Cảm biến mực nước
* Module Relay
* Máy bơm nước mini
* Nguồn cấp

## Công nghệ sử dụng

* STM32CubeIDE
* Ngôn ngữ C
* GPIO
* ADC
* External Interrupt (EXTI)
* Embedded Systems

## Nguyên lý hoạt động

1. STM32 đọc tín hiệu từ cảm biến mực nước thông qua ADC.
2. Giá trị ADC được xử lý để xác định trạng thái mực nước.
3. Khi mực nước thấp hơn ngưỡng cho phép, STM32 kích relay để bật máy bơm.
4. Khi mực nước đạt mức yêu cầu, relay được tắt để ngừng bơm.
5. Các sự kiện điều khiển được xử lý thông qua cơ chế ngắt ngoài nhằm tăng khả năng phản hồi của hệ thống.

## Kết quả đạt được

* Hệ thống hoạt động ổn định trên kit STM32 thực tế.
* Đọc dữ liệu cảm biến chính xác.
* Điều khiển máy bơm tự động theo ngưỡng mực nước.
* Thực hiện thành công việc sử dụng ADC và ngắt ngoài trong ứng dụng nhúng.

## Tác giả

Hoàng Huỳnh

Sinh viên ngành Kỹ thuật Vi mạch bán dẫn.
