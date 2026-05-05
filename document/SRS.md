# SOFTWARE REQUIREMENTS SPECIFICATION  
# HỆ THỐNG QUẢN LÝ QUÁN CÀ PHÊ

---

## 1. Thông tin tài liệu

| Mục | Nội dung |
|---|---|
| Tên dự án | Hệ thống quản lý quán cà phê |
| Tên tiếng Anh | Coffee Shop Management System |
| Loại tài liệu | Software Requirements Specification |
| Phiên bản | 1.0 |
| Ngày cập nhật | [Điền ngày] |
| Nhóm thực hiện | [Điền tên nhóm] |
| Môn học | Công nghệ phần mềm |
| Giảng viên hướng dẫn | [Điền tên giảng viên] |

---

## 2. Mục đích tài liệu

Tài liệu này mô tả chi tiết các yêu cầu phần mềm của **Hệ thống quản lý quán cà phê**. SRS được xây dựng dựa trên tài liệu BRD nhằm chuyển các yêu cầu nghiệp vụ thành các yêu cầu cụ thể để phục vụ cho quá trình thiết kế, lập trình, kiểm thử và nghiệm thu hệ thống.

Mục tiêu của tài liệu gồm:

- Xác định rõ các chức năng mà hệ thống phải cung cấp.
- Xác định actor sử dụng từng chức năng.
- Mô tả đầu vào, xử lý, đầu ra và điều kiện chấp nhận của từng yêu cầu chức năng.
- Xác định các yêu cầu phi chức năng.
- Làm cơ sở xây dựng Use Case Diagram, Sequence Diagram, Class Diagram, ERD và Test Case.
- Đảm bảo các thành viên trong nhóm hiểu thống nhất về phạm vi và cách hoạt động của hệ thống.

---

## 3. Phạm vi hệ thống

Hệ thống quản lý quán cà phê là một ứng dụng web hỗ trợ số hóa hoạt động vận hành của quán cà phê quy mô nhỏ hoặc vừa.

Trong phiên bản hiện tại, hệ thống tập trung vào các chức năng chính sau:

- Đăng nhập hệ thống.
- Phân quyền người dùng theo vai trò.
- Quản lý tài khoản nhân viên.
- Quản lý bàn.
- Xem trạng thái bàn.
- Quản lý menu.
- Tạo order cho từng bàn.
- Cập nhật order trong quá trình phục vụ.
- Theo dõi trạng thái order.
- Thanh toán hóa đơn.
- Tra cứu lịch sử giao dịch.
- Xem báo cáo doanh thu cơ bản.

Các nhóm người dùng chính của hệ thống gồm:

- Quản lý.
- Nhân viên phục vụ.
- Thu ngân.

Trong phiên bản hiện tại, hệ thống không bao gồm:

- Thanh toán online qua cổng thanh toán thật.
- Tích hợp máy in hóa đơn vật lý.
- Quản lý kho nguyên liệu chi tiết.
- Quản lý nhà cung cấp.
- Quản lý khách hàng thân thiết phức tạp.
- Tích điểm hoặc xếp hạng thành viên.
- Quản lý nhiều chi nhánh.
- Ứng dụng di động độc lập.
- Đặt hàng online từ khách hàng ngoài quán.
- Tích hợp giao hàng với bên thứ ba.

---

## 4. Định nghĩa và từ viết tắt

| Thuật ngữ | Giải thích |
|---|---|
| Actor | Người dùng hoặc vai trò tương tác với hệ thống |
| User | Người dùng có tài khoản đăng nhập vào hệ thống |
| Role | Vai trò của người dùng trong hệ thống |
| Menu | Danh sách món ăn, đồ uống mà quán đang kinh doanh |
| Order | Danh sách món mà khách hàng gọi tại một bàn |
| Order Item | Một món cụ thể trong order, gồm món, số lượng, đơn giá và thành tiền |
| Hóa đơn | Thông tin thanh toán được tạo từ order |
| Payment | Thông tin phương thức và trạng thái thanh toán |
| BRD | Business Requirements Document |
| SRS | Software Requirements Specification |
| FR | Functional Requirement |
| NFR | Non-functional Requirement |
| AC | Acceptance Criteria |

---

## 5. Mô tả tổng quan hệ thống

### 5.1. Bối cảnh hệ thống

Nhiều quán cà phê hiện vẫn quản lý hoạt động phục vụ bằng phương pháp thủ công như ghi order bằng giấy, tính tiền bằng máy tính đơn giản hoặc tổng hợp doanh thu bằng Excel. Cách làm này dễ dẫn đến nhầm món, nhầm bàn, sai tổng tiền, khó kiểm soát trạng thái phục vụ và mất thời gian tra cứu lịch sử giao dịch.

