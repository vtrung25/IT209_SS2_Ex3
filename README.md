# Bài 3 — Nginx static website (mô phỏng cấu hình)

Thư mục này chứa Server Block mẫu trong `ptit-web.conf` và trang tĩnh tại `html/index.html`. Cấu hình phục vụ nội dung từ `/var/www/ptit-web/html` trên HTTP port 80. Các tệp được chuẩn bị để nộp; không có Nginx nào được cài đặt hoặc cấu hình trên Droplet.

## Ánh xạ khi triển khai

```text
ptit-web.conf  -> /etc/nginx/sites-available/ptit-web.conf
html/          -> /var/www/ptit-web/html/
sites-enabled  -> symlink tới sites-available/ptit-web.conf
```

Khi thực hành trên máy Ubuntu, cần tạo symlink, bỏ kích hoạt site `default`, chạy `nginx -t` rồi mới reload dịch vụ. Output minh họa dự kiến nằm ở [evidence/nginx-check-example.txt](evidence/nginx-check-example.txt); đây là nội dung mẫu, không phải output chạy trên server thật.
