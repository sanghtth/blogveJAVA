---
title: "Lớp (Class) và Đối tượng (Object) - Cốt lõi của OOP"
date: 2025-10-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## **Chào mừng bạn đến với Lập trình Hướng đối tượng (OOP)! Đây là khái niệm quan trọng nhất của Java.**

Hãy nghĩ về thế giới thực: chúng ta được bao quanh bởi các đối tượng (con người, xe hơi, con mèo). Mỗi đối tượng có:

- Thuộc tính (Properties): Đặc điểm (ví dụ: ConMèo có mauLong, canNang).

- Hành vi (Methods): Hành động (ví dụ: ConMèo có thể keu(), an()).

- **1. Lớp (Class) - Bản thiết kế**

- Lớp (Class) là một bản thiết kế hoặc khuôn mẫu để tạo ra các đối tượng. Lớp ConMeo định nghĩa rằng tất cả con mèo sẽ có mauLong và có thể keu().

- **2. Đối tượng (Object) - Thể hiện**

- Đối tượng (Object) là một thể hiện (instance) cụ thể của lớp đó. Bạn có thể tạo nhiều đối tượng từ một lớp.

Đối tượng meoTom (từ lớp ConMeo) có mauLong là "Xám".

Đối tượng meoMun (từ lớp ConMeo) có mauLong là "Đen".

-**Ví dụ:** Xây dựng Lớp SinhVien

```java
// Đây là LỚP (Bản thiết kế)
public class SinhVien {

    // 1. Thuộc tính (Attributes / Fields)
    String maSo;
    String hoTen;
    double diemTB;

    // 2. Phương thức khởi tạo (Constructor)
    // Đây là phương thức đặc biệt, được gọi khi tạo đối tượng mới (dùng 'new')
    // Tên của nó phải trùng với tên Lớp
    public SinhVien(String ms, String ten, double diem) {
        // 'this' ám chỉ thuộc tính của chính đối tượng này
        this.maSo = ms;
        this.hoTen = ten;
        this.diemTB = diem;
    }

    // 3. Phương thức (Hành vi / Methods)
    public void hienThiThongTin() {
        System.out.println("--- Thông tin Sinh viên ---");
        System.out.println("MSSV: " + this.maSo);
        System.out.println("Tên: " + this.hoTen);
        System.out.println("Điểm: " + this.diemTB);
    }

    public boolean kiemTraHocBong() {
        return this.diemTB >= 8.0;
    }
}
```

- **Sử dụng Lớp SinhVien để tạo Đối tượng:**

Bây giờ, trong file QuanLyTruongHoc.java (hoặc file có hàm main):

```java
public class QuanLyTruongHoc {
    public static void main(String[] args) {

        // Tạo 2 ĐỐI TƯỢNG (instances) từ lớp SinhVien
        // Chúng ta gọi Constructor bằng từ khóa 'new'
        SinhVien sv1 = new SinhVien("SV001", "Nguyễn Văn A", 7.5);
        SinhVien sv2 = new SinhVien("SV002", "Trần Thị B", 8.5);

        // Gọi phương thức (hành vi) của từng đối tượng
        sv1.hienThiThongTin();
        // Output:
        // --- Thông tin Sinh viên ---
        // MSSV: SV001
        // Tên: Nguyễn Văn A
        // Điểm: 7.5

        sv2.hienThiThongTin();
        // Output:
        // --- Thông tin Sinh viên ---
        // MSSV: SV002
        // Tên: Trần Thị B
        // Điểm: 8.5

        // Kiểm tra học bổng
        System.out.println("SV1 có học bổng? " + sv1.kiemTraHocBong()); // false
        System.out.println("SV2 có học bổng? " + sv2.kiemTraHocBong()); // true
    }
}
```