Hệ thống quản lý quán cà phê được xây dựng nhằm hỗ trợ các hoạt động quản lý bàn, menu, order, thanh toán, nhân viên và doanh thu trên cùng một nền tảng.

### 5.2. Mục tiêu hệ thống

Hệ thống cần đạt các mục tiêu sau:

- Giảm sai sót khi nhận order và thanh toán.
- Tăng tốc độ phục vụ khách hàng.
- Quản lý tập trung bàn, menu, order và hóa đơn.
- Hỗ trợ phân quyền rõ ràng giữa quản lý, nhân viên phục vụ và thu ngân.
- Hỗ trợ quản lý xem doanh thu cơ bản.
- Tạo nền tảng để mở rộng thêm các chức năng trong tương lai.

### 5.3. Nhóm người dùng

#### 5.3.1. Quản lý

Quản lý là người có quyền cao trong hệ thống. Quản lý có thể:

- Quản lý tài khoản nhân viên.
- Quản lý danh sách bàn.
- Quản lý menu.
- Xem báo cáo doanh thu.
- Tra cứu lịch sử giao dịch.
- Theo dõi hoạt động order và thanh toán.

#### 5.3.2. Nhân viên phục vụ

Nhân viên phục vụ là người trực tiếp tiếp nhận yêu cầu gọi món từ khách hàng. Nhân viên phục vụ có thể:

- Xem danh sách bàn.
- Xem trạng thái bàn.
- Tạo order cho bàn.
- Thêm món vào order.
- Sửa số lượng món trong order.
- Xóa món khỏi order trước khi thanh toán.

#### 5.3.3. Thu ngân

Thu ngân là người chịu trách nhiệm thanh toán hóa đơn cho khách hàng. Thu ngân có thể:

- Xem order cần thanh toán.
- Xem chi tiết hóa đơn.
- Kiểm tra tổng tiền.
- Chọn phương thức thanh toán.
- Xác nhận thanh toán.
- Tra cứu lịch sử hóa đơn.

### 5.4. Giả định

- Mỗi người dùng có một tài khoản riêng để đăng nhập.
- Mỗi tài khoản được gán một vai trò cụ thể.
- Mỗi bàn tại một thời điểm chỉ có một order đang hoạt động.
- Các món trong menu có trạng thái “Còn bán” hoặc “Tạm ngừng bán”.
- Dữ liệu sử dụng trong đồ án là dữ liệu mô phỏng.
- Hệ thống được triển khai ở mức phục vụ demo môn học.

### 5.5. Ràng buộc

- Hệ thống được phát triển trong phạm vi đồ án môn học nên thời gian triển khai có hạn.
- Hệ thống chưa tích hợp máy POS, máy in hóa đơn hoặc thiết bị phần cứng thật.
- Thanh toán chuyển khoản chỉ được mô phỏng, chưa kết nối ngân hàng hoặc ví điện tử thật.
- Một số chức năng nâng cao sẽ không nằm trong phiên bản đầu tiên.

---

## 6. Yêu cầu chức năng

---

### FR-01. Đăng nhập

**Mô tả:**  
Hệ thống cho phép người dùng đăng nhập bằng tên đăng nhập và mật khẩu.

**Actor:**  
Quản lý, Nhân viên phục vụ, Thu ngân.

**Đầu vào:**

- Tên đăng nhập.
- Mật khẩu.

**Xử lý:**

- Kiểm tra người dùng đã nhập đầy đủ tên đăng nhập và mật khẩu.
- Đối chiếu thông tin tài khoản trong cơ sở dữ liệu.
- Kiểm tra trạng thái tài khoản còn hoạt động hay không.
- Xác định vai trò của người dùng.
- Tạo phiên đăng nhập nếu thông tin hợp lệ.

**Đầu ra:**

- Nếu đăng nhập thành công, hệ thống chuyển người dùng đến giao diện chính phù hợp với vai trò.
- Nếu đăng nhập thất bại, hệ thống hiển thị thông báo lỗi.

**Điều kiện chấp nhận:**

- Người dùng có tài khoản hợp lệ có thể đăng nhập vào hệ thống.
- Người dùng nhập sai tên đăng nhập hoặc mật khẩu không thể truy cập hệ thống.
- Người dùng bị khóa tài khoản không thể đăng nhập.
- Sau khi đăng nhập thành công, người dùng được nhận đúng vai trò.

---

### FR-02. Phân quyền người dùng

**Mô tả:**  
Hệ thống phải giới hạn chức năng mà người dùng có thể truy cập dựa trên vai trò của họ.

**Actor:**  
Hệ thống.

**Đầu vào:**

- Thông tin tài khoản người dùng.
- Vai trò của người dùng.

**Xử lý:**

