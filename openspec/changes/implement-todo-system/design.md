# Design: To-Do List System
# 設計：待辦事項清單系統

## Architecture
## 架構
The application will be structured to support both backend and frontend development within the existing repository.
應用程式將構建為在現有儲存庫中同時支援後端與前端開發。

### Backend (Spring Boot)
### 後端 (Spring Boot)
-   **Framework:** Spring Boot (Web, Data JPA).
    **框架：** Spring Boot (Web, Data JPA)。
-   **Database:** H2 In-Memory Database.
    **資料庫：** H2 記憶體資料庫。
-   **Layered Architecture:**
    **分層架構：**
    -   **Controller Layer:** Handles HTTP requests and defines REST endpoints (`TodoController`).
        **控制器層：** 處理 HTTP 請求並定義 REST 端點 (`TodoController`)。
    -   **Service Layer:** Contains business logic (`TodoService`).
        **服務層：** 包含商業邏輯 (`TodoService`)。
    -   **Repository Layer:** Interfaces with the database (`TodoRepository`).
        **儲存庫層：** 與資料庫介接 (`TodoRepository`)。
    -   **Entity:** Represents the data structure (`Todo` entity).
        **實體：** 代表資料結構 (`Todo` entity)。

### Frontend (Angular)
### 前端 (Angular)
-   **Framework:** Angular.
    **框架：** Angular。
-   **Location:** A new `frontend` directory (or integrated if using a specific plugin, but separate is standard).
    **位置：** 一個新的 `frontend` 目錄（或如果使用特定插件則整合，但分開是標準做法）。
-   **Key Components:**
    **關鍵組件：**
    -   `TodoListComponent`: Displays the list of items.
        `TodoListComponent`: 顯示項目清單。
    -   `TodoItemComponent`: Renders individual items.
        `TodoItemComponent`: 渲染個別項目。
    -   `TodoInputComponent`: Handles adding new items.
        `TodoInputComponent`: 處理新增項目。
-   **Service:** `TodoService` to communicate with the backend API.
    **服務：** `TodoService` 用於與後端 API 通訊。

## Data Model
## 資料模型

### Todo Entity
### 待辦事項實體
```java
@Entity
public class Todo {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String title; // 標題
    private boolean completed; // 是否完成
    // Getters and Setters // Getter 和 Setter 方法
}
```

## API Specification
## API 規格

| Method | Endpoint          | Description             | Payload (Request) | Payload (Response) |
| :----- | :---------------- | :---------------------- | :---------------- | :----------------- |
| GET    | `/api/todos`      | Get all to-dos (取得所有待辦事項)          | N/A               | `[Todo]`           |
| POST   | `/api/todos`      | Create a new to-do (建立新待辦事項)      | `{"title": "..."}`| `Todo`             |
| PUT    | `/api/todos/{id}` | Update a to-do (更新待辦事項)          | `Todo` fields     | `Todo`             |
| DELETE | `/api/todos/{id}` | Delete a to-do (刪除待辦事項)          | N/A               | `204 No Content`   |

## Build & Deployment
## 建置與部署
-   **Gradle:** Will be configured to build the Spring Boot app.
    **Gradle:** 將配置用於建置 Spring Boot 應用程式。
-   **npm/ng:** Used for the Angular frontend.
    **npm/ng:** 用於 Angular 前端。