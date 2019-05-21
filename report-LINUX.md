# Linux report 
## 1. Basic Commands

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

## 2. working with files 

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
## 3. File permission 

> chown [owner name] [file name ]

` chown ` là lệnh thay đổi chủ sở hữu của 1 file 

> chgrp [ group name ] [file name]

` chgrp ` là lệnh có thể thay đổi group sở hữu cho file 

> chmod 

` chmod ` là một lệnh dùng để thay đổi các quyền được thực thi, đọc, ghi trên file 
cá quyền được cài đặt theo các số `  4 là đọc ` ,` 2 là quyền ghi ` , ` 1 là quyền thực thi file `
ex: ` chmod 746 file.txt ` có 3 số là ` 7 ` , ` 4 `, ` 6 `.
số ` 7 ` là thể hiện quyền của ngừơi sở hữu file, ở đây 7 là 4+2+1 là có đủ quyền đọc ghi và thực thi 
số ` 4 ` là thể hiện quyền của nhóm sở hữu , 4 ở đây là nhóm sở hữu chỉ có thể đọc file 
số ` 6 ` là quyền đối với nhóm user khác , 6 = 4 +2 như vậy quyền của các nhóm khác ở đây là đọc ghi vào file.

## 4. Packet Managerment

`Packet Managerment ` là trình quản lý gói tập tin của hệ thống mà trong đó chứa những công cụ, phần mềm tự động hoá quá trình cài đặt , cập nhật , định dạng cấu hình và xoá ứng dụng.
Vì linux có nhiều contributions khác nhau nến gói quản lý trên các contributions cũng khác nhau 

### Trình quản ký gói dựa trên Debian 

<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-2.jpg">

 - ` Gói dpkg ` Dpkg là một phần mềm quản lý gói cơ bản, với những công cụ để cài đặt, gỡ bỏ và xây dựng các gói.Tuy nhiên, dpkg lại thiếu những tính năng nâng cao như tải xuống các gói từ Internet hoặc cài đặt dependency tự động. Việc có thể làm tải xuống các gói từ Internet rất hữu ích, vì nó cho phép người dùng thêm kho lưu trữ cho các gói, giúp tăng đáng kể việc lựa chọn phần mềm có thể dễ dàng cài đặt trên hệ thống.
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-3.jpg">

 - ` Gói APT ` Đây là nơi mà các frontend như apt và aptitude phát huy tác dụng. APT, viết tắt của Advanced Package Tool, có chức năng nâng cao hơn nhiều khi so sánh với dpkg. APT cũng có thể cài đặt, gỡ bỏ và xây dựng các gói - tuy nhiên, chức năng của nó không chỉ dừng lại ở đó. APT có thể tự động cập nhật gói, tự động cài đặt các dependency cũng như tải xuống những gói bạn cần từ Internet. Đây là một trong những trình quản lý gói phổ biến nhất được cài đặt trên các bản phân phối hiện đại. APT được cài đặt sẵn trên Ubuntu, Debian và hầu hết các hệ điều hành dựa trên Debian khác.
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-4.jpg">

 - ` Gói Aptitude `Aptitude rất giống với APT và cung cấp hầu hết các chức năng tương tự như trình quản lý gói này. Nhưng, Aptitude còn cung cấp một vài tính năng bổ sung, chẳng hạn như nâng cấp an toàn, cho phép người dùng nâng cấp các gói mà không cần xóa những gói hiện có khỏi hệ thống. Tính năng giữ nguyên gói cũng có sẵn, điều này ngăn các gói nhất định được nâng cấp tự động.Cả hai trình quản lý gói này thực sự sử dụng dpkg cho các hoạt động cơ bản và chỉ sử dụng phần mềm của riêng chúng để tải xuống và quản lý gói.

### Trình quản lý gói dựa trên RedHat Enterprise Linux

<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-5.jpg">

 - ` Gói RPM ` RedHat và CentOS là một trong những hệ điều hành được sử dụng rộng rãi nhất và dễ dàng được tìm thấy trên các máy chủ hiện nay. Phần mềm quản lý gói cơ bản được tìm thấy trên các hệ thống này là RPM, viết tắt của Red Hat Package Manager. Trình quản lý gói này cũng thực hiện những hoạt động cơ bản như cài đặt và gỡ bỏ các gói, và giống như dpkg, RPM cũng không thể quản lý các gói hoặc cài đặt chúng trực tiếp từ Internet.
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-6.jpg">

 - ` Gói YUM ` Giống như các hệ điều hành dựa trên Debian khác, hệ điều hành RHEL cũng có phần mềm riêng để quản lý gói. YUM, viết tắt của Yellow Dog Updater, là lựa chọn phổ biến nhất dưới dạng RPM frontend. YUM mở ra nhiều chức năng hơn cho các file RPM thông qua những kho lưu trữ, khả năng theo dõi những gì được cài đặt trên hệ thống, cập nhật hợp lý và hơn thế nữa. YUM là tùy chọn dựa trên RHEL tương đương của trình quản lý gói APT.
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-7.jpg">

 - ` Gói DNF ` DNF, viết tắt của Dandified Packaging Tool, là phiên bản hiện đại và tiên tiến hơn của trình quản lý YUM. DNF kết hợp các tính năng của YUM, đồng thời cải thiện hiệu suất và việc sử dụng tài nguyên. Hiện tại, mới chỉ có Fedora sử dụng phiên bản YUM thế hệ tiếp theo này, nhưng hy vọng, người dùng sẽ thấy nó xuất hiện trên nhiều hệ điều hành hơn trong tương lai.Có một số công cụ quản lý gói khác có sẵn cho những hệ thống dựa trên RPM, chẳng hạn như up2date, urpmi và ZYpp. Tuy nhiên, những trình quản lý gói này được sử dụng rộng rãi như YUM hoặc DNF.

