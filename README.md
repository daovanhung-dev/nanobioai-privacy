# nanobioai-privacy

Static-site chính sách công khai cho **NanoBio** (`com.nanobioai.app`), tối ưu để deploy bằng GitHub Pages và dùng trong Google Play Console.

## Các trang

- `index.html` — Trust Center / policy hub
- `privacy-policy.html` — Chính sách quyền riêng tư
- `data-safety.html` — Bản đồ dữ liệu hỗ trợ Google Play Data Safety
- `terms-of-service.html` — Điều khoản sử dụng
- `account-deletion.html` — Trang yêu cầu xóa tài khoản bên ngoài ứng dụng
- `health-ai-disclaimer.html` — Lưu ý sức khỏe & AI
- `cookie-policy.html` — Chính sách cookie của website

## Deploy GitHub Pages

1. Tạo repository public tên `nanobioai-privacy` dưới tài khoản `daovanhung-dev`.
2. Upload toàn bộ nội dung thư mục này vào **root** của branch `main`.
3. Vào `Settings → Pages`.
4. Chọn `Deploy from a branch` → branch `main` → folder `/(root)` → Save.
5. Chờ GitHub Pages publish.

URL dự kiến:

- Hub: `https://daovanhung-dev.github.io/nanobioai-privacy/`
- **Privacy Policy dùng cho Play Console:** `https://daovanhung-dev.github.io/nanobioai-privacy/privacy-policy.html`
- **Account deletion URL dùng cho Play Console:** `https://daovanhung-dev.github.io/nanobioai-privacy/account-deletion.html`
- Data Safety reference: `https://daovanhung-dev.github.io/nanobioai-privacy/data-safety.html`

## Thông tin đã đồng bộ với source NanoBioAI

- App name: NanoBio
- Android package/applicationId: `com.nanobioai.app`
- Permissions hiện có trong Android manifest: Internet/network, Camera, Record Audio, Foreground Service Microphone, Biometric/Fingerprint, Notifications, Boot Completed, Exact Alarm, Vibration.
- Auth/backend/cloud sync: Supabase.
- AI production path: Supabase Edge Function → Google Gemini.
- Food Scan: ảnh được gửi để phân tích AI; handler hiện tại xử lý ảnh inline.
- Sleep Safety audio capture: PCM xử lý trong RAM theo native implementation hiện tại.
- Sleep Safety contact/dispatch: Supabase + Twilio khi feature được cấu hình/kích hoạt.
- Purchases/subscriptions: Google Play Billing + server-side verification path.
- Account deletion backend: authenticated deletion flow; dọn user-owned schedule completion proof files trước khi xóa Supabase Auth identity.

## Việc cần làm trước mỗi lần phát hành

1. So sánh privacy policy với **AAB/commit thực tế** được đưa lên Play Console.
2. Kiểm tra merged Android Manifest và loại bỏ permission không còn dùng.
3. Cập nhật Data Safety nếu thêm SDK, analytics, quảng cáo, provider hoặc data type mới.
4. Đảm bảo trong app có link tới Privacy Policy.
5. Đảm bảo account deletion vẫn có cả đường dẫn trong app và web ngoài app.
6. Hoàn thành Health apps declaration theo tính năng thực tế.
7. Kiểm tra link public ở chế độ ẩn danh, không cần đăng nhập và không bị geo-block.

## Tham chiếu Google Play (kiểm tra ngày 02/09/2026)

- User Data / Privacy / Account deletion: https://support.google.com/googleplay/android-developer/answer/10144311
- Health Content and Services: https://support.google.com/googleplay/android-developer/answer/16679511
- Health apps declaration: https://support.google.com/googleplay/android-developer/answer/14738291

## Liên hệ

- Developer: Đào Văn Hùng (daovanhung-dev)
- Privacy contact: Daohungmt2005@gmail.com
- GitHub: https://github.com/daovanhung-dev

> Đây là bộ tài liệu minh bạch dữ liệu dựa trên source kỹ thuật đã đối chiếu. Nó không thay thế tư vấn pháp lý chuyên nghiệp; khi mô hình kinh doanh, phạm vi quốc gia hoặc quy định áp dụng thay đổi, nên được rà soát pháp lý lại.
# nanobioai-privacy
