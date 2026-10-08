# ban84vn.com

BẢN84 — kênh phân tích & góc nhìn về kinh tế, chính sách và AI ứng dụng cho người trẻ Việt Nam. Không phải cơ quan báo chí.

Trang tĩnh, phát hành qua GitHub Pages tại https://ban84vn.com (tên miền khai báo trong tệp `CNAME`). Không cần hosting hay cơ sở dữ liệu.

## Video
Video phát trực tiếp trên trang bằng trình phát HTML5, không chuyển sang Facebook/TikTok.
- `vid/<slug>.mp4`: bản web 720×1280, H.264 + AAC, `faststart`, mỗi tệp dưới 10 MB (nén 2 lượt từ bản gốc 1080×1920).
- `img/poster/<slug>.jpg`: ảnh chờ 9:16 (`s/` = 360w cho thanh chọn video).
- Bài chưa có bản web thì tự quay về trình phát Facebook.

## DNS (Squarespace Domains)
- `@` A → 185.199.108.153 · 185.199.109.153 · 185.199.110.153 · 185.199.111.153
- `www` CNAME → oceantreasurevn-coder.github.io
- Giữ nguyên MX `smtp.google.com` và TXT SPF của Google Workspace (email Infor@ban84vn.com).

## Cấu trúc
- `index.html` (video mới nhất + thanh chọn video), `video.html` (lưới video), `chu-de/*.html`
- `bai/<slug>.html`: video cạnh tiêu đề, điểm chính, câu hỏi mở, toàn văn, số liệu đã kiểm & nguồn, chia sẻ
- `gioi-thieu.html`, `nguyen-tac.html`, `tim-kiem.html` + `data/search.json`, `data/posts.json`
- `feed.xml` (RSS), `sitemap.xml` (kèm thẻ video), `robots.txt`, `manifest.webmanifest`, `404.html`

## Thêm bài mới
Trang được sinh bằng `news/build.py` (trong kho dựng của BẢN84) từ `published.json` + `stories/<key>.json` + `photos/photos.json` + `videos/web/<slug>.mp4`. Chạy `python3 build.py` rồi tải thư mục `out/` lên đây.