- Kiểm tra vai trò sau khi người dùng đăng nhập.
- Hiển thị menu chức năng tương ứng với vai trò.
- Chặn truy cập nếu người dùng cố truy cập chức năng không thuộc quyền của mình.

**Đầu ra:**

- Người dùng chỉ nhìn thấy và sử dụng được các chức năng phù hợp với vai trò.

**Điều kiện chấp nhận:**

- Quản lý có thể truy cập chức năng quản lý bàn, menu, nhân viên, báo cáo và lịch sử giao dịch.
- Nhân viên phục vụ chỉ có thể xem bàn, tạo order và cập nhật order.
- Thu ngân chỉ có thể xem hóa đơn, thanh toán và tra cứu lịch sử hóa đơn.
- Người dùng không có quyền không thể truy cập chức năng quản lý.

---

### FR-03. Quản lý nhân viên

**Mô tả:**  
Hệ thống cho phép quản lý thêm, sửa, khóa hoặc cập nhật thông tin tài khoản nhân viên.

**Actor:**  
Quản lý.

**Đầu vào:**

- Mã nhân viên.
- Họ tên nhân viên.
- Tên đăng nhập.
- Mật khẩu.
- Vai trò.
- Trạng thái tài khoản.

**Xử lý:**

- Kiểm tra dữ liệu bắt buộc.
- Kiểm tra tên đăng nhập có bị trùng hay không.
- Tạo mới hoặc cập nhật tài khoản nhân viên.
- Cho phép khóa tài khoản nhân viên nếu cần.

**Đầu ra:**

- Danh sách nhân viên được cập nhật.
- Thông báo kết quả thao tác.

**Điều kiện chấp nhận:**

- Quản lý có thể thêm nhân viên mới khi dữ liệu hợp lệ.
- Không cho phép tạo hai tài khoản trùng tên đăng nhập.
- Quản lý có thể cập nhật vai trò và trạng thái tài khoản.
- Chỉ quản lý mới được sử dụng chức năng này.

---

### FR-04. Quản lý bàn

**Mô tả:**  
Hệ thống cho phép quản lý thêm, sửa, xóa và cập nhật trạng thái bàn trong quán.

**Actor:**  
Quản lý.

**Đầu vào:**

- Mã bàn.
- Tên bàn hoặc số bàn.
- Khu vực nếu có.
- Trạng thái bàn.

**Xử lý:**

- Kiểm tra dữ liệu bàn hợp lệ.
- Lưu hoặc cập nhật thông tin bàn.
- Kiểm tra trạng thái bàn trước khi xóa.
- Không cho phép xóa bàn đang có order hoạt động.

**Đầu ra:**

- Danh sách bàn được cập nhật.
- Thông báo kết quả thao tác.

**Điều kiện chấp nhận:**

- Quản lý có thể thêm bàn mới khi dữ liệu hợp lệ.
- Quản lý có thể sửa thông tin bàn.
- Không cho phép xóa bàn nếu bàn đang có order hoạt động.
- Trạng thái bàn được hiển thị chính xác.

---

### FR-05. Xem trạng thái bàn

**Mô tả:**  
Hệ thống cho phép người dùng xem danh sách bàn và trạng thái hiện tại của từng bàn.

**Actor:**  
Quản lý, Nhân viên phục vụ, Thu ngân.

**Đầu vào:**

- Yêu cầu xem danh sách bàn.

**Xử lý:**

- Truy xuất danh sách bàn từ cơ sở dữ liệu.
- Lấy trạng thái hiện tại của từng bàn.
- Hiển thị danh sách bàn theo dạng dễ quan sát.

**Đầu ra:**

- Danh sách bàn.
- Trạng thái từng bàn.

**Trạng thái bàn gồm:**

- Trống.
- Đang phục vụ.
- Chờ thanh toán.
- Tạm ngừng sử dụng.

**Điều kiện chấp nhận:**

- Hệ thống hiển thị đầy đủ danh sách bàn.
- Mỗi bàn có trạng thái rõ ràng.
- Trạng thái bàn được cập nhật sau khi tạo order hoặc thanh toán.

---

### FR-06. Quản lý menu

**Mô tả:**  
Hệ thống cho phép quản lý thêm, sửa, xóa hoặc cập nhật thông tin món trong menu.

**Actor:**  
Quản lý.

**Đầu vào:**

- Mã món.
- Tên món.
- Loại món.
- Giá bán.
- Mô tả ngắn.
- Trạng thái món.

**Xử lý:**

- Kiểm tra dữ liệu món.
- Kiểm tra giá bán phải lớn hơn hoặc bằng 0.
- Lưu thông tin món vào hệ thống.
- Cập nhật trạng thái món còn bán hoặc tạm ngừng bán.
- Không cho phép chọn món tạm ngừng bán khi tạo order.

