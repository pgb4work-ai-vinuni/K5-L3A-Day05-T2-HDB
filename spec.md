## §3. Khi AI sai

Mốc thời gian chung: **22:30 ngày 12/11/2026**, ngoài giờ trực TA (08:00–22:00). Bài tập 3 hết hạn **23:59 ngày 13/11/2026**.

| Mã | Tin nhắn học viên |
|---|---|
| **S04 ★** | "Em tính trung vị của 9, 10, 10, 11, 12, 12, 13, 45 ra 11,5 đúng không ạ?" *(không nhắc tới bài 3; dãy trùng §3.5)* |
| **S06 ★** | "Em tính phương sai ra 0,25 mà độ lệch chuẩn lại ra 0,5, lớn hơn. §3.3 bảo luôn nhỏ hơn mà, em sai chỗ nào ạ? Chắc em dốt toán thật." |

---

### S04: Xin xác nhận đáp số bài đang mở, không nhắc tới bài 3

#### 1. Khi không chắc: hỏi lại, trả lời kèm giới hạn hay chuyển người?

AI không chắc đây có phải bài 3 hay không.
- **Hỏi lại "Đây có phải bài 3 không?": loại.** Học viên chỉ cần trả lời "không" là mở được đáp án, và câu hỏi còn ngầm nghi họ gian lận.
- **Dừng và chuyển TA: loại.** Lúc 22:30 không có TA, học viên phải chờ cả đêm trong khi vẫn có thể tự kiểm ngay.
- **Trả lời kèm giới hạn: chọn.** Dãy trùng §3.5 là đủ căn cứ để coi đây là bài đang mở. AI không nói đúng hay sai, mà làm mẫu trên một dãy khác.

Ngưỡng nhận diện: dãy trùng, hoặc gần trùng (cùng 8 giá trị, khác tối đa 2), đều đi nhánh bài đang mở. Lý do: đổi 45 thành 46 thì trung vị vẫn là đáp số bài 3.

#### 2. AI nói gì (nguyên văn)? Có hứa điều không làm được không?

> Dãy bạn gửi trùng với dãy lương ở Bài tập 3 (§3.5). Bài này đang mở đến 23:59 ngày 13/11, nên mình không nói được con số đó đúng hay sai, kể cả khi bạn đã tự tính xong.
>
> Bạn tự kiểm bằng ví dụ khác nhé: dãy 3, 5, 7, 20 có 4 giá trị, là số chẵn, nên theo §3.2 trung vị là (5 + 7) / 2 = 6. So cách làm này với cách của bạn.
>
> Mai TA trực từ 08:00, vẫn trước hạn nộp. Mình có thể soạn sẵn câu hỏi để bạn xem trước khi gửi.

Câu này không hứa giờ TA trả lời, không nói đã báo TA, và không nhận xét cách làm trên dữ liệu bài 3 (nói "lấy (11 + 12) / 2 là đúng" cũng là đưa đáp số).

#### 3. Người dùng thấy gì?

- Nhãn **Bài đang mở · hạn 13/11 23:59 (trang khoá học)**.
- Thẻ **"Vì sao mình không xác nhận: dãy khớp §3.5"**.
- Thẻ nguồn **§3.2**.
- Khối ví dụ có nhãn **"Ví dụ khác, không phải bài 3"**.
- Nút: **Gửi dãy khác để luyện** · **Soạn câu hỏi cho TA** · **Báo câu trả lời sai**.
- **Không có** nút kiểm tra đáp số hay "vẫn xác nhận". Không hiện phần trăm tin cậy, vì không có dữ liệu hiệu chuẩn.

#### 4. Làm gì tiếp? Nếu không làm gì?

Học viên tự đối chiếu với ví dụ, gửi dãy khác để luyện, hoặc soạn câu hỏi cho TA (xem trước rồi mới gửi). Nếu không làm gì thì không có gì được gửi đi, con số cũng không được lưu.

#### 5. Ai được báo, sau bao lâu?

- **Không ai được báo tự động.** Đã loại phương án báo TA mỗi lần học viên xin xác nhận, vì biến trợ lý thành công cụ giám sát và học viên sẽ ngại hỏi.
- **Nếu học viên gửi:** yêu cầu vào hàng chờ ngay, TA thấy từ 08:00 ngày 13/11, còn khoảng 16 tiếng trước hạn. TA thấy câu hỏi, nhãn "Bài đang mở · xin xác nhận đáp số", và thẻ nguồn.
- **Nếu AI đã lỡ xác nhận:** ghi một sự cố cho TA xem vào ca sáng.

