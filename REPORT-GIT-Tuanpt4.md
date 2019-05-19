# Report about Git- Github

## I. Git-Github-Gitlap


### 1. Git
<img src="http://blog.davidecoppola.com/wp-content/uploads/2016/11/git_logo-header.png">
Git là một trong những Hệ thống Quản lý Phiên bản Phân tán, vốn được phát triển nhằm quản lý mã nguồn (source code) của Linux.

Trên Git, ta có thể lưu trạng thái của file dưới dạng lịch sử cập nhật. Vì thế, có thể đưa file đã chỉnh sửa về trạng thái cũ hay có thể biết được file đã được chỉnh sửa chỗ nào do ai đã chỉnh sửa.

Thêm nữa, khi định ghi đè (overwrite) lên file mới nhất đã chỉnh sửa của người khác bằng file đã chỉnh sửa dựa trên file cũ, thì khi upload lên server sẽ hiện ra cảnh cáo. Vì thế, sẽ không xảy ra lỗi khi ghi đè lên nội dung chỉnh sửa của người khác mà không hề hay biết.

Git sử dụng mô hình phân tán, mỗi thành viên trong team sẽ có một repository ở máy của riêng mình. Điều đó có nghĩa là nếu có 3 người A,B,C cùng làm việc trong một project. Thì bản thân repo trên máy của người A, người B, và người C có thể kết nối được với nhau.

Trong mô hình Git sẽ luôn có một server lưu trữ chính để cả team cùng kết nối thông qua đó (Có thể là Github, bitbucket, ...). Ngoài ra mỗi người trong team đều có thể kết nối đến máy tính của nhau thông qua SSH.
### 2. Github-Gitlap
<img src="https://cdn-images-1.medium.com/max/1600/1*OLsrVuctE2DO924KoSkNLA.png">
GitHub là một dịch vụ cung cấp kho lưu trữ mã nguồn Git dựa trên nền web cho các dự án phát triển phần mềm. GitHub cung cấp cả phiên bản trả tiền lẫn miễn phí cho các tài khoản. 

GitLab là một phần mềm có nhiệm vụ quản lý kho code Git. Gitlab sở hữu các tính năng đơn giản, góp phần to lớn trong việc giúp các doanh nghiệp, cá nhân, tổ chức lưu trữ code một cách nhanh chóng vô cùng, người dùng hoàn toàn có thể truy cập mọi lúc mọi nơi miễn là có kết nối Internet.

Gitlab cũng có khá nhiều điểm tương đồng với GitHub nhưng GitHub đi theo hướng kinh doanh nhiều hơn, bởi vì nếu bạn sở hữu kho code riêng và muốn ẩn chúng khỏi cộng đồng hoặc mở rộng hơn nữa thì bạn sẽ phải trả phí cho dịch vụ này. Gitlab hoàn toàn ngược lại, bạn có thể ẩn kho code của mình, không công khai chúng cho bất kỳ ai, trong trường hợp vượt quá ngưỡng miễn phí thì bạn mới phải mất phí để mua thêm dịch vụ.

## II. các khái niệm liên quan và thực hành với Git

### 1. Repository (repo)

Repository hay được gọi tắt là Repo, đơn giản là nơi chứa tất cả những thông tin cần thiết để quản lý các sửa đổi và lịch sử của toàn bộ project. Tất cả dữ liệu của Repo đều được chứa trong thư mục bạn đang làm việc dưới dạng folder ẩn có tên là .git

Nên bạn phải chú ý không được xóa thư mục này đi, nếu không sẽ mất thông tin quan trọng.

Repository của Git được phân thành 2 loại là remote repository và local repository.

Remote repository: Là repository dùng để chia sẽ giữa nhiều người và bố trí trên server chuyên dụng.

Local repository: Là repository ở trên máy tính của chính bản thân mình, dành cho một người dùng sử dụng.

Thường thì trong quá trình làm việc chúng ta sẽ làm việc trên local repo, tức là lưu trữ trên máy của mình. Khi muốn chia sẽ nó đến người dùng khác khi đã hoàn thành thì sẽ đẩy code (Push) lên Remote repo.

