---
title: "Vòng lặp (Loops) - Đừng tự lặp lại chính mình!"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## **1. Vòng lặp for:**

- Thường dùng khi bạn biết chính xác số lần bạn muốn lặp.

- Cú pháp: for (khởi tạo; điều kiện; bước nhảy)

- Khởi tạo: Chạy 1 lần duy nhất trước khi vòng lặp bắt đầu (ví dụ: int i = 0).

- Điều kiện: Kiểm tra trước mỗi lần lặp. Nếu true thì lặp, false thì dừng.

- Bước nhảy: Chạy sau mỗi lần lặp (ví dụ: i++ tức là i = i + 1).

- **Ví dụ: In các số từ 1 đến 5.**

```java
    for (int i = 1; i <= 5; i++) {
    System.out.println("Số: " + i);
}
// Kết quả:
// Số: 1
// Số: 2
// Số: 3
// Số: 4
// Số: 5
```

## **2. Vòng lặp while:**

- Thường dùng khi bạn không biết trước số lần lặp, bạn chỉ biết điều kiện dừng. Vòng lặp sẽ chạy miễn là điều kiện còn true.

- **Ví dụ: Chương trình đoán số (đoán sai thì phải nhập lại)**

```java
import java.util.Scanner;

public class GuessNumber {
    public static void main(String[] args) {
        int soBiMat = 7;
        int soDoan = 0;
        Scanner scanner = new Scanner(System.in);

        // Chừng nào soDoan còn khác soBiMat thì còn lặp
        while (soDoan != soBiMat) {
            System.out.print("Hãy đoán số (1-10): ");
            soDoan = scanner.nextInt();

            if (soDoan != soBiMat) {
                System.out.println("Đoán sai rồi, thử lại!");
            }
        }

        System.out.println("Chúc mừng! Bạn đã đoán đúng số 7!");
        scanner.close();
    }
}
```

## **3. do-while (Biến thể của while)**

- Giống hệt while, nhưng nó luôn đảm bảo chạy code bên trong ít nhất một lần trước khi kiểm tra điều kiện.

```java
int i = 100;
do {
    // Khối code này vẫn chạy 1 lần dù i (100) không < 10
    System.out.println("Chạy ít nhất 1 lần");
} while (i < 10);

```
