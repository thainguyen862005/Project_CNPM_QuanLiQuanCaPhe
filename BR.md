# BUSINESS REQUIREMENTS DOCUMENT (BRD)
# Hệ thống quản lý quán cà phê

## 1. Thông tin tài liệu

| Mục | Nội dung |
|---|---|
| Tên dự án | Hệ thống quản lý quán cà phê |
| Tên tiếng Anh | Coffee Shop Management System |
| Môn học | Công nghệ phần mềm |
| Loại tài liệu | Business Requirements Document |
| Phiên bản | 1.0 |
| Ngày cập nhật | [Điền ngày] |
| Nhóm thực hiện | [Điền tên nhóm] |
| Giảng viên hướng dẫn | [Điền tên giảng viên] |

---

## 2. Mục đích tài liệu

Tài liệu này mô tả các yêu cầu nghiệp vụ cho dự án **Hệ thống quản lý quán cà phê**.  
Mục tiêu của tài liệu là:

- Xác định bài toán thực tế cần giải quyết.
- Làm rõ mục tiêu kinh doanh và nhu cầu của các bên liên quan.
- Xác định phạm vi dự án.
- Mô tả các chức năng nghiệp vụ chính của hệ thống.
- Làm cơ sở cho các giai đoạn phân tích, thiết kế, lập trình và kiểm thử.

---

## 3. Bối cảnh và bài toán thực tế

Trong thực tế, nhiều quán cà phê nhỏ và vừa vẫn quản lý hoạt động bán hàng bằng phương pháp thủ công hoặc sử dụng nhiều công cụ rời rạc như sổ tay, Excel, ghi chú giấy hoặc ứng dụng đơn lẻ. Điều này dẫn đến nhiều vấn đề trong vận hành hằng ngày, bao gồm:

- Nhân viên dễ ghi nhầm món hoặc nhầm bàn.
- Khó theo dõi trạng thái bàn đang trống, đang phục vụ hoặc đã thanh toán.
- Việc tính tiền dễ sai sót khi order thay đổi nhiều lần.
- Chủ quán khó theo dõi doanh thu theo ngày, tuần, tháng.
- Khó quản lý menu, giá bán và tình trạng hoạt động của món.
- Mất nhiều thời gian tổng hợp báo cáo thủ công cuối ngày.
- Khó phân quyền giữa nhân viên phục vụ, thu ngân và quản lý.

Từ đó, cần xây dựng một hệ thống phần mềm giúp số hóa quy trình vận hành quán cà phê, hỗ trợ quản lý tập trung, giảm sai sót và nâng cao hiệu quả kinh doanh.

---

## 4. Mục tiêu kinh doanh

Hệ thống được xây dựng nhằm đáp ứng các mục tiêu kinh doanh sau:

1. **Tăng tốc độ phục vụ khách hàng** thông qua việc tạo và xử lý order nhanh chóng.
2. **Giảm sai sót trong ghi nhận order và thanh toán**.
3. **Quản lý bàn, menu và hóa đơn tập trung** trên cùng một hệ thống.
4. **Hỗ trợ kiểm soát doanh thu** theo từng khoảng thời gian.
5. **Nâng cao hiệu quả làm việc của nhân viên** nhờ giao diện đơn giản, trực quan.
6. **Tạo nền tảng để mở rộng trong tương lai**, ví dụ như đặt bàn trước, quản lý kho hoặc tích hợp thanh toán điện tử.

---

## 5. Phạm vi dự án

### 5.1. Phạm vi trong dự án

Hệ thống sẽ hỗ trợ các nghiệp vụ chính sau:

- Đăng nhập và phân quyền người dùng.
- Quản lý thông tin bàn.
- Quản lý menu đồ uống và món ăn.
- Tạo order cho từng bàn.
- Cập nhật order trong quá trình phục vụ.
- Tính tiền và thanh toán hóa đơn.
- Quản lý tài khoản nhân viên.
- Theo dõi doanh thu và báo cáo cơ bản.

### 5.2. Phạm vi ngoài dự án

Trong giai đoạn hiện tại, hệ thống **chưa** bao gồm các tính năng sau:

