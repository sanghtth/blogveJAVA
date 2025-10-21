---
title: "Mảng (Arrays) - Quản lý danh sách dữ liệu"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

- **Mảng là một cấu trúc dữ liệu cho phép bạn lưu trữ một danh sách các giá trị cùng kiểu (ví dụ: một mảng int, một mảng String).**

---

## **1. Khai báo và Khởi tạo mảng:**

```java
// Cách 1: Khai báo kích thước trước (ví dụ: 5 phần tử)
// Các giá trị mặc định sẽ là 0 (cho int), false (cho boolean), null (cho String)
int[] danhSachDiem = new int[5];

// Cách 2: Khởi tạo với các giá trị cụ thể
String[] danhSachTen = {"An", "Bình", "Cường", "Dũng"};
```

## **2. Truy cập phần tử (Index):**

- Mảng trong Java được đánh chỉ số (index) bắt đầu từ 0. Để truy cập phần tử, ta dùng tenMang[chiSo].

```java
String[] danhSachTen = {"An", "Bình", "Cường"};

System.out.println(danhSachTen[0]); // In ra "An" (phần tử đầu tiên)
System.out.println(danhSachTen[2]); // In ra "Cường" (phần tử cuối cùng)

// Gán lại giá trị
danhSachTen[1] = "Bình Mới";
System.out.println(danhSachTen[1]); // In ra "Bình Mới"
```

## **3. Lấy độ dài mảng:**

- Sử dụng thuộc tính .length.

```java
System.out.println("Mảng tên có: " + danhSachTen.length + " phần tử."); // 3
```

## **4. Duyệt mảng (Kết hợp với Vòng lặp for):**

- **Cách 1: Dùng for truyền thống (với index)**

```java
double[] diemToan = {8.5, 7.0, 9.5, 10.0};
for (int i = 0; i < diemToan.length; i++) {
    System.out.println("Điểm sinh viên " + (i+1) + ": " + diemToan[i]);
}
```

- **Cách 2: Dùng for-each (Đơn giản hơn) (Dùng khi bạn chỉ cần giá trị, không cần index)**

```java
// Đọc là: "Với mỗi 'diem' là double TRONG mảng 'diemToan'..."
for (double diem : diemToan) {
    System.out.println("Điểm: " + diem);
}
```
