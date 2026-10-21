# AgentDek — Changelog

Bản phát hành cho Windows tại mục **Releases**. App tự kiểm tra bản mới; mỗi phiên bản dưới đây ghi những gì thay đổi với người dùng.

## 0.1.12 — 2026-10-21
- Chạy song song có kiểm soát: giới hạn số run nhân sự đồng thời (Cài đặt → Chạy song song, mặc định 3); vượt thì xếp hàng.
- Khoá workspace: hai run sửa trực tiếp cùng một thư mục không chạy cùng lúc — run sau chờ run trước, trang run hiện đang chờ ai.
- Kế hoạch mới mặc định chạy 2 task song song (task khác workspace).
- Cài đặt: sửa bố cục ô tick thông báo; mục Cập nhật chỉ còn trạng thái và nút tải/cài, không còn ô nhập nguồn phát hành.
- Phát hành: `pnpm desktop:release` đọc token từ `.env`, tự đẩy changelog lên repo phát hành.

## 0.1.11 — 2026-10-21
- Tự cập nhật qua GitHub Releases: app kiểm tra 30 giây sau khi mở và mỗi 6 giờ, chỉ tải khi bạn bấm, tải xong có thông báo "Cài & khởi động lại". Menu khay có "Kiểm tra cập nhật".

## 0.1.10 — 2026-10-21
- Di chuyển kho dự án sang thư mục khác (hoặc về lại trong AgentDek) ngay trong Cài đặt dự án; sao chép → kiểm tra → xoá bản cũ.
- Tự dọn run cũ hơn N ngày (Cài đặt), hiện dung lượng thư mục run.

## 0.1.9 — 2026-10-21
- Thông báo Windows khi có việc chờ bạn, run xong, run lỗi, hoặc phát hiện run gián đoạn; bấm vào mở đúng run.
- Chấm đỏ trên icon taskbar + tooltip khay "n việc chờ bạn"; badge số việc chờ ở menu Lịch sử giao việc.
- Trang Cài đặt mới: bật/tắt từng loại thông báo.

## 0.1.8 — 2026-10-21
- Chi phí tham khảo ≈USD cho mọi run (kể cả gói thuê bao/OAuth và model local), tính cả token cache.
- Bảng giá `org/pricing.yaml` sửa được trong app (Kết nối AI → Bảng giá tham khảo).
- Thẻ Chi phí: hôm nay / 7 ngày / 30 ngày / tổng, theo nhân sự và theo dự án — ở tab Kết quả của dự án và Lịch sử giao việc.
- Ngân sách tham khảo theo dự án: chạm ngưỡng thì không giao việc mới.

## 0.1.7 — 2026-10-20
- Run bị gián đoạn khi app tắt được đánh dấu rõ; nút **Chạy tiếp**: workflow tiếp tục từ bước đang dở (bước đã xong giữ nguyên), nhân sự mở lại phiên và làm nốt.
- Task Kanban đang làm lúc tắt app trở về To do kèm ghi chú.

## 0.1.6 — 2026-10-20
- Tách bạch **Workspace** (thư mục làm việc) và **Kho dự án** (dữ liệu AgentDek của dự án); kho dự án đặt được ở thư mục bạn chọn khi tạo dự án.
- Thư mục run gom theo ngày và dự án (`runs/<ngày>/<dự án>`); Lịch sử giao việc gom theo ngày, có xoá từng run và "Dọn run cũ".
- Nút mở thư mục trong Explorer ở trang dự án, trang run, Kiến thức chung.

## 0.1.5 — 2026-10-20
- Nhân sự có thể **đề xuất** cập nhật kiến thức chung hoặc ghi chú dự án; bạn xem diff, sửa tay nếu cần rồi áp dụng hoặc bỏ. Không có gì được ghi khi chưa duyệt.

## 0.1.4 — 2026-10-20
- **Kiến thức chung** (`org/knowledge`): quy tắc áp dụng cho mọi dự án, mọi nhân sự — chép vào mọi run, không phải lặp lại trong từng dự án.
- Guard an toàn cứng trong app: chặn mọi lệnh giết process theo tên (`taskkill /IM node.exe`, `pkill node`, …) ở mọi chế độ quyền; nhân sự nhận hướng dẫn kill đúng PID và làm tiếp.

## 0.1.3 — 2026-10-20
- Sửa lỗi so khớp quyền ghi (`**` chỉ khớp một cấp thư mục) khiến nhân sự bị từ chối ghi file trong workspace.

## 0.1.2 — 2026-10-20
- Hộp thoại trong app thay cho `window.prompt` (Electron không hỗ trợ) — nút Publish nhân sự, đặt tên file… hoạt động lại.
- Sửa thanh cuộn thừa ở thanh tab, hộp thoại chọn thư mục gắn đúng cửa sổ, thứ tự transcript.

## 0.1.1 — 2026-10-20
- Sửa lỗi Claude Code không khởi chạy được từ bên trong `app.asar` (tách binary ra ngoài asar).

## 0.1.0 — 2026-10-19
- Bản desktop đầu tiên (Windows): nhân sự AI có phiên bản, workflow với review và duyệt, lập kế hoạch Kanban theo dự án, kết nối nhiều nhà cung cấp AI, hỏi–đáp và cấp phép giữa chừng, nhắn tiếp sau khi xong.
