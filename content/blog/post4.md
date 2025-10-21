---
title: "Rẽ nhánh - Câu lệnh If-Else và Switch-Case"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## Trong đời thực, chúng ta luôn ra quyết định: "Nếu trời mưa, tôi sẽ ở nhà. Ngược lại, tôi sẽ đi chơi." Lập trình cũng vậy. Câu lệnh điều kiện cho phép chương trình của bạn thực thi các khối code khác nhau dựa trên một điều kiện (boolean) là true hay false.

---

- **1. Cú pháp if:**

- Thực thi code nếu điều kiện là true.

```java
    int tuoi = 20;
if (tuoi >= 18) {
    System.out.println("Bạn đã đủ tuổi vị thành niên.");
}
```

- **2. Cú pháp if-else:**
- Nếu điều kiện true thì làm A, ngược lại (false) thì làm B.

```java
    int diem = 4;
if (diem >= 5) {
    System.out.println("Bạn đã qua môn!");
} else {
    System.out.println("Bạn đã rớt môn. Cố gắng lên!");
}
```

## **3. Cú pháp if - else if - else:**

- Dùng khi có nhiều điều kiện cần kiểm tra.

```java
    double diemTB = 8.2;
char xepLoai;

if (diemTB >= 8.0) {
    xepLoai = 'A'; // Giỏi
} else if (diemTB >= 6.5) {
    xepLoai = 'B'; // Khá
} else if (diemTB >= 5.0) {
    xepLoai = 'C'; // Trung bình
} else {
    xepLoai = 'F'; // Yếu
}

System.out.println("Xếp loại của bạn: " + xepLoai);
```

## **4. switch-case (Một giải pháp thay thế cho if):**

- Dùng khi bạn muốn so sánh một biến với nhiều giá trị cụ thể. Thường dùng với int, char, hoặc String.

```java
    int thu = 2;
String tenThu;

switch (thu) {
    case 2:
        tenThu = "Thứ Hai";
        break; // Rất quan trọng: 'break' để thoát khỏi switch
    case 3:
        tenThu = "Thứ Ba";
        break;
    // ... các case khác ...
    case 8: // Chủ nhật
        tenThu = "Chủ Nhật";
        break;
    default: // Tương tự 'else'
        tenThu = "Giá trị không hợp lệ";
        break;
}
System.out.println("Hôm nay là: " + tenThu);
```
