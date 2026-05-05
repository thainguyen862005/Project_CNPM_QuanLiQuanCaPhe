# BUSINESS REQUIREMENTS DOCUMENT  
# HỆ THỐNG QUẢN LÝ QUÁN CÀ PHÊ

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

## 2. Giới thiệu tổng quan đề tài

Trong hoạt động kinh doanh quán cà phê, đặc biệt là các quán có quy mô nhỏ và vừa, việc quản lý bán hàng, bàn, order, thanh toán và doanh thu thường được thực hiện bằng phương pháp thủ công hoặc thông qua nhiều công cụ rời rạc như giấy ghi order, sổ tay, Excel hoặc các ứng dụng đơn lẻ. Cách quản lý này có thể đáp ứng nhu cầu cơ bản, nhưng khi số lượng khách tăng hoặc quán hoạt động vào giờ cao điểm, nhiều vấn đề dễ phát sinh như ghi nhầm món, nhầm bàn, tính tiền sai, khó kiểm soát trạng thái phục vụ và mất nhiều thời gian tổng hợp doanh thu cuối ngày.

Vì vậy, đề tài **Hệ thống quản lý quán cà phê** được đề xuất nhằm xây dựng một phần mềm hỗ trợ số hóa quy trình vận hành quán cà phê. Hệ thống giúp nhân viên phục vụ tạo và cập nhật order nhanh chóng, thu ngân thanh toán chính xác, quản lý theo dõi bàn, menu, nhân viên và doanh thu trên cùng một nền tảng. Đây là một đề tài có tính thực tế cao, phù hợp với môn Công nghệ phần mềm vì có đầy đủ các hoạt động phân tích yêu cầu, thiết kế hệ thống, lập trình, kiểm thử và triển khai sản phẩm mô phỏng.

---

## 3. Mục đích tài liệu

Tài liệu này được xây dựng nhằm mô tả các yêu cầu nghiệp vụ của dự án **Hệ thống quản lý quán cà phê**. Đây là cơ sở để nhóm phát triển hiểu rõ bài toán, phạm vi, người dùng, chức năng cần xây dựng và tiêu chí đánh giá sản phẩm.

Cụ thể, tài liệu nhằm các mục đích sau:

- Xác định bài toán thực tế mà hệ thống cần giải quyết.
- Làm rõ mục tiêu kinh doanh của dự án.
- Xác định các bên liên quan và người dùng mục tiêu.
- Mô tả phạm vi chức năng của hệ thống.
- Đưa ra các yêu cầu nghiệp vụ, yêu cầu chức năng và yêu cầu phi chức năng.
- Làm cơ sở để xây dựng Use Case Diagram, Sequence Diagram, Class Diagram, Database Diagram, phần implement và kiểm thử.

---

## 4. Bối cảnh và bài toán thực tế

Hiện nay, nhiều quán cà phê vẫn quản lý hoạt động phục vụ và bán hàng bằng phương pháp thủ công. Khi khách vào quán, nhân viên thường ghi order bằng giấy hoặc ghi nhớ, sau đó chuyển thông tin cho thu ngân hoặc quầy pha chế. Khi khách gọi thêm món, đổi món hoặc chuyển bàn, thông tin có thể không được cập nhật kịp thời. Điều này làm tăng nguy cơ sai sót trong quá trình phục vụ.

Một số vấn đề thường gặp trong quy trình quản lý thủ công gồm:

- Nhân viên dễ ghi sai món, sai số lượng hoặc nhầm bàn.
- Khó theo dõi bàn nào đang trống, đang phục vụ hoặc chờ thanh toán.
- Khi khách gọi thêm món, việc cập nhật order dễ bị thiếu hoặc trùng.
- Thu ngân có thể tính sai tổng tiền nếu order thay đổi nhiều lần.
- Chủ quán khó xem doanh thu theo ngày, tháng hoặc khoảng thời gian cụ thể.
- Khó quản lý menu, giá bán và trạng thái món còn bán hoặc tạm ngừng bán.
- Việc phân quyền giữa quản lý, nhân viên phục vụ và thu ngân chưa rõ ràng.
- Dữ liệu bán hàng phân tán, khó tra cứu lại lịch sử giao dịch.

