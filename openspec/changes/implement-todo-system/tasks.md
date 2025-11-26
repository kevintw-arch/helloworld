# Tasks: Implement To-Do System
# 任務：實作待辦事項系統

1.  [ ] **Scaffold Spring Boot Backend**
        **搭建 Spring Boot 後端鷹架**
    -   Modify `build.gradle` to include Spring Boot starter dependencies (Web, Data JPA, H2) and the Spring Boot plugin.
        修改 `build.gradle` 以包含 Spring Boot 啟動依賴 (Web, Data JPA, H2) 和 Spring Boot 插件。
    -   Create the main application class `org.example.TodoApplication`.
        建立主應用程式類別 `org.example.TodoApplication`。
    -   Validation: Run `./gradlew bootRun` and verify the server starts on port 8080.
        驗證：執行 `./gradlew bootRun` 並確認伺服器在 8080 埠啟動。

2.  [ ] **Implement Backend API**
        **實作後端 API**
    -   Create the `Todo` entity class.
        建立 `Todo` 實體類別。
    -   Create the `TodoRepository` interface extending `JpaRepository`.
        建立繼承 `JpaRepository` 的 `TodoRepository` 介面。
    -   Create `TodoService` for logic.
        建立用於邏輯處理的 `TodoService`。
    -   Create `TodoController` implementing the REST endpoints defined in `design.md`.
        建立實作 `design.md` 中定義的 REST 端點的 `TodoController`。
    -   Validation: Use `curl` or a tool to test GET, POST, PUT, DELETE endpoints against the running server.
        驗證：使用 `curl` 或工具針對執行中的伺服器測試 GET、POST、PUT、DELETE 端點。

3.  [ ] **Scaffold Angular Frontend**
        **搭建 Angular 前端鷹架**
    -   Generate a new Angular application in the `frontend` directory.
        在 `frontend` 目錄中產生一個新的 Angular 應用程式。
    -   Configure proxy to redirect API calls to the backend (localhost:8080).
        配置代理以將 API 呼叫重新導向至後端 (localhost:8080)。
    -   Validation: Run `ng serve` and see the default Angular welcome page.
        驗證：執行 `ng serve` 並查看預設的 Angular 歡迎頁面。

4.  [ ] **Implement Frontend Logic & UI**
        **實作前端邏輯與使用者介面**
    -   Generate `TodoService` in Angular to fetch data from `/api/todos`.
        在 Angular 中產生 `TodoService` 以從 `/api/todos` 獲取資料。
    -   Generate components: `todo-list`, `todo-item`.
        產生組件：`todo-list`、`todo-item`。
    -   Implement the view to list items.
        實作列出項目的視圖。
    -   Implement the form to add items.
        實作新增項目的表單。
    -   Implement actions to toggle completion and delete items.
        實作切換完成狀態與刪除項目的動作。
    -   Validation: Verify full functionality in the browser.
        驗證：在瀏覽器中驗證完整功能。

5.  [ ] **Integration & Final Polish**
        **整合與最終修飾**
    -   Ensure CORS settings allow frontend-backend communication.
        確保 CORS 設定允許前端與後端通訊。
    -   Clean up UI styles.
        清理 UI 樣式。
    -   Run full build `./gradlew build` (optionally configure Gradle to build frontend too).
        執行完整建置 `./gradlew build`（可選配置 Gradle 也建置前端）。