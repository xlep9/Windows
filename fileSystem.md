NTFS (New Technology File System) là một cách (một phương thức) mà Windows dùng để tổ chức và quản lý dữ liệu trên ổ cứng.
Hãy tưởng tượng ổ cứng = thư viện lớn
NTFS chính là cách thư viện đó sắp xếp sách
NTFS thuộc về phần mềm của hệ điều hành Windows.
Ổ cứng chỉ là thiết bị để chứa dữ liệu. Còn NTFS là “cách Windows quản lý dữ liệu trên ổ cứng”.
NTFS được tích hợp sẵn trong hệ điều hành Windows.

On NTFS volumes, you can set permissions that grant or deny access to files and folders.

The permissions are:

<img width="880" height="439" alt="image" src="https://github.com/user-attachments/assets/0e76ffb2-0fb4-4d32-b87a-f35477363a73" />


======================================================================

Remote Desktop Protocol (RDP) là một giao thức (protocol) do Microsoft tạo ra, cho phép bạn điều khiển một máy tính từ xa thông qua mạng Internet hoặc mạng nội bộ.

======================================================================

Biến môi trường (Environment variables) = đặt biệt danh (tên ngắn) cho những đường dẫn hoặc thông tin dài và khó nhớ.
example: environment variable for the Windows directory is %windir%.
Xem all Environment variables: 
Windows + R, gõ cmd, nhấn Enter
Gõ set

<img width="736" height="362" alt="image" src="https://github.com/user-attachments/assets/34decaaa-b08a-4a31-81bd-cc8d474ec9ec" />

======================================================================

ADS (Alternate Data Streams) - Luồng Dữ liệu Thay thế. Đây là một tính năng của hệ thống tệp tin NTFS trong các hệ điều hành Windows, cho phép một tệp tin có thể chứa nhiều hơn một luồng dữ liệu (data stream). Luồng dữ liệu chính chứa nội dung tệp tin như bình thường, nhưng có thể có các luồng phụ ẩn chứa thêm các thông tin khác, chẳng hạn như thông tin bảo mật, thuộc tính tệp tin, hoặc thậm chí là các tệp thực thi độc hại, khiến cho người dùng thông thường khó phát hiện bằng các công cụ quản lý tệp tin tiêu chuẩn.
Mỗi file bình thường có 1 “Luồng dữ liệu chính” chứa nội dung file.
ADS cho phép tạo nhiều dòng dữ liệu khác, ẩn bên trong cùng 1 file, mà Windows Explorer không hiển thị.

<img width="765" height="646" alt="image" src="https://github.com/user-attachments/assets/438a8d4e-9334-44d1-a5ac-091c6ff7a697" />


https://www.malwarebytes.com/blog/101/2015/07/introduction-to-alternate-data-streams

=======================================================================

UAC (User Account Control)

1. Người dùng gia đình thường dùng tài khoản Admin

Nhiều người dùng Windows đăng nhập bằng tài khoản quản trị viên (Admin).
→ Nghĩa là họ có quyền thay đổi hệ thống: cài phần mềm, chỉnh cấu hình, thêm tài khoản, v.v.

2. Nhưng không cần quyền Admin cho các công việc bình thường

Ví dụ:

Lướt web

Gõ Word

Xem phim

Những việc này không cần quyền cao, nhưng nếu bạn vẫn dùng Admin, bạn tự tăng rủi ro bị malware tấn công.

3. Vì sao nguy hiểm?

Nếu bạn dùng tài khoản Admin:

Malware chạy = nó cũng có quyền Admin

Nó có thể cài phần mềm độc, thay đổi hệ thống, ẩn mình, cướp quyền…
-> UAC (User Account Control) ra đời để bảo vệ người dùng

Microsoft tạo ra UAC để giảm rủi ro khi người dùng dùng tài khoản Admin.
UAC hoạt động như thế nào?

Khi bạn dùng tài khoản Admin:
Windows không cho bạn quyền Admin toàn bộ ngay lập tức.
Bạn chỉ chạy ở quyền thông thường.
Khi phần mềm cần quyền cao → Windows sẽ hiện cửa sổ UAC hỏi:
“Bạn có cho phép chương trình này làm thay đổi hệ thống không?”

Nếu bạn đồng ý → Windows cấp quyền admin tạm thời.
Nếu không → chương trình không được cài đặt/thực thi.

===================================================