Từ những vấn đề trên, cần xây dựng một hệ thống phần mềm giúp quản lý tập trung các hoạt động chính trong quán cà phê, giảm thao tác thủ công, hạn chế sai sót và nâng cao hiệu quả vận hành.

---

## 5. Mục tiêu kinh doanh

Hệ thống quản lý quán cà phê được xây dựng nhằm đạt các mục tiêu sau:

1. **Tăng tốc độ phục vụ khách hàng**  
   Hỗ trợ nhân viên tạo order nhanh, cập nhật món dễ dàng và theo dõi trạng thái bàn trực quan.

2. **Giảm sai sót trong quá trình order và thanh toán**  
   Hệ thống lưu trữ thông tin order theo từng bàn, tự động tính tổng tiền dựa trên món và số lượng đã chọn.

3. **Quản lý tập trung bàn, menu, order và hóa đơn**  
   Tất cả dữ liệu quan trọng được quản lý trên cùng một hệ thống thay vì ghi chép rời rạc.

4. **Hỗ trợ quản lý doanh thu**  
   Chủ quán hoặc quản lý có thể xem báo cáo doanh thu theo ngày, tháng hoặc khoảng thời gian tùy chọn.

5. **Phân quyền người dùng rõ ràng**  
   Mỗi vai trò như quản lý, nhân viên phục vụ và thu ngân chỉ được sử dụng các chức năng phù hợp với nhiệm vụ.

6. **Tạo nền tảng mở rộng trong tương lai**  
   Hệ thống có thể phát triển thêm các chức năng như đặt bàn online, quét mã QR để xem menu, quản lý kho nguyên liệu hoặc tích hợp thanh toán điện tử.

---

## 6. Phạm vi dự án

### 6.1. Phạm vi trong dự án

Trong phiên bản hiện tại, hệ thống tập trung vào các chức năng cốt lõi phục vụ hoạt động quản lý quán cà phê, bao gồm:

- Đăng nhập hệ thống.
- Phân quyền người dùng theo vai trò.
- Quản lý tài khoản nhân viên.
- Quản lý danh sách bàn.
- Theo dõi trạng thái bàn.
- Quản lý menu đồ uống và món ăn.
- Tạo order cho từng bàn.
- Cập nhật order khi khách gọi thêm, đổi số lượng hoặc xóa món.
- Theo dõi trạng thái order.
- Tính tiền và thanh toán hóa đơn.
- Lưu lịch sử hóa đơn đã thanh toán.
- Xem báo cáo doanh thu cơ bản.
- Thống kê món bán chạy ở mức cơ bản nếu đủ thời gian triển khai.

### 6.2. Phạm vi ngoài dự án

Trong giai đoạn hiện tại, hệ thống chưa triển khai các chức năng nâng cao sau:

- Thanh toán online qua cổng thanh toán thật.
- Tích hợp máy in hóa đơn vật lý.
- Quản lý kho nguyên liệu chi tiết.
- Quản lý nhà cung cấp.
- Quản lý khách hàng thân thiết phức tạp.
- Tích điểm, xếp hạng thành viên.
- Quản lý nhiều chi nhánh.
- Ứng dụng di động độc lập.
- Tích hợp giao hàng với bên thứ ba.
- Đặt hàng online từ khách hàng ngoài quán.

---

## 7. Các bên liên quan

| Bên liên quan | Vai trò | Mối quan tâm |
|---|---|---|
| Chủ quán | Người sở hữu hệ thống | Theo dõi doanh thu, kiểm soát hoạt động, đánh giá hiệu quả kinh doanh |
| Quản lý | Người điều hành quán | Quản lý nhân viên, bàn, menu, order và báo cáo |
| Nhân viên phục vụ | Người tiếp nhận và cập nhật order | Thao tác nhanh, dễ dùng, tránh nhầm bàn và nhầm món |
| Thu ngân | Người thực hiện thanh toán | Tính tiền chính xác, lưu hóa đơn, cập nhật trạng thái bàn |
| Khách hàng | Người sử dụng dịch vụ tại quán | Được phục vụ nhanh, hóa đơn rõ ràng, thanh toán thuận tiện |
| Nhóm phát triển | Người xây dựng hệ thống | Yêu cầu rõ ràng, phạm vi phù hợp, dễ thiết kế và triển khai |
| Giảng viên hướng dẫn | Người đánh giá đồ án | Tính thực tế, đầy đủ tài liệu, có sản phẩm demo và kiểm thử |

