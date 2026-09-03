# Day28_Track01_TeamMoi

## 1. Thành viên

| Họ tên | MSSV | Phần phụ trách | Góp ý đã đưa cho nhóm bạn |
|---|---|---|---|
| Hiển | 2A202601162 | Gartner-Lite (readiness) + AS-IS/TO-BE + kiến trúc tin cậy + setup repo/README | Phản biện với Vũ Nguyễn Bảo Sơn (case AI trong giáo dục): nội dung giáo dục cần chú trọng độ chính xác vì sai là dạy sai cho người học; cần làm rõ system prompt và nguồn tài liệu cho AI để tránh trả lời sai/lan man |
| Hồ Lương An | 2A202601332 | Mollick (phân chia người–AI) + ADKAR (người dùng) + Lộ trình 30-60-90 + Dashboard v2/Memo | Phản biện với Vũ Nguyễn Bảo Sơn (case AI trong giáo dục): nội dung giáo dục cần chú trọng độ chính xác vì sai là dạy sai cho người học; cần làm rõ system prompt và nguồn tài liệu cho AI để tránh trả lời sai/lan man |


## 2. Phạm vi

- Sản phẩm AI: ChatGPT dùng viết content marketing cho TUVNORD.
- Nhóm người dùng chính: Nhân viên marketing.
- Quy trình liên quan (1 workflow, 4 bước): tham khảo content đã viết trước đó → đọc brief/yêu cầu mới → viết content bằng AI → kiểm chứng trước khi dùng/xuất bản.
- Vấn đề quan sát được: đầu ra AI dài dòng, có phần thừa và làm tăng công sức biên tập lại.

## 3. Nguyên nhân gốc

- Nguyên nhân 1: ChatGPT chưa nắm được workflow, các tiêu chí hoàn thành chưa rõ (framework: Mollick + ADKAR Ability/Reinforcement + Gartner-Lite Vận hành; bằng chứng: quan sát trực tiếp cho thấy người viết phải tự xử lý đầu ra dài dòng sau khi AI viết).
- Nguyên nhân 2: Chưa có guardrail chất lượng bắt buộc, brief, độ dài mục tiêu, nguồn/phiên bản và checklist QA. Vậy nên AI không biết phần nào cần giữ hoặc loại bỏ (framework: ADKAR Desire/Knowledge + Gartner-Lite Readiness; bằng chứng: vấn đề được quan sát trực tiếp trong workflow là nội dung thừa, dẫn đến con người phải tốn thời gian để review lại).

**Gartner-Lite — tổ chức đã sẵn sàng chưa?**

| Trục | Nhận định | Kết quả |
|---|---|---|
| Direction | Mục tiêu rõ: dùng AI tăng tốc viết nháp content marketing, giảm thời gian tạo bản đầu; đối tượng và use case đã xác định. | ĐẠT |
| Dữ liệu / Readiness | Có kho content cũ để tham khảo, nhưng chưa có brief chuẩn hoá (không quy định độ dài mục tiêu, tone, cấu trúc); tài liệu tham khảo không có version/ngày cập nhật rõ. | THIẾU |
| Governance | Chưa có quy định bắt buộc về giới hạn độ dài hay checklist trước khi xuất bản; chưa rõ tiêu chí để từ chối một bản nháp quá dài. | THIẾU |
| Vận hành (owner) | Bước "kiểm chứng" cuối workflow tồn tại nhưng chung chung, không có ai chịu trách nhiệm cụ thể rà soát độ dài/nội dung thừa một cách hệ thống. | THIẾU |
| Hấp thụ (feedback loop) | Chưa có cơ chế ghi lại các lần AI viết dài để điều chỉnh prompt/brief về sau — lỗi lặp lại là sửa tay, không học được. | THIẾU |

Kết luận: Direction đạt, nhưng Readiness và Absorption đều thiếu → chưa nên mở rộng dùng AI cho toàn bộ content, cần pilot nhỏ để sửa readiness trước khi mở rộng — khớp và củng cố 2 nguyên nhân gốc ở trên.

