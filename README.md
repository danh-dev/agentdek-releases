# AgentDek — Changelog

Bản phát hành cho Windows tại mục **Releases**. App tự kiểm tra bản mới; mỗi phiên bản dưới đây ghi những gì thay đổi với người dùng.

## 0.2.1 — 2026-10-21
Giao diện làm lại toàn bộ theo design system AgentDek (Claude Design, phong cách desktop app như Jira / VS Code: khối rõ, nút to dễ bấm, bố cục rộng, Manrope 14px, Lucide). Không đổi dữ liệu trên đĩa — mở lên là dùng ngay.

**Khung ứng dụng**
- Thanh tiêu đề 32px riêng của app (menu Tệp · Xem · Trợ giúp, tên cửa sổ, nút thu/phóng/đóng của Windows); thanh trạng thái 24px dưới cùng (server, kết nối AI, run đang chạy, việc chờ bạn, phiên bản/cập nhật).
- Thanh trên 48px: chọn dự án (phạm vi làm việc hiện tại), ô **Tìm hoặc gõ lệnh (Ctrl+K)**, chuông việc chờ, nút **Giao việc (Ctrl+N)** dùng chung cho nhân sự lẫn workflow — form 2 cột, gợi ý theo loại việc, báo khi kết nối AI chưa sẵn sàng.
- Thanh bên 260px thu gọn được (Ctrl+B): Làm việc (Hộp thư · Dự án với tab con · Lịch sử) · Xây đội (Nhân sự · Workflows · Kiến thức chung) · Hệ thống (Kết nối AI · Cài đặt); đổi giao diện sáng/tối ở đáy.
- Dữ liệu dùng chung một bộ nhớ đệm, tự cập nhật theo luồng sự kiện; thông báo trong app (toast) song song với toast Windows.

**Các màn hình**
- **Hộp thư** — màn mặc định: *Chờ bạn* (câu hỏi, xin phép, review, duyệt, nhập liệu — kể cả từ run con), *Đang chạy*, *Cần chú ý* (run gián đoạn có nút Chạy tiếp, run lỗi 24h, đề xuất kiến thức chờ duyệt); lọc theo dự án.
- **Run** — màn theo dõi 3 cột: trái là timeline các bước (nhánh song song thụt vào, link run con, bấm để lọc), giữa là transcript (lượt của bạn / của nhân sự, mỗi lần gọi tool là một dòng gập được, sơ đồ workflow thu gọn được) hoặc chi tiết từng bước, phải là việc đã giao · artifacts · chi phí & thời gian · run con. Khi run chờ bạn, **khung trả lời** neo ngay trên ô nhắn tin (câu hỏi dạng nút chọn, xin phép hiện lệnh, form nhập liệu, duyệt/review có ô nhận xét). Nhắn tiếp cho nhân sự ngay dưới transcript (Ctrl+Enter).
- **Nhân sự** — danh sách bên trái (tìm theo tên / chức danh / loại việc), hồ sơ bên phải với tab Hồ sơ (form có thanh Lưu/Hoàn tác) · System prompt · Kỹ năng (danh sách + trình soạn, Ctrl+S) · Phiên bản · Lịch sử. **Tuyển nhân sự** là hộp thoại; **Giao việc** mở form chung đã chọn sẵn nhân sự.
- **Workflows** — canvas toàn khung với thanh công cụ 48px (menu **Thêm khối**, Sắp xếp, Vừa khung, Thuộc tính workflow); bấm khối → bảng thuộc tính 420px bên phải; tab YAML (Ctrl+S kiểm tra schema rồi lưu), Phiên bản (xem YAML / khôi phục), Lịch sử. Triggers (org/triggers.yaml) nằm cuối danh sách.
- **Dự án** — danh sách bên trái, tiêu đề dự án có đường dẫn workspace / kho dự án kèm nút Mở; tab Kanban (6 cột, kéo thả, hộp thoại task, lập kế hoạch từ yêu cầu) · Kết quả (chi phí tham khảo + bảng run) · Code map (đồ thị / map.md, quét lại) · Knowledge · Notes (đề xuất chờ duyệt) · Cài đặt (form có thanh Lưu, quyền workspace, di chuyển kho dự án). **Dự án mới** là hộp thoại với bộ chọn thư mục kiểu desktop.
- **Lịch sử giao việc** — gom theo ngày, chi phí tham khảo 30 ngày, dọn run cũ.
- **Kết nối AI** — danh sách bên trái + form bên phải (Thông tin · Kết nối với nút Kiểm tra · Model & giá · Nâng cao), bảng giá tham khảo là một mục trong danh sách.
- **Cài đặt** — kiểu VS Code: cây mục bên trái + ô tìm cài đặt; Chung · Thông báo · Chạy song song · Cập nhật · Sao lưu & chuyển máy · Dọn run cũ · Giới thiệu.
- **Kiến thức chung** — danh sách file + trình soạn có lịch sử phiên bản và đề xuất của nhân sự.
- **Form tạo/sửa mở dạng bảng trượt bên phải** (full chiều cao, 640–960px tuỳ form): Giao việc, Tuyển nhân sự, Dự án mới, Thêm kết nối, Task Kanban, Lập kế hoạch, Đề xuất kiến thức. Đóng khi đang nhập dở sẽ hỏi trước. Hộp thoại nhỏ giữa màn chỉ còn cho xác nhận, nhập một dòng và chọn thư mục.

