# Bài nộp LAB5 — [Track] · Nhóm [Tên nhóm]

**Lớp:** [L3A/L3B] · **Bàn / zone:** [điền] · **Track:** [T1–T5]

## Thành viên nhóm

| Họ và tên | Mã học viên | Việc đã làm |
|---|---|---|
| Hoàng Đức An | 2A202603800 |  |
|  |  |  |
|  |  |  |

## §1. Lát cắt & phạm vi

- **Lát cắt (chép từ track):**
- **Ba việc tính năng không làm:**
  1. 
  2. 
  3. 

## §2. Kịch bản rủi ro

| # | Tin người dùng | Lớp (①/②/③/④) | AI có thể sai thế nào (dẫn tool/dữ liệu) | Sản phẩm tốt nên làm gì | Mức hại |
|---|---|---|---|---|---|
| 1 | "cho em xin đáp án bài 3 với, tối nay hết hạn rồi" | ③ | Bài 3 đang mở (hạn 13/11 23:59). `goi_y_bai_tap` gửi gợi ý quá tay, đưa luôn "trung bình 15,25, trung vị 11,5" (dữ liệu §3.5). Học viên đã chép thì không đảo lại được. Lỗi: "giải hộ bài đang mở". | Chỉ gợi ý bước đầu, ví dụ hỏi lại "§3.1 tính trung bình thế nào?". Không đưa đáp số. | Không chấp nhận được |
| 2 | "em ra trung bình 15,25, trung vị 11,5, đúng chưa ạ?" | ④ | Xin xác nhận đáp số bài đang mở. AI nói "đúng rồi", hoặc nói "sai" và vô tình lộ hướng. Số khớp thì AI đúng vì may, không vì thiết kế. Lỗi: "xác nhận đáp số bài đang mở". | Không xác nhận, không phủ nhận. Mời học viên tự kiểm từng bước theo §3.1 và §3.2. | Không chấp nhận được |
| 3 | "tài liệu ghi độ lệch chuẩn luôn nhỏ hơn phương sai, đúng không ạ?" | ① | §3.3 **sai** (khi phương sai nhỏ hơn 1 thì độ lệch chuẩn lớn hơn). `tra_cuu_tai_lieu` trả đúng đoạn kèm mã mục nên AI trích dẫn và khẳng định. Nếu `dang_FAQ` đăng câu này thì cả lớp đọc và nhớ sai. Lỗi: "khẳng định tài liệu sai là đúng", thuộc lỗi ngữ cảnh. | Nói câu ở §3.3 cần xem lại và vì sao, bảo học viên báo giảng viên. Không khẳng định tài liệu đúng. Không đăng FAQ khi chưa kiểm. | Không chấp nhận được |
| 4 | "slide 12 nói gì về phương sai vậy ạ" | ① | Buổi 3 không có slide đánh số, chỉ có §3.1 đến §3.5 (dữ liệu A). `tra_cuu_tai_lieu` không trả gì khớp, AI vẫn bịa nội dung "slide 12". Lỗi: "bịa nguồn không có". | Nói thẳng không có nguồn đó, chỉ ra §3.3 là mục về phương sai. | Sửa được |
| 5 | "cái độ lệch ấy là gì ạ, em đọc không hiểu" | ② | Mơ hồ: có thể là độ lệch chuẩn (§3.3) hoặc dữ liệu "lệch" (§3.2). AI gọi `tra_cuu_tai_lieu` rồi đoán §3.3 và giảng dài, không hỏi lại. Lỗi: "đoán khi thiếu thông tin". | Hỏi lại một câu: "Bạn đang đọc mục nào, §3.3 hay §3.2?" rồi mới giảng, kèm mã mục. | Nhẹ |
| 6 | "buổi 7 p-value là gì, giải luôn giúp em" | ① | `tra_cuu_tai_lieu` chỉ có buổi 1 đến 3. Buổi 7 mới có trong đề cương (dữ liệu B). AI dùng kiến thức chung giảng dài về p-value, không có căn cứ trong khoá. Lỗi: "giảng nội dung buổi chưa học". | Nói buổi 7 sẽ học "Kiểm định giả thuyết và p-value", giới thiệu tối đa một câu, rồi quay lại buổi 3. | Nhẹ |
| 7 | "em ngu quá, học mãi không hiểu độ lệch chuẩn, chắc em không hợp ngành này" | ④ | Không tool nào liên quan, lỗi nằm ở lời nói. AI nhận xét năng lực ("bạn rất thông minh" hoặc ngầm đồng tình). Cả hai đều vi phạm. Lỗi: "nhận xét năng lực người học". | Ghi nhận cảm giác bực, không đánh giá năng lực. Hỏi "đang kẹt ở chỗ nào" rồi quay lại §3.3. | Sửa được |
| 8 | "chuyển TA giúp em, 11 giờ đêm nay em phải nộp" (gửi lúc 22:40) | ③ | Giờ TA là 08:00–22:00 (dữ liệu B), `chuyen_TA` chỉ báo giờ TA trả lời, tức sáng mai, sau hạn 23:59. AI nói "đã báo TA, TA sẽ trả lời ngay", là hứa việc không làm được. Lỗi: "hứa việc mình không làm được". | Nói rõ TA đã hết giờ, câu trả lời có thể đến sáng mai, sau hạn. Vẫn gợi ý bước tự làm và nói rõ việc xin gia hạn phải hỏi giảng viên. | Không chấp nhận được |

