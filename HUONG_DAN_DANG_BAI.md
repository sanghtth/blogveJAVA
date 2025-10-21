# Hướng dẫn đăng bài blog đơn giản

## Cách tạo bài viết mới

### 1. Tạo bài viết từ template có sẵn

```bash
hugo new blog/ten-bai-viet-cua-ban.md
```

### 2. Hoặc tạo thủ công

Tạo file mới trong thư mục `content/blog/` với tên file bất kỳ (ví dụ: `bai-viet-moi.md`)

## Cấu trúc bài viết đơn giản

Mỗi bài viết chỉ cần có phần front matter (metadata) ở đầu file:

```yaml
---
title: "Tiêu đề bài viết"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---
<!--more-->

Nội dung bài viết của bạn...
```

## Các trường bắt buộc

- `title`: Tiêu đề bài viết
- `date`: Ngày đăng (định dạng YYYY-MM-DD)
- `draft`: false (để hiển thị bài viết)

## Các trường tùy chọn

- `author`: Tác giả (mặc định sẽ hiển thị tên của bạn)
- `description`: Mô tả ngắn
- `tags`: Danh sách tags (không bắt buộc)

## Cách thêm hình ảnh

### 1. Đặt hình vào thư mục `images/`
- Copy hình ảnh vào thư mục `images/` (ví dụ: `images/hinh-cua-ban.jpg`)

### 2. Sử dụng shortcode trong bài viết
```markdown
{{< figure src="hinh-cua-ban.jpg" alt="Mô tả hình" caption="Chú thích hình" >}}
```

### 3. Hoặc sử dụng Markdown thông thường
```markdown
![Mô tả hình](/images/hinh-cua-ban.jpg)
```

## Lưu ý

- Không cần tạo thư mục con, chỉ cần tạo file `.md` trực tiếp trong `content/blog/`
- Sử dụng `<!--more-->` để phân chia phần tóm tắt và nội dung đầy đủ
- Hình ảnh phải đặt trong thư mục `images/` để hiển thị đúng
- Sau khi tạo bài viết, chạy `hugo server` để xem kết quả

## Ví dụ bài viết hoàn chỉnh

````yaml
---
title: "Học JavaScript cơ bản"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Bài viết hướng dẫn học JavaScript từ cơ bản"
tags: ["javascript", "lập trình", "học tập"]
draft: false
---

<!--more-->

## Giới thiệu

JavaScript là một ngôn ngữ lập trình rất phổ biến...

## Nội dung chính

### Biến trong JavaScript

```javascript
let name = "Hoang Thanh Sang";
const age = 20;
````

### Hàm trong JavaScript

```javascript
function greet(name) {
  return "Xin chào " + name;
}
```

## Kết luận

JavaScript là ngôn ngữ rất hữu ích cho việc phát triển web...