---

## 8. Người dùng mục tiêu

### 8.1. Quản lý

Quản lý là người có quyền cao trong hệ thống, chịu trách nhiệm điều hành hoạt động của quán. Người dùng này có thể quản lý nhân viên, bàn, menu, xem báo cáo doanh thu và theo dõi hoạt động bán hàng.

Các chức năng chính của quản lý gồm:

- Quản lý tài khoản nhân viên.
- Quản lý danh sách bàn.
- Quản lý menu.
- Xem báo cáo doanh thu.
- Tra cứu lịch sử giao dịch.
- Theo dõi hoạt động order và thanh toán.

### 8.2. Nhân viên phục vụ

Nhân viên phục vụ là người trực tiếp tiếp nhận yêu cầu gọi món từ khách hàng. Vai trò này cần giao diện đơn giản, thao tác nhanh và dễ theo dõi trạng thái bàn.

Các chức năng chính của nhân viên phục vụ gồm:

- Xem danh sách bàn.
- Xem trạng thái bàn.
- Tạo order cho bàn.
- Thêm món vào order.
- Cập nhật số lượng món.
- Xóa món khỏi order khi khách thay đổi yêu cầu.

### 8.3. Thu ngân

Thu ngân là người chịu trách nhiệm kiểm tra hóa đơn và thực hiện thanh toán cho khách hàng.

Các chức năng chính của thu ngân gồm:

- Xem order cần thanh toán.
- Xem chi tiết hóa đơn.
- Kiểm tra tổng tiền.
- Chọn phương thức thanh toán.
- Xác nhận thanh toán.
- Lưu hóa đơn.
- Tra cứu lịch sử thanh toán.

### 8.4. Khách hàng

Khách hàng không trực tiếp sử dụng hệ thống trong phiên bản hiện tại. Tuy nhiên, khách hàng là đối tượng được hưởng lợi từ hệ thống thông qua việc được phục vụ nhanh hơn, order chính xác hơn và nhận hóa đơn rõ ràng hơn.

Trong phiên bản mở rộng, khách hàng có thể được hỗ trợ xem menu qua mã QR hoặc đặt bàn trước qua website.

---

## 9. Quy trình nghiệp vụ hiện tại

### 9.1. Quy trình thủ công hiện tại

Quy trình phục vụ tại nhiều quán cà phê hiện nay thường diễn ra như sau:

1. Khách hàng vào quán và chọn bàn.
2. Nhân viên phục vụ đến bàn để ghi nhận món khách gọi.
3. Nhân viên ghi order bằng giấy hoặc ghi nhớ.
4. Order được chuyển cho quầy pha chế hoặc thu ngân.
5. Khi khách gọi thêm món, nhân viên tiếp tục ghi bổ sung.
6. Khi khách yêu cầu thanh toán, thu ngân kiểm tra order.
7. Thu ngân tính tổng tiền thủ công hoặc bằng máy tính đơn giản.
8. Khách thanh toán.
9. Cuối ngày, quản lý tổng hợp doanh thu bằng sổ hoặc Excel.

### 9.2. Hạn chế của quy trình hiện tại

Quy trình thủ công tồn tại nhiều hạn chế:

- Dễ xảy ra sai sót khi ghi order.
- Dễ nhầm lẫn giữa các bàn khi quán đông khách.
- Khó cập nhật order khi khách gọi thêm hoặc thay đổi món.
- Thu ngân mất thời gian kiểm tra và tính tiền.
- Dữ liệu doanh thu không được cập nhật tự động.
- Quản lý khó tra cứu lịch sử giao dịch.
- Không có phân quyền rõ ràng giữa các vai trò.
- Việc tổng hợp báo cáo cuối ngày tốn thời gian và dễ sai số liệu.

---

## 10. Giải pháp đề xuất