### 2. Nhánh (Branch)
> Tính năng nổi bật của Git 
<img src="https://github.com/nghuuquyen/sociss-class-nodejs/blob/master/src/git-tutorials/images/feature-branch.png">
Nhánh có thể hiểu như là một không gian làm việc (workspace), Ví dụ khi bạn muốn tạo một tính năng A mới bạn sẽ tạo ra một nhánh mới để làm tính năng A. Đồng thời trong lúc bạn làm tính năng A thì bạn cũng có thể tạo ra một nhánh mới để sửa lỗi cho dự án của mình. Hai không gian làm việc này hoàn toàn không động đến nhau, nên dù tính năng A đã làm xong hay chưa đều không ảnh hưởng đến các nhánh (không gian làm việc) khác.

Trong một project sẽ luôn có một nhánh chính (mặc định) gọi là master. Tính năng được tạo ra trong các nhánh phụ sẽ được hợp nhất lại vào master khi đã làm xong, hành động này gọi là merge

### 3. Merge
<img src="https://github.com/hocchudong/ghichep-Git/blob/master/images/git-term-5.png">

Merge là hành động khi bạn muốn nhập mã nguồn từ một nhánh khác vào nhánh hiện tại.
### 4. Commit
<img src="https://github.com/nghuuquyen/sociss-class-nodejs/blob/master/src/git-tutorials/images/git-commits.png">

` Commit ` là thao tác để ghi lại lịch sử việc thêm, thay đổi file hay thư mục vào repository.

Khi thực hiện commit, trong repository sẽ tạo ra commit (hoặc revision) đã ghi lại sự khác biệt từ trạng thái đã commit lần trước với trạng thái hiện tại.

Commit này đang được chứa tại repository, các commit nối tiếp với nhau theo thứ tự thời gian. Bằng việc lần theo commit thì có thể biết được lịch sử thay đổi trong quá khứ.
### 5. Conflict 
<img src="https://github.com/hocchudong/ghichep-Git/blob/master/images/git-term-4.png">

` Conflic ` là trường hợp có 2 sự thay đổi trong một dòng code và máy tính không thể tự quyết định dòng code nào là “đúng”.
Để giải quyết mâu thuẫn bạn phải dùng “tay không” để sữa các xung đột này. Bạn chỉ việc nhìn vào file bị conflict và tự quyết định dòng code nào giữ lại, dòng nào xóa bỏ.
### 6. Thao tác với git 
> Thao tác trên macOS
#### Mô hình làm việc của Git
<img src="https://trello-attachments.s3.amazonaws.com/5bfb91aab58a9002b322f5e7/5cde24cbd3bec82328d65b18/7ec5305a3695462484544ce3a1fae804/image.png">

- Clone
là thao tác tải mã nguồn từ một remote server về máy tính,chỉ tải về máy local repository nhánh master.

> git clone [ link github]

ex: git clone https://github.com/dhvsplg99999/dummy.git

#### Sơ đồ Commit
<img src="https://github.com/nghuuquyen/sociss-class-nodejs/blob/master/src/git-tutorials/images/git-staging-area.png">

- Add
là thao tác đẩy một tệp tin từ working directory vào staging area để chuẩn bị cho việc commit.
> git add [tên file]
ex : muốn add file README.md t dùng lệnh ` git add README.md `
Ngoài ra khi muốn add các file đã thực hiện ta dùng lệnh ` git add . `
- Staging area
là nơi để chuẩn bị cho việc commit vào repository.
- Commit
> git commit -m "nội dung commit"
- Push 
là thao tác đẩy mã nguồn hiện tại đã được commit của bạn lên remote server.
> git push origin [tên nhánh]
- Pull 
là thao tác lấy mã nguồn từ một hoặc nhiều nhánh cụ thể nào đó ở remote server nào đó về local repository trên máy tính của bạn
> git pull origin [tên nhánh]

[Note](https://github.com/dhvsplg99999/dummy/blob/master/note.md)