- Thanh toán online qua cổng thanh toán thực tế.
- Quản lý kho nguyên liệu chi tiết.
- Tích hợp máy in hóa đơn thật.
- Chương trình khách hàng thân thiết phức tạp.
- Quản lý chuỗi nhiều chi nhánh.
- Ứng dụng di động độc lập.
- Tích hợp giao hàng với bên thứ ba.

---

## 6. Các bên liên quan

| Bên liên quan | Vai trò | Mối quan tâm |
|---|---|---|
| Chủ quán | Người sở hữu hệ thống | Quản lý doanh thu, kiểm soát vận hành, xem báo cáo |
| Quản lý | Điều hành hoạt động quán | Quản lý nhân viên, bàn, menu, giám sát order |
| Nhân viên phục vụ | Tạo và cập nhật order | Thao tác nhanh, dễ dùng, chính xác |
| Thu ngân | Thanh toán hóa đơn | Tính tiền đúng, thao tác ổn định |
| Khách hàng | Người sử dụng dịch vụ quán | Phục vụ nhanh, hóa đơn rõ ràng |
| Nhóm phát triển | Xây dựng hệ thống | Yêu cầu rõ ràng, phạm vi phù hợp |
| Giảng viên hướng dẫn | Đánh giá đồ án | Tính thực tế, đầy đủ tài liệu, khả năng triển khai |

---

## 7. Người dùng mục tiêu

Hệ thống có các nhóm người dùng chính như sau:

### 7.1. Quản trị viên / Quản lý
- Quản lý tài khoản nhân viên.
- Quản lý bàn và menu.
- Xem báo cáo doanh thu.
- Kiểm soát hoạt động chung của quán.

### 7.2. Nhân viên phục vụ
- Xem trạng thái bàn.
- Tạo order cho khách.
- Cập nhật món trong order.
- Gửi yêu cầu phục vụ đến quầy pha chế hoặc bộ phận liên quan.

### 7.3. Thu ngân
- Xem thông tin order cần thanh toán.
- Tính tổng tiền hóa đơn.
- Ghi nhận hình thức thanh toán.
- Hoàn tất giao dịch.

### 7.4. Khách hàng
- Gọi món tại quán thông qua nhân viên.
- Nhận hóa đơn và thanh toán.
- Trong phiên bản mở rộng có thể xem menu bằng QR hoặc đặt bàn trước.

---

## 8. Mô tả quy trình nghiệp vụ hiện tại

### 8.1. Quy trình hiện tại
Quy trình hoạt động ở nhiều quán cà phê hiện nay thường diễn ra như sau:

1. Khách vào quán và chọn bàn.
2. Nhân viên ghi order bằng giấy hoặc ghi nhớ thủ công.
3. Order được chuyển cho quầy pha chế.
4. Khi khách gọi thêm món, nhân viên tiếp tục cập nhật bằng tay.
5. Khi thanh toán, thu ngân cộng tiền thủ công hoặc dùng máy tính đơn giản.
6. Cuối ngày, quản lý tổng hợp doanh thu bằng sổ hoặc Excel.

### 8.2. Hạn chế của quy trình hiện tại
- Dễ ghi sai món hoặc sai số lượng.
- Dễ nhầm bàn khi quán đông.
- Không đồng bộ dữ liệu giữa phục vụ, thu ngân và quản lý.
- Tốn thời gian đối chiếu hóa đơn.
- Khó truy xuất báo cáo, lịch sử giao dịch và thống kê doanh thu.

---

## 9. Giải pháp đề xuất

Đề xuất xây dựng một hệ thống quản lý quán cà phê dưới dạng ứng dụng web, cho phép các vai trò trong quán thao tác trên cùng một nền tảng.

Hệ thống sẽ cung cấp các khả năng chính:

- Quản lý tập trung thông tin bàn, menu, order và hóa đơn.
- Hỗ trợ nhân viên phục vụ thao tác nhanh khi nhận món.
- Hỗ trợ thu ngân tính tiền chính xác.
- Hỗ trợ quản lý theo dõi doanh thu và giám sát hoạt động quán.
- Cung cấp dữ liệu rõ ràng, giảm phụ thuộc vào thao tác thủ công.

---

## 10. Yêu cầu nghiệp vụ

