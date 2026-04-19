1. **Thêm cảnh báo – Chỉ tiêu có sẵn**
   1. **Thông tin chung chức năng**

![](Aspose.Words.853bc717-dbd7-44de-9d75-db0041407460.001.png)

LĐPTTT, CVPTTT thực hiện truy cập chức năng từ đường dẫn: Phân hệ quản lý rủi ro 🡪 Chức năng cảnh báo 🡪 Danh sách cảnh báo 🡪 Thêm cảnh báo🡪 Tabs Chỉ tiêu có sẵn. Chức năng cho phép LĐPTTT, CVPTTT thực hiện thêm chỉ tiêu cảnh báo đang có sắn. 

Điều kiện: 

- Người dùng đã đăng nhập thành công vào hệ thống và được phân quyền chức năng. 
- Người dùng có quyền truy cập phân hệ Cảnh báo.
2. **Màn hình**

   ![](Aspose.Words.853bc717-dbd7-44de-9d75-db0041407460.002.png)

3. **Mô tả chi tiết các thành phần**

   |STT|Tên|<p>Kiểu dữ liệu</p><p>[Độ dài dữ liệu]</p>|Input/Output|Giá trị khởi tạo|Mô tả (Mapping với CSDL nếu có)|
   | :- | :- | :- | :- | :- | :- |
   ||Thêm cảnh báo|Label|||- Tên modal: "Thêm cảnh báo "|
   ||Mô tả modal|Label|||- Mô tả: "Chọn chỉ tiêu từ hệ thống hoặc tạo cảnh báo tùy chỉnh"|
   ||Tab Chỉ tiêu có sẵn|Tab|||- Khi chọn: hiển thị form chọn chỉ tiêu đã có trong hệ thống|
   ||Tab Chỉ tiêu mới|Tab|||- Chuyển sang form nhập chỉ tiêu hoàn toàn mới.|
   ||Ô tìm kiếm|<p>Textview</p><p>(255)</p>|Input||<p>- Trường để lọc: Tìm kiếm gần đúng theo [Tên chỉ tiêu]</p><p>- Hỗ trợ tìm kiếm 1 tiêu chí; người dùng có thể dán (copy/paste), hệ thống trả về danh sách kết quả tương ứng với dữ liệu đã nhập.</p>|
   ||Nút Tra cứu|Button||Enable|<p>- Click button, thực hiện tra cứu dữ liệu theo input đầu vào</p><p>- Disable khi đang loading</p>|
   ||Danh sách chỉ tiêu|Radio button|Output|N/A|<p>- Hiển thị mặc định toàn bộ tất cá các chỉ tiêu Tài chính trong nước và quốc tế, sắp xếp theo thứ tự tại Danh sách chỉ tiêu tài chính trong nước và quốc tế. Trong đó Chỉ tiêu tài chính trong nước xếp ưu tiên trước</p><p>- Hiển thị thông tin chỉ tiêu như giao diện</p><p>- Hiển thị dữ liệu chỉ tiêu theo điều kiện tìm kiếm</p><p>- Bắt buộc chọn 1 chỉ tiêu</p><p>- Mặc định: Trống</p><p>- Hệ thống chỉ hiển thị các chỉ tiêu chưa được cấu hình cảnh báo</p><p>- Lựa chọn Lựa chọn thông tin chỉ tiêu cảnh báo=> Hệ thống tự động fill thông tin tên+giá trị kỳ này+ đơn vị của giá trị kỳ này vào các biến tương ứng của Nội dung cảnh báo</p>|
   ||Ngưỡng cảnh báo|Dropdown|Input|N/A|<p>- Place holder: Chọn</p><p>- Bắt buộc</p><p>- Dữ liệu gồm:</p><p>- Tăng/Giảm</p><p>- Tăng</p><p>- Giảm</p><p>- Chỉ được chọn 1 giá trị</p><p>- Lựa chọn thông tin ngưỡng cảnh báo=> Hệ thống tự động fill thông tin ngưỡng cảnh báo vào biến {Ngưỡng cảnh báo} của Nội dung cảnh báo</p><p>- Action: Nhấn button Thêm cảnh báo, hệ thống validate, nếu</p><p>- Để trống ⇒ Hiển thị thông báo lỗi: “Vui lòng nhập đủ thông tin!” đồng thời highlight đỏ vào textbox</p>|
   ||<p>Giá trị cảnh báo</p><p>![](Aspose.Words.853bc717-dbd7-44de-9d75-db0041407460.003.png)</p>|InputNumber (19,4)|Input| |<p>- Placeholder: Nhập </p><p>- Bắt buộc</p><p>- Click [+]=> hệ thống + 1 đơn vị so với giá trị hiện tại. Nếu dữ liệu hiện tại là 0=> Không click được tiếp</p><p>- Click [-]=> hệ thống - 1 đơn vị so với giá trị hiện tại. Nếu dữ liệu hiện tại là 0=> Không click được tiếp</p><p>- Nhập thông tin giá trị cảnh báo=> Hệ thống tự động fill thông tin ngưỡng cảnh báo vào biến {Giá trị cảnh báo}</p><p>- Action: Nhấn button Thêm cảnh báo, hệ thống validate, nếu</p><p>- Để trống ⇒ Hiển thị thông báo lỗi: “Vui lòng nhập đủ thông tin!” đồng thời highlight đỏ vào textbox</p>|
   ||Đơn vị cảnh báo|Dropdown list|||<p>- Place holder: Chọn</p><p>- Bắt buộc</p><p>- Dữ liệu gồm:</p><p>- Đơn vị theo chọn chỉ tiêu=> chưa chọn chỉ tiêu=> chỉ hiển thị đơn vị %</p><p>- ` `%</p><p>- Chỉ được chọn 1 giá trị</p><p>- Lựa chọn thông tin Đơn vị cảnh báo => Hệ thống tự động fill thông tin Đơn vị cảnh báo vào biến { Đơn vị cảnh báo } của Nội dung cảnh báo</p><p>- Action: Nhấn button Thêm cảnh báo, hệ thống validate, nếu</p><p>- Để trống ⇒ Hiển thị thông báo lỗi: “Vui lòng nhập đủ thông tin!” đồng thời highlight đỏ vào textbox</p>|
   ||Số kỳ so sánh|InputNumber |Input| |<p>- Placeholder: Nhập </p><p>- Bắt buộc</p><p>- Là số nguyên dương(>=1), validate giá trị trong khoảng 1-100</p><p>- Chặn ký tự 0, chặn các ký tự số âm, số thập phân và ký tự khác số</p><p>- Click [+]=> hệ thống + 1 đơn vị so với giá trị hiện tại. Nếu dữ liệu hiện tại là 1=> Không click được tiếp</p><p>- Click [-]=> hệ thống - 1 đơn vị so với giá trị hiện tại. Nếu dữ liệu hiện tại là 1=> Không click được tiếp</p><p>- Nhập thông tin giá trị cảnh báo</p><p>- + Nếu nhập số kỳ so sánh > 1=> Hệ thống tự động fill thông tin ngưỡng cảnh báo vào biến {Số kỳ so sánh} của Nội dung cảnh báo</p><p>- + Nếu nhập số kỳ so sánh = 1 => Không cần hiển thị số kỳ so sánh </p><p>- Action: Nhấn button Thêm cảnh báo, hệ thống validate, nếu</p><p>- Để trống ⇒ Hiển thị thông báo lỗi: “Vui lòng nhập đủ thông tin!” đồng thời highlight đỏ vào textbox</p>|
   ||Người được phân công xử lý|Selector|Input|N/A|<p>- Place holder: Chọn</p><p>- Mặc định: Hiển thị trống</p><p>- Bắt buộc</p><p>- Không nhập điều kiện tìm kiếm=> Click Enter/icon kính lúp hiển thị toàn bộ dữ liệu user trong phân hệ Quản lý rủi ro</p><p>- Cho phép tìm kiếm gần đúng theo họ và tên user</p><p>- Hiển thị thông tin người xử lý dạng: Họ và tên- ID</p><p>- Action: Nhấn button Thêm cảnh báo, hệ thống validate, nếu</p><p>- Để trống ⇒ Hiển thị thông báo lỗi: “Vui lòng nhập đủ thông tin!” đồng thời highlight đỏ vào textbox</p>|
   ||Nội dung cảnh báo|InputDesc(1000)||N/A|<p>- Mặc định hiển thị: {Tên chỉ tiêu} đang đạt {Giá trị kỳ này}{ Đơn vị giá trị kỳ này}, {Ngưỡng cảnh báo} {Giá trị cảnh báo}{ Đơn vị cảnh báo} so với {Số kỳ so sánh} {tần suất} trước. Đề nghị đơn vị phụ trách kiểm tra nguyên nhân và cập nhật thông tin xử lý.</p><p>- Không cho phép chỉnh sửa</p><p>- Click chọn 1 trong các thông tin : Tên chỉ tiêu/ Ngưỡng cảnh báo/ Giá trị cảnh báo/ Đơn vị cảnh báo/ Số kỳ so sánh/ Tần suất => Hệ thống tự động fill dữ liệu vào các biến tương ứng</p><p>- Trường tần suất lấy dữ liệu từ tần suất dữ liệu của từng chỉ tiêu cảnh báo</p>|
   ||Nút Đóng|Button|Input|N/A|- Đóng modal, không cần xử lý gì thêm. Trở về giao diện Danh sách cảnh báo|
   ||Nút Thêm cảnh báo|Button|Input|N/A|<p>- Xác nhận lưu cấu hình cảnh báo mới</p><p>- Thực hiện validate dữ liệu đã nhập vào tại các trường thông tin trên form.</p><p>+ Nếu nhập đủ thông tin các trường bắt buộc=> Thêm mới cảnh báo thành công</p><p>+ Nếu nhập thiếu 1 trong các trường bắt buộc => Hiển thị cảnh báo” Vui lòng nhập đủ thông tin” đồng thời highlight vào các textbox tương ứng.</p><p>- Lưu vào cấu hình cảnh báo mới trên danh sách giao diện Danh sách cảnh báo( Xếp sau 10 cảnh báo mặc định). </p>|
