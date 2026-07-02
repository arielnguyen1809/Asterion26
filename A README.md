# Hướng dẫn thêm bài học mới — Asterion Academy

## Từ giờ, bạn KHÔNG cần sửa `index.html` nữa.

## Cách thêm bài học mới (ví dụ Lesson 0.5)

1. Tạo 1 file text mới, đặt tên chính xác theo quy tắc: `{module}.{lesson}.md`
   - Ví dụ: `0.5.md`, `0.6.md`, `1.1.md` (nếu sau này có Module 1)
   - **Không dùng số thập phân kiểu `0.10` gây nhầm** — hệ thống đã tự xử lý đúng thứ tự dù bạn dùng `0.10`, `0.11`... nhưng tên file phải luôn có dạng `số.số.md`

2. Nội dung file, 2 dòng đầu tiên **bắt buộc** theo đúng cú pháp:
   ```
   # Lesson 0.5: Tiêu đề tiếng Anh ở đây
   > Phụ đề tiếng Việt ở đây

   Nội dung bài học viết bằng Markdown bình thường từ đây trở xuống...
   ```
   - Dòng 1: bắt đầu bằng `# ` (một dấu thăng + khoảng trắng) → đây là tiêu đề
   - Dòng 2: bắt đầu bằng `> ` (dấu ngoặc nhọn + khoảng trắng) → đây là phụ đề
   - Dòng 3 trở đi: nội dung bài học, dùng Markdown chuẩn:
     - `## Heading` cho tiêu đề phụ
     - `**chữ đậm**`, `*chữ nghiêng*`
     - `- ` cho gạch đầu dòng
     - `> ` cho blockquote/trích dẫn
     - `` `code` `` cho từ khóa kỹ thuật
     - Nếu muốn box highlight kiểu cũ, vẫn có thể chèn thẳng HTML: `<div class="highlight-box">...</div>` — hệ thống vẫn hiểu.

3. Upload file `.md` này vào đúng folder **`lessons/`** trong repo GitHub `Asterion` (dùng nút "Add file → Upload files" trên GitHub, hoặc kéo-thả).

4. Xong. Không cần sửa `index.html`, không cần sửa file danh mục nào khác.
   - Trang sẽ tự động gọi GitHub API, quét toàn bộ folder `lessons/`, sắp xếp theo số thứ tự, và hiện bài mới trong sidebar.
   - Trang có cache 5 phút để tránh gọi GitHub API quá nhiều — nếu vừa upload xong mà chưa thấy bài mới, bấm nút 🔄 (refresh) cạnh chữ "Module 0 · Foundations" ở sidebar để tải lại ngay.

## Cấu trúc repo sau khi cập nhật

```
Asterion/
├── index.html          ← Vỏ khung (shell), gần như không cần sửa lại nữa
└── lessons/
    ├── 0.1.md
    ├── 0.2.md
    ├── 0.3.md
    ├── 0.4.md
    └── 0.5.md           ← chỉ cần thêm file này khi có bài mới
```

## Lưu ý quan trọng

- Repo phải luôn ở chế độ **Public** thì trang mới đọc được danh sách file qua GitHub API mà không cần đăng nhập.
- Tính năng "Custom Notes" (ghi chú lưu trên trình duyệt) đã được gỡ bỏ theo yêu cầu — toàn bộ nội dung giờ đến từ GitHub, đồng bộ trên mọi thiết bị bạn dùng để xem trang.