### BR-01. Quản lý người dùng và phân quyền
Hệ thống phải cho phép tạo, chỉnh sửa và quản lý tài khoản người dùng theo vai trò, bao gồm quản lý, nhân viên phục vụ và thu ngân.  
Mỗi vai trò chỉ được sử dụng các chức năng phù hợp với phạm vi công việc.

**Giá trị nghiệp vụ:**  
Đảm bảo an toàn thông tin và phân chia trách nhiệm rõ ràng trong vận hành.

---

### BR-02. Quản lý bàn trong quán
Hệ thống phải cho phép quản lý danh sách bàn và trạng thái của từng bàn như:
- Trống
- Đang phục vụ
- Đã đặt trước
- Chờ thanh toán

**Giá trị nghiệp vụ:**  
Giúp nhân viên theo dõi bàn nhanh chóng, tránh nhầm lẫn trong quá trình phục vụ.

---

### BR-03. Quản lý menu
Hệ thống phải cho phép quản lý danh mục món và thông tin từng sản phẩm, bao gồm:
- Tên món
- Loại món
- Giá bán
- Mô tả ngắn
- Trạng thái còn bán / tạm ngừng bán

**Giá trị nghiệp vụ:**  
Giúp chủ quán dễ dàng cập nhật menu khi thay đổi giá hoặc thêm món mới.

---

### BR-04. Tạo và quản lý order
Hệ thống phải cho phép nhân viên tạo order theo từng bàn, thêm món, chỉnh sửa số lượng hoặc xóa món nếu khách thay đổi yêu cầu.

**Giá trị nghiệp vụ:**  
Giúp quá trình phục vụ chính xác, cập nhật kịp thời và giảm nhầm lẫn.

---

### BR-05. Theo dõi trạng thái order
Hệ thống phải cho phép theo dõi trạng thái order trong quá trình phục vụ, ví dụ:
- Mới tạo
- Đang chuẩn bị
- Đã phục vụ
- Đã thanh toán

**Giá trị nghiệp vụ:**  
Hỗ trợ điều phối công việc trong quán và kiểm soát tiến độ phục vụ.

---

### BR-06. Tính tiền và thanh toán
Hệ thống phải tự động tính tổng tiền hóa đơn dựa trên các món đã order, số lượng, giảm giá hoặc voucher nếu có.

Hệ thống phải hỗ trợ ghi nhận ít nhất các hình thức thanh toán:
- Tiền mặt
- Chuyển khoản giả lập

**Giá trị nghiệp vụ:**  
Giảm sai sót khi thanh toán và rút ngắn thời gian tính hóa đơn.

---

### BR-07. Báo cáo doanh thu
Hệ thống phải cung cấp báo cáo doanh thu cơ bản theo:
- Ngày
- Tháng
- Khoảng thời gian tùy chọn

Ngoài ra, hệ thống nên hỗ trợ thống kê:
- Số lượng hóa đơn
- Món bán chạy
- Tổng doanh thu theo ca hoặc theo nhân viên nếu mở rộng

**Giá trị nghiệp vụ:**  
Giúp chủ quán và quản lý nắm được tình hình kinh doanh, từ đó ra quyết định phù hợp.

---

### BR-08. Quản lý nhân viên
Hệ thống phải cho phép quản lý danh sách nhân viên, trạng thái làm việc và vai trò của từng người dùng trong hệ thống.

**Giá trị nghiệp vụ:**  
Giúp quản lý dễ kiểm soát tài khoản và trách nhiệm của từng nhân viên.

---

### BR-09. Tra cứu lịch sử giao dịch
Hệ thống phải cho phép tra cứu các order và hóa đơn đã thanh toán theo thời gian, bàn hoặc người lập order.

**Giá trị nghiệp vụ:**  
Hỗ trợ đối soát dữ liệu, kiểm tra sai sót và phục vụ công tác quản lý.

---

## 11. Danh sách yêu cầu chức năng mức cao