#### 6. Loại lỗi, cách nói và cách sửa

**Lỗi ngữ cảnh:** nói "đúng rồi" thì đúng về toán học nhưng sai tình huống, vì đây là bài đang chấm.
- **Cách nói:** không xin lỗi vì từ chối; nêu lý do cụ thể.
- **Cách sửa:** sửa thiết kế (xem câu 7).
- **Nếu AI đã lỡ xác nhận** thì thành lỗi hệ thống, và sản phẩm nhận lỗi: "Mình vừa xác nhận một con số của bài đang mở, việc này mình không được làm. Lỗi ở trợ lý, không phải ở bạn."

#### 7. Lỗi sửa câu chữ không cứu được

Câu "đúng rồi" đi qua chat thường, không gọi tool nào, nên hàng rào đặt ở `goi_y_bai_tap` không chặn được. Viết câu hệ thống kỹ đến đâu, AI cũng không biết dãy số này là bài 3.

**Thiết kế cứu:** luật L1 (§4) so đầu vào với bài đang mở **trước khi** AI trả lời, cộng với giao diện không có nút vượt rào.

---

### S06: Học viên đúng, tài liệu sai

#### 1. Khi không chắc: hỏi lại, trả lời kèm giới hạn hay chuyển người?

AI không chắc tài liệu hay học viên đúng, nhưng phép tính kiểm được ngay: căn bậc hai của 0,25 là 0,5.
- **Hỏi lại "Bạn tính phương sai thế nào?": loại.** Không đổi được kết luận, và ngầm nói học viên sai trong khi họ vừa tự chê mình.
- **Dừng và chuyển TA: loại.** Học viên sẽ đi ngủ với ý nghĩ mình sai, trong khi điều cần nói đã kiểm được ngay.
- **Trả lời kèm giới hạn và tự báo lỗi tài liệu: chọn.** AI nói §3.3 "cần xem lại" chứ không nói "sai" (gắn cờ nhầm một câu đúng cũng có giá), đưa phản ví dụ để học viên tự kiểm, và gọi `bao_loi_tai_lieu`.

#### 2. AI nói gì (nguyên văn)? Có hứa điều không làm được không?

> Nếu phương sai là 0,25 thì độ lệch chuẩn 0,5 là đúng. Chỗ này dễ gây rối, không phải do bạn.
>
> Câu ở §3.3 nói độ lệch chuẩn "luôn nhỏ hơn" phương sai cần được xem lại: câu đó chỉ đúng khi phương sai lớn hơn 1 (phương sai 4 thì độ lệch chuẩn là 2). Bạn bấm máy tính căn của 0,25 và căn của 4 là thấy.
>
> Mình đã gửi báo lỗi §3.3 cho TA (mã BL-031), không kèm tin nhắn của bạn. Sớm nhất sáng mai TA mới xem; sửa tài liệu hay không do giảng viên quyết định. Bạn cũng có thể nhắc giảng viên ở buổi tới.

Câu này không hứa tài liệu sẽ được sửa, không hứa giờ TA xử lý, và không nhận xét năng lực. Câu "đã gửi… BL-031" chỉ hiện khi bản ghi đã được tạo; nếu gửi lỗi thì đổi thành "Mình chưa gửi được báo lỗi, bạn bấm Thử lại."

#### 3. Người dùng thấy gì?

- Thẻ nguồn **§3.3** trích nguyên văn, gắn nhãn **Cần xem lại**.
- Khối **"Kiểm tra của trợ lý · chưa được giảng viên xác nhận"** chứa phản ví dụ.
- Dòng trạng thái **"Đã gửi báo lỗi · BL-031 · chờ ca TA 08:00"**.
- Nút: **Xem §3.3** · **Soạn câu hỏi cho TA** · **Báo câu trả lời sai**.

#### 4. Làm gì tiếp? Nếu không làm gì?

Học viên tự kiểm bằng máy tính rồi học tiếp, hoặc soạn câu hỏi cho TA (có bước xác nhận). Nếu thấy AI kiểm nhầm thì bấm **Báo câu trả lời sai**; phản hồi được gắn vào mục BL-031. Nếu không làm gì, báo lỗi **vẫn đã nằm trong hàng chờ TA**, nên lỗi tài liệu không còn âm thầm.

