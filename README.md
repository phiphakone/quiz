# Lotus & Champa — bản sẵn sàng đưa lên GitHub

Bản này được chuẩn bị từ thư mục `mới`. Website tĩnh, không cần npm hoặc bước build.

## Đưa lên GitHub và bật website

1. Tạo repository mới trên GitHub, ví dụ `lotus-champa`. Chọn Public nếu dùng GitHub Free.
2. Chọn **Add file → Upload files**, tải toàn bộ nội dung trong thư mục này lên repository. `index.html` và thư mục `images` phải nằm ngay ở gốc repository, không nằm trong một thư mục bọc bên ngoài. Không tải file ZIP thay cho nội dung website.
3. Commit các file vào nhánh `main`.
4. Vào **Settings → Pages → Build and deployment**. Chọn **Deploy from a branch**, nhánh **main**, thư mục **/(root)**, rồi **Save**.
5. Sau khi GitHub triển khai thành công, lấy địa chỉ website tại trang Pages. Địa chỉ thường có dạng `https://TEN-TAI-KHOAN.github.io/lotus-champa/`.

Tài liệu chính thức: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Nội dung đã chuẩn bị

- Giữ mã website từ bản `mới`; bổ sung 45 file ảnh từ các bản có sẵn trên máy.
- Đặt ảnh logo và QR ngân hàng đúng đường dẫn, đúng chữ hoa/thường.
- Bổ sung ảnh sản phẩm, bao gồm ảnh sá sùng set 2.
- Bỏ các ô ảnh giới thiệu tham chiếu 2 file không có (1781956435067... và 1781956435144...).
- Đã bổ sung ảnh minh họa thổ cẩm từ `Website lên github/images/products/p-lao-tranhthocam-reference-web.jpg`, có chú thích ảnh minh họa tại danh sách và chi tiết sản phẩm. Đây chưa phải ảnh xác nhận của sản phẩm thực tế.
- Tăng phiên bản dữ liệu lên 12 để cập nhật đường dẫn ảnh trong bộ nhớ trình duyệt. Cơ chế có sẵn của website sẽ nạp lại danh mục sản phẩm và blog mẫu khi phiên bản đổi.
- Có `.nojekyll` và `.gitignore`. Không đưa file Python tính tiền điện, tài liệu Word hoặc ảnh trùng không dùng vào bản phát hành.

## Những phần cần lưu ý khi vận hành

- Đã kiểm tra cú pháp JavaScript và các tham chiếu ảnh cục bộ. Phiên bản sửa Firebase đã qua 48 bài kiểm thử Rules bằng Emulator và 8 bài kiểm thử checkout mô phỏng.
- Chưa triển khai lên tài khoản GitHub; chưa kiểm thử giao dịch thật trên tên miền công khai. Xem FIREBASE-SETUP-TH.md để bật Authentication, Publish firestore.rules và storage.rules, và tạo quyền admin.
- Website dùng Firebase project lotus-1a491; đơn hàng giờ gắn ownerUid và cần bật Anonymous Authentication. GitHub Pages chỉ phục vụ giao diện; đơn hàng, đăng nhập và tải biên lai vẫn phụ thuộc Firebase Auth, Firestore, Storage và quyền truy cập được cấu hình ở dự án đó.
- Form liên hệ hiện chỉ hiện thông báo cảm ơn, chưa gửi nội dung. Một số đường dẫn Facebook/chính sách vẫn là đường dẫn chung có sẵn trong bản gốc.
- Danh mục, blog và một số dữ liệu quản trị vẫn dùng localStorage; thay đổi tại một trình duyệt không tự đồng bộ cho tất cả khách truy cập.

