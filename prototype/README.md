# Prototype dự thảo — T2 Giáo dục · Nhóm [Tên nhóm]

> Hoàn thiện sau khi nhóm chọn track và dựng prototype. Thêm 1–2 ảnh chụp màn hình có đánh số để dẫn chiếu từ `spec.md` §5.

## Prototype

- **Link hoặc file HTML:**
- **Công cụ:**
- **Phần được mô phỏng:**
- **Có lời gọi AI thật không:**

## Ảnh minh hoạ

### Ảnh 1 — Tài liệu §3.3 sai

- **Ảnh:** ![Ảnh 1: Cảnh báo tài liệu §3.3 sai và chuyển TA](anh-1-tai-lieu-sai-sec3-3.png)
- **Các số chú thích và ý nghĩa:**
  1. Mã mục §3.3 và câu sai trong tài liệu giúp học viên đối chiếu nguồn.
  2. Cảnh báo kèm phản ví dụ chỉ rõ vì sao không thể khẳng định câu đó đúng.
  3. Nút gửi TA, chặn đăng FAQ và hoàn tác ticket thể hiện giới hạn hành động.
- **Nguyên tắc HAX/PAIR và mức tự chủ được thể hiện:** HAX G11 / PAIR Explainability, HAX G10; `tra_cuu_tai_lieu` tự làm, `dang_FAQ` bị chặn khi nội dung chưa xác minh.

### Ảnh 2 — TA ngoài giờ trước hạn nộp

- **Ảnh:** ![Ảnh 2: Giờ TA, hạn bài 3, ticket trong hàng đợi và nút xem gợi ý](anh-2-ta-ngoai-gio.png)
- **Các số chú thích và ý nghĩa:**
  1. Đồng hồ 22:40, hạn 23:59 và giờ TA 08:00–22:00 cho thấy TA đã hết giờ trước hạn nộp.
  2. Ticket trong hàng đợi ghi thời gian nhận hỗ trợ từ 08:00 sáng mai.
  3. Nút xem gợi ý bước 1 chỉ mở nội dung khi học viên chọn, không đưa đáp số bài đang mở.
- **Nguyên tắc HAX/PAIR và mức tự chủ được thể hiện:** HAX G2, G11 / PAIR Graceful Failure; `chuyen_TA` mô phỏng hàng đợi, `goi_y_bai_tap` cần học viên chọn xem.

## Luồng đề xuất từ kịch bản #3 và #8

Prototype dùng một màn hình chat học viên. Có thể thêm panel hàng chờ TA làm màn hình thứ hai. Nút chọn **Ca #3 / Ca #8** chỉ phục vụ demo. Các hành động dưới đây là dự thảo; chốt mức tự chủ của tool trong `spec.md` §4 trước khi hoàn thiện prototype.

### Ca #3 — tài liệu §3.3 có câu sai

1. Học viên hỏi: “Tài liệu ghi độ lệch chuẩn luôn nhỏ hơn phương sai, đúng không ạ?”.
2. Trợ lý AI hiển thị nguồn `tra_cuu_tai_lieu`: §3.3, kèm nhãn **Tài liệu cần kiểm tra**. Cho thấy phản ví dụ: phương sai 0,25 thì độ lệch chuẩn 0,5. Ghi rõ chưa có xác nhận của giảng viên.
3. Hiện **Gửi câu hỏi cho TA** và **Sao chép đoạn cần hỏi giảng viên**. Nút gửi mở bước xác nhận, cho xem câu hỏi và trích dẫn sắp chuyển. Không có nút đăng FAQ cho câu đang tranh chấp.
4. Nếu học viên gửi, hiển thị **Đã vào hàng chờ TA** và giờ TA 08:00–22:00; nếu không gửi, không ai được báo. Không nói đã báo giảng viên vì bộ tool không có chức năng đó.

### Ca #8 — xin TA lúc 22:40 trước hạn bài 3

1. Học viên nhắn xin chuyển TA lúc 22:40. Thẻ thời gian cho thấy TA làm việc 08:00–22:00; bài 3 hạn 23:59 ngày 13/11/2026.
2. Trợ lý nói rõ TA có thể xem từ 08:00 sáng mai, sau hạn; không hứa trả lời ngay hay gia hạn bài.
3. Nút **Xem gợi ý bước đầu** mở gợi ý từ §3.1–§3.5, không đưa hoặc xác nhận đáp số bài đang mở.
4. Nút **Gửi câu hỏi cho TA (xem từ 08:00)** mở xác nhận có cảnh báo phản hồi có thể đến muộn. Sau khi gửi, hiển thị **Đã vào hàng chờ**, không hiển thị **TA đang trả lời**. Nếu không gửi, không có thông báo cho TA.

### Các chỗ cần đánh số trên ảnh

| Số | Chỗ trên màn hình | Ý nghĩa |
|---|---|---|
| 1 | Nhãn “Trợ lý AI” | HAX G1: biết đang tương tác với AI |
| 2 | Trích §3.3 hoặc dữ liệu giờ TA/hạn bài | HAX G11 / PAIR Explainability: thấy căn cứ |
| 3 | “Tài liệu cần kiểm tra” hoặc “TA đã hết giờ” | HAX G2/G10: thấy giới hạn và độ chắc |
| 4 | Nút gợi ý hoặc chuyển TA | PAIR Graceful Failure: có bước tiếp theo |
| 5 | “Đã vào hàng chờ” | Phân biệt gửi câu hỏi với TA đã trả lời |

### Chờ §4 chốt trước khi dựng bản cuối

- `tra_cuu_tai_lieu` có tự chạy không.
- `chuyen_TA` cần học viên xác nhận hay AI tự chuyển trong trường hợp nào.
- `dang_FAQ` bị cấm, cần duyệt, hay chỉ chặn nội dung đang tranh chấp.
- `goi_y_bai_tap` được gợi ý tới mức nào với bài đang mở.