#### 5. Ai được báo, sau bao lâu?

- **TA:** báo lỗi tạo lúc 22:30, TA xem từ 08:00 ngày 13/11. TA thấy câu §3.3, lý do, phản ví dụ và số học viên đã vấp cùng chỗ; không thấy tin nhắn gốc của học viên.
- **Giảng viên:** được TA chuyển tiếp, ngoài phạm vi trợ lý.
- **Cả lớp:** chỉ biết khi TA duyệt đăng một lưu ý FAQ.

#### 6. Loại lỗi, cách nói và cách sửa

**Lỗi hệ thống:** nội dung nguồn sai, học viên không có lỗi.
- **Cách nói:** nói rõ chỗ rối đến từ tài liệu, không bảo học viên "đọc kỹ lại".
- **Cách sửa:** sửa ở nguồn (xem câu 7).

#### 7. Lỗi sửa câu chữ không cứu được

- **AI tin nguồn sai vì có mã mục thật.** Câu nhắc "cẩn thận với tài liệu" không chỉ ra được câu nào sai, và §3.3 vẫn sai với người học khác. **Thiết kế cứu:** luật L2 và tool `bao_loi_tai_lieu` tự làm, nên lỗi đi tới TA kể cả khi học viên không bấm gì.
- **Nói "đã gửi" khi chưa có bản ghi.** **Thiết kế cứu:** luật L3, câu trạng thái chỉ sinh từ bản ghi thật.

---

### Lỗi người dùng (để đủ ba loại)

Ca **S03**: "Giải thích công thức trên slide 12 đi." Tài liệu không có slide đánh số. AI không đổ lỗi và không cần xin lỗi, chỉ hỏi lại một câu:

> Tài liệu buổi 3 không có slide đánh số, chỉ có các mục §3.1–§3.5. Bạn đang xem đoạn nói về gì, mình tìm đúng mục.

Không cần chuyển người.

### Bốn đường trải nghiệm

| Đường | Ca | AI làm gì |
|---|---|---|
| Suôn sẻ | S01 | Giải thích kèm thẻ nguồn §3.1, §3.2 |
| Không chắc | S02 · S04 | S02: hỏi lại một câu. S04: dùng ngưỡng nhận diện |
| Không căn cứ / nguồn sai | S03 · S06 | S03: nói không có slide 12. S06: gắn cờ §3.3 và báo lỗi |
| Học viên sửa AI | Nút **Báo câu trả lời sai** | Mở ô "sai chỗ nào?"; trả lời lại hoặc gắn phản hồi vào hàng chờ |

### Nguyên tắc HAX và vị trí trên prototype

| Nguyên tắc | Ở đâu | Vị trí |
|---|---|---|
| **G11 · Giải thích vì sao** | Thẻ nguồn §3.3 tách khỏi khối "Kiểm tra của trợ lý" (S06); thẻ "Vì sao mình không xác nhận" (S04) | Ảnh 01, dấu 1 |
| **G10 · Thu hẹp khi nghi ngờ** | Nhãn **Cần xem lại** (S06); không xác nhận, chuyển sang ví dụ khác (S04) | Ảnh 01, dấu 2 |
| **G15 · Mời phản hồi chi tiết** | Nút **Báo câu trả lời sai** mở ô "sai chỗ nào?" | Ảnh 01, dấu 3 |

Dấu 4–6 thể hiện mức tự chủ, không tính là nguyên tắc HAX.

---

## §4. Mức tự chủ

Bộ tool sau khi tách (vì sao tách: mục "Tool tách và luật thêm"): `tra_cuu_tai_lieu`, `goi_y_buoc_dau`, `giai_thich_bai_da_dong`, phần cấm "đưa hoặc xác nhận đáp số bài đang mở", `bao_loi_tai_lieu`, `soan_yeu_cau_TA` → `chuyen_TA`, và `soan_FAQ` → `dang_FAQ`. AI không gia hạn, sửa điểm, nộp bài hay sửa tài liệu được.

### Câu 1. Nếu AI làm sai, ai chịu gì? Đảo lại được không, mất bao lâu, ai làm?

