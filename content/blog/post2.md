---
title: "Cửa hàng dữ liệu - Biến và Các kiểu dữ liệu cơ bản"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## **1. Biến trong Java**

- Trong lập trình, chúng ta cần một nơi để lưu trữ dữ liệu (như con số, văn bản,...) để có thể sử dụng sau này. Nơi đó được gọi là biến (variable).

### Cú pháp khai báo biến:

```java
kiểu_dữ_liệu tên_biến = giá_trị;
```

### Ví dụ:

```java
int tuoi = 20;           // Số nguyên
String ten = "Sang";     // Chuỗi
double diem = 8.5;       // Số thực
boolean hocGioi = true;  // Boolean
```

## **2. Các kiểu dữ liệu cơ bản**

### **Kiểu số nguyên:**

- `byte`: -128 đến 127 (1 byte)
- `short`: -32,768 đến 32,767 (2 bytes)
- `int`: -2,147,483,648 đến 2,147,483,647 (4 bytes)
- `long`: Rất lớn (8 bytes)

### **Kiểu số thực:**

- `float`: Số thực 4 bytes
- `double`: Số thực 8 bytes (chính xác hơn)

### **Kiểu ký tự:**

- `char`: Một ký tự đơn
- `String`: Chuỗi ký tự

### **Kiểu logic:**

- `boolean`: true hoặc false

## **3. Ví dụ thực tế**

```java
public class BienVaKieuDuLieu {
    public static void main(String[] args) {
        // Khai báo các biến
        String hoTen = "Hoang Thanh Sang";
        int tuoi = 20;
        double diemTB = 8.5;
        boolean laSinhVien = true;

        // In ra màn hình
        System.out.println("Họ tên: " + hoTen);
        System.out.println("Tuổi: " + tuoi);
        System.out.println("Điểm TB: " + diemTB);
        System.out.println("Là sinh viên: " + laSinhVien);
    }
}
```

## **4. Lưu ý quan trọng**

- **Tên biến** không được bắt đầu bằng số
- **Tên biến** phân biệt hoa thường (case-sensitive)
- **Tên biến** không được trùng với từ khóa Java
- Sử dụng **camelCase** cho tên biến (ví dụ: `diemTrungBinh`)

## **Kết luận**: Biến là khái niệm nền tảng. Bài tiếp theo, chúng ta sẽ học cách thực hiện các phép toán trên những biến này!