**ADKAR — người dùng đang kẹt ở đâu?**

| Bước | Chẩn đoán | Trạng thái |
|---|---|---|
| Awareness | Người dùng thấy AI viết dài nhưng chưa có chuẩn chung để nhận diện đây là vấn đề workflow. | NGHẼN |
| Desire | Đầu ra dài làm giảm niềm tin và khiến người viết quay về cách chỉnh thủ công. | NGHẼN |
| Knowledge | Chưa có cách đưa brief, content tham chiếu và giới hạn độ dài vào prompt. | Cần làm |
| Ability | Chưa thực hành human handoff trong brief thật. | Cần làm |
| Reinforcement | Chưa có log lỗi, phản hồi và chỉ số gắn với quyết định. | Cần làm |

## 4. Cách làm mới

- Nguồn kiểm chứng: brief mới + kho content đã được duyệt (kèm link/phiên bản/ngày cập nhật).
- Người chịu trách nhiệm: AI chỉ tạo bản nháp, nhân viên marketing kiểm chứng, chủ quy trình content phê duyệt cuối và chịu trách nhiệm xuất bản, An theo dõi dashboard/feedback.
- Khi AI không chắc chắn hoặc thiếu nguồn: gắn cờ `[CẦN KIỂM CHỨNG]`, không xuất bản, chuyển người duyệt claim, ghi log lỗi để cập nhật prompt, checklist hoặc kho nguồn.
- Phân chia theo Mollick: người giữ quyền phê duyệt và ngoại lệ; AI hỗ trợ tham khảo, đọc brief, tạo và rút gọn nháp; chỉ tự động hóa kiểm tra định dạng/độ dài thấp rủi ro, không tự động xuất bản.
- System prompt: viết rõ vai trò, giới hạn độ dài, tone, cấu trúc và yêu cầu bám sát brief ngay trong system prompt — để ChatGPT hiểu đúng ý định thay vì đoán, giảm sai sót và nội dung thừa.

**Mollick — phân chia quyền hạn chi tiết**

| Vùng | Cách áp dụng cho content marketing |
|---|---|
| Người giữ quyền | Chọn góc nội dung, duyệt giọng thương hiệu/claim, xử lý ngoại lệ và chịu trách nhiệm bản cuối trước khi xuất bản. |
| AI hỗ trợ, người kiểm | Tham khảo content đã duyệt, bóc tách brief, tạo bản nháp, rút gọn và đề xuất biến thể; người marketing kiểm tra từng đầu ra theo brief và nguồn. |
| AI tự động có kiểm soát | Chỉ kiểm tra định dạng, độ dài và các mục checklist có tiêu chí rõ; không tự động duyệt claim hoặc xuất bản. |

**AS-IS / TO-BE**

| TRƯỚC (AS-IS) | SAU (TO-BE) |
|---|---|
| Đọc brief: không có chuẩn độ dài/tone, dễ hiểu khác nhau giữa các brief | Đọc brief theo prompt template: có giới hạn độ dài, tone, cấu trúc bắt buộc |
| Viết content bằng AI: AI không biết giới hạn nên viết dài, thừa | Viết content bằng AI: có checklist ràng buộc (độ dài, bám brief, có nguồn cho claim) |
| Kiểm chứng: chung chung, không rõ tiêu chí, người viết tự cắt gọt tay | Kiểm chứng theo checklist QA: có tiêu chí rõ (đạt/không đạt độ dài, bám brief, nguồn claim) |
| Không có bước xử lý khi content không đạt | Không đạt → gắn cờ, chuyển người duyệt xử lý, log lại để cập nhật prompt/brief |

**Kiến trúc tin cậy**

```
Nguồn → Trích nguồn → QA mẫu → Chuyển người → Phản hồi
```

