# GEMINI.md

請一律使用正體中文互動

## 專案概觀

這是一個名為 "Hello" 的簡單 "Hello World" Java 專案。它使用 Gradle 建置，並使用 JUnit 5 進行測試。主要應用程式進入點是 `org.example.Main` 類別中的 `main` 方法。
問題都在在 ai/prompts/*.md
AI產出的資料請儲存至 ai/outputs/*.md

## 建置與執行

### 建置專案

若要建置專案並建立 JAR 檔案，請在您的終端機中執行下列指令：

```bash
./gradlew build
```

### 執行應用程式

若要執行應用程式，請使用下列 Gradle 指令：

```bash
./gradlew run
```

### 執行測試

若要執行測試，請使用下列指令：

```bash
./gradlew test
```

## 開發慣例

*   **語言:** Java
*   **建置工具:** Gradle
*   **測試框架:** JUnit 5
*   **程式碼風格:** 本專案遵循標準 Java 程式碼慣例。