| Mã | Tên yêu cầu | Mô tả ngắn |
|---|---|---|
| FR-01 | Đăng nhập | Người dùng đăng nhập bằng tài khoản và mật khẩu |
| FR-02 | Phân quyền | Hệ thống giới hạn chức năng theo vai trò |
| FR-03 | Quản lý bàn | Thêm, sửa, xóa, cập nhật trạng thái bàn |
| FR-04 | Quản lý menu | Thêm, sửa, xóa món và cập nhật giá |
| FR-05 | Tạo order | Tạo order cho từng bàn |
| FR-06 | Cập nhật order | Thêm món, sửa số lượng, xóa món |
| FR-07 | Xem chi tiết hóa đơn | Hiển thị danh sách món và tổng tiền |
| FR-08 | Thanh toán | Xác nhận thanh toán và lưu giao dịch |
| FR-09 | Quản lý nhân viên | Thêm, sửa, khóa tài khoản nhân viên |
| FR-10 | Báo cáo doanh thu | Xem doanh thu theo ngày, tháng |
| FR-11 | Tra cứu lịch sử | Tìm lại các hóa đơn đã thanh toán |

---

## 12. Yêu cầu phi chức năng

### 12.1. Hiệu năng
- Hệ thống phải phản hồi thao tác thông thường trong thời gian ngắn.
- Thời gian tải dữ liệu đối với các chức năng chính nên dưới 3 giây trong điều kiện sử dụng thông thường.

### 12.2. Tính dễ sử dụng
- Giao diện phải đơn giản, dễ hiểu, phù hợp với người dùng không chuyên về công nghệ.
- Các thao tác tạo order và thanh toán phải ngắn gọn, trực quan.

### 12.3. Bảo mật
- Người dùng phải đăng nhập để sử dụng hệ thống.
- Mật khẩu cần được lưu trữ an toàn.
- Phải có phân quyền để tránh truy cập trái phép.

### 12.4. Tính sẵn sàng
- Hệ thống cần hoạt động ổn định trong giờ mở cửa của quán.
- Dữ liệu phải được lưu trữ và truy xuất nhất quán.

### 12.5. Khả năng mở rộng
- Thiết kế hệ thống cần cho phép mở rộng thêm các chức năng trong tương lai như quản lý kho, đặt bàn online hoặc khách hàng thân thiết.

### 12.6. Khả năng bảo trì
- Mã nguồn cần được tổ chức rõ ràng, dễ đọc, dễ chỉnh sửa.
- Dữ liệu và tài liệu cần được lưu trữ có cấu trúc phục vụ cho bảo trì sau này.

---

## 13. Giả định và ràng buộc

### 13.1. Giả định
- Quán cà phê có quy mô nhỏ hoặc vừa.
- Mỗi bàn tại một thời điểm chỉ có một order đang hoạt động.
- Nhân viên được đào tạo cơ bản để sử dụng hệ thống.
- Dữ liệu mạng nội bộ hoặc kết nối cơ bản luôn sẵn sàng trong quá trình sử dụng.

### 13.2. Ràng buộc
- Dự án thực hiện trong phạm vi môn học nên thời gian phát triển có hạn.
- Hệ thống được xây dựng ở mức mô phỏng thực tế, chưa tích hợp các thiết bị phần cứng thật.
- Một số chức năng nâng cao sẽ không nằm trong phiên bản đầu tiên.

---

## 14. Tiêu chí thành công của dự án

Dự án được xem là thành công khi đáp ứng được các tiêu chí sau:

1. Hệ thống cho phép quản lý bàn, menu, order và thanh toán trên cùng một nền tảng.
2. Nhân viên có thể tạo và cập nhật order nhanh chóng.
3. Thu ngân có thể tính tiền chính xác và lưu giao dịch.
4. Quản lý có thể xem báo cáo doanh thu cơ bản.
5. Hệ thống có phân quyền người dùng rõ ràng.
6. Hệ thống chạy ổn định và demo được các luồng nghiệp vụ chính.
7. Tài liệu phân tích, thiết kế và mã nguồn được tổ chức đầy đủ trên GitHub.

---

## 15. Tiêu chí chấp nhận nghiệp vụ

### AC-01. Đăng nhập
- Người dùng hợp lệ có thể đăng nhập vào hệ thống.
- Người dùng không hợp lệ không được truy cập.