Nhóm đề xuất xây dựng **Hệ thống quản lý quán cà phê** dưới dạng ứng dụng web. Hệ thống cho phép các vai trò trong quán như quản lý, nhân viên phục vụ và thu ngân thao tác trên cùng một nền tảng.

Khi áp dụng hệ thống, quy trình vận hành được cải thiện như sau:

1. Nhân viên đăng nhập vào hệ thống.
2. Nhân viên xem danh sách bàn và trạng thái bàn.
3. Khi khách gọi món, nhân viên chọn bàn và tạo order.
4. Hệ thống lưu thông tin order theo từng bàn.
5. Khi khách gọi thêm hoặc đổi món, nhân viên cập nhật order trên hệ thống.
6. Khi khách thanh toán, thu ngân xem hóa đơn từ order đã lưu.
7. Hệ thống tự động tính tổng tiền.
8. Thu ngân xác nhận thanh toán.
9. Hệ thống lưu hóa đơn, cập nhật trạng thái bàn và ghi nhận doanh thu.
10. Quản lý có thể xem báo cáo doanh thu và tra cứu lịch sử giao dịch.

Giải pháp này giúp giảm sai sót trong phục vụ, tăng tính chính xác khi thanh toán và hỗ trợ quản lý quán hiệu quả hơn.

---

## 11. Yêu cầu nghiệp vụ

### BR-01. Quản lý đăng nhập và phân quyền

Hệ thống phải cho phép người dùng đăng nhập bằng tài khoản và mật khẩu. Sau khi đăng nhập thành công, hệ thống xác định vai trò của người dùng để hiển thị các chức năng phù hợp.

Các vai trò chính gồm:

- Quản lý.
- Nhân viên phục vụ.
- Thu ngân.

Mỗi vai trò chỉ được truy cập các chức năng nằm trong phạm vi công việc của mình.

**Giá trị nghiệp vụ:**  
Đảm bảo an toàn thông tin, tránh truy cập trái phép và phân chia trách nhiệm rõ ràng trong quá trình vận hành.

---

### BR-02. Quản lý nhân viên

Hệ thống phải cho phép quản lý tạo, chỉnh sửa, khóa hoặc cập nhật thông tin tài khoản nhân viên. Mỗi nhân viên được gán một vai trò cụ thể trong hệ thống.

Thông tin nhân viên gồm:

- Mã nhân viên.
- Họ tên.
- Tên đăng nhập.
- Mật khẩu.
- Vai trò.
- Trạng thái hoạt động.

**Giá trị nghiệp vụ:**  
Giúp quản lý kiểm soát nhân sự, phân quyền rõ ràng và đảm bảo chỉ nhân viên hợp lệ mới được sử dụng hệ thống.

---

### BR-03. Quản lý bàn

Hệ thống phải cho phép quản lý danh sách bàn trong quán. Mỗi bàn có thông tin tên bàn, khu vực nếu có và trạng thái hiện tại.

Các trạng thái bàn gồm:

- Trống.
- Đang phục vụ.
- Chờ thanh toán.
- Tạm ngừng sử dụng.

**Giá trị nghiệp vụ:**  
Giúp nhân viên theo dõi tình trạng bàn nhanh chóng, tránh nhầm lẫn khi tạo order hoặc thanh toán.

---

### BR-04. Quản lý menu

Hệ thống phải cho phép quản lý thêm, sửa, xóa hoặc cập nhật thông tin món trong menu.

Thông tin món gồm:

- Mã món.
- Tên món.
- Loại món.
- Giá bán.
- Mô tả ngắn.
- Trạng thái còn bán hoặc tạm ngừng bán.

**Giá trị nghiệp vụ:**  
Giúp quán dễ dàng cập nhật menu, thay đổi giá bán và kiểm soát các món đang được phục vụ.

---

### BR-05. Tạo order cho bàn

Hệ thống phải cho phép nhân viên phục vụ tạo order cho một bàn cụ thể. Nhân viên có thể chọn món từ menu, nhập số lượng và xác nhận order.

Khi order được tạo thành công, hệ thống phải:

- Lưu thông tin order.
- Lưu chi tiết các món trong order.
- Cập nhật trạng thái bàn thành “Đang phục vụ”.
- Hiển thị thông báo tạo order thành công.

**Giá trị nghiệp vụ:**  
Giúp quá trình ghi nhận món gọi của khách chính xác hơn, giảm tình trạng ghi nhầm món hoặc nhầm bàn.

---

### BR-06. Cập nhật order

Hệ thống phải cho phép nhân viên phục vụ cập nhật order khi khách gọi thêm món, thay đổi số lượng hoặc yêu cầu xóa món trước khi thanh toán.

Các thao tác cập nhật order gồm:

- Thêm món mới.
- Sửa số lượng món.
- Xóa món khỏi order.
- Xem tổng tiền tạm tính.

**Giá trị nghiệp vụ:**  
Giúp order được cập nhật kịp thời theo yêu cầu của khách hàng và hỗ trợ thu ngân thanh toán chính xác.

---

### BR-07. Theo dõi trạng thái order

Hệ thống phải cho phép theo dõi trạng thái của order trong quá trình phục vụ.

Các trạng thái order gồm:

- Mới tạo.
- Đang phục vụ.
- Chờ thanh toán.
- Đã thanh toán.
- Đã hủy.

**Giá trị nghiệp vụ:**  
Giúp nhân viên và thu ngân nắm được tình trạng phục vụ của từng bàn, từ đó xử lý công việc nhanh và chính xác hơn.

---

### BR-08. Thanh toán hóa đơn

Hệ thống phải cho phép thu ngân xem chi tiết order, kiểm tra danh sách món, số lượng, đơn giá, thành tiền và tổng tiền cần thanh toán.

Hệ thống phải hỗ trợ ghi nhận tối thiểu các hình thức thanh toán sau:

- Tiền mặt.
- Chuyển khoản giả lập.

Sau khi thanh toán thành công, hệ thống phải:

- Lưu hóa đơn.
- Cập nhật trạng thái order thành “Đã thanh toán”.
- Cập nhật trạng thái bàn về “Trống”.
- Ghi nhận doanh thu.

**Giá trị nghiệp vụ:**  
Giúp giảm sai sót khi tính tiền, rút ngắn thời gian thanh toán và đảm bảo dữ liệu doanh thu chính xác.

---

### BR-09. Tra cứu lịch sử giao dịch

Hệ thống phải cho phép quản lý hoặc thu ngân tra cứu các hóa đơn đã thanh toán theo thời gian, bàn hoặc nhân viên lập order.

Thông tin lịch sử giao dịch gồm:

- Mã hóa đơn.
- Thời gian thanh toán.
- Bàn.
- Nhân viên phục vụ.
- Tổng tiền.
- Phương thức thanh toán.
- Trạng thái thanh toán.

**Giá trị nghiệp vụ:**  
Hỗ trợ đối soát doanh thu, kiểm tra sai sót và tra cứu thông tin giao dịch khi cần.

---

### BR-10. Báo cáo doanh thu

Hệ thống phải cung cấp báo cáo doanh thu cơ bản cho quản lý.

Các loại báo cáo gồm:

- Doanh thu theo ngày.
- Doanh thu theo tháng.
- Doanh thu theo khoảng thời gian tùy chọn.
- Số lượng hóa đơn đã thanh toán.
- Món bán chạy nếu có dữ liệu.

**Giá trị nghiệp vụ:**  
Giúp chủ quán và quản lý nắm được tình hình kinh doanh, đánh giá hiệu quả bán hàng và hỗ trợ ra quyết định.

---

## 12. Quy tắc nghiệp vụ

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

---

## 13. Danh sách yêu cầu chức năng