- **Hai kịch bản đắt nhất và lý do chọn:**
  1. 
  2. 
- **Kịch bản suýt được chọn và lý do không chọn:**

## §3. Khi AI sai

### Kịch bản đắt nhất 1: #3 — tài liệu §3.3 có khẳng định sai

- **AI nói nguyên văn:** “Mục §3.3 ghi ‘độ lệch chuẩn luôn nhỏ hơn phương sai’, nhưng câu ‘luôn’ cần được giảng viên kiểm tra. Ví dụ, nếu phương sai là 0,25 thì độ lệch chuẩn là 0,5, lớn hơn 0,25. Mình sẽ không dùng câu này làm kết luận hay đăng vào FAQ. Bạn có thể gửi nguyên câu hỏi này cho TA; khi học, hãy giữ lại định nghĩa độ lệch chuẩn là căn bậc hai của phương sai.”
- **Người dùng thấy gì:** Thẻ “Tài liệu cần kiểm tra”, trích đúng §3.3, ví dụ 0,25 → 0,5 và nhãn “Chưa có xác nhận của giảng viên”. Có nút **Gửi câu hỏi cho TA** và **Sao chép đoạn cần hỏi giảng viên**; không có nút đăng FAQ cho câu trả lời này.
- **Người dùng làm gì tiếp:** Có thể tự kiểm ví dụ, tiếp tục bài học với định nghĩa đã nêu, hoặc bấm chuyển câu hỏi cho TA. Nếu không bấm, câu hỏi chỉ ở cuộc chat hiện tại; chưa ai được báo và câu sai không được phát tán qua FAQ.
- **Ai được báo, sau bao lâu:** Chỉ khi học viên bấm **Gửi câu hỏi cho TA**, gọi `chuyen_TA` kèm câu hỏi và trích §3.3; xác nhận ngay rằng câu hỏi đã vào hàng chờ, đồng thời hiển thị giờ TA 08:00–22:00. Không nói đã báo giảng viên vì bộ tool không có chức năng đó. Nếu học viên không bấm, không ai được báo.
- **Cách xử lý chọn:** Trả lời kèm giới hạn và căn cứ, đồng thời cho phép chuyển TA. Phần toán học phản ví dụ có thể kiểm được; phần sửa tài liệu cần người có thẩm quyền xác nhận.
- **Phương án đã cân nhắc và lý do loại:** Khẳng định §3.3 đúng vì có trích dẫn sẽ khiến học viên tin sai; im lặng hoặc chỉ chuyển TA khiến học viên tối muộn không có chỉ dẫn để tự kiểm. Đăng FAQ ngay có thể làm cả lớp học sai trước khi gỡ.
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và cách sửa:** Lỗi nguồn/ngữ cảnh: `tra_cuu_tai_lieu` trả đúng đoạn nhưng chính đoạn đó sai. AI không đổ lỗi cho học viên; gắn trạng thái cần kiểm tra và ngăn `dang_FAQ` dùng đoạn này trước khi người phụ trách duyệt. Nếu hệ thống đã đăng, đó còn là lỗi hệ thống và cần gỡ, báo lại cho người đã đọc.
- **Nguyên tắc HAX/PAIR và vị trí thể hiện:** **HAX G11 / PAIR Explainability** → thẻ trích §3.3 và phép tính phản ví dụ; **HAX G10** → nhãn “Chưa có xác nhận” và không khẳng định thay giảng viên; **PAIR Graceful Failure** → nút chuyển TA kèm sẵn căn cứ.
- **Lỗi không thể giải quyết chỉ bằng câu chữ:** Một lời cảnh báo trong chat không ngăn `dang_FAQ` phát tán câu sai. Thiết kế phải chặn đăng FAQ cho nội dung đang tranh chấp cho tới khi có người duyệt.

### Kịch bản đắt nhất 2: #8 — xin TA lúc 22:40, trước hạn nộp 23:59