| Bước | Áp dụng cho case content marketing |
|---|---|
| Nguồn | Kho content đã duyệt + brief mới, có link/phiên bản/ngày cập nhật rõ. |
| Trích nguồn | Mọi claim/ý chính trong bản nháp phải đối chiếu được với brief hoặc nguồn đã duyệt. |
| QA mẫu | Checklist QA kiểm tra độ dài, bám brief, có nguồn cho claim (checklist trong dashboard v2). |
| Chuyển người | Bản nháp không đạt checklist hoặc thiếu nguồn → gắn cờ `[CẦN KIỂM CHỨNG]`, không xuất bản, chuyển người duyệt. |
| Phản hồi | Ghi log lỗi (vì sao dài/thiếu nguồn) để cập nhật prompt template, brief hoặc checklist cho vòng sau. |

**Lộ trình 30-60-90 — ba cổng quyết định**

| Giai đoạn | Việc chính | Owner | Dấu hiệu hoàn thành / cổng quyết định |
|---|---|---|---|
| 0-30 ngày: chứng minh vấn đề | Vẽ AS-IS/TO-BE; chọn nhóm marketing pilot; chốt kho content đã duyệt; đo T0 trên 20 bài và 10 brief; ban hành prompt template + checklist. | Trưởng nhóm content (owner chính) — Hiển hỗ trợ nguồn/workflow, An hỗ trợ đo lường | Có baseline, data owner, nguồn có version và log được 4 bước. Chưa đủ thì sửa phạm vi/nguồn, chưa mở rộng. |
| 31-60 ngày: chứng minh chất lượng | Chạy pilot; QA mẫu 10 bài/tuần; log thời gian, vòng sửa, claim thiếu nguồn; review ADKAR hằng tuần và điều chỉnh prompt. | Chủ quy trình content + QA content | Tỷ lệ đạt QA lần đầu ≥80%, claim có nguồn ≥95%, sửa vì dài dòng/không bám brief ≤20% và không có claim chưa duyệt được xuất bản. Không đạt thì quay lại chỉnh workflow. |
| 61-90 ngày: quyết định mở rộng | So sánh với T0; chốt SOP, owner vận hành và quy tắc handoff; kiểm tra governance; đề xuất mở rộng theo loại content hoặc giữ pilot. | Trưởng nhóm marketing + An (dashboard/memo) | Chỉ mở rộng nếu mục tiêu chất lượng, thời gian và rủi ro đạt liên tiếp 2 tuần; nếu không, sửa tiếp hoặc dừng use case. |

## 5. Chỉ số

Xem chi tiết tại [`dashboard/dashboard_hanh_dong_v2.xlsx`](dashboard/dashboard_hanh_dong_v2.xlsx) (bản trước phản biện: [`v1/dashboard_hanh_dong_v1.xlsx`](v1/dashboard_hanh_dong_v1.xlsx)).

- Product metric: tỷ lệ bản nháp đạt checklist chất lượng ngay lần QA đầu, T0 đo 20 bài gần nhất, mục tiêu ≥80% ngày 60 và ≥85% ngày 90, nguồn bảng QA, owner An + QA content.
- Workflow metric: thời gian từ lúc brief được duyệt hợp lệ đến lúc bản nháp đầu tiên gửi QA — tính bằng giờ (timestamp brief duyệt trừ timestamp gửi QA), T0 đo 10 brief hiện tại, mục tiêu ≤70% baseline ngày 60, nguồn log timestamp brief/draft, owner chủ quy trình content.
- Chỉ số kiểm soát bổ sung: tỷ lệ claim/ý chính có nguồn kiểm chứng ≥95% và tỷ lệ phải sửa vì dài dòng/không bám brief ≤20% ngày 60, khi chỉ số xấu thì mổ lỗi mẫu, cập nhật prompt/checklist và giữ pilot.

## 6. Quyết định

**Sửa**: chưa mở rộng ngay. Trước hết chạy pilot 30 ngày với prompt template, checklist QA, nguồn có phiên bản và human handoff. So với v1, v2 (1) đổi từ nhãn chỉ số chung sang metric chất lượng product + thời gian/rework theo workflow, có T0/target/source/owner. (2) thêm ngưỡng và hành động khi chỉ số xấu, gồm chặn xuất bản và chuyển người.
Xem chi tiết tại [`memo/memo_quyet_dinh.md`](memo/memo_quyet_dinh.md).
