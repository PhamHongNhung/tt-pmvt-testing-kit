HỌC VIỆN CÔNG NGHỆ BƯU CHÍNH VIỄN THÔNG KHOA
SAU ĐẠI HỌC
-----🙞🙜🕮🙞🙜-----
BÁO CÁO CUỐI KỲ MÔN KHAI PHÁ DỮ LIỆU
Giảng viên: TS. Trần Tiến Công
Sinh viên thực hiện:
Phạm Hồng Nhung - B25CHHT045
Hà Nội, 03/2026
1
MỤC LỤC
MỞ ĐẦU – LÝ DO CHỌN ĐỀ TÀI ....................................................................................................... 3
1. Mô tả dữ liệu thu thập được, nguồn dữ liệu và các bản ghi ................................................................. 3
1.1. Bối cảnh nghiệp vụ ....................................................................................................................... 3
1.2. Nguồn dữ liệu ................................................................................................................................ 4
1.3. Dữ liệu thu thập và cấu trúc bản ghi ............................................................................................. 5
1.3.1 Quy mô dữ liệu ........................................................................................................................... 5
1.3.2 Các thuộc tính dữ liệu ................................................................................................................. 5
1.3.3 Ý nghĩa của dữ liệu đối với quản lý chất lượng .......................................................................... 6
2. Ứng dụng dữ liệu vào bài toán thực tế tại doanh nghiệp ..................................................................... 6
2.1 Bài toán đánh giá chất lượng dự án ................................................................................................ 6
2.2 Bài toán phân tích nguyên nhân ảnh hưởng đến chất lượng .......................................................... 7
2.3 Bài toán dự báo rủi ro chất lượng .................................................................................................. 7
2.4 Bài toán phân loại mức độ rủi ro dự án .......................................................................................... 8
2.5 Vai trò của khai phá dữ liệu trong quản lý chất lượng ................................................................... 8
3. Xây dựng mô hình khai phá dữ liệu .................................................................................................... 8
3.1. Mục tiêu khai phá .......................................................................................................................... 8
3.2. Tiền xử lý dữ liệu .......................................................................................................................... 9
3.2.1 Làm sạch dữ liệu (Data Cleaning) .............................................................................................. 9
3.2.2 Chuẩn hóa dữ liệu (Data Normalization) .................................................................................. 10
3.2.3 Mã hóa dữ liệu định tính (Data Encoding) ................................................................................ 10
3.2.4 Tích hợp và chuyển đổi dữ liệu (Data Integration and Transformation) .................................. 10
3.3. Kỹ thuật khai phá dữ liệu áp dụng .............................................................................................. 10
3.3.1 Khai phá mô tả (Descriptive Data Mining) ............................................................................... 11
3.3.2 Phân cụm dữ liệu (Clustering) .................................................................................................. 11
3.3.3 Phân lớp dữ liệu (Classification) ............................................................................................... 11
3.3.4 Ý nghĩa ứng dụng của các kỹ thuật khai phá dữ liệu ................................................................ 12
4. Báo cáo tóm tắt kết quả thu được ...................................................................................................... 12
4.1 Kết quả phân tích mô tả dữ liệu ................................................................................................... 12
4.2 Kết quả phân cụm dự án theo mức độ rủi ro ................................................................................ 13
4.3 Kết quả xây dựng mô hình dự báo defect leakage ....................................................................... 13
4.4 Giá trị ứng dụng trong quản lý chất lượng phần mềm ................................................................. 13
4.5 Hạn chế và hướng phát triển ........................................................................................................ 14
Kết luận .................................................................................................................................................. 14
5. Demo ứng dụng khai phá dữ liệu defect leakage ............................................................................... 15
TÀI LIỆU THAM KHẢO ..................................................................................................................... 152
ỨNG DỤNG KHAI PHÁ DỮ LIỆU TRONG QUẢN LÝ DEFECT VÀ LEAKAGE TẠI ĐƠN VỊ
PHÁT TRIỂN PHẦN MỀM
MỞ ĐẦU – LÝ DO CHỌN ĐỀ TÀI
Trong bối cảnh chuyển đổi số và phát triển phần mềm nhanh chóng hiện nay, chất lượng sản phẩm phần
mềm ngày càng đóng vai trò quan trọng đối với uy tín và hiệu quả hoạt động của các cơ quan, doanh
nghiệp. Tuy nhiên, cùng với sự gia tăng về quy mô và độ phức tạp của các dự án phần mềm, công tác đảm
bảo chất lượng và kiểm soát lỗi (defect) cũng đối mặt với nhiều thách thức, đặc biệt là tình trạng defect
leakage – lỗi lọt sang các giai đoạn sau hoặc môi trường sản xuất.
Tại nơi công tác, với vai trò là Test Manager, tôi thường xuyên phải tổng hợp, phân tích dữ liệu defect và
leakage của nhiều dự án khác nhau để báo cáo lên Ban Giám đốc. Thực tế cho thấy, các báo cáo truyền
thống chủ yếu dừng lại ở mức thống kê mô tả, chưa khai thác hết tiềm năng của dữ liệu trong việc phát
hiện xu hướng, mối quan hệ ẩn và hỗ trợ ra quyết định quản lý chất lượng một cách chủ động.
Xuất phát từ yêu cầu thực tiễn đó, cùng với kiến thức được trang bị trong học phần Khai phá dữ liệu, tôi
lựa chọn đề tài “Ứng dụng khai phá dữ liệu trong quản lý defect và leakage tại trung tâm kiểm thử phần
mềm”. Đề tài nhằm nghiên cứu khả năng áp dụng các kỹ thuật khai phá dữ liệu vào dữ liệu kiểm thử thực
tế, từ đó hỗ trợ nâng cao hiệu quả quản lý chất lượng, giảm thiểu rủi ro defect leakage và góp phần cải
tiến quy trình kiểm thử tại doanh nghiệp.
Đề tài không chỉ mang ý nghĩa học thuật mà còn có giá trị ứng dụng cao, phù hợp với định hướng nghiên
cứu gắn liền với thực tiễn công việc của học viên cao học.
1. Mô tả dữ liệu thu thập được, nguồn dữ liệu và các bản ghi
1.1. Bối cảnh nghiệp vụ
Tại đơn vị công tác, tôi đang đảm nhiệm vai trò Test Manager, chịu trách nhiệm quản lý và giám sát chất
lượng kiểm thử cho nhiều dự án phần mềm thuộc trung tâm. Trong quá trình thực hiện công việc, hàng
tuần và hàng tháng tôi phải tổng hợp, phân tích các chỉ số liên quan đến defect, defect leakage và hiệu quả
kiểm thử của từng dự án để báo cáo Ban Giám đốc.
Trong thực tế quản lý chất lượng phần mềm tại doanh nghiệp, các chỉ số defect và defect leakage đóng
vai trò là những thước đo quan trọng để đánh giá mức độ ổn định và chất lượng đầu ra của sản phẩm trước
khi bàn giao cho khách hàng. Việc kiểm soát tốt các chỉ số này không chỉ giúp hạn chế rủi ro lỗi phát sinh
trên môi trường vận hành mà còn góp phần nâng cao chất lượng phát triển phần mềm ngay từ các giai
đoạn đầu của vòng đời dự án.
Tại trung tâm, Ban Giám đốc và các cấp quản lý dự án luôn dựa trên các ngưỡng chuẩn chất lượng nội bộ
(NORM defect/leakage) do công ty ban hành để đánh giá hiệu quả làm việc của các vai trò tham gia dự
án như Developer, Tester và Business Analyst. Các chỉ số này được sử dụng để theo dõi chất lượng theo
từng dự án, từng giai đoạn và từng nhóm nhân sự.
3
Trong trường hợp các dự án hoặc cá nhân có chỉ số defect hoặc defect leakage vượt ngưỡng NORM cho
phép, Test Manager và Project Manager sẽ tiến hành phân tích nguyên nhân, đánh giá các yếu tố ảnh
hưởng và phối hợp với các thành viên trong nhóm để đề xuất các giải pháp cải thiện chất lượng. Các giải
pháp có thể bao gồm tăng cường hoạt động review, cải tiến quy trình kiểm thử, điều chỉnh nguồn lực hoặc
nâng cao năng lực chuyên môn của đội ngũ.
Do đó, việc khai thác và phân tích dữ liệu defect không chỉ phục vụ mục tiêu báo cáo mà còn đóng vai trò
quan trọng trong việc hỗ trợ quản lý chất lượng dự án, nâng cao hiệu quả phối hợp giữa các bộ phận và
đảm bảo chất lượng đầu ra sản phẩm phần mềm trước khi bàn giao cho khách hàng.
1.2. Nguồn dữ liệu
Dữ liệu phục vụ cho nghiên cứu được thu thập từ các nguồn chính trong quy trình quản lý chất lượng
kiểm thử phần mềm tại đơn vị công tác. Các nguồn dữ liệu này có tính hệ thống, được cập nhật thường
xuyên và phản ánh trực tiếp thực trạng chất lượng của các dự án phần mềm trong trung tâm. Cụ thể bao
gồm:
Thứ nhất, hệ thống quản lý lỗi JIRA.
Đây là nguồn dữ liệu chính và có độ tin cậy cao nhất trong nghiên cứu. Hệ thống JIRA được sử dụng để
quản lý toàn bộ vòng đời của defect trong dự án, từ khi phát sinh đến khi được xử lý và đóng lỗi. Dữ liệu
trích xuất từ hệ thống này bao gồm các thông tin quan trọng như tổng số defect, số lượng defect leakage,
mức độ nghiêm trọng của lỗi (severity), người gây lỗi, thời điểm phát sinh lỗi và thời điểm đóng lỗi. Nhờ
đó, hệ thống JIRA cung cấp dữ liệu chi tiết, đầy đủ và có khả năng truy vết, phục vụ hiệu quả cho việc
phân tích và khai phá dữ liệu.
Thứ hai, báo cáo kiểm thử định kỳ của Test Lead.
Hàng tuần, Test Lead của từng dự án thực hiện báo cáo tình trạng kiểm thử cho Test Manager. Nội dung
báo cáo bao gồm tình hình cập nhật defect, số lượng defect leakage, các vấn đề tồn đọng (issue) trong quá
trình kiểm thử, tiến độ thực hiện test case và các rủi ro chất lượng của dự án. Đây là nguồn dữ liệu bổ
sung quan trọng giúp cung cấp bối cảnh nghiệp vụ và thông tin định tính liên quan đến hoạt động kiểm
thử thực tế.
Thứ ba, báo cáo tổng hợp chất lượng dự án.
Báo cáo này được lập định kỳ hàng tuần để phục vụ công tác quản lý của Ban Giám đốc trung tâm. Nội
dung báo cáo tổng hợp các chỉ số chất lượng của từng dự án như tổng số defect, defect leakage, tỷ lệ
leakage, tình trạng chất lượng dự án so với ngưỡng chuẩn (NORM) của công ty. Đây là nguồn dữ liệu
giúp cung cấp góc nhìn tổng thể về chất lượng dự án theo thời gian.
Toàn bộ dữ liệu từ các nguồn trên được tổng hợp, làm sạch và chuẩn hóa dưới dạng bảng dữ liệu
(Excel/CSV), tạo thành dataset đầu vào cho quá trình tiền xử lý và khai phá dữ liệu trong nghiên cứu.
4
1.3. Dữ liệu thu thập và cấu trúc bản ghi
Dữ liệu được sử dụng trong nghiên cứu được tổng hợp từ các nguồn đã nêu, phản ánh tình hình quản lý
defect và chất lượng kiểm thử của các dự án phần mềm tại trung tâm trong một khoảng thời gian nhất
định.
Dataset được xây dựng theo dạng bảng dữ liệu (tabular data), trong đó mỗi bản ghi (record) đại diện cho
một dự án trong một kỳ báo cáo định kỳ (tuần hoặc tháng). Cách tổ chức dữ liệu này phù hợp với mục
tiêu phân tích xu hướng chất lượng theo thời gian và so sánh giữa các dự án.
1.3.1 Quy mô dữ liệu
Tập dữ liệu nghiên cứu bao gồm:
- Dữ liệu của nhiều dự án phần mềm thuộc các lĩnh vực nghiệp vụ khác nhau
- Dữ liệu được thu thập theo chu kỳ báo cáo định kỳ (tuần/tháng)
- Tổng số bản ghi dữ liệu đủ lớn để phục vụ phân tích thống kê và khai phá dữ liệu
Việc thu thập dữ liệu theo nhiều giai đoạn giúp đảm bảo tính liên tục, phản ánh được sự biến động chất
lượng dự án theo thời gian.
1.3.2 Các thuộc tính dữ liệu
Mỗi bản ghi dữ liệu bao gồm các nhóm thuộc tính chính sau:
Nhóm thông tin dự án
- Mã dự án
- Tên dự án
- Lĩnh vực nghiệp vụ (Finance, E-commerce, Government,…)
- Quy mô dự án (nhỏ, vừa, lớn)
- Thời gian báo cáo
Nhóm thuộc tính này giúp phân loại và so sánh chất lượng giữa các loại dự án khác nhau.
5
Nhóm thông tin defect
- Tổng số defect phát hiện trong giai đoạn kiểm thử
- Số defect theo mức độ nghiêm trọng (Critical, Major, Minor)
- Số defect leakage (lỗi lọt sang UAT hoặc Production)
- Tỷ lệ defect leakage (%)
Đây là nhóm thuộc tính quan trọng nhất, phản ánh trực tiếp mức độ ổn định và chất lượng sản phẩm phần
mềm.
Nhóm thông tin hoạt động kiểm thử
- Số lượng test case được thực thi
- Tỷ lệ test case pass/fail
- Số lượng nhân sự kiểm thử tham gia
Nhóm thuộc tính này phản ánh hiệu quả hoạt động kiểm thử và nguồn lực dự án.
1.3.3 Ý nghĩa của dữ liệu đối với quản lý chất lượng
Các thuộc tính trong dataset cho phép đánh giá toàn diện chất lượng dự án phần mềm, từ khía cạnh số
lượng lỗi, mức độ nghiêm trọng, hiệu quả kiểm thử đến năng lực nguồn lực tham gia.
Đặc biệt, các chỉ số defect và defect leakage đóng vai trò là các chỉ số cốt lõi để so sánh với ngưỡng chất
lượng chuẩn (NORM) của công ty, từ đó hỗ trợ Ban Giám đốc, Project Manager và Test Manager đánh
giá mức độ ổn định của dự án, xác định nguyên nhân ảnh hưởng đến chất lượng và đề xuất các biện pháp
cải tiến phù hợp.
2. Ứng dụng dữ liệu vào bài toán thực tế tại doanh nghiệp
Trong hoạt động quản lý chất lượng phần mềm tại doanh nghiệp, dữ liệu defect và defect leakage không
chỉ được sử dụng cho mục đích thống kê mà còn đóng vai trò quan trọng trong việc đánh giá hiệu quả
phát triển, kiểm thử và mức độ ổn định của sản phẩm trước khi bàn giao cho khách hàng.
Từ góc độ quản lý, việc khai thác dữ liệu defect đặt ra một số bài toán thực tiễn quan trọng cần được giải
quyết.
2.1 Bài toán đánh giá chất lượng dự án
Tại đơn vị công tác, Ban Giám đốc trung tâm và các cấp quản lý dự án sử dụng các chỉ số defect và defect
leakage như những thước đo chính để đánh giá chất lượng đầu ra của dự án. Các chỉ số này được so sánh
với ngưỡng chất lượng chuẩn nội bộ (NORM defect/leakage) do công ty ban hành.
6
Thông qua đó, Test Manager có thể xác định:
- Dự án nào đang có nguy cơ chất lượng thấp do tỷ lệ defect leakage cao
- Các giai đoạn phát triển hoặc kiểm thử có phát sinh nhiều lỗi bất thường
- Mức độ ổn định của sản phẩm trước khi bàn giao cho khách hàng
Việc đánh giá này giúp đảm bảo rằng chất lượng đầu ra của sản phẩm phần mềm đáp ứng các tiêu chuẩn
chất lượng nội bộ cũng như yêu cầu của khách hàng.
2.2 Bài toán phân tích nguyên nhân ảnh hưởng đến chất lượng
Bên cạnh việc theo dõi số lượng defect, doanh nghiệp cần xác định các yếu tố ảnh hưởng đến chất lượng
dự án. Dữ liệu thu thập cho phép phân tích mối quan hệ giữa defect leakage và các đặc điểm của dự án
như:
- Quy mô dự án
- Lĩnh vực nghiệp vụ
- Khối lượng test case
- Nguồn lực kiểm thử
- Hiệu quả thực hiện kiểm thử
Kết quả phân tích giúp Test Manager và Project Manager hiểu rõ nguyên nhân gốc rễ gây ra tình trạng
leakage cao, từ đó đưa ra các biện pháp cải tiến phù hợp.
2.3 Bài toán dự báo rủi ro chất lượng
Trong thực tế quản lý dự án, việc phát hiện sớm nguy cơ chất lượng có ý nghĩa quan trọng trong việc giảm
thiểu chi phí sửa lỗi và tránh ảnh hưởng đến tiến độ bàn giao.
Do đó, một bài toán quan trọng được đặt ra là:
- Có thể dự đoán sớm khả năng xảy ra defect leakage cao của một dự án dựa trên dữ liệu lịch sử hay
không?
Việc áp dụng các kỹ thuật khai phá dữ liệu cho phép xây dựng mô hình dự báo rủi ro chất lượng,
giúp Test Manager chủ động điều chỉnh kế hoạch kiểm thử, tăng cường nguồn lực hoặc cải tiến
quy trình ngay từ giai đoạn sớm của dự án.
7
2.4 Bài toán phân loại mức độ rủi ro dự án
Một nhu cầu thực tiễn khác trong quản lý chất lượng là phân loại các dự án theo mức độ rủi ro để ưu tiên
nguồn lực kiểm thử.
Dựa trên dữ liệu defect và leakage, các dự án có thể được phân nhóm thành:
- Nhóm dự án có chất lượng ổn định
- Nhóm dự án có rủi ro trung bình
- Nhóm dự án có rủi ro cao cần giám sát đặc biệt
Kết quả phân loại giúp Ban Giám đốc và Test Manager đưa ra quyết định phân bổ nguồn lực, lập kế hoạch
kiểm thử phù hợp và nâng cao hiệu quả quản lý chất lượng tổng thể.
2.5 Vai trò của khai phá dữ liệu trong quản lý chất lượng
Việc ứng dụng khai phá dữ liệu giúp chuyển đổi phương thức quản lý chất lượng từ mô hình báo cáo
thống kê truyền thống (descriptive reporting) sang mô hình phân tích và dự báo dựa trên dữ liệu (analytical
and predictive management).
Nhờ đó, doanh nghiệp có thể:
- Phát hiện sớm xu hướng rủi ro chất lượng
- Hỗ trợ ra quyết định quản lý dựa trên dữ liệu khách quan
- Nâng cao hiệu quả phối hợp giữa các vai trò trong dự án
- Đảm bảo chất lượng sản phẩm trước khi bàn giao cho khách hàng
3. Xây dựng mô hình khai phá dữ liệu
3.1. Mục tiêu khai phá
Xuất phát từ các bài toán quản lý chất lượng thực tế tại doanh nghiệp đã được trình bày ở phần trước, việc
áp dụng khai phá dữ liệu trong nghiên cứu này hướng tới mục tiêu khai thác giá trị tiềm ẩn từ dữ liệu
defect nhằm hỗ trợ công tác đánh giá, dự báo và kiểm soát chất lượng dự án phần mềm.
Cụ thể, các mục tiêu khai phá dữ liệu được xác định như sau:
Thứ nhất, phát hiện các mẫu và xu hướng liên quan đến defect leakage
Mục tiêu đầu tiên của quá trình khai phá dữ liệu là phân tích và phát hiện các mẫu (patterns) tiềm ẩn trong
dữ liệu defect, đặc biệt là các xu hướng liên quan đến defect leakage theo thời gian, theo loại dự án và
theo điều kiện kiểm thử.
8
Việc nhận diện các quy luật này giúp Test Manager hiểu rõ sự biến động chất lượng dự án, từ đó xác định
những yếu tố có khả năng làm gia tăng rủi ro leakage và chủ động đưa ra các biện pháp kiểm soát phù
hợp.
Thứ hai, phân nhóm dự án theo mức độ rủi ro chất lượng
Một mục tiêu quan trọng khác là sử dụng các kỹ thuật khai phá dữ liệu để phân loại các dự án thành các
nhóm có đặc điểm chất lượng tương đồng, dựa trên các chỉ số defect và defect leakage.
Kết quả phân nhóm cho phép xác định các nhóm dự án có mức độ rủi ro cao, trung bình và thấp, qua đó
hỗ trợ Ban Giám đốc và Test Manager trong việc theo dõi chất lượng, ưu tiên nguồn lực kiểm thử và xây
dựng các chiến lược cải tiến phù hợp.
Thứ ba, dự đoán sớm khả năng xảy ra defect leakage
Bên cạnh việc phân tích dữ liệu quá khứ, nghiên cứu hướng tới mục tiêu xây dựng mô hình dự đoán khả
năng xảy ra defect leakage của dự án trong tương lai dựa trên các đặc điểm đầu vào như quy mô dự án, số
lượng test case, nguồn lực kiểm thử và lịch sử defect.
Mô hình dự báo này giúp Test Manager phát hiện sớm các dự án có nguy cơ chất lượng thấp, từ đó có thể
chủ động điều chỉnh kế hoạch kiểm thử, tăng cường kiểm soát chất lượng và giảm thiểu rủi ro trước khi
sản phẩm được bàn giao cho khách hàng.
Thứ tư, hỗ trợ ra quyết định quản lý chất lượng dự án
Mục tiêu tổng thể của việc khai phá dữ liệu là xây dựng một cơ sở phân tích dựa trên dữ liệu để hỗ trợ
quá trình ra quyết định trong quản lý chất lượng phần mềm.
Thông qua các kết quả khai phá, các cấp quản lý có thể:
- Đánh giá khách quan chất lượng dự án dựa trên dữ liệu thực tế
- So sánh các chỉ số defect với ngưỡng chuẩn (NORM) của công ty
- Xác định nguyên nhân ảnh hưởng đến chất lượng dự án
- Đề xuất các biện pháp cải tiến quy trình kiểm thử
3.2. Tiền xử lý dữ liệu
Trước khi áp dụng các kỹ thuật khai phá dữ liệu, dữ liệu thu thập cần được xử lý và chuẩn hóa nhằm đảm
bảo tính chính xác, nhất quán và phù hợp với yêu cầu của các thuật toán phân tích. Quá trình tiền xử lý
dữ liệu trong nghiên cứu được thực hiện theo một quy trình gồm các bước chính sau.
3.2.1 Làm sạch dữ liệu (Data Cleaning)
Do dữ liệu được tổng hợp từ nhiều nguồn khác nhau như hệ thống JIRA và các báo cáo kiểm thử định kỳ,
một số bản ghi có thể tồn tại tình trạng thiếu thông tin, trùng lặp hoặc không nhất quán.
9
Trong bước này, các hoạt động xử lý được thực hiện bao gồm:
- Loại bỏ các bản ghi bị thiếu thông tin quan trọng như số defect hoặc leakage
- Xử lý các giá trị bất thường hoặc sai lệch trong dữ liệu
- Loại bỏ các bản ghi trùng lặp phát sinh trong quá trình tổng hợp dữ liệu
Việc làm sạch dữ liệu giúp đảm bảo độ tin cậy và tính chính xác của dataset trước khi tiến hành phân tích.
3.2.2 Chuẩn hóa dữ liệu (Data Normalization)
Các thuộc tính số trong dataset như số lượng defect, số test case và tỷ lệ leakage có phạm vi giá trị khác
nhau. Do đó, cần thực hiện chuẩn hóa dữ liệu để đưa các thuộc tính về cùng một thang đo, giúp nâng cao
hiệu quả của các thuật toán khai phá dữ liệu.
Trong nghiên cứu này, các phương pháp chuẩn hóa được áp dụng bao gồm:
- Chuẩn hóa tỷ lệ defect leakage về dạng phần trăm
- Điều chỉnh các giá trị số về cùng đơn vị đo
3.2.3 Mã hóa dữ liệu định tính (Data Encoding)
Một số thuộc tính trong dataset thuộc dạng định tính, chẳng hạn như quy mô dự án hoặc lĩnh vực nghiệp
vụ. Các thuộc tính này cần được chuyển đổi sang dạng số để có thể sử dụng trong các thuật toán khai phá
dữ liệu.
Quá trình mã hóa được thực hiện thông qua:
- Chuyển đổi quy mô dự án thành các giá trị số tương ứng
- Mã hóa lĩnh vực nghiệp vụ thành các nhóm dữ liệu phân loại
Bước này giúp đảm bảo dữ liệu có thể được xử lý hiệu quả trong các mô hình phân cụm và phân lớp.
3.2.4 Tích hợp và chuyển đổi dữ liệu (Data Integration and Transformation)
Sau khi được làm sạch và chuẩn hóa, dữ liệu từ các nguồn khác nhau được tích hợp thành một dataset
thống nhất. Các bước thực hiện bao gồm:
- Kết hợp dữ liệu defect từ hệ thống JIRA với dữ liệu kiểm thử từ các báo cáo định kỳ
- Tính toán các chỉ số tổng hợp như tỷ lệ leakage và mật độ defect
- Chuyển đổi dữ liệu về định dạng phù hợp với công cụ khai phá dữ liệu
Dataset cuối cùng sau khi tiền xử lý được sử dụng làm dữ liệu đầu vào cho các bước phân tích và xây
dựng mô hình khai phá dữ liệu.
3.3. Kỹ thuật khai phá dữ liệu áp dụng
10
Dựa trên mục tiêu khai phá dữ liệu đã xác định, nghiên cứu lựa chọn các kỹ thuật khai phá dữ liệu phù
hợp nhằm phân tích, phát hiện mẫu và xây dựng mô hình dự báo chất lượng dự án phần mềm. Các kỹ
thuật được lựa chọn bao gồm khai phá mô tả, phân cụm và phân lớp, tương ứng với các bài toán quản lý
chất lượng thực tế tại doanh nghiệp.
3.3.1 Khai phá mô tả (Descriptive Data Mining)
Khai phá mô tả được sử dụng nhằm phân tích đặc điểm tổng quan của dữ liệu defect và xác định các xu
hướng chất lượng dự án theo thời gian.
Trong nghiên cứu này, các phương pháp phân tích mô tả được áp dụng bao gồm:
- Thống kê số lượng defect và defect leakage theo từng dự án và từng giai đoạn báo cáo
- Phân tích xu hướng biến động defect theo thời gian
- Xác định mối tương quan giữa các yếu tố như số lượng test case, nguồn lực kiểm thử và tỷ lệ
leakage
Kết quả của khai phá mô tả giúp cung cấp cái nhìn tổng thể về chất lượng dự án, đồng thời hỗ trợ phát
hiện các dấu hiệu bất thường trong dữ liệu.
3.3.2 Phân cụm dữ liệu (Clustering)
Kỹ thuật phân cụm được sử dụng nhằm phân nhóm các dự án có đặc điểm chất lượng tương đồng, từ đó
hỗ trợ việc phân loại mức độ rủi ro dự án.
Trong nghiên cứu này, thuật toán K-Means Clustering được lựa chọn do có khả năng xử lý hiệu quả dữ
liệu số và phù hợp với bài toán phân nhóm dự án dựa trên các chỉ số defect.
Các thuộc tính chính được sử dụng cho phân cụm bao gồm:
- Tổng số defect
- Tỷ lệ defect leakage
- Số lượng test case
- Số lượng nhân sự kiểm thử
Kết quả phân cụm giúp chia các dự án thành các nhóm rủi ro thấp, trung bình và cao, hỗ trợ Test Manager
và Ban Giám đốc trong việc ưu tiên nguồn lực kiểm thử và giám sát chất lượng.
3.3.3 Phân lớp dữ liệu (Classification)
Bên cạnh việc phân tích và phân nhóm, nghiên cứu còn áp dụng kỹ thuật phân lớp nhằm xây dựng mô
hình dự báo khả năng xảy ra defect leakage của dự án.
Trong nghiên cứu này, thuật toán Decision Tree được lựa chọn do có các ưu điểm:
- Dễ hiểu và dễ diễn giải kết quả
11
- Phù hợp với dữ liệu quản lý dự án
- Có khả năng xác định rõ các yếu tố ảnh hưởng đến chất lượng
Mô hình phân lớp sử dụng các thuộc tính đầu vào như quy mô dự án, số lượng test case, số nhân sự kiểm
thử và lịch sử defect để dự đoán khả năng dự án có nguy cơ leakage cao hay thấp.
Kết quả của mô hình giúp hỗ trợ Test Manager trong việc phát hiện sớm rủi ro chất lượng và chủ động
đưa ra các biện pháp kiểm soát phù hợp.
3.3.4 Ý nghĩa ứng dụng của các kỹ thuật khai phá dữ liệu
Việc kết hợp các kỹ thuật khai phá dữ liệu trên cho phép xây dựng một hệ thống phân tích chất lượng dự
án toàn diện, từ việc mô tả hiện trạng, phân nhóm rủi ro đến dự báo chất lượng trong tương lai.
Các kết quả khai phá không chỉ phục vụ mục tiêu nghiên cứu mà còn có ý nghĩa thực tiễn quan trọng trong
việc hỗ trợ ra quyết định quản lý chất lượng phần mềm tại doanh nghiệp.
4. Báo cáo tóm tắt kết quả thu được
Sau khi thực hiện quá trình tiền xử lý và áp dụng các kỹ thuật khai phá dữ liệu, nghiên cứu đã thu được
các kết quả quan trọng liên quan đến đặc điểm chất lượng dự án phần mềm và các yếu tố ảnh hưởng đến
defect leakage.
4.1 Kết quả phân tích mô tả dữ liệu
Kết quả phân tích mô tả cho thấy dữ liệu defect có sự khác biệt đáng kể giữa các dự án về số lượng lỗi,
mức độ nghiêm trọng và tỷ lệ defect leakage.
Một số xu hướng chính được ghi nhận như sau:
- Các dự án có quy mô lớn thường phát sinh số lượng defect cao hơn so với các dự án quy mô nhỏ
và trung bì
- Tỷ lệ defect leakage có xu hướng tăng trong các dự án có thời gian kiểm thử ngắn hoặc khối
lượng test case không tương xứng với độ phức tạp của hệ thống.
- Các dự án có tỷ lệ test case pass thấp thường có nguy cơ defect leakage cao hơn.
Kết quả này cung cấp cơ sở dữ liệu quan trọng giúp Test Manager nhận diện sớm các dấu hiệu rủi ro chất
lượng dự án.
12
4.2 Kết quả phân cụm dự án theo mức độ rủi ro
Áp dụng thuật toán K-Means Clustering đã giúp phân nhóm các dự án thành ba nhóm chính dựa trên các
chỉ số defect và leakage:
Nhóm rủi ro thấp:
Bao gồm các dự án có số lượng defect thấp, tỷ lệ leakage nhỏ và hiệu quả kiểm thử cao. Đây là các dự
án có chất lượng ổn định và ít cần giám sát đặc biệt.
Nhóm rủi ro trung bình:
Bao gồm các dự án có số lượng defect ở mức trung bình và tỷ lệ leakage dao động trong ngưỡng cho
phép. Nhóm này cần được theo dõi định kỳ để đảm bảo chất lượng không suy giảm.
Nhóm rủi ro cao:
Bao gồm các dự án có tỷ lệ defect leakage vượt ngưỡng NORM của công ty. Đây là các dự án cần được
ưu tiên kiểm soát chất lượng và có các biện pháp cải thiện kịp thời.
Kết quả phân cụm giúp Test Manager và Ban Giám đốc nhanh chóng xác định các dự án có rủi ro cao và
phân bổ nguồn lực kiểm thử một cách hiệu quả.
4.3 Kết quả xây dựng mô hình dự báo defect leakage
Mô hình Decision Tree được xây dựng nhằm dự đoán khả năng xảy ra defect leakage cao của dự án dựa
trên các đặc điểm đầu vào.
Kết quả phân tích cho thấy các yếu tố ảnh hưởng mạnh nhất đến defect leakage bao gồm:
- Quy mô dự án
- Số lượng test case được thực thi
- Số lượng nhân sự kiểm thử tham gia
- Tỷ lệ test case pass
Mô hình dự báo có khả năng hỗ trợ phát hiện sớm các dự án có nguy cơ chất lượng thấp, giúp Test
Manager chủ động thực hiện các biện pháp kiểm soát chất lượng trước khi sản phẩm được bàn giao.
4.4 Giá trị ứng dụng trong quản lý chất lượng phần mềm
Các kết quả khai phá dữ liệu mang lại nhiều giá trị thực tiễn cho doanh nghiệp, cụ thể:
- Hỗ trợ đánh giá chất lượng dự án dựa trên dữ liệu khách quan thay vì cảm tính
- Giúp so sánh các chỉ số defect với ngưỡng chuẩn NORM của công ty
- Hỗ trợ phân loại dự án theo mức độ rủi ro chất lượng
- Giúp Test Manager và Project Manager chủ động đưa ra giải pháp cải thiện chất lượng dự án
- Nâng cao hiệu quả phân bổ nguồn lực kiểm thử
13
Nhờ đó, việc áp dụng khai phá dữ liệu góp phần đảm bảo chất lượng đầu ra của sản phẩm phần mềm trước
khi bàn giao cho khách hàng.
4.5 Hạn chế và hướng phát triển
Mặc dù đạt được các kết quả tích cực, nghiên cứu vẫn còn một số hạn chế nhất định:
- Dữ liệu phụ thuộc vào mức độ chính xác của việc ghi nhận defect trên hệ thống JIRA.
- Một số yếu tố ảnh hưởng đến chất lượng dự án như độ phức tạp nghiệp vụ hoặc năng lực nhân sự
chưa được lượng hóa đầy đủ trong dataset.
Trong tương lai, nghiên cứu có thể được mở rộng bằng cách:
- Tích hợp thêm dữ liệu về yêu cầu thay đổi (change request) và mức độ phức tạp hệ thống.
- Áp dụng các mô hình học máy nâng cao nhằm nâng cao độ chính xác dự báo.
Kết luận
Trong bối cảnh các dự án phần mềm ngày càng có quy mô lớn và độ phức tạp cao, việc đảm bảo chất
lượng sản phẩm trước khi bàn giao cho khách hàng trở thành một yêu cầu cấp thiết đối với các doanh
nghiệp phát triển phần mềm. Trong đó, các chỉ số defect và defect leakage đóng vai trò là những thước đo
quan trọng phản ánh mức độ ổn định và chất lượng đầu ra của dự án.
Xuất phát từ nhu cầu thực tiễn tại đơn vị công tác, nghiên cứu đã tiến hành thu thập, xử lý và phân tích
dữ liệu defect từ hệ thống quản lý lỗi và các báo cáo kiểm thử định kỳ, nhằm ứng dụng các kỹ thuật khai
phá dữ liệu trong quản lý chất lượng phần mềm.
Kết quả nghiên cứu đã đạt được một số nội dung chính như sau:
- Xây dựng được dataset phản ánh đầy đủ tình hình defect và defect leakage của các dự án phần
mềm tại doanh nghiệp.
- Phân tích và phát hiện các xu hướng, đặc điểm liên quan đến chất lượng dự án dựa trên dữ liệu
thực tế.
- Áp dụng các kỹ thuật khai phá dữ liệu như phân tích mô tả, phân cụm và phân lớp để xác định
các yếu tố ảnh hưởng đến defect leakage và phân nhóm dự án theo mức độ rủi ro chất lượng.
- Xây dựng mô hình dự báo giúp phát hiện sớm các dự án có nguy cơ defect leakage cao, hỗ trợ
Test Manager trong việc chủ động kiểm soát chất lượng.
Thông qua việc khai thác dữ liệu defect, doanh nghiệp có thể chuyển từ phương thức quản lý dựa trên báo
cáo thống kê sang quản lý dựa trên phân tích và dự báo dữ liệu, từ đó nâng cao hiệu quả ra quyết định, tối
ưu nguồn lực kiểm thử và đảm bảo chất lượng sản phẩm trước khi bàn giao cho khách hàng.
14
Tuy nhiên, nghiên cứu vẫn còn một số hạn chế do phạm vi dữ liệu chưa bao quát toàn bộ các yếu tố ảnh
hưởng đến chất lượng dự án, đặc biệt là các yếu tố định tính như mức độ phức tạp nghiệp vụ hoặc năng
lực nhân sự. Trong tương lai, nghiên cứu có thể được mở rộng bằng cách tích hợp thêm các nguồn dữ liệu
liên quan đến quy trình phát triển phần mềm và áp dụng các mô hình học máy nâng cao để cải thiện độ
chính xác dự báo.
Tổng thể, nghiên cứu đã chứng minh tính khả thi và hiệu quả của việc ứng dụng khai phá dữ liệu trong
quản lý defect và defect leakage tại doanh nghiệp, góp phần nâng cao chất lượng phát triển phần mềm và
hỗ trợ công tác quản lý chất lượng một cách khoa học, khách quan và chủ động.
5. Demo ứng dụng khai phá dữ liệu defect leakage
(Do tính bảo mật an toàn thông tin của dự án, đơn vị công tác, học viên xin phép không public data thật
mà sẽ đưa ra demo minh hoạ)
TÀI LIỆU THAM KHẢO
1. 2. IEEE Computer Society. (2014). IEEE Standard for Software Quality Assurance Processes.
Tài liệu và báo cáo nội bộ về quản lý defect và chất lượng dự án tại đơn vị công tác.
15