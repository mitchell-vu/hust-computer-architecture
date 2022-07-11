# Bài 2 - Vẽ hình trên màn hình Bitmap

Viết chương trình vẽ một quả bóng hình tròn di chuyển trên màn hình mô phỏng Bitmap của Mars. Nếu đối tượng đập vào cạnh của màn hình thì sẽ di chuyển theo chiều ngược lại.

![Keyboard and Display MMIO Simulator](https://github.com/mitchell-vu/hust-computer-architecture/blob/main/Bai2/screen-example-2.png?raw=true)

## Yêu cầu

- Thiết lập màn hình ở kích thước 512x512.  
Kích thước pixel 1x1.
- Chiều di chuyển phụ thuộc vào phím người dùng bấm trong bộ giả lập Keyboard and Display MMIO Simulator, gồm có:
  - Di chuyển lên (W)
  - Di chuyển xuống (S)
  - Sang trái (A)
  - Sang phải (D)
  - Tăng tốc độ (Z)
  - Giảm tốc độ (X)
- Vị trí bóng ban đầu ở giữa màn hình.

## Gợi ý

- Để làm một đối tượng di chuyển thì chúng ta sẽ xóa đối tượng ở vị trí cũ và vẽ đối tượng ở vị trí mới.
- Để xóa đối tượng chúng ta chỉ cần vẽ đối tượng đó với màu là màu nền.
