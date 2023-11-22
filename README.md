# Django-React Xác thực JWT

Dự án này mô tả cách triển khai xác thực JWT (JSON Web Token) bằng cách sử dụng Django và React, với một máy chủ Express làm máy chủ backend.

Thông tin chứng nhận JWT trong dự án này được lưu trữ an toàn trong cookies, được cấu hình với cờ `httpOnly` được đặt thành `true` để ngăn chặn JavaScript trên trình duyệt truy cập vào các giá trị này.

## Bắt đầu

Thực hiện các bước sau để kiểm thử dự án:

1. **Clone Repository:**
    ```bash
    git clone https://github.com/Duong-1309/auth-site
    ```

2. **Cài đặt Backend:**
    - Di chuyển đến thư mục `backend`.
    - Tạo một môi trường ảo:
        ```bash
        python3 -m venv venv
        ```
    - Kích hoạt môi trường ảo:
        - MacOS/Linux:
            ```bash
            source venv/bin/activate
            ```
        - Windows:
            ```bash
            .\venv\Scripts\activate
            ```
    - Cài đặt các gói Python:
        ```bash
        pip install -r requirements.txt
        ```
    - Di chuyển đến cơ sở dữ liệu Sqlite3:
        ```bash
        python manage.py migrate
        ```
    - Tạo một super user
        ```
        python manage.py createsuperuser
        ```
    - Chạy máy chủ Django:
        ```bash
        python manage.py runserver
        ```
        Lúc này máy chủ django sẽ chạy ở cổng mặc định là 8000
       

3. **Cài đặt Frontend:**
    - Di chuyển đến thư mục `frontend/client`.
    - Cài đặt các phụ thuộc Node.js:
        ```bash
        npm install
        ```
    - Xây dựng frontend:
        ```bash
        npm run build
        ```

4. **Chạy Frontend:**
    - Di chuyển đến thư mục `frontend`.
    - Cài đặt các phụ thuộc Node.js:
        ```bash
        npm install
        ```
    - Khởi chạy frontend:
        ```bash
        npm start
        ```
    - Mở trình duyệt và truy cập [http://localhost:5000](http://localhost:5000) cho môi trường sản xuất.
    - Tùy chọn, bạn có thể di chuyển đến `frontend/client` và chạy:
        ```bash
        npm start
        ```
        - Sau đó, trong trình duyệt, truy cập [http://localhost:3000](http://localhost:3000) cho môi trường phát triển.

Hãy thoải mái tùy chỉnh và khám phá dự án. Chúc bạn lập trình vui vẻ!