**Đầu ra:**

- Danh sách món được cập nhật.
- Thông báo kết quả thao tác.

**Điều kiện chấp nhận:**

- Quản lý có thể thêm món mới.
- Quản lý có thể sửa tên món, giá bán, loại món và trạng thái món.
- Không cho phép nhập giá âm.
- Món tạm ngừng bán không được thêm vào order mới.

---

### FR-07. Tạo order cho bàn

**Mô tả:**  
Hệ thống cho phép nhân viên phục vụ tạo order cho một bàn cụ thể.

**Actor:**  
Nhân viên phục vụ.

**Đầu vào:**

- Bàn được chọn.
- Danh sách món.
- Số lượng từng món.
- Ghi chú nếu có.

**Xử lý:**

- Kiểm tra bàn có tồn tại hay không.
- Kiểm tra bàn có được phép tạo order hay không.
- Hiển thị danh sách món còn bán.
- Kiểm tra số lượng món phải lớn hơn 0.
- Tạo order mới.
- Lưu chi tiết các món trong order.
- Tính tổng tiền tạm tính.
- Cập nhật trạng thái bàn thành “Đang phục vụ”.

**Đầu ra:**

- Order mới được tạo.
- Chi tiết order được lưu.
- Tổng tiền tạm tính được hiển thị.
- Bàn chuyển sang trạng thái “Đang phục vụ”.

**Điều kiện chấp nhận:**

- Nhân viên có thể tạo order khi bàn hợp lệ.
- Nhân viên có thể thêm nhiều món vào một order.
- Không cho phép tạo order nếu không chọn món.
- Không cho phép thêm món đang tạm ngừng bán.
- Sau khi tạo order thành công, trạng thái bàn chuyển thành “Đang phục vụ”.

---

### FR-08. Cập nhật order

**Mô tả:**  
Hệ thống cho phép nhân viên phục vụ cập nhật order trong quá trình phục vụ khi khách gọi thêm món, đổi số lượng hoặc xóa món trước khi thanh toán.

**Actor:**  
Nhân viên phục vụ.

**Đầu vào:**

- Mã order.
- Món cần thêm.
- Số lượng cần sửa.
- Món cần xóa.
- Ghi chú nếu có.

**Xử lý:**

- Kiểm tra order có tồn tại hay không.
- Kiểm tra order còn đang hoạt động hay đã thanh toán.
- Cho phép thêm món mới nếu món còn bán.
- Cho phép sửa số lượng nếu số lượng hợp lệ.
- Cho phép xóa món khỏi order nếu order chưa thanh toán.
- Tính lại tổng tiền tạm tính.

**Đầu ra:**

- Order được cập nhật.
- Danh sách món trong order được thay đổi.
- Tổng tiền tạm tính được cập nhật.

**Điều kiện chấp nhận:**

- Có thể thêm món vào order chưa thanh toán.
- Có thể sửa số lượng món trong order chưa thanh toán.
- Có thể xóa món khỏi order chưa thanh toán.
- Order đã thanh toán không được phép chỉnh sửa.
- Tổng tiền tạm tính thay đổi đúng theo dữ liệu order.

---

### FR-09. Theo dõi trạng thái order

**Mô tả:**  
Hệ thống cho phép theo dõi trạng thái order trong quá trình phục vụ.

**Actor:**  
Quản lý, Nhân viên phục vụ, Thu ngân.

**Đầu vào:**

- Mã order.
- Yêu cầu xem trạng thái order.

**Xử lý:**

- Truy xuất thông tin order.
- Xác định trạng thái hiện tại của order.
- Hiển thị trạng thái order trên giao diện.

**Đầu ra:**

- Trạng thái order hiện tại.

**Trạng thái order gồm:**

- Mới tạo.
- Đang phục vụ.
- Chờ thanh toán.
- Đã thanh toán.
- Đã hủy.

**Điều kiện chấp nhận:**

- Hệ thống hiển thị đúng trạng thái của order.
- Khi order được tạo, trạng thái ban đầu là “Mới tạo” hoặc “Đang phục vụ”.
- Khi khách yêu cầu thanh toán, trạng thái order chuyển thành “Chờ thanh toán”.
- Sau khi thanh toán thành công, trạng thái order chuyển thành “Đã thanh toán”.

---

### FR-10. Thanh toán hóa đơn

**Mô tả:**  
Hệ thống cho phép thu ngân thực hiện thanh toán cho order.

**Actor:**  
Thu ngân.

**Đầu vào:**

- Mã order.
- Phương thức thanh toán.
- Ghi chú thanh toán nếu có.

**Xử lý:**