| Tool | Sai thế nào → ai chịu gì | Đảo được? | Mất bao lâu, ai làm |
|---|---|---|---|
| `tra_cuu_tai_lieu` | Trích nhầm mục hoặc câu sai → học viên hiểu sai | Được (chỉ đọc) | Vài giây, học viên tự thấy qua thẻ nguồn; nếu không thì tới khi TA phát hiện |
| `goi_y_buoc_dau` | Gợi ý quá tay → học viên chép, cả lớp mất công bằng | Không | Không ai đảo được; chỉ ghi sự cố cho TA |
| `giai_thich_bai_da_dong` | Áp nhầm cho bài đang mở → lộ đáp án | Không | Phòng trước: trạng thái bài lấy từ trang khoá học |
| Xác nhận đáp số bài đang mở | Chính hành động là cái sai → học viên, cả lớp | Không | Không ai |
| `bao_loi_tai_lieu` | Báo nhầm câu đúng → TA mất vài phút | Được | Vài phút, TA đóng mục trong ca 08:00 |
| `chuyen_TA` | Gửi nội dung học viên chưa muốn chia sẻ → học viên; hàng chờ nhiễu → TA | Được, trước khi TA nhận | Ngay lập tức, học viên bấm **Rút yêu cầu** |
| `dang_FAQ` | Đăng nội dung sai hoặc bài đang mở → cả lớp | Gỡ được, nhưng người đã đọc thì không | TA gỡ trong vài phút; đính chính có thể tới buổi sau |

### Câu 2. Nếu bắt chờ người duyệt thì mất gì? Chờ có phải cũng là một kiểu sai?

Lúc 22:30, chờ người nghĩa là chờ hơn 9 tiếng.

| Tool | Chờ thì mất gì | Chờ là kiểu sai? |
|---|---|---|
| `tra_cuu_tai_lieu` · `goi_y_buoc_dau` | Kẹt cả đêm, kể cả câu đơn giản như S01 | **Có** |
| `giai_thich_bai_da_dong` | S11 chờ cả đêm cho đáp án đã công khai | **Có** |
| `bao_loi_tai_lieu` | Chờ học viên bấm thì nhiều người không bấm, lỗi §3.3 âm thầm | **Có, đắt nhất** |
| `chuyen_TA` (học viên duyệt) | Chỉ một cú bấm | Không |
| `dang_FAQ` (TA duyệt) | FAQ đến chậm; từng học viên đã có câu trả lời riêng | Không |

Kết luận: chờ chỉ đáng khi hành động đưa nội dung ra khỏi cuộc trò chuyện.

### Câu 3. Tool khó xếp nhất

**`goi_y_bai_tap`** (trước khi tách): ba người chọn ba mức khác nhau.

| Ai | Chọn | Cái giá (trỏ về §2) |
|---|---|---|
| Thành viên 1 | Cần TA duyệt mọi gợi ý | S01, S11 chờ tới 08:00 cho câu không rủi ro |
| Thành viên 2 | Tự làm mọi mức, sau khi học viên đồng ý | S04, S05 không bị chặn: người đồng ý chính là người muốn đáp án |
| Thành viên 3 | Tách: bước đầu tự làm, đáp số cấm | Dãy 8 số quá nhỏ, nên bước đầu trên chính dãy đó gần như là đáp số |

**Cách chốt:** lộ đáp án thì không đảo được; chờ thì đắt nhưng sáng hôm sau vẫn còn khoảng 16 tiếng. Vì vậy loại phương án 2 trước. Nhóm chọn phương án 3, sửa đúng chỗ rủi ro: "bước đầu" không được dùng số liệu bài đang mở, chỉ trỏ định nghĩa và làm mẫu trên dãy khác. Thêm luật L1 cho trường hợp không đi qua tool.

### Câu 4. Mức tự chủ đã đổi lời hứa nào?

- **`chuyen_TA` cần học viên duyệt.** Lời hứa đổi từ "Khi trợ lý không chắc, TA sẽ được báo" thành **"Lỗi trong tài liệu luôn đến tay TA. Câu hỏi riêng của bạn chỉ đến khi bạn gửi."** `bao_loi_tai_lieu` bù lại phần giảng viên cần.
- **Cấm xác nhận đáp số.** Lời hứa mới, nói rõ từ đầu (G1): **"Trợ lý không bao giờ nói bài đang mở đúng hay sai, kể cả khi bạn đã làm đúng."**

### Mức chốt và phương án đã loại

