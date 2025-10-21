---
title: "Xử lý sự cố - Exception Handling (Try-Catch)"
date: 2025-10-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

- Bạn đã bao giờ chạy chương trình và thấy terminal hiển thị một đống chữ đỏ báo lỗi và chương trình bị "sập" (crash) chưa? Đó gọi là Ngoại lệ (Exception).

- Ngoại lệ là những sự kiện không mong muốn xảy ra khi chương trình đang chạy, làm gián đoạn luồng bình thường.

1. Ví dụ: Chia một số cho 0 ( ArithmeticException ).

2. Ví dụ: Cố gắng truy cập phần tử thứ 10 của mảng chỉ có 5 phần tử ( ArrayIndexOutOfBoundsException ).

3. Ví dụ: Người dùng nhập "abc" khi bạn yêu cầu nhập một số ( InputMismatchException ).

Nếu không xử lý, chương trình sẽ dừng đột ngột. Chúng ta dùng try-catch để bắt lấy lỗi này và xử lý một cách mượt mà.

- **1. Cú pháp try-catch:**

```java
try {
    // Đặt code có nguy cơ gây lỗi vào đây
} catch (TenLoaiException e) {
    // Xử lý lỗi nếu nó xảy ra
    // 'e' là đối tượng chứa thông tin về lỗi
}
```

- Nếu không có try-catch, chương trình sẽ "sập" ngay tại phép chia và dòng "Chương trình vẫn tiếp tục chạy..." sẽ không bao giờ được in ra.

- **2. finally (Tùy chọn):**

- Khối finally là khối code luôn luôn được thực thi, dù lỗi có xảy ra hay không. Thường dùng để dọn dẹp tài nguyên (ví dụ: đóng file, đóng kết nối database).

```java
Scanner scanner = null;
try {
    scanner = new Scanner(System.in);
    System.out.print("Nhập một số: ");
    int num = scanner.nextInt(); // Nguy cơ lỗi nếu nhập chữ
    System.out.println("Bạn đã nhập: " + num);
} catch (Exception e) { // 'Exception' là lớp cha, bắt được mọi loại lỗi
    System.out.println("Lỗi: Vui lòng nhập đúng định dạng số.");
} finally {
    // Dù thành công hay thất bại, cũng phải đóng scanner
    if (scanner != null) {
        scanner.close();
        System.out.println("Đã đóng scanner.");
    }
}
```
