#Command dd

##Lệnh dd
"dd" (data-duplocator) là 1 trong những công cụ IO đa năng dành cho Linux. Nó được sử dụng để sao chép hoặc chuyển đổi dữ liệu.

lệnh "dd" có cấu trúc sau:

    dd  if=<source file name> of=<target file name> [Options]


- if: là tên hoặc vị trí của file đầu vào
- of: là tên hoặc vị trí của file đầu ra
- bs: là block size được sử dụng để đọc hoặc ghi - file. Tăng thông số này có thể giúp hiệu suất với việc đọc hoặc ghi dữ liệu
- count: là số block sẽ được sử dụng
- seek: là số block của file đầu ra sẽ được bỏ qua trước khi ghi dữ liệu
- skip: là số block của file đầu vào sẽ được bỏ qua trước khi đọc dữ liệu
- conv: chuyển đổi các fie

##Sử dụng lênh dd
###1.Backup partion với dd
   
    dd if=/dev/sda1 of=~/localdisk_sda1.img

<img src="http://i.prntscr.com/1029ff24cb114a1983f0db420f58cd2a.png">

###2. Tạo SWap file với dd

    dd if=/dev/zero of=/mnt/swapdrive/swapfile bs=1M count=4096

<img src ="http://i.imgur.com/UNUcz3n.png">

###3.Bạn có thể cắt hoặc nối nhiều file với dd cùng thông số skip hoặc seek

    dd if=<file muốn cắt> of=<file sau cắt> bs=<kích thước> count=<số block> skip=<số block bỏ qua>

Kiểm tra file cirros.image dung lượng 24M.

Ta cắt thành 8 file 3M như sau:

<img src="http://i.imgur.com/ZRARwTH.png">

Ktra sau khi cắt

<img src="http://i.prntscr.com/a010d1829eff4ff291a767716edb9a40.png">


###4.Chuyển đổi định dạng với conv
Tạo 1 file test1 với nội dung như sau:

<img src="http://i.imgur.com/mDvHaQe.png">

Sử dụng lệnh 

    dd if=/root/test1 of=/root/test2 conv=lcase

Kết quả:

<img src="http://i.imgur.com/GoqxGuI.png">