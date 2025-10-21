---
title: "Chào thế giới Java! ☕ Cài đặt JDK và Viết chương trình đầu tiên"
date: 2025-01-16
author: "Hoang Thanh Sang"
description: "Mô tả ngắn về bài viết"
tags: ["lập trình", "học tập"]
draft: false
---

<!--more-->

## Chào mừng các bạn đến với loạt bài học lập trình Java! Java là một trong những ngôn ngữ lập trình phổ biến nhất thế giới, chạy trên hàng tỷ thiết bị. Nó nổi tiếng với triết lý "Write Once, Run Anywhere" (Viết một lần, chạy mọi nơi).

---

## **1. JDK, JRE, và JVM là gì?**

- JVM (Java Virtual Machine): Máy ảo Java, là môi trường thực thi code. Đây là lý do Java chạy được mọi nơi.

- JRE (Java Runtime Environment): Môi trường chạy Java, bao gồm JVM và các thư viện cần thiết để chạy ứng dụng.

- JDK (Java Development Kit): Bộ công cụ phát triển Java, bao gồm JRE và các công cụ cho lập trình viên (như trình biên dịch javac).

- Để lập trình, bạn cần cài đặt JDK.

## **2. Viết Chương trình "Hello, World!"**

- Sau khi cài đặt JDK và một IDE (như IntelliJ, Eclipse, hoặc VS Code), hãy tạo file đầu tiên: HelloWorld.java.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

- **Cách chạy (trên terminal/cmd):**

- Biên dịch code: javac HelloWorld.java (Thao tác này tạo ra file HelloWorld.class)

- Chạy chương trình: java HelloWorld
- Kết quả: Hello, World!

##
