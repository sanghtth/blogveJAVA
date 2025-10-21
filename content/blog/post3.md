---
title: "Công cụ xử lý - Toán tử (Operators) trong Java"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## Chúng ta đã biết cách lưu dữ liệu (biến), giờ là lúc học cách xử lý chúng. Toán tử (Operators) là các ký hiệu đặc biệt dùng để thực hiện các phép toán.

- **1. Toán tử số học (Arithmetic Operators)**

- Dùng cho các phép tính cơ bản: cộng (+), trừ (-), nhân (\*), chia (/), chia lấy dư (%).

```java
int a = 10;
int b = 3;
System.out.println("a + b = " + (a + b)); // 13
System.out.println("a / b = " + (a / b)); // 3 (Vì a và b là int, kết quả là int)
System.out.println("a % b = " + (a % b)); // 1 (10 chia 3 dư 1)
```

- **2. Toán tử gán (Assignment Operators)**

- Dùng để gán giá trị:

= (Gán)

+=, -=, \*=, /=, %= (Gán kết hợp, ví dụ: a += 5 tương đương a = a + 5).

- **3. Toán tử so sánh (Comparison Operators)**

- Dùng để so sánh hai giá trị, luôn trả về boolean (true hoặc false):

== (Bằng)

!= (Không bằng)

/> (Lớn hơn)

< (Nhỏ hơn)

- /> = (Lớn hơn hoặc bằng)

<= (Nhỏ hơn hoặc bằng)

- **4. Toán tử Logic (Logical Operators)**

Dùng để kết hợp các biểu thức boolean:

&& (VÀ - AND): Cả hai vế phải là true thì kết quả là true.

|| (HOẶC - OR): Chỉ cần một vế là true thì kết quả là true.

! (PHỦ ĐỊNH - NOT): Đảo ngược giá trị (!true thành false).

## VÍ DỤ

```java
public class OperatorsDemo {
    public static void main(String[] args) {
        int tuoi = 20;
        double diem = 8.5;

        // Kiểm tra xem có phải sinh viên giỏi và đủ tuổi trưởng thành không
        boolean laSinhVienGioi = diem >= 8.0; // true
        boolean daTruongThanh = tuoi >= 18;  // true

        // Toán tử AND (&&)
        if (laSinhVienGioi && daTruongThanh) {
            System.out.println("Bạn là sinh viên giỏi đã trưởng thành.");
        }

        // Toán tử NOT (!)
        boolean troiMua = false;
        if (!troiMua) {
            System.out.println("Trời không mưa, đi chơi thôi!");
        }
    }
}
```
