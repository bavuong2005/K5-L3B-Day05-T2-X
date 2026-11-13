# Bài nộp LAB5 — T2 Giáo dục · Nhóm [TÊN NHÓM]

> **Bản nháp — làm xong §1, §2.** Copy file này sang repo nộp bài mới, đổi tên thành `spec.md`, điền bảng thành viên. Repo nộp đặt tên `K5-<lớp>-Day05-T2-<tên nhóm>`, để công khai.

**Lớp:** [L3A / L3B] · **Bàn / zone:** ____ · **Track:** T2 Giáo dục

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
|  |  | §1–§2 · kịch bản rủi ro, bằng chứng, chọn 2 ca đắt |
|  |  | §3–§4 · UX khi AI sai, mức tự chủ |
|  |  | §5 · prototype + màn TA, 2 ảnh đánh số |

---

## §1. Lát cắt & phạm vi

**Lát cắt (chép từ track):**

> Trong **trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode)**, khi **học viên** đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, **AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên"**, để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

- **Một người dùng:** học viên khoá "Nhập môn phân tích dữ liệu", đang học buổi 3.
- **Một việc:** hỏi bài lúc tối muộn, khi không còn ai để hỏi.
- **Một quyết định của AI:** giảng kèm trích tài liệu · hỏi lại cho rõ · gợi ý từng bước · hay nói "tài liệu không có, hỏi giảng viên".
- **Một kết quả:** học viên hiểu đúng bài, không chép đáp án, không học sai mà không biết.

**Phạm vi bản prototype:** 1 màn học viên + 1 màn TA (hàng chờ và hàng duyệt), dựng đúng ca **22:47 ngày 12/11/2026 — bài tập 3 đang mở, hạn 13/11 23:59, TA đã hết giờ** kèm nhánh **tài liệu §3.3 có câu sai**. Không dựng đăng nhập, danh sách học viên, hay các buổi khác — không lệch khỏi lát cắt.

**Ba việc tính năng KHÔNG làm:**

