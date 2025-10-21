---
title: "Phương thức (Methods) - Đóng gói và Tái sử dụng Code"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## **Khi bạn viết các chương trình lớn, phương thức main sẽ trở nên rất dài và khó quản lý. Phương thức (Method) (hay còn gọi là hàm - function) là một khối code được đặt tên, thực hiện một nhiệm vụ cụ thể.**

---

- Lợi ích của Phương thức:

* Tái sử dụng (Reusability): Viết 1 lần, gọi nhiều lần.

* Tổ chức (Organization): Chia một chương trình lớn thành các phần nhỏ, dễ hiểu.

- **1. Cấu trúc một phương thức:**

```java
 <kiểu_truy_cập> <static (tùy chọn)> <kiểu_trả_về> <tên_phương_thức>
 (<tham_số_1>, <tham_số_2>, ...) {

     return <giá trị>; // (Nếu kiểu_trả_về không phải là void)
 }

```

- Kiểu_trả_về:

- **_void:_** Phương thức này không trả về giá trị nào (nó chỉ thực hiện hành động, ví dụ: System.out.println).

- **_int, String, double,...:_** Phương thức này phải trả về một giá trị thuộc kiểu đó bằng từ khóa return.

- **_tham_số (Parameters):_** Dữ liệu đầu vào mà phương thức cần để hoạt động.

- **2. Ví dụ 1: Phương thức void (Không trả về)**

```java
public class MethodDemo {

    // Phương thức main là nơi chương trình bắt đầu
    public static void main(String[] args) {
        // Gọi phương thức chaoHoi
        chaoHoi("Tuấn"); // Output: Chào mừng Tuấn đến với blog!
        chaoHoi("Lan");  // Output: Chào mừng Lan đến với blog!
    }

    // Đây là phương thức chaoHoi
    // Nó nhận 1 tham số (parameter) tên là 'ten' kiểu String
    public static void chaoHoi(String ten) {
        System.out.println("Chào mừng " + ten + " đến với blog!");
    }
}
```

- **3. Ví dụ 2: Phương thức có trả về (Return value)**

```java
public class Calculator {

    public static void main(String[] args) {
        // Gọi phương thức tinhTong và lưu kết quả vào biến 'ketQua'
        int ketQua = tinhTong(5, 10);

        System.out.println("Tổng là: " + ketQua); // Output: Tổng là: 15
        System.out.println("100 + 200 = " + tinhTong(100, 200)); // Output: 100 + 200 = 300
    }

    // Phương thức này trả về một giá trị kiểu 'int'
    // Nó nhận 2 tham số kiểu 'int'
    public static void int tinhTong(int soA, int soB) {
        int tong = soA + soB;
        return tong; // Trả về kết quả
    }
}
```

## **Kết luận: Phương thức giúp code của bạn sạch sẽ và dễ bảo trì. Chúng ta đã học xong các kiến thức cơ bản về lập trình thủ tục. Ở bài tiếp theo, chúng ta sẽ bước vào "trái tim" thực sự của Java: Lập trình Hướng đối tượng (OOP) với Lớp và Đối tượng.**
