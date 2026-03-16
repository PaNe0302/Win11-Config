Win11-Config 🧊



Bộ sưu tập các file cấu hình (config) Windows 11 ricing cá nhân, tập trung vào sự tối giản, hiệu suất và khả năng tự động hóa công việc.

🖥️ Thành phần chính



&#x20;   Window Manager: Komorebi (Tiling WM cho Windows)



&#x20;   Bar: YASB Reborn (Thanh bar tùy biến cao)



&#x20;   Tùy biến hệ thống: Winhawk



🛠️ Hướng dẫn cá nhân hóa



Để các file config này hoạt động chuẩn trên máy của bạn, hãy thực hiện các thay đổi sau trong file config.yaml của Yasb Reborn:

1\. Cấu hình API Thời tiết



Tìm đến widget weather (khoảng dòng 159). Tôi đã để sẵn placeholder, bạn cần thay bằng mã API của mình:



&#x20;   Đăng ký lấy mã tại: WeatherAPI.com



&#x20;   Thay đổi trong file:

&#x20;   YAML



&#x20;   weather:

&#x20;     options:

&#x20;       api\_key: "MÃ\_API\_CỦA\_BẠN" # Thay YOUR\_API\_KEY\_HERE bằng mã thật

&#x20;       location: "Hanoi" # Thay đổi tên thành phố của bạn



2\. Sửa đường dẫn Menu Home (Widget Home)



Các đường dẫn trong menu Home (dòng 40-47) được thiết lập theo cấu trúc ổ đĩa cá nhân. Bạn cần sửa lại để trỏ đúng vào các thư mục trên máy bạn:



&#x20;   Sử dụng biến môi trường: Tôi đã cấu hình sẵn %USERPROFILE% cho các thư mục hệ thống để tự động nhận diện tên người dùng của bạn.



&#x20;   Sửa thủ công các ổ đĩa khác:

&#x20;   YAML



&#x20;   menu\_list:

&#x20;     - { title: "Tools", path: "D:\\\\Tools" }      # Sửa lại ổ đĩa hoặc tên thư mục

&#x20;     - { title: "Game", path: "D:\\\\Games" }      # Sửa lại ổ đĩa hoặc tên thư mục

&#x20;     - { title: "Wallpaper", path: "D:\\\\Wallpaper" } # Sửa lại ổ đĩa hoặc tên thư mục



&#x20;   Lưu ý: Luôn sử dụng dấu gạch chéo ngược kép (\\\\) khi viết đường dẫn trong file YAML để tránh lỗi.



3\. Cấu hình Wallpaper



Tìm tới widget wallpapers, hãy đổi image\_path tới thư mục chứa ảnh nền của bạn:

YAML



wallpapers:

&#x20; options:

&#x20;   image\_path: "D:\\\\Wallpaper\\\\Full HD picture" # Sửa đường dẫn này





📄 Lưu ý chung



&#x20;   Đảm bảo bạn đã cài đặt các Font chữ cần thiết (như Nerd Fonts) để các icon hiển thị chính xác.



&#x20;   Các file cấu hình này được tối ưu cho độ phân giải màn hình và quy trình làm việc cá nhân, hãy thoải mái điều chỉnh padding và dimensions trong file config.yaml để vừa vặn với màn hình của bạn.