## 0.2.0 — 2026-10-21
Giai đoạn 1 của giao diện mới — khung ứng dụng (thanh tiêu đề, thanh trên, thanh bên, thanh trạng thái, Hộp thư, nút Giao việc chung, Ctrl+K). Các trang còn lại được làm lại trọn vẹn ở 0.2.1.

## 0.1.18 — 2026-10-21
- **Khối Song song** trong workflow: nhiều nhánh (nhân sự hoặc workflow) chạy cùng lúc, mỗi nhánh là run con riêng. Kết thúc khi *tất cả* / *nhánh đầu tiên* / *đủ N nhánh* xong (nhánh còn lại được huỷ); nhánh lỗi thì dừng ngay hoặc để nhánh khác chạy tiếp; giới hạn số nhánh cùng lúc; workspace chung (mỗi nhánh được dặn phạm vi) hoặc git worktree riêng.
- **Khối Fan-out** (map): tự tạo nhánh theo danh sách — ví dụ từng task trong JSON của bước lập kế hoạch, hoặc mỗi dòng một mục — với cùng một nhánh mẫu (`{{item}}`, `{{index}}`).
- Kết quả gộp dùng tiếp như khối thường: `outputs.<khối>.branches.<nhánh>.summary`, file của mọi nhánh vào `inputs/<khối>/<nhánh>/`; review/duyệt sau khối song song xem toàn bộ.
- Canvas: khối song song hiện từng nhánh với trạng thái riêng (đang chạy / xong / lỗi / huỷ); trang run liệt kê nhánh thụt vào dưới khối, mỗi nhánh có link run con. Gián đoạn giữa chừng: nhánh đã xong được giữ, Chạy tiếp chỉ làm lại nhánh dở; nhiều nhánh cùng chờ bạn thì run cha báo "+n nhánh khác".
- Workflow mẫu `parallel-feature` (thiết kế + backend song song → reviewer → duyệt).

## 0.1.17 — 2026-10-21
- **Sao lưu & chuyển máy** (Cài đặt): xuất một file zip gồm tổ chức (nhân sự kèm lịch sử phiên bản, workflow, kiến thức chung, bảng giá, nhà cung cấp) + mọi kho dự án (kể cả kho đặt ngoài AgentDek) + cài đặt app; tuỳ chọn kèm lịch sử run; hoặc chỉ xuất tổ chức để chia sẻ bộ nhân sự. API key không bao giờ nằm trong bản sao lưu.
- Nhập: chọn file zip (hoặc gõ đường dẫn) → xem trước nội dung và mục trùng tên → **Gộp** (tick từng mục muốn ghi đè, phần còn lại giữ bản hiện có) hoặc **Thay toàn bộ**. Trước khi nhập, app tự sao lưu dữ liệu hiện tại vào `data/backups`. Không nhập khi còn run đang chạy.
- Bản sao lưu tạo trên máy hiện ở danh sách trong Cài đặt: tải về (hộp thoại Lưu của Windows), nhập lại, xoá. Trong app desktop, tải xong tự mở Explorer đến file.