| Mã | Tên chức năng | Actor chính | Mô tả ngắn | Mức ưu tiên |
|---|---|---|---|---|
| FR-01 | Đăng nhập | Tất cả người dùng | Người dùng đăng nhập bằng tài khoản và mật khẩu | Must have |
| FR-02 | Phân quyền | Hệ thống | Hiển thị chức năng phù hợp với vai trò | Must have |
| FR-03 | Quản lý nhân viên | Quản lý | Thêm, sửa, khóa tài khoản nhân viên | Should have |
| FR-04 | Quản lý bàn | Quản lý | Thêm, sửa, xóa, cập nhật trạng thái bàn | Must have |
| FR-05 | Xem trạng thái bàn | Nhân viên phục vụ, thu ngân | Hiển thị danh sách bàn và trạng thái hiện tại | Must have |
| FR-06 | Quản lý menu | Quản lý | Thêm, sửa, xóa món và cập nhật giá | Must have |
| FR-07 | Tạo order | Nhân viên phục vụ | Tạo order cho từng bàn | Must have |
| FR-08 | Cập nhật order | Nhân viên phục vụ | Thêm món, sửa số lượng, xóa món | Must have |
| FR-09 | Xem chi tiết hóa đơn | Thu ngân | Hiển thị danh sách món, số lượng và tổng tiền | Must have |
| FR-10 | Thanh toán hóa đơn | Thu ngân | Xác nhận thanh toán và lưu hóa đơn | Must have |
| FR-11 | Tra cứu lịch sử giao dịch | Quản lý, thu ngân | Tìm lại hóa đơn đã thanh toán | Should have |
| FR-12 | Xem báo cáo doanh thu | Quản lý | Xem doanh thu theo ngày, tháng hoặc khoảng thời gian | Should have |
| FR-13 | Thống kê món bán chạy | Quản lý | Xem danh sách món được bán nhiều | Could have |

---

## 14. Yêu cầu phi chức năng

### 14.1. Hiệu năng

- Các thao tác chính như đăng nhập, xem danh sách bàn, tạo order, cập nhật order và thanh toán phải phản hồi trong thời gian dưới 3 giây với dữ liệu demo.
- Hệ thống phải xử lý ổn định khi có nhiều bàn đang được phục vụ cùng lúc trong phạm vi quán nhỏ hoặc vừa.

### 14.2. Tính dễ sử dụng

- Giao diện phải rõ ràng, dễ nhìn và phù hợp với người dùng không chuyên về công nghệ.
- Các chức năng thường dùng như chọn bàn, chọn món, tạo order và thanh toán phải thao tác đơn giản.
- Thông báo lỗi phải dễ hiểu để người dùng biết cách xử lý.

### 14.3. Bảo mật

- Người dùng phải đăng nhập trước khi sử dụng hệ thống.
- Mật khẩu cần được lưu trữ an toàn, không hiển thị trực tiếp trên giao diện.
- Hệ thống phải kiểm tra quyền truy cập theo vai trò.
- Người dùng không có quyền không được truy cập chức năng quản lý.

### 14.4. Tính ổn định

- Hệ thống cần hoạt động ổn định trong quá trình demo các luồng nghiệp vụ chính.
- Dữ liệu order, hóa đơn và doanh thu phải được lưu nhất quán.
- Khi thao tác thất bại, hệ thống cần thông báo lỗi rõ ràng.

### 14.5. Khả năng mở rộng

- Thiết kế hệ thống cần cho phép mở rộng thêm các chức năng như quản lý kho, đặt bàn online, khách hàng thân thiết hoặc thanh toán điện tử.
- Cấu trúc mã nguồn cần được chia thành các module rõ ràng để dễ nâng cấp.

### 14.6. Khả năng bảo trì

- Mã nguồn cần được tổ chức theo cấu trúc rõ ràng.
- Tên biến, tên hàm, tên class và tên bảng dữ liệu cần dễ hiểu.
- Tài liệu hướng dẫn cài đặt, deployment và kiểm thử cần được chuẩn bị đầy đủ.

---

## 15. Giả định và ràng buộc

### 15.1. Giả định

- Hệ thống được áp dụng cho quán cà phê quy mô nhỏ hoặc vừa.
- Mỗi bàn tại một thời điểm chỉ có một order đang hoạt động.
- Người dùng hệ thống gồm quản lý, nhân viên phục vụ và thu ngân.
- Nhân viên được hướng dẫn cơ bản trước khi sử dụng hệ thống.
- Dữ liệu sử dụng trong đồ án là dữ liệu mô phỏng.
- Hệ thống được triển khai ở mức phục vụ demo môn học.

### 15.2. Ràng buộc

