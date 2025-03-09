# Embedded-System
## Kiến trúc tổng quan hệ nhúng
- Kiến trúc tổng quan hệ nhúng
  - Khối xử lý: 
    - Microprocessor (Bộ vi xử lý): Bộ xử lý độc lập không thực hiện được nhiêm vụ gì.
    - Microcontroller (Bộ vi điều khiển):Giống vi xử lý nhưng rẻ tiền hơn, yếu hơn.
    - SoC (System-on-chip): Nhiều thành phần được đóng gói lại trên một vi mạch. Ví dụ là CPU và GPU.
- Bộ nhớ
  - RAM (SRAM và DRAM): SRAM nhanh hơn, đắt hơn, tiêu tốn ít điện năng hơn, dung lượng nhỏ hơn DRAM. SRAM thường được dùng làm cache còn DRAM dùng làm bộ nhớ chính.
  - Hybrid (NVRAM, Flash, EEPROM): 
    - NVRAM: Tốc độ truy cập nhanh, có thể lưu trữ dữ liệu khi mất điện. Nhưng giá cao.
    - Flash: Dung lượng lớn, giá thành rẻ hơn NVRAM, tốc độ đọc nhanh nhưng ghi chậm hơn RAM, giới hạn số lần ghi xóa (độ bền), và phải xóa theo khối thay vì từng byte.
    - EEPROM: Tốc độ đọc/ghi chậm nhất, độ bền ghi xóa giới hạn, dung lượng thường nhỏ hơn Flash. Giá thành rẻ nhất.
    > Hiện tại không còn dùng Flash và EEPROM nữa.
  - ROM (EPROM, PROM, Masked): 
    - Masked và PROM: chỉ có thể lập trình 1 lần trong đó Masked sẽ được lập trình sẵn từ khi sản xuất, còn PROM có thể lập trình MỘT lần bỞi người sử dụng. 
    - EPROM: có thể được lập trình nhiều lần nhưng khi xóa chương trình cũ cần sử dụng tia UV => bất tiện. Đắt nhất trong 3 loại
## Phương pháp vào ra
| Tính năng| Programmed I/O (I/O lập trình) | Interrupt-driven I/O (I/O điều khiển bằng ngắt) | Direct Memory Access (DMA - Truy cập bộ nhớ trực tiếp) |
|---------------------------|----------------------------------|---------------------------------------|---------------------------------------------------------|
| **CPU Involvement**      | Cao (CPU trực tiếp tham gia)       | Trung bình (CPU tham gia khi có ngắt) | Thấp (CPU ít tham gia sau khi khởi tạo)               |
| **Hiệu suất CPU**         | Kém (CPU busy-waiting)            | Tốt hơn Programmed I/O              | Tốt nhất (CPU được giải phóng)                            |
| **Tốc độ truyền dữ liệu** | Chậm                             | Nhanh hơn Programmed I/O             | Nhanh nhất                                                |
| **Độ phức tạp phần cứng** | Đơn giản                         | Phức tạp hơn Programmed I/O           | Phức tạp nhất (DMA Controller)                             |
| **Độ phức tạp phần mềm** | Đơn giản                         | Phức tạp hơn Programmed I/O           | Phức tạp hơn Interrupt-driven I/O                          |
| **Chi phí hệ thống**     | Thấp nhất                         | Cao hơn Programmed I/O               | Cao nhất                                                   |
| **Ứng dụng điển hình**    | I/O tốc độ thấp, đơn giản         | I/O tốc độ trung bình, thời gian thực mềm | I/O tốc độ cao, truyền dữ liệu lớn, thời gian thực cứng     |

## Các chuẩn giao tiếp

- UART 
- I2C
- SPI 
- CAN

## Mở rộng chân

## Ngắt

## Băm xung :)))