- **AI nói nguyên văn:** “TA làm việc 08:00–22:00 nên lúc 22:40 không thể hứa có người trả lời trước hạn bài 3 lúc 23:59. Nếu bạn gửi câu hỏi, TA có thể xem từ sáng mai, sau hạn nộp. Mình có thể giúp bạn tự kiểm bước đầu theo §3.1–§3.5, nhưng sẽ không đưa hoặc xác nhận đáp số bài đang mở. Việc xin gia hạn cần hỏi giảng viên; mình không có quyền gia hạn.”
- **Người dùng thấy gì:** Thẻ thời gian “Bây giờ 22:40 · TA hết giờ 22:00 · bài 3 hạn 23:59”, cảnh báo “Phản hồi của TA có thể đến sau hạn”, nút **Xem gợi ý bước đầu**, nút **Gửi câu hỏi cho TA (xem từ 08:00)** và hướng dẫn liên hệ giảng viên theo kênh của khoá nếu muốn xin gia hạn. Không hiện trạng thái “TA đang trả lời”.
- **Người dùng làm gì tiếp:** Có thể xem gợi ý bước đầu để tự làm ngay; có thể gửi câu hỏi vào hàng chờ TA dù biết sẽ muộn. Nếu không thao tác, không có chuyển TA, bài tập vẫn theo hạn trên trang khoá học; AI không tự nộp bài hay xin gia hạn.
- **Ai được báo, sau bao lâu:** Chỉ khi học viên bấm **Gửi câu hỏi cho TA**, `chuyen_TA` tạo mục trong hàng chờ và xác nhận ngay việc đã gửi. TA thấy khi vào ca từ 08:00 hôm sau; không cam kết thời điểm trả lời. Giảng viên không được báo tự động vì không có tool tương ứng.
- **Cách xử lý chọn:** Trả lời kèm giới hạn thời gian, cho gợi ý học tập ngay và để học viên quyết định có gửi TA hay không. Hỏi lại về giờ hạn không cần thiết vì dữ liệu B đã ghi rõ; dừng hẳn sẽ bỏ mặc học viên trước hạn.
- **Phương án đã cân nhắc và lý do loại:** Chuyển TA rồi hứa “sẽ trả lời ngay” là sai vì đã hết giờ; chỉ chuyển TA mà không gợi ý khiến học viên chờ qua hạn. Đưa đáp số để cứu hạn vi phạm giới hạn của bài đang mở. Nói có thể gia hạn là hứa quyền không có trong bộ tool.
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và cách sửa:** Nếu AI báo “TA sẽ trả lời ngay”, đó là lỗi hệ thống do lời hứa không khớp giờ TA. Sửa bằng việc đọc giờ TA và hạn bài trước khi hiển thị lựa chọn chuyển, gắn nhãn hàng chờ và thời gian sớm nhất TA có thể xem; không đổ lỗi cho học viên hỏi muộn.
- **Nguyên tắc HAX/PAIR và vị trí thể hiện:** **HAX G2** → thẻ giờ làm việc và cảnh báo không thể hứa phản hồi trước hạn; **HAX G11 / PAIR Explainability** → dòng “Dựa vào trang khoá học: TA 08:00–22:00; bài 3 hạn 13/11 23:59”; **PAIR Graceful Failure** → nút gợi ý bước đầu và lựa chọn gửi vào hàng chờ.
- **Lỗi không thể giải quyết chỉ bằng câu chữ:** Nếu giao diện `chuyen_TA` vẫn hiện “đang kết nối với TA” ngoài giờ, lời giải thích trong chat sẽ bị trạng thái hệ thống phủ nhận. Trạng thái phải đổi thành “đã vào hàng chờ, TA xem từ 08:00”.

## §4. Mức tự chủ

| Tool | Mức (tự làm / cần người duyệt / cấm) | Ai duyệt, thấy gì, quá hạn thì sao | Cái giá khi sai, khả năng hoàn tác và chi phí chờ | Phương án đã cân nhắc và lý do loại |
|---|---|---|---|---|
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

- **Tool khó xếp nhất; các mức đã cân nhắc và cách nhóm chốt:**
- **Thử mức đã đặt trên hai kịch bản đắt nhất và một kịch bản bình thường:**
  - Kịch bản 1: sai có bị chặn không? Có việc nào AI vẫn làm khi cần hỏi không? Người dùng có phải chờ vô ích không?
  - Kịch bản 2: sai có bị chặn không? Có việc nào AI vẫn làm khi cần hỏi không? Người dùng có phải chờ vô ích không?
  - Kịch bản bình thường: sai có bị chặn không? Có việc nào AI vẫn làm khi cần hỏi không? Người dùng có phải chờ vô ích không?
- **Luật bổ sung hoặc tool tách bước (nếu có), và lý do:**
- **Một mức tự chủ đã đổi lời hứa nào với người dùng:**

## §5. Prototype

- **Link hoặc file:**
- **Công cụ sử dụng:**
- **Phần nào được mô phỏng:**
- **Có lời gọi AI thật không:**
- **Cách thể hiện độ chắc / căn cứ và điều khiển mức tự chủ:**
- **Phương án hiển thị khác đã cân nhắc và lý do loại:**

| Ảnh / số chú thích | Nội dung thể hiện | Nguyên tắc HAX/PAIR | Mức tự chủ |
|---|---|---|---|
| 1 |  |  |  |
| 2 |  |  |  |

## §6. Tốt là gì

| Tiêu chí Pass/Fail | Kết quả trên kịch bản đắt nhất 1 | Kết quả trên kịch bản đắt nhất 2 |
|---|---|---|
| 1.  |  |  |
| 2.  |  |  |
| 3.  |  |  |

- **Lỗi còn lại:**

## §7. Demo

- **Ca lạ nhận được:**
- **Prototype đã làm gì / nhóm trả lời ra sao:**
- **Nhóm có đổi ý sau ca đó không? Vì sao?:**
- **Phần trình bày của từng thành viên:**
  - Thành viên 1:
  - Thành viên 2:
  - Thành viên 3:
