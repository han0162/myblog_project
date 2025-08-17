# 個人Blog網站開發

---

## 專案簡介

一個使用 **Flask + MySQL** 開發的個人部落格系統，支援登入、文章發佈、編輯與刪除，介面簡潔直覺，並搭配 Bootstrap 5 進行前端設計。

## 專案功能

- 使用者登入驗證（bcrypt + flask-login）
- 文章 CRUD 功能（Create / Read / Update / Delete）
- Markdown 預覽支援（showdown.js）
- Bootstrap 5 響應式介面
- SQLAlchemy ORM 操作 MySQL 資料庫
- Docker & Docker Compose 一鍵部署

## 快速開始
以下說明將引導你在本地機器上搭建和運行此專案，以便進行開發和測試。

### 環境需求
請先在系統上安裝 Docker。若使用 Windows 或 macOS，建議安裝 Docker Desktop：

- Docker Desktop：https://www.docker.com/products/docker-desktop/

### 安裝步驟
### 1. 複製專案：
```bash
git clone https://github.com/han0162/myblog_project.git
cd myblog_project
```

### 2.使用 Docker Compose 建立並運行：
此指令會自動建構映像檔，並啟動 Flask 與 MySQL 服務 (適合第一次執行或有修改 Dockerfile 時使用)。
若你已經建構過映像檔，僅需執行 docker-compose up 即可啟動。
```bash
docker-compose up --build
```


### 3.瀏覽網站：
根據你的執行環境，請依照以下方式在瀏覽器中開啟部落格：

- 🖥️ 本機端執行
請在瀏覽器中輸入：
(本專案將容器內的 Flask 服務（8080 埠）映射至主機的 80 埠，因此無需加上埠號。)
```bash
http://localhost
```

- ☁️ 虛擬機或遠端主機執行
請使用該主機的 IP 位址或網域名稱：
```bash
http://<虛擬機的 IP 位址>
```


---

## 使用說明
### 管理員登入
請注意：此為開發環境的預設帳密。在生產環境中務必修改！

預設的管理員帳密是：root/1234566，您可以透過 http://localhost/login.html 進行登入。
<img width="934" height="431" alt="image" src="https://github.com/user-attachments/assets/c8d1e988-c56d-49a3-9071-46b9ca8d2b53" />

---

### 建立/編輯文章

- 登入管理員帳號後，將看到「發布新文章」和「編輯」、「刪除」的選項。
- 文章編輯頁面支援 Markdown 內容撰寫，並包含即時預覽功能。
<img width="946" height="495" alt="image" src="https://github.com/user-attachments/assets/99be5c72-495d-4511-8ead-d88b7f495b6a" />
<img width="929" height="178" alt="image" src="https://github.com/user-attachments/assets/cb79a94a-2556-4ac7-89f7-afe5076548af" />



