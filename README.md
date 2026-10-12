# Spring Boot CI – Gradle Build & Artifact

## Giới thiệu

Dự án minh họa quy trình CI cho ứng dụng Spring Boot sử dụng Gradle và GitHub Actions. Khi có commit được push lên nhánh `main`, workflow chạy JUnit Test, đóng gói ứng dụng thành file JAR và lưu thành phẩm dưới dạng GitHub Actions Artifact.

## Công nghệ

- Java 17 (Eclipse Temurin)
- Spring Boot 3
- Gradle 8
- JUnit 5
- GitHub Actions

## API

`GET /hello` trả về `Hello CI!`.

## Quy trình CI

1. Checkout mã nguồn.
2. Thiết lập JDK 17.
3. Cấp quyền thực thi cho Gradle.
4. Chạy `./gradlew test`.
5. Đóng gói với `./gradlew bootJar`.
6. Lưu file `build/libs/*.jar` thành artifact `app-jar`.

## Kết quả

Sau khi workflow thành công, artifact `app-jar` xuất hiện trong phần **Artifacts** trên trang **Summary** của workflow run.
