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

### Kịch bản đắt nhất 1: [mô tả]

- **AI nói nguyên văn:**
- **Người dùng thấy gì:**
- **Người dùng làm gì tiếp:**
- **Ai được báo, sau bao lâu:**
- **Cách xử lý chọn (hỏi lại / trả lời kèm giới hạn / dừng và chuyển người):**
- **Phương án đã cân nhắc và lý do loại:**
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và cách sửa:**
- **Nguyên tắc HAX/PAIR và vị trí thể hiện:**
- **Lỗi không thể giải quyết chỉ bằng câu chữ, nếu có:**

### Kịch bản đắt nhất 2: [mô tả]

- **AI nói nguyên văn:**
- **Người dùng thấy gì:**
- **Người dùng làm gì tiếp:**
- **Ai được báo, sau bao lâu:**
- **Cách xử lý chọn (hỏi lại / trả lời kèm giới hạn / dừng và chuyển người):**
- **Phương án đã cân nhắc và lý do loại:**
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và cách sửa:**
- **Nguyên tắc HAX/PAIR và vị trí thể hiện:**
- **Lỗi không thể giải quyết chỉ bằng câu chữ, nếu có:**

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