- Hiển thị chi tiết order.
- Kiểm tra order chưa thanh toán.
- Tính tổng tiền dựa trên danh sách món, số lượng và đơn giá.
- Ghi nhận phương thức thanh toán.
- Tạo hóa đơn thanh toán.
- Cập nhật trạng thái order thành “Đã thanh toán”.
- Cập nhật trạng thái bàn về “Trống”.
- Lưu lịch sử thanh toán.

**Đầu ra:**

- Hóa đơn được tạo.
- Thanh toán được ghi nhận thành công.
- Order chuyển sang trạng thái “Đã thanh toán”.
- Bàn chuyển về trạng thái “Trống”.

**Phương thức thanh toán tối thiểu:**

- Tiền mặt.
- Chuyển khoản giả lập.

**Điều kiện chấp nhận:**

- Thu ngân có thể xem chi tiết order cần thanh toán.
- Hệ thống tính tổng tiền chính xác.
- Thu ngân có thể chọn phương thức thanh toán.
- Sau khi xác nhận thanh toán, hóa đơn được lưu.
- Sau thanh toán, order chuyển sang trạng thái “Đã thanh toán”.
- Sau thanh toán, bàn chuyển về trạng thái “Trống”.

---

### FR-11. Tra cứu lịch sử giao dịch

**Mô tả:**  
Hệ thống cho phép quản lý hoặc thu ngân tra cứu các hóa đơn đã thanh toán.

**Actor:**  
Quản lý, Thu ngân.

**Đầu vào:**

- Mã hóa đơn.
- Ngày thanh toán.
- Khoảng thời gian.
- Bàn.
- Nhân viên lập order.

**Xử lý:**

- Tìm kiếm hóa đơn trong cơ sở dữ liệu.
- Lọc hóa đơn theo tiêu chí được nhập.
- Hiển thị danh sách kết quả phù hợp.
- Cho phép xem chi tiết hóa đơn.

**Đầu ra:**

- Danh sách hóa đơn tìm được.
- Thông tin chi tiết hóa đơn.

**Điều kiện chấp nhận:**

- Có thể tìm hóa đơn theo thời gian.
- Có thể tìm hóa đơn theo bàn.
- Có thể tìm hóa đơn theo mã hóa đơn.
- Nếu không có kết quả, hệ thống hiển thị thông báo phù hợp.
- Người dùng có thể xem chi tiết hóa đơn đã thanh toán.

---

### FR-12. Xem báo cáo doanh thu

**Mô tả:**  
Hệ thống cho phép quản lý xem báo cáo doanh thu theo thời gian.

**Actor:**  
Quản lý.

**Đầu vào:**

- Ngày.
- Tháng.
- Khoảng thời gian tùy chọn.

**Xử lý:**

- Lấy dữ liệu từ các hóa đơn đã thanh toán.
- Tính tổng doanh thu.
- Tính số lượng hóa đơn đã thanh toán.
- Thống kê món bán chạy nếu có dữ liệu.
- Hiển thị kết quả báo cáo.

**Đầu ra:**

- Báo cáo doanh thu theo ngày.
- Báo cáo doanh thu theo tháng.
- Báo cáo doanh thu theo khoảng thời gian.
- Số lượng hóa đơn.
- Món bán chạy nếu có.

**Điều kiện chấp nhận:**

- Báo cáo chỉ tính các hóa đơn đã thanh toán.
- Quản lý có thể xem doanh thu theo ngày.
- Quản lý có thể xem doanh thu theo tháng.
- Quản lý có thể xem doanh thu theo khoảng thời gian tùy chọn.
- Tổng doanh thu hiển thị đúng theo dữ liệu hóa đơn.

---

### FR-13. Thống kê món bán chạy

**Mô tả:**  
Hệ thống cho phép quản lý xem danh sách các món được bán nhiều trong một khoảng thời gian.

**Actor:**  
Quản lý.

**Đầu vào:**

- Ngày.
- Tháng.
- Khoảng thời gian tùy chọn.

**Xử lý:**

- Lấy dữ liệu từ order item của các hóa đơn đã thanh toán.
- Tính tổng số lượng bán ra của từng món.
- Sắp xếp danh sách món theo số lượng bán giảm dần.

**Đầu ra:**

- Danh sách món bán chạy.
- Số lượng bán ra của từng món.

**Điều kiện chấp nhận:**

- Chỉ thống kê món thuộc các hóa đơn đã thanh toán.
- Hiển thị được tên món và số lượng bán.
- Kết quả được sắp xếp theo số lượng bán ra.

---

## 7. Yêu cầu phi chức năng

### NFR-01. Hiệu năng

- Các thao tác chính như đăng nhập, xem danh sách bàn, tạo order, cập nhật order và thanh toán phải phản hồi dưới 3 giây với dữ liệu demo.
- Hệ thống phải xử lý ổn định khi có nhiều bàn đang được phục vụ cùng lúc trong phạm vi quán nhỏ hoặc vừa.

### NFR-02. Tính dễ sử dụng

- Giao diện phải rõ ràng, dễ nhìn và phù hợp với người dùng không chuyên về công nghệ.
- Các chức năng thường dùng như chọn bàn, chọn món, tạo order và thanh toán phải thao tác đơn giản.
- Thông báo lỗi phải dễ hiểu để người dùng biết cách xử lý.

### NFR-03. Bảo mật

- Người dùng phải đăng nhập trước khi sử dụng hệ thống.
- Mật khẩu cần được lưu trữ an toàn, không hiển thị trực tiếp trên giao diện.
- Hệ thống phải kiểm tra quyền truy cập theo vai trò.
- Người dùng không có quyền không được truy cập chức năng quản lý.

### NFR-04. Tính ổn định

- Hệ thống cần hoạt động ổn định trong quá trình demo các luồng nghiệp vụ chính.
- Dữ liệu order, hóa đơn và doanh thu phải được lưu nhất quán.
- Khi thao tác thất bại, hệ thống cần thông báo lỗi rõ ràng.

### NFR-05. Khả năng mở rộng

- Hệ thống cần cho phép mở rộng trong tương lai như quản lý kho, đặt bàn online, khách hàng thân thiết hoặc thanh toán điện tử.
- Cấu trúc hệ thống cần được chia thành các module rõ ràng để dễ nâng cấp.

### NFR-06. Khả năng bảo trì

- Mã nguồn cần được tổ chức theo cấu trúc rõ ràng.
- Tên biến, tên hàm, tên class và tên bảng dữ liệu cần dễ hiểu.
- Các thành phần giao diện, xử lý nghiệp vụ và truy cập dữ liệu nên được tách biệt.
- Tài liệu hướng dẫn cài đặt, deployment và kiểm thử cần được chuẩn bị đầy đủ.

---

## 8. Business Rules

| Mã | Quy tắc nghiệp vụ |
|---|---|
| Rule-01 | Mỗi bàn tại một thời điểm chỉ có một order đang hoạt động. |
| Rule-02 | Chỉ bàn có trạng thái “Trống” hoặc “Đang phục vụ” mới được tạo hoặc cập nhật order. |
| Rule-03 | Khi tạo order cho bàn trống, trạng thái bàn phải chuyển thành “Đang phục vụ”. |
| Rule-04 | Món có trạng thái “Tạm ngừng bán” không được thêm vào order mới. |
| Rule-05 | Order đã thanh toán không được phép chỉnh sửa món hoặc số lượng. |
| Rule-06 | Khi khách yêu cầu thanh toán, trạng thái order chuyển thành “Chờ thanh toán”. |
| Rule-07 | Sau khi thanh toán thành công, trạng thái order chuyển thành “Đã thanh toán”. |
| Rule-08 | Sau khi thanh toán thành công, trạng thái bàn chuyển về “Trống”. |
| Rule-09 | Doanh thu chỉ tính các hóa đơn đã thanh toán thành công. |
| Rule-10 | Người dùng chỉ được sử dụng chức năng phù hợp với vai trò được phân quyền. |
| Rule-11 | Tên đăng nhập của mỗi nhân viên phải là duy nhất. |
| Rule-12 | Không được xóa bàn nếu bàn đang có order hoạt động. |

---

## 9. Use Case liên quan

| Mã Use Case | Tên Use Case | Actor chính | Yêu cầu chức năng liên quan |
|---|---|---|---|
| UC-01 | Đăng nhập | Quản lý, Nhân viên phục vụ, Thu ngân | FR-01 |
| UC-02 | Phân quyền người dùng | Hệ thống | FR-02 |
| UC-03 | Quản lý nhân viên | Quản lý | FR-03 |
| UC-04 | Quản lý bàn | Quản lý | FR-04 |
| UC-05 | Xem trạng thái bàn | Quản lý, Nhân viên phục vụ, Thu ngân | FR-05 |
| UC-06 | Quản lý menu | Quản lý | FR-06 |
| UC-07 | Tạo order cho bàn | Nhân viên phục vụ | FR-07 |
| UC-08 | Cập nhật order | Nhân viên phục vụ | FR-08 |
| UC-09 | Theo dõi trạng thái order | Quản lý, Nhân viên phục vụ, Thu ngân | FR-09 |
| UC-10 | Thanh toán hóa đơn | Thu ngân | FR-10 |
| UC-11 | Tra cứu lịch sử giao dịch | Quản lý, Thu ngân | FR-11 |
| UC-12 | Xem báo cáo doanh thu | Quản lý | FR-12 |
| UC-13 | Thống kê món bán chạy | Quản lý | FR-13 |

---

## 10. Ràng buộc giao diện

Hệ thống cần có tối thiểu các màn hình sau:

| Màn hình | Người dùng sử dụng | Mô tả |
|---|---|---|
| Màn hình đăng nhập | Tất cả người dùng | Nhập tên đăng nhập và mật khẩu |
| Màn hình trang chính | Tất cả người dùng | Hiển thị chức năng theo vai trò |
| Màn hình quản lý nhân viên | Quản lý | Thêm, sửa, khóa tài khoản nhân viên |
| Màn hình quản lý bàn | Quản lý | Thêm, sửa, xóa và cập nhật bàn |
| Màn hình danh sách bàn | Quản lý, Nhân viên phục vụ, Thu ngân | Xem trạng thái bàn |
| Màn hình quản lý menu | Quản lý | Thêm, sửa, xóa món và cập nhật giá |
| Màn hình tạo order | Nhân viên phục vụ | Chọn bàn, chọn món, nhập số lượng |
| Màn hình cập nhật order | Nhân viên phục vụ | Thêm, sửa, xóa món trong order |
| Màn hình thanh toán hóa đơn | Thu ngân | Xem chi tiết order và xác nhận thanh toán |
| Màn hình lịch sử giao dịch | Quản lý, Thu ngân | Tra cứu hóa đơn đã thanh toán |
| Màn hình báo cáo doanh thu | Quản lý | Xem doanh thu theo thời gian |
| Màn hình thống kê món bán chạy | Quản lý | Xem món bán nhiều |

---

## 11. Ràng buộc dữ liệu

Hệ thống cần có các thực thể dữ liệu cơ bản sau:

| Thực thể | Mô tả |
|---|---|
| Role | Lưu thông tin vai trò người dùng |
| User | Lưu thông tin tài khoản nhân viên |
| CoffeeTable | Lưu thông tin bàn trong quán |
| Category | Lưu loại món |
| MenuItem | Lưu thông tin món ăn, đồ uống |
| Order | Lưu thông tin order của từng bàn |
| OrderDetail | Lưu chi tiết các món trong order |
| Invoice | Lưu thông tin hóa đơn |
| Payment | Lưu thông tin thanh toán |

### 11.1. Quan hệ dữ liệu cơ bản

- Một Role có nhiều User.
- Một User có thể tạo nhiều Order.
- Một CoffeeTable có nhiều Order theo thời gian.
- Tại một thời điểm, một CoffeeTable chỉ có một Order đang hoạt động.
- Một Category có nhiều MenuItem.
- Một Order có nhiều OrderDetail.
- Một MenuItem có thể xuất hiện trong nhiều OrderDetail.
- Một Order sau khi thanh toán sẽ tạo một Invoice.
- Một Invoice có một Payment.

### 11.2. Trạng thái dữ liệu

#### Trạng thái bàn

- Trống.
- Đang phục vụ.
- Chờ thanh toán.
- Tạm ngừng sử dụng.

#### Trạng thái món

- Còn bán.
- Tạm ngừng bán.

#### Trạng thái order

- Mới tạo.
- Đang phục vụ.
- Chờ thanh toán.
- Đã thanh toán.
- Đã hủy.

#### Trạng thái thanh toán

- Chưa thanh toán.
- Đã thanh toán.
- Đã hủy.

---

## 12. Tiêu chí chấp nhận hệ thống

Hệ thống được xem là đạt yêu cầu khi:

1. Người dùng đăng nhập được đúng với tài khoản và vai trò đã cấp.
2. Hệ thống phân quyền đúng theo vai trò quản lý, nhân viên phục vụ và thu ngân.
3. Quản lý có thể quản lý bàn, menu và nhân viên.
4. Nhân viên phục vụ có thể xem bàn, tạo order và cập nhật order.
5. Thu ngân có thể xem chi tiết order và thanh toán hóa đơn.
6. Sau khi tạo order, trạng thái bàn chuyển thành “Đang phục vụ”.
7. Sau khi thanh toán, order chuyển thành “Đã thanh toán”.
8. Sau khi thanh toán, bàn chuyển về trạng thái “Trống”.
9. Quản lý có thể xem báo cáo doanh thu cơ bản.
10. Doanh thu chỉ tính từ các hóa đơn đã thanh toán.
11. Người dùng có thể tra cứu lịch sử giao dịch.
12. Hệ thống hoạt động ổn định trong các luồng nghiệp vụ chính khi demo.

---

## 13. Ma trận truy vết yêu cầu

