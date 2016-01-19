#Command df

##Lệnh df (disk filesystem)

Được sử dụng để lấy được tổng số dung lượng có sẵn và đã sử dụng trong ổ đĩa của hệ thống tập tin trên linux

##Sử dụng

###1. Hiển thị thông tin về tên thiết bị, tổng block, tổng số sẵn còn, tổng số đã được sử dụng, phần trăm sử dụng và điểm mount

    df

<img src="http://i.imgur.com/nc7pSpJ.png">

###2. Thêm tham số -a để hiển thị hệ thống tập tin giả cùng với tất cả hệ thống tập tin ổ đĩa cùng với bộ nhớ của nó

    df -a

<img src="http://i.imgur.com/gIYVcnT.png">


###3. Thêm tham số -h để hiển thị dưới dạng kích thướng như byte, gigabyte...

    df -h

<img src="http://i.imgur.com/3sDhowp.png">

###4. Thêm tham số -m hoặc -k để hiển thị dưới dạng kilobyte hoặc megabyte

<img src="http://i.imgur.com/fV4540F.png">

###5. Tham số -i để hiện số inode và % của file hệ thống

<img src="http://i.imgur.com/NvQ2Hiq.png">


###6. Tham số -T để hiển thị định dạng của tập hệ thống

Nếu muốn hiển thị kiểu định dạng nhất định có thể thêm -t

Nếu không muốn hiển thị kiểu định dạng nhất định có thể thêm -x

<img src="http://i.imgur.com/UrMvZpp.png">