### AC-02. Quản lý bàn
- Hệ thống hiển thị được danh sách bàn và trạng thái của từng bàn.
- Nhân viên có thể chọn đúng bàn để tạo order.

### AC-03. Tạo order
- Nhân viên có thể thêm nhiều món vào một order.
- Có thể cập nhật số lượng hoặc xóa món trước khi thanh toán.

### AC-04. Thanh toán
- Hệ thống tự động tính tổng tiền chính xác.
- Sau khi thanh toán, trạng thái bàn được cập nhật về trống.

### AC-05. Báo cáo
- Quản lý có thể xem tổng doanh thu theo ngày hoặc tháng.
- Dữ liệu doanh thu phản ánh đúng các hóa đơn đã thanh toán.

---

## 16. Rủi ro nghiệp vụ

| Rủi ro | Mô tả | Hướng xử lý |
|---|---|---|
| Sai phạm vi | Làm quá nhiều tính năng so với thời gian | Giới hạn phạm vi vào các chức năng cốt lõi |
| Thiếu tính thực tế | Chức năng không phản ánh đúng quán cà phê | Bám sát quy trình order, bàn, thanh toán thực tế |
| Giao diện khó dùng | Nhân viên thao tác chậm | Thiết kế giao diện đơn giản, ưu tiên luồng chính |
| Sai số liệu doanh thu | Tính toán hóa đơn không chính xác | Kiểm thử kỹ các ca order và thanh toán |
| Phân quyền chưa rõ | Người dùng truy cập sai chức năng | Thiết kế role rõ ngay từ đầu |

---

## 17. Định hướng mở rộng trong tương lai

Sau khi hoàn thành phiên bản đầu tiên, hệ thống có thể được mở rộng theo các hướng sau:

- Khách hàng xem menu bằng mã QR.
- Đặt bàn trước qua website.
- Quản lý kho nguyên liệu.
- Quản lý chương trình khuyến mãi và voucher nâng cao.
- Quản lý khách hàng thân thiết.
- Tích hợp thanh toán online.
- Hỗ trợ nhiều chi nhánh.

---

## 18. Kết luận

Hệ thống quản lý quán cà phê là một đề tài phù hợp với môn Công nghệ phần mềm vì có tính thực tế cao, quy trình nghiệp vụ rõ ràng và có thể triển khai thành một sản phẩm mô phỏng hoàn chỉnh.

Việc xây dựng hệ thống này giúp giải quyết các vấn đề thường gặp trong quản lý quán cà phê như sai sót trong order, khó kiểm soát bàn, mất thời gian tính tiền và thiếu báo cáo doanh thu. Đồng thời, đây cũng là nền tảng tốt để áp dụng các kiến thức về phân tích yêu cầu, thiết kế hệ thống, lập trình, kiểm thử và quản lý tài liệu dự án.

---
## 19. Phụ lục: Danh sách module đề xuất

### Module 1: Quản lý đăng nhập và phân quyền
- Đăng nhập
- Đăng xuất
- Phân quyền theo vai trò

### Module 2: Quản lý bàn
- Danh sách bàn
- Trạng thái bàn
- Cập nhật trạng thái

### Module 3: Quản lý menu
- Danh mục món
- Danh sách sản phẩm
- Giá bán
- Trạng thái món

### Module 4: Quản lý order
- Tạo order
- Cập nhật order
- Xem chi tiết order

### Module 5: Thanh toán
- Tính tổng tiền
- Chọn phương thức thanh toán
- Xác nhận thanh toán

### Module 6: Báo cáo
- Doanh thu theo ngày
- Doanh thu theo tháng
- Thống kê món bán chạy

### Module 7: Quản lý nhân viên
- Danh sách nhân viên
- Tạo tài khoản
- Phân vai trò

---
## 20. Thông tin nhóm thực hiện

| Họ và tên | MSSV | Vai trò trong nhóm |
|---|---|---|
| [Thành viên 1] | [MSSV] | [Ví dụ: Phân tích yêu cầu, backend] |
| Nguyễn Hoàng Thái | 23130296 | Phân tích yêu cầu, backend,Cơ sở dữ liệu, kiểm thử |
| [Thành viên 3] | [MSSV] | [Ví dụ: Cơ sở dữ liệu, kiểm thử] |