### Những trình quản lý gói khác 

<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-8.jpg">

 - ` Gói Pacman ` Pacman là trình quản lý gói được tìm thấy trên Arch Linux. Pacman là công cụ quản lý gói duy nhất được tìm thấy trên Arch, khiến nó không phải là một frontend. Arch Linux là một hệ điều hành phát hành dạng rolling release, với các bản cập nhật, được thêm vào mỗi ngày. Chỉ có một vài lệnh với Pacman, dùng để tìm kiếm, cài đặt và xóa gói. Trình quản lý gói này có thể kết nối với Internet và lấy các gói từ đó, khiến Pacman thân thiện hơn với người dùng. Tuy nhiên, Pacman được thiết kế để cài đặt phần mềm từ kho Arch, nên không thể cài đặt từ kho của bên thứ ba. 
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-9.jpg">

 - ` Gói ABS ` ABS, viết tắt của Arch Build System, là một hệ thống các công cụ dành cho việc tạo những gói phần mềm có thể cài đặt cho Arch Linux ngoài mã nguồn. Trình quản lý gói ABS bao gồm một số công cụ hoạt động song hành để tạo ra các gói. Những công cụ này là tất cả các chương trình độc lập, chẳng hạn như makepkg, pacman, asp, v.v... Phương pháp tạo/cài đặt gói sử dụng ABS khác với những bản phân phối Linux thông thường. Thay vì cài đặt các gói được biên dịch sẵn, bạn cần tạo file PKGBUILD từ nhánh Svn hoặc Git bằng cách sử dụng gói asp. Sau đó, bạn sử dụng lệnh makepkg, dùng file PKGBUILD để tải xuống và biên dịch mã nguồn cho hệ thống của mình. Điều này làm cho ABS trở thành một phương pháp cài đặt gói ít trực quan hơn trên Arch Linux. Cũng có một số cách khác để sử dụng ABS, chẳng hạn như tùy chỉnh các gói hiện có hoặc xây dựng và cài đặt kernel tùy chỉnh.
<img src="https://st.quantrimang.com/photos/image/2019/05/20/trinh-quan-ly-goi-linux-pho-bien-nhat-10.jpg">

 -` Gói Portage ` Portage là trình quản lý gói cho Gentoo, một hệ điều hành đơn giản, nhưng phải được biên dịch từ đầu khi cài đặt trên bất kỳ hệ thống nào. Đây là một trong những trình quản lý gói tiên tiến nhất hiện có, với các tính năng và cải tiến mới được bổ sung liên tục.

## 5. Systerm info
- Các dữ liệu hệ thống như name , version, release , dítributon... đều được hiển thị sau câu lệnh ` cat /etc/*release `
- Thông tin về Kernel version được biết qua câu lệnh ` uname -r `
- Các thông số về Memory được lưu trữ ở file meninfo nên có thể xem băng cách ` head /proc/neminfo/ `
- Thông tin về phân vùng ổ cứng đc biết qua câu lệnh ` df -h `
- Thông tin hostname của hệ thống bằng câu lệnh ` hostnamectl status ` 

### Proc Filesysterm

Proc là hệ thống file ảo bởi vì trên thực tế nó không tồn tại trong bất kì phương tiện lưu trữ nào. Nó tồn tại dựa trên bộ nhớ ảo và dữ liệu luôn thay đổi động cùng với trạgn thái của hệ thống. Hầu hết các dữ liệu trong proc FS được cập nhật liên tục để phù hợp với trạng thái hiện tại của hệ điều hành. Nội dung của proc FS có thể được đọc bởi user có quyền thích hợp, trong đó một số phần chỉ dó thể đọc bởi owner của process và root. Nếu liệt kê thư mục root (/) ra bạn sẽ thấy. Một vài files quan trọng in trong ` /proc ` :
```
/proc/cpuinfo
/proc/interrupts
/proc/meminfo
/proc/mounts
/proc/partitions
/proc/version
/proc/<process-id-#>
/proc/sys
```
## 6. Networking 
Ở CentOS routing và host được chứa tại đường dẫn ` /etc/sysconfig/network ` .
---To be continuted---
(Em đang đọc thêm về network em sẽ hoàn thành phần này sau ạ!)