| Mã yêu cầu | Nguồn gốc từ BRD | Use Case | Kiểm thử dự kiến |
|---|---|---|---|
| FR-01 | BR-01 | UC-01 | TC-01, TC-02, TC-03 |
| FR-02 | BR-01 | UC-02 | TC-04, TC-05 |
| FR-03 | BR-02 | UC-03 | TC-06, TC-07 |
| FR-04 | BR-03 | UC-04 | TC-08, TC-09, TC-10 |
| FR-05 | BR-03 | UC-05 | TC-11 |
| FR-06 | BR-04 | UC-06 | TC-12, TC-13, TC-14 |
| FR-07 | BR-05 | UC-07 | TC-15, TC-16, TC-17 |
| FR-08 | BR-06 | UC-08 | TC-18, TC-19, TC-20 |
| FR-09 | BR-07 | UC-09 | TC-21, TC-22 |
| FR-10 | BR-08 | UC-10 | TC-23, TC-24, TC-25 |
| FR-11 | BR-09 | UC-11 | TC-26, TC-27 |
| FR-12 | BR-10 | UC-12 | TC-28, TC-29 |
| FR-13 | BR-10 | UC-13 | TC-30 |

---

## 14. Danh sách kiểm thử dự kiến

| Mã test case | Chức năng | Mục tiêu kiểm thử |
|---|---|---|
| TC-01 | Đăng nhập | Đăng nhập thành công với tài khoản hợp lệ |
| TC-02 | Đăng nhập | Đăng nhập thất bại khi sai mật khẩu |
| TC-03 | Đăng nhập | Tài khoản bị khóa không thể đăng nhập |
| TC-04 | Phân quyền | Quản lý thấy đúng chức năng quản lý |
| TC-05 | Phân quyền | Nhân viên không truy cập được chức năng quản lý |
| TC-06 | Quản lý nhân viên | Thêm nhân viên hợp lệ |
| TC-07 | Quản lý nhân viên | Không cho tạo tài khoản trùng tên đăng nhập |
| TC-08 | Quản lý bàn | Thêm bàn mới |
| TC-09 | Quản lý bàn | Cập nhật trạng thái bàn |
| TC-10 | Quản lý bàn | Không cho xóa bàn đang có order hoạt động |
| TC-11 | Xem trạng thái bàn | Hiển thị đúng trạng thái từng bàn |
| TC-12 | Quản lý menu | Thêm món hợp lệ |
| TC-13 | Quản lý menu | Không cho nhập giá âm |
| TC-14 | Quản lý menu | Món tạm ngừng bán không được chọn khi tạo order |
| TC-15 | Tạo order | Tạo order thành công cho bàn hợp lệ |
| TC-16 | Tạo order | Không cho tạo order nếu không chọn món |
| TC-17 | Tạo order | Sau khi tạo order, bàn chuyển sang đang phục vụ |
| TC-18 | Cập nhật order | Thêm món vào order chưa thanh toán |
| TC-19 | Cập nhật order | Sửa số lượng món trong order |
| TC-20 | Cập nhật order | Không cho sửa order đã thanh toán |
| TC-21 | Trạng thái order | Order chuyển đúng trạng thái trong quá trình phục vụ |
| TC-22 | Trạng thái order | Order chuyển thành đã thanh toán sau khi thanh toán |
| TC-23 | Thanh toán | Tính tổng tiền chính xác |
| TC-24 | Thanh toán | Thanh toán thành công và lưu hóa đơn |
| TC-25 | Thanh toán | Sau thanh toán, bàn chuyển về trống |
| TC-26 | Lịch sử giao dịch | Tra cứu hóa đơn theo thời gian |
| TC-27 | Lịch sử giao dịch | Hiển thị thông báo nếu không tìm thấy hóa đơn |
| TC-28 | Báo cáo doanh thu | Xem doanh thu theo ngày |
| TC-29 | Báo cáo doanh thu | Doanh thu chỉ tính hóa đơn đã thanh toán |
| TC-30 | Thống kê món bán chạy | Hiển thị món bán chạy theo số lượng bán |

---

## 15. Kết luận

Tài liệu SRS này mô tả chi tiết các yêu cầu phần mềm của **Hệ thống quản lý quán cà phê** dựa trên tài liệu BRD. Nội dung SRS giúp chuyển các yêu cầu nghiệp vụ thành các yêu cầu chức năng, phi chức năng, quy tắc nghiệp vụ, ràng buộc giao diện, ràng buộc dữ liệu và tiêu chí kiểm thử cụ thể.

Tài liệu này là cơ sở để nhóm tiếp tục thực hiện các bước tiếp theo gồm:

- Xây dựng Use Case Diagram.
- Mô tả Use Case.
- Thiết kế Activity Diagram.
- Thiết kế Sequence Diagram.
- Thiết kế Class Diagram.
- Thiết kế ERD.
- Lập kế hoạch kiểm thử.
- Xây dựng test case.
- Lập trình chức năng.
- Chuẩn bị hướng dẫn cài đặt và deployment.
- Hoàn thiện slide và video demo.
