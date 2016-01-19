#Command

##Lệnh "du" (dick usage): 
Được sử dụng để kiểm tra thông tin ổ đĩa của các tập tin và thư mục trên máy. Lệnh du có 1 vài tham số được sử dụng để đưa ra kết quả ở nhiều định dạng khác nhau. Lệnh này cũng hiển thị các file và thư mục theo hình thức đệ quy

##Sử dụng

###1.Để tóm tắt thông số sử dụng của cây thư mục /home/stack/devstack và thư mục con của nó sử dụng lệnh:

    du /home/stack/devstack

<img src="http://i.imgur.com/PwXpXo3.png">

Đầu ra của lệnh trên là số ổ block trong thư much /home/devstack/stack, (mỗi disk block này tương ứng với 1024K) và chỉ hiện ra thông số của các thư mục con trong đường dẫn mà mình chỉ ra


###2.Sử dụng thêm tham số -h để hiện ra thông số tính theo đơn vị Bytes, Kilobytes, Megabytes, Gigabytes...

    du -h /home/stack/devstack

<img src="http://i.imgur.com/77rfXHt.png">

###3.Để hiện ra tổng dung lượng của thư mục mà ko hiện thư mục con ở trong sử dụng lệnh

    du -sh /home/stack/devstack

<img src="http://i.imgur.com/0xyJrDg.png">

###4.Tham số -a để hiện tất cả file và thư mục
    du -ah /home/stack/devstack/

<img src="http://i.imgur.com/ptGup44.png">

###5.Tham số -c để hiện ra tổng dung lượng ổ đữa ở cuối
    du -ac /home/stack/devstack/

<img src="http://i.imgur.com/Q5uyBWr.png:">

##6.Tham số --exclude="file" đửaa màn hình tất cả các file trừ file đc khai báo
    du --exclude="*.sh" /home/stack/devstack/

<img src="http://i.imgur.com/0udqDeT.png">

###7.Thêm tham số --time để hiện ra thời gian khởi tạo file đó
    du -ha --time /home/stack/devstack/
 
<img src="http://i.imgur.com/hLY9RDy.png">	