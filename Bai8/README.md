# Bài 8 - Mô phỏng ổ đĩa RAID 5

Hệ thống ổ đĩa RAID 5 cần tối thiểu 3 ổ đĩa cứng, trong đó phần dữ liệu parity sẽ được chứa lần lượt lên 3 ổ đĩa như trong hình dưới.

<pre>
Nhap chuoi ki tu : DCE.****ABCD1234HUSTHUST

Disk 1                   Disk 2                Disk 3
----------------      ----------------      ----------------
|     DCE.     |      |     ****     |      [[ 6e,69,6f,04]]
|     ABCD     |      [[ 70,70,70,70]]      |     1234     |
[[ 00,00,00,00]]      |     HUST     |      |     HUST     |
----------------      ----------------      ----------------
</pre>

Hãy viết chương trình mô phỏng hoạt động của RAID 5 với 3 ổ đĩa, với giả định rằng, mỗi block dữ liệu có 4 kí tự. Giao diện như trong minh họa dưới. Giới hạn chuỗi kí tự nhập vào có độ dài là bội của 8.

Trong ví dụ trên, chuỗi kí tự nhập vào từ bàn phím `DCE.****ABCD1234HUSTHUST` sẽ được chia thành các block 4 byte.

- Block 4 byte đầu tiên `DCE.` sẽ được lưu trên Disk 1
- Block 4 byte tiếp theo `****` sẽ lưu trên Disk 2
- Dữ liệu trên Disk 3 sẽ là 4 byte parity được tính từ 2 block đầu tiên  với mã ASCII là `6e=’D’ xor ‘*’ ;  69=’C’ xor ‘*’;  6f=’E’ xor ‘*’;  04=’.’ xor ‘*’`