## 0.1.16 — 2026-10-21
- Sửa lỗi app sập ngay khi mở ("The argument 'filename' must be a file URL…"): module đồ thị code resolve grammar tree-sitter lúc khởi động theo cách chỉ chạy được trong ESM; giờ resolve khi cần và tương thích bundle của Electron.

## 0.1.15 — 2026-10-21
- **Code map v2 — đồ thị code thật** (tree-sitter, chạy local): file, class, function, method và các cạnh import / gọi hàm / kế thừa, có số dòng và độ tin cậy. Quét ICard (131 file) dưới 3 giây, quét lại chỉ parse file đã đổi.
- Tab Code map có canvas tương tác: mức **file** (màu theo cụm, cạnh gộp số lời gọi) và mức **symbol** (lân cận N cấp của node đã chọn); tìm symbol/file, lọc thư mục, ẩn test; panel bên phải hiện ai gọi / gọi ai / thành viên; nút **Ảnh hưởng** tô những gì phụ thuộc vào node (đỏ → vàng theo khoảng cách).
- `map.md` có thêm mục Hub (symbol được dùng nhiều nhất) và Cụm; `graph.json` tương thích định dạng graphify.
- Nhân sự có tool `code_graph` (search / explain / path / impact / file) để hỏi "symbol này được ai dùng", "sửa file này ảnh hưởng đâu" trước khi sửa code; brief nhắc dùng, reviewer dùng `impact` để chấm phạm vi sửa.
- Ignore mặc định tránh nhiễu (`*.d.ts` sinh tự động, dist, lockfile, test) + file `.agentdekignore` trong workspace.

## 0.1.14 — 2026-10-21
- Canvas workflow thiết kế lại: nút **Bắt đầu** riêng nối vào khối đầu (kéo sang khối khác để đổi điểm vào), nhãn **kết thúc** ở khối cuối; khối có dải màu theo loại, nhân sự hiện avatar; cổng ra có nhãn `pass/fail`, `then/else`, `approve/reject` ngay cạnh cổng.
- Cạnh có mũi tên, màu theo ý nghĩa (xanh/đỏ/xám); **vòng sửa lại** vẽ thành cung riêng phía dưới, không còn đè lên cạnh tiến; rê chuột lên cạnh để xoá bằng nút ×; khi kéo nối, cổng hợp lệ sáng lên.
- Theo dõi run ngay trên canvas: khối đang chạy nhấp nháy xanh, khối chờ bạn viền vàng, cạnh đang đi "chảy" theo mũi tên, cạnh đã qua có dấu ✓, khối đã xong mờ nhẹ, hiện "vòng 2"; nút **Theo dõi** tự cuộn tới khối đang hoạt động.
- Nút **Sắp xếp** tự động (phím A), **Vừa khung** (phím F), lưới bắt dính 20px, chú giải màu; xoá khối bằng phím Delete (tự gỡ mọi liên kết); hỗ trợ giao diện sáng.

## 0.1.13 — 2026-10-21
- Editor workflow: khối mới đặt cạnh khối đang chọn và tự cuộn tới; Hoàn tác (Ctrl+Z) cho mọi thao tác trên canvas/panel; xoá hay khôi phục khối thì canvas tự vừa khung.
- Workflow có lịch sử phiên bản: mỗi lần Lưu giữ bản trước, nút Lịch sử để xem YAML cũ hoặc khôi phục.
- Changelog của dự án (file này) được đẩy lên repo phát hành và dùng làm ghi chú release.

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