4. **Luồng nghiệp vụ**

   ![](Aspose.Words.853bc717-dbd7-44de-9d75-db0041407460.004.png)

- Luồng xử lý chính: 
- Người dùng nhấn nút "+ Thêm cảnh báo" (⑨) từ màn hình Danh sách cảnh báo → Hệ thống mở modal "Thêm cấu hình cảnh báo mới" (①), tab "Chỉ tiêu có sẵn" (③) được chọn mặc định; toàn bộ trường ở trạng thái rỗng / giá trị mặc định.
- Người dùng nhập từ khóa vào ô tìm kiếm chỉ tiêu (⑤) rồi nhấn "Tra cứu" (⑥) → Hệ thống tìm kiếm và hiển thị danh sách chỉ tiêu phù hợp (⑦) theo tên.
- Người dùng chọn chỉ tiêu và cấu hình chỉ tiêu: 
- Người dùng chọn một chỉ tiêu từ danh sách kết quả (⑦) bằng radio button → Hệ thống highlight dòng được chọn; ghi nhận chỉ tiêu.
- Người dùng nhấn nút "Thêm cảnh báo" (⑭) → Hệ thống validate toàn bộ dữ liệu (xem mục Validate). Nếu có lỗi: hiển thị thông báo lỗi inline tại trường tương ứng, không đóng modal. Nếu hợp lệ: lưu cấu hình, đóng modal, hiển thị toast thông báo thành công, cập nhật danh sách cảnh báo.
- Người dùng nhấn nút "Đóng" (⑬) → Hệ thống đóng modal, quay về màn hình Danh sách cảnh báo.
- Luồng phụ: 
- Nếu không tìm thấy chỉ tiêu nào theo từ khóa: hệ thống hiển thị thông báo "Không tìm thấy chỉ tiêu phù hợp".
- Nếu người dùng nhấn "Thêm cảnh báo" khi chưa chọn chỉ tiêu: hệ thống hiển thị lỗi tại vùng danh sách chỉ tiêu.

