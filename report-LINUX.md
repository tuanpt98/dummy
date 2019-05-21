# Linux report 
## Basic Commands

> which diff

Là câu lệnh để xác định vị trí của programs. Như trong ví dụ trên kết quả trả về sẽ là : ` /bin/diff `

> whereis diff

Lệnh trả về đường dẫn của các binary file, source code, man page nếu tồn tại mang tên [dif]. Các tuỳ chọn có thể sử dụng  ` -b : cho file binary ` , ` -m : cho man page ` , ` -s : cho source code ` .

> ls [option] 

` ls ` dùng để liệt kê toàn bộ những file trong thư mục hiện tại.

- ` ls -l ` là lệnh hiển thị user sở hữu và permission , ngày thành chỉnh sửa gần nhất của các file trong thư mục 

- ` ls -a ` hiển thị tất cả các files bao gồm cả file ẩn 

> cd 

` cd ` là lệnh chuyển đổi đường dẫn thư mục 

- ` cd ../ ` là lệnh đưa trở về thư mục trước đó 

- ` cd ~ ` là lệnh đưa thư mục về thư mục mặc định khi đăng nhập vào .

> ln file1.txt file2.txt

` ln ` là một lệnh link file hoặc thư mục đến một thư mục khác. Như ví dụ file1.txt là một file tồn tại có sẵn mà file2.txt sẽ là empty file được link đến file1.txt do đó dữ liệu trong hai file đều giống nhau.

##working with files 

> locate [file name ]

` locate ` là command đùng dể tìm kiếm file theo tên trên toàn bộ thư mục 

> touch [file name]
 
là lệnh dùng để tạo 1 file 

> rm [file name ]

là lệnh remove một file 

>cp [filee name] [other name]

là lệnh dùng dể copy một file sang một file khác

> mv [old name] [new name]

đùng để thay đổi tên một file ( mv sẽ ghi đè lên file nếu có sẵn dẫn đến mất dữ liệu do đó khuyến cáo không nên sử dụng ) 

> mv [path/file name ] [new path]

lệnh đùng để di chuyển một file đến đường dẫn mới 

> mkdir [ directory name ]

là một lệnh tạo 1 directory mới ( ở đây hiểu là thư mục ) 

> rdir [ dỉrectory name ] 

là một lệnh remove một directory 

> cat [file name]

là lệnh đùng dể xem dữ liệu trên file. Ngoài ra có thể dùng có lệnh khác như ` tail `, `head ` .
 
> vi [file name]

lệnh đùng để sửa đổi file. Thao tác cơ bản là ` i ` là insert sau khi thay đổi ` esc ` và ` :x ` để thoát và lưu lại thay đổi hoặc ` :q! ` là thoát và không lưu bất kỳ thay đôir nào.