1. **Không chấm bài, không chốt điểm, không xác nhận đáp số bài đang mở** — AI không phải giảng viên; chốt sai một con số thì học viên nộp sai mà tin là đúng, và đã đọc thì không đảo lại được (kịch bản #7, #8, #13 ở §2).
2. **Không dạy trước nội dung buổi chưa học (buổi 4–10)** — đề cương trên trang khoá học chỉ có tên buổi, chưa có tài liệu; dạy trước là bịa nội dung không có nguồn (kịch bản #2).
3. **Không tự sửa tài liệu, không tự đăng FAQ công khai** — sửa tài liệu là đổi nguồn sự thật cho cả lớp; FAQ nhiều người đã đọc trước khi gỡ kịp; cả hai phải qua người (giảng viên / TA) duyệt (kịch bản #3, #9).
4. **Không dạy công cụ ngoài chương trình (Excel…)** — tài liệu khoá chỉ ghi "bài tập làm bằng bảng tính", không có tên hàm nào; không có nguồn mà dạy là bịa (kịch bản #11).
5. **Không nhận xét năng lực học viên** — một câu đánh giá sai ("em yếu phần này") đúng lúc học viên mười giờ tối cần giúp thì học viên bỏ học; đánh giá là việc của giảng viên (kịch bản #10).

---

## §2. Kịch bản rủi ro *(chặng 2)*

**Nhãn:** `nhẹ` = học viên tự thấy, tự sửa · `sửa được` = tốn công, có người gỡ · `không chấp nhận được` = học sai / đánh mất thứ không đảo lại được.
**⭐ = hai kịch bản đắt nhất (lập luận ở cuối mục).**

| # | Tin người dùng nhắn | Lớp | AI có thể sai thế nào *(bằng chứng: tool / dòng dữ liệu của track)* | Sản phẩm tốt nên làm gì | Tên lỗi | Nhãn |
|---|---|---|---|---|---|---|
| 1 | "Slide 12 nói gì về trung vị ạ?" | ① | `tra_cuu_tai_lieu` trả đúng §3.2 nhưng gán nhãn "slide 12" — trong khi Dữ liệu A ghi rõ *tài liệu buổi 3 không có slide đánh số* → bịa nguồn | Nói rõ tài liệu chỉ có §3.1–§3.5; trả nội dung kèm mã mục; không nhắc slide | Bịa nguồn không tồn tại | sửa được |
| 2 | "Buổi 4 học gì, cần chuẩn bị gì không?" | ① | Đề cương (Dữ liệu B) chỉ có tên "Trực quan hoá dữ liệu", chưa có tài liệu → AI kể luôn "biểu đồ cột, Tableau, cần cài phần mềm" | Chỉ nêu tên buổi 4 lấy từ trang khoá học + tối đa một câu; nói rõ tài liệu chưa mở | Bịa nội dung buổi chưa học | sửa được |
| 3 ⭐ | "Tài liệu ghi 'độ lệch chuẩn luôn nhỏ hơn phương sai', đúng không ạ?" | ①+④ | §3.3 khẳng định **sai** (chỉ đúng khi phương sai > 1; bộ 0, 0, 1, 1 có phương sai 0,25 < độ lệch chuẩn 0,5); AI đọc nguyên văn và lặp lại như sự thật → cả lớp học sai, không ai báo | Tách thẻ "nguồn có thể sai": nêu phản ví dụ bằng bộ số khác, gắn cờ "§3.3 cần xem lại", đưa vào hàng chờ giảng viên duyệt; không sửa tài liệu | Khẳng định lại câu sai của nguồn | không chấp nhận được |
| 4 | "Bài 3 làm sao ạ?" | ② | Trang khoá học đang có cả "Buổi 3" và "Bài tập 3 (đang mở)" → AI chọn nhầm, nhảy thẳng vào bài tập đang mở và đưa lời giải | Hỏi lại một câu, hai lựa chọn: "học nội dung buổi 3" hay "làm bài tập 3", kèm trạng thái bài | Đoán khi thiếu thông tin | sửa được |
| 5 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | ② | §3.3 chỉ có "độ lệch chuẩn"; học viên có thể đang hỏi độ lệch của một giá trị so với trung bình → AI giảng lệch chủ đề | Hỏi lại một câu với hai cách hiểu; vẫn mơ hồ thì cho ví dụ ngắn | Giảng lệch chủ đề | nhẹ |
| 6 | "Bài 2 em ra trung bình 6 đúng không ạ?" | ② | Bài 2 đã hết hạn, đáp án công bố 07/11 là 6 (Dữ liệu B) → được giải thích đầy đủ; rủi ro ngược lại: AI từ chối máy móc vì không đọc trạng thái bài | Đọc trạng thái từ trang khoá học; giải thích đầy đủ + cách tính; không lẫn với bài 3 đang mở | Từ chối oan việc được phép làm | nhẹ |
| 7 | "Chị giải hộ em bài 3 luôn, 12h rồi em ngủ" | ③+④ | `goi_y_bai_tap` bị đẩy thành lời giải trọn vẹn — bảng tool ghi rõ *"gợi ý quá tay thì học viên đã chép"*, đã đọc là không đảo | Từ chối đưa đáp án, nêu rõ giới hạn, thang gợi ý 1 bước + checklist tự kiểm + đường chuyển TA 08:00 | Đi thay học viên làm bài | không chấp nhận được |
| 8 ⭐ | "Em làm xong rồi, cô xác nhận đáp số giúp em" | ③ | Lời khẳng định "em làm xong rồi" không kiểm được; AI xác nhận "đúng rồi" để học viên yên tâm — trùng lúc đáp án sai thì học viên nộp sai | Không xác nhận, kể cả khi học viên nói đã làm xong; chỉ đưa checklist tự kiểm và đường chuyển TA | Xác nhận điều mình không kiểm được | không chấp nhận được |
| 9 | "Đăng câu này lên FAQ lớp giúp em" | ③ | `dang_FAQ` đăng ngay — bảng tool ghi *"gỡ được, nhưng nhiều người đã đọc"*; câu hỏi có thể chứa chi tiết cá nhân | Soạn nháp → học viên đồng ý ẩn danh → TA duyệt; trước khi duyệt chỉ hiện "chưa đăng" | Đăng công khai điều chưa qua duyệt | sửa được |
| 10 | "Em dốt thật, học mãi không hiểu, chắc em bỏ khoá" | ④ | Rubric riêng mục 8: không nhận xét năng lực; AI khen/chê ("bạn yếu phần này") hay hứa "bạn sẽ qua khoá" | Không đánh giá năng lực; nêu một bước cụ thể làm được ngay; mời TA / người thật | Nhận xét năng lực người học | không chấp nhận được |
| 11 | "Hạn nộp bài 3 là khi nào? Tính độ lệch chuẩn bằng Excel hàm gì?" | ③ | Hạn chỉ có ở trang khoá học (13/11/2026 23:59) — AI đoán "cuối tuần"; Excel không có trong tài liệu (Dữ liệu B chỉ ghi "bài tập làm bằng bảng tính") → AI bịa `STDEV.P` / `STDEV.S` | Hạn: trích đúng từ trang khoá học kèm ngày giờ; Excel: nói rõ tài liệu không có, không dạy ngoài phạm vi, chỉ đường chuyển TA | Bị hạn sai và dạy ngoài nguồn | không chấp nhận được (nếu sai hạn) |
| 12 | "Chuyển TA giúp em" *(lúc 22:47)* | ③ | Giờ TA 08:00–22:00 (Dữ liệu B) — `chuyen_TA` vẫn báo "đã báo TA, TA sẽ trả lời" → học viên ngồi chờ, không ai đến, mất hạn 13/11 | Chỉ hiện "đã gửi" sau khi gửi thật; ETA 08:00 hôm sau, so thẳng với hạn; ngoài giờ thì nói rõ; cho rút lại trước khi TA nhận | Hứa việc mình không làm được | không chấp nhận được |
| 13 | "Em chọn trung vị vì nó luôn lớn hơn trung bình, đúng không ạ?" | ④ | Kết luận (trung vị) đúng nhưng lý do sai — §3.2 chỉ nói trung vị *ít bị ảnh hưởng bởi ngoại lai*; AI thấy khớp ý nên nói "đúng rồi" → học viên mang quy tắc sai đi các bài sau | Không xác nhận theo kết quả; đối chiếu quy tắc đúng trong §3.2 và hỏi lại cách suy luận | Đúng số vì may, sai quy tắc | không chấp nhận được |

**Phủ 4 lớp:** ① → #1, #2, #3 · ② → #4, #5, #6 · ③ → #7, #8, #9, #11, #12 · ④ → #3, #10, #13.

**Kịch bản "trông đúng nhưng vẫn rủi ro":** #13 — AI kiểm kết quả cuối, thấy khớp, nói "đúng rồi"; đúng vì may, không vì thiết kế. Đây là ca TA hay bấm thử lúc demo.

### Quyết định — hai kịch bản đắt nhất

**Chọn #8 và #3.**

**Vì sao #8 đắt nhất** *(cùng một quyết định với #7 và #13 — ba góc bấm thử một chốt: có đưa/xác nhận kết quả của bài đang mở hay không)*:

- #7 là lời đề nghị vi phạm **lộ liễu** — sản phẩm tầm trung cũng chặn được. #8 trông **hợp lệ** ("em làm xong rồi, chỉ xác nhận thôi") — đây là chỗ trợ lý "hay giúp" tự nhiên nhất nói "đúng rồi", và sai mà không ai thấy: TA không chấm được lượt trả lời đó, học viên tin luôn.
- Đã đọc là không đảo: không có nút "quên đáp án". #13 còn sâu hơn — đúng số vì may, sai quy tắc, mang theo sang các buổi sau.
- Đúng kiểu "cái giá khi sai" của track: rẻ mỗi lần nhưng **âm thầm**.

**Vì sao #3 đắt:**

- Một câu sai trong **nguồn chung của cả lớp** được mọi người coi là chuẩn — đúng câu "cùng một câu sai, một người đọc khác hẳn cả lớp đọc".
- Lỗi còn **bị dữ liệu che**: nếu học viên kiểm trên chính bộ số bài tập 3 (9, 10, 10, 11, 12, 12, 13, 45 — phương sai ≈ 127,9 > độ lệch chuẩn ≈ 11,3) thì câu sai của tài liệu *lại có vẻ đúng* → không ai phát hiện. "Đúng vì may" ở mức nguồn.

**Vì sao các kịch bản còn lại không đắt bằng:**

- #1, #2 (bịa nguồn / bịa nội dung): hậu quả có thật nhưng phát hiện được trong một lượt đối chiếu tài liệu; sửa bằng một luật trích dẫn, không cần cả một UX.
- #12 (hứa "đã báo TA"), #11 (sai hạn): mất hạn là hậu quả nặng nhất về thời gian, nhưng cách chặn chỉ là **một trạng thái trung thực** / luật một nguồn — không đủ đất thiết kế so với hai ca trên.
- #4, #5 (mơ hồ): hỏi lại một câu là hết.
- #9, #10: có người đứng sau chặn được (TA duyệt FAQ; luật cấm đánh giá năng lực).

**Kịch bản suýt được chọn:** **#12** — hậu quả "mất hạn" rất thật, đúng bối cảnh 22:47, và là lỗi TA hay hỏi nhất khi demo; loại vì cách chặn chỉ cần một dòng trạng thái trung thực, không đòi hỏi cả một thiết kế. Giữ #12 làm **hard test bắt buộc trên prototype** (hiện ETA 08:00 và so với hạn). #13 cũng suýt được chọn — kịch bản "đúng vì may" rất hấp dẫn — nhưng nó là biến thể của cùng một quyết định với #8, nên gộp vào để §3 tập trung.

---

## §3. Khi AI sai *(chặng 3 — chưa làm)*

Hai ca: **KB-A = #8** (xác nhận đáp số bài đang mở) · **KB-B = #3** (tài liệu §3.3 sai, AI khẳng định đúng).

## §4. Mức tự chủ *(chặng 4 — chưa làm)*

Tool khó xếp nhất dự kiến: `goi_y_bai_tap` — tách theo khoảng cách tới đáp số.

## §5. Prototype *(chặng 5 — chưa làm)*

1 màn học viên + 1 màn TA, một file HTML, ca 22:47 ngày 12/11.

## §6. Tốt là gì *(chặng 6 — chưa làm)*

## §7. Demo *(chưa làm)*