- Dự án được thực hiện trong phạm vi môn học nên thời gian phát triển có hạn.
- Hệ thống chưa tích hợp thiết bị phần cứng thật như máy in hóa đơn, máy POS hoặc máy quét mã QR.
- Thanh toán chuyển khoản chỉ được mô phỏng, chưa kết nối với ngân hàng hoặc ví điện tử thật.
- Một số chức năng nâng cao sẽ được đưa vào phần định hướng phát triển tương lai thay vì triển khai trong phiên bản đầu tiên.

---

## 16. Tiêu chí chấp nhận nghiệp vụ

### AC-01. Đăng nhập

- Người dùng có tài khoản hợp lệ có thể đăng nhập vào hệ thống.
- Người dùng nhập sai tài khoản hoặc mật khẩu sẽ nhận được thông báo lỗi.
- Sau khi đăng nhập, người dùng chỉ thấy các chức năng phù hợp với vai trò.

### AC-02. Quản lý bàn

- Hệ thống hiển thị danh sách bàn.
- Mỗi bàn có trạng thái rõ ràng.
- Khi order được tạo, trạng thái bàn chuyển thành “Đang phục vụ”.
- Khi thanh toán xong, trạng thái bàn chuyển về “Trống”.

### AC-03. Quản lý menu

- Quản lý có thể thêm món mới.
- Quản lý có thể sửa tên món, giá bán, loại món và trạng thái món.
- Món tạm ngừng bán không được chọn khi tạo order mới.

### AC-04. Tạo order

- Nhân viên có thể chọn bàn để tạo order.
- Nhân viên có thể thêm nhiều món vào một order.
- Hệ thống hiển thị tổng tiền tạm tính.
- Order được lưu thành công vào hệ thống.
- Chi tiết order được lưu đầy đủ gồm món, số lượng, đơn giá và thành tiền.

### AC-05. Cập nhật order

- Nhân viên có thể thêm món vào order chưa thanh toán.
- Nhân viên có thể sửa số lượng món trong order chưa thanh toán.
- Nhân viên có thể xóa món khỏi order chưa thanh toán.
- Order đã thanh toán không được phép chỉnh sửa.

### AC-06. Thanh toán hóa đơn

- Thu ngân có thể xem chi tiết order cần thanh toán.
- Hệ thống tính tổng tiền chính xác.
- Thu ngân có thể chọn phương thức thanh toán.
- Sau khi xác nhận thanh toán, hóa đơn được lưu.
- Trạng thái order chuyển thành “Đã thanh toán”.
- Trạng thái bàn chuyển về “Trống”.

### AC-07. Báo cáo doanh thu

- Quản lý có thể xem doanh thu theo ngày.
- Quản lý có thể xem doanh thu theo tháng.
- Doanh thu chỉ bao gồm các hóa đơn đã thanh toán.
- Tổng doanh thu hiển thị đúng theo dữ liệu hóa đơn.

### AC-08. Tra cứu lịch sử giao dịch

- Quản lý hoặc thu ngân có thể tra cứu hóa đơn đã thanh toán.
- Có thể lọc hóa đơn theo thời gian, bàn hoặc nhân viên.
- Hệ thống hiển thị thông tin cơ bản của hóa đơn.

---

## 17. Rủi ro nghiệp vụ

| Rủi ro | Mô tả | Hướng xử lý |
|---|---|---|
| Phạm vi quá rộng | Nhóm làm quá nhiều chức năng so với thời gian môn học | Tập trung vào các chức năng cốt lõi: bàn, menu, order, thanh toán, báo cáo |
| Sai luồng nghiệp vụ | Chức năng không phản ánh đúng quy trình quán cà phê | Bám sát quy trình thực tế: chọn bàn, gọi món, cập nhật order, thanh toán |
| Giao diện khó dùng | Nhân viên thao tác chậm hoặc dễ nhầm | Thiết kế giao diện đơn giản, ưu tiên thao tác chính |
| Sai dữ liệu doanh thu | Hóa đơn chưa thanh toán vẫn bị tính vào doanh thu | Chỉ tính doanh thu từ hóa đơn có trạng thái đã thanh toán |
| Phân quyền chưa rõ | Người dùng truy cập sai chức năng | Thiết kế role rõ ràng ngay từ đầu |
| Lỗi khi cập nhật order | Thêm, sửa, xóa món làm sai tổng tiền | Kiểm thử kỹ các trường hợp thay đổi order |
| Thiếu dữ liệu demo | Demo không thuyết phục | Chuẩn bị dữ liệu mẫu cho bàn, menu, nhân viên, order và hóa đơn |

---

## 18. Tiêu chí thành công của dự án

Dự án được xem là thành công khi đáp ứng các tiêu chí sau:

1. Hệ thống cho phép người dùng đăng nhập và phân quyền theo vai trò.
2. Quản lý có thể quản lý bàn, menu và nhân viên.
3. Nhân viên phục vụ có thể tạo và cập nhật order cho từng bàn.
4. Thu ngân có thể xem hóa đơn và xác nhận thanh toán.
5. Sau khi thanh toán, trạng thái bàn và order được cập nhật chính xác.
6. Quản lý có thể xem báo cáo doanh thu cơ bản.
7. Hệ thống có giao diện dễ sử dụng và phù hợp với quy trình quán cà phê.
8. Cơ sở dữ liệu lưu được thông tin bàn, menu, order, chi tiết order, hóa đơn và người dùng.
9. Hệ thống chạy ổn định trong quá trình demo.
10. Nhóm chuẩn bị đầy đủ tài liệu phân tích, thiết kế, source code, hướng dẫn cài đặt, hướng dẫn deployment, slide và video demo.

---

## 19. Định hướng mở rộng trong tương lai

Sau khi hoàn thành phiên bản đầu tiên, hệ thống có thể được mở rộng theo các hướng sau:

- Cho phép khách hàng xem menu bằng mã QR.
- Cho phép khách đặt bàn trước qua website.
- Tích hợp thanh toán online qua ví điện tử hoặc ngân hàng.
- Tích hợp máy in hóa đơn.
- Quản lý kho nguyên liệu.
- Quản lý nhà cung cấp.
- Quản lý chương trình khuyến mãi và voucher.
- Quản lý khách hàng thân thiết.
- Thống kê doanh thu nâng cao.
- Quản lý nhiều chi nhánh.
- Xây dựng ứng dụng mobile cho nhân viên hoặc khách hàng.

---

## 20. Danh sách module đề xuất

| Module | Tên module | Chức năng chính |
|---|---|---|
| Module 1 | Đăng nhập và phân quyền | Đăng nhập, đăng xuất, kiểm tra vai trò |
| Module 2 | Quản lý nhân viên | Thêm, sửa, khóa tài khoản nhân viên |
| Module 3 | Quản lý bàn | Quản lý danh sách bàn và trạng thái bàn |
| Module 4 | Quản lý menu | Quản lý món, loại món, giá bán, trạng thái món |
| Module 5 | Quản lý order | Tạo order, cập nhật order, xem chi tiết order |
| Module 6 | Thanh toán | Tính tiền, xác nhận thanh toán, lưu hóa đơn |
| Module 7 | Lịch sử giao dịch | Tra cứu hóa đơn đã thanh toán |
| Module 8 | Báo cáo | Báo cáo doanh thu, số hóa đơn, món bán chạy |

---

## 21. Kết luận

Hệ thống quản lý quán cà phê là một đề tài phù hợp với môn Công nghệ phần mềm vì có quy trình nghiệp vụ rõ ràng, gần gũi với thực tế và có thể triển khai thành một sản phẩm mô phỏng hoàn chỉnh. Hệ thống giúp giải quyết các vấn đề thường gặp trong hoạt động quán cà phê như ghi nhầm order, khó kiểm soát bàn, tính tiền sai, mất thời gian tổng hợp doanh thu và thiếu phân quyền trong quản lý.

Tài liệu Business Requirements Document này là cơ sở để nhóm tiếp tục thực hiện các bước tiếp theo như xây dựng Use Case Diagram, mô tả Use Case, thiết kế Sequence Diagram, thiết kế cơ sở dữ liệu, lập trình chức năng, kiểm thử và chuẩn bị tài liệu triển khai. Trong phạm vi đồ án, hệ thống tập trung vào các chức năng cốt lõi gồm quản lý bàn, quản lý menu, tạo order, cập nhật order, thanh toán hóa đơn và báo cáo doanh thu cơ bản.