| Tool | Mức | Lý do (Câu 1–2) | Đã loại và vì sao |
|---|---|---|---|
| `tra_cuu_tai_lieu` | Tự làm | Chỉ đọc; chờ mất cả đêm | Cần duyệt: chặn việc học vì một tác vụ đọc |
| `goi_y_buoc_dau` | Tự làm, trong giới hạn nội dung | Không đảo được nên giới hạn ở nội dung | Xem Câu 3 |
| `giai_thich_bai_da_dong` | Tự làm | Đáp án đã công khai | Gộp luật với bài đang mở: S11 chờ vô ích |
| Xác nhận đáp số bài đang mở | **Cấm** | Không đảo được; bước xác nhận vô hiệu | Cần học viên xác nhận: vô hiệu · cần TA duyệt: trợ lý không cần quyền này |
| `bao_loi_tai_lieu` | Tự làm | Rẻ, đảo được; chờ thì lỗi âm thầm | Học viên duyệt: lỗi âm thầm · TA duyệt: TA là người nhận |
| `chuyen_TA` | **Cần học viên duyệt** | Gửi nhầm thì lộ nội dung riêng; chờ chỉ một cú bấm | Tự gửi khi không chắc: chia sẻ ngoài ý muốn · cấm ngoài giờ: TA sáng mai vẫn cần nhận |
| `dang_FAQ` | **Cần TA duyệt**; bài đang mở: **cấm** | Sai thì cả lớp học sai | Tự đăng khi học viên đồng ý: người hỏi không đại diện cả lớp · cấm mọi FAQ: mất kênh báo về §3.3 |

### Ai duyệt, thấy gì, không ai duyệt kịp thì sao

- **`chuyen_TA` (học viên duyệt):** thấy câu sẽ gửi, thẻ nguồn, trạng thái bài, giờ trực TA, và lựa chọn kèm con số hay không. Không bấm thì bản xem trước **không bao giờ tự gửi**.
- **`dang_FAQ` (TA duyệt):** thấy bản nháp, nguồn, cờ "cần xem lại", trạng thái bài. Chưa tích "Đã đối chiếu nguồn" thì nút **Duyệt và đăng** bị khoá; nút này tách riêng khỏi **Nhận xử lý**. Không ai duyệt thì bản nháp chờ, **không tự đăng**.

### Tool tách và luật thêm

Cách xếp: mỗi người tự xếp mức trong 5 phút, không bàn, rồi cả nhóm so và chốt.

| Thay đổi | Vì sao | Chặn kịch bản |
|---|---|---|
| Tách `goi_y_bai_tap` thành ba phần | Một tool không thể vừa tự làm vừa cấm | S04, S05; S11 không phải chờ |
| Tách `soan_yeu_cau_TA` khỏi `chuyen_TA` | Soạn thì vô hại, gửi mới chia sẻ nội dung | S12 |
| Tách `soan_FAQ` khỏi `dang_FAQ` | Đăng mới ảnh hưởng cả lớp | S06, S07 |
| Thêm `bao_loi_tai_lieu` | Báo lỗi không chứa nội dung riêng của học viên | S06 |
| **L1** · So đầu vào với bài đang mở trước khi trả lời | Chặn xác nhận qua chat thường | S04, S05 |
| **L2** · Phép toán mâu thuẫn tài liệu thì không mặc định tài liệu đúng | Chặn lặp lại nguồn sai | S06 |
| **L3** · Câu trạng thái chỉ sinh từ bản ghi thật | Chặn hứa sai | S06, S12 |
| **L4** · Bài đang mở không vào FAQ, kể cả với TA | Chặn lộ đáp án ra cả lớp | S07 |

### Thử mức trên ba kịch bản

| Ca | Cái sai có bị chặn? | Còn làm khi lẽ ra phải hỏi? | Người bình thường phải chờ vô ích? |
|---|---|---|---|
| **S04** | Có (L1). Còn hở: đổi quá 2 giá trị thì L1 không bắt được; nhóm chấp nhận vì khi đó là luyện trên dãy khác thật, ghi vào §6 | Không | Không, có ví dụ để tự kiểm ngay |
| **S06** | Có (L2; FAQ cần TA duyệt) | Có một việc, cố ý: `bao_loi_tai_lieu` gửi không hỏi học viên (Câu 2) | Không, được trả lời ngay |
| **S01** | Không có gì cần chặn; có thẻ nguồn | Không | Không |
