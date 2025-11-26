# Spec: Manage To-Dos
# 規格：管理待辦事項

## ADDED Requirements
## 新增需求

#### Requirement: Create To-Do Item
#### 需求：建立待辦事項
The system shall allow a user to create a new To-Do item by providing a title.
系統應允許使用者透過提供標題來建立新的待辦事項。
-   **Scenario 1:** User sends a valid title. The system creates the item, assigns a unique ID, sets `completed` to false, and returns the created item.
    **情境 1:** 使用者傳送有效的標題。系統建立項目，分配唯一的 ID，將 `completed` 設為 false，並回傳建立的項目。
-   **Scenario 2:** User provides an empty title. The system should validate and return an error (Bad Request).
    **情境 2:** 使用者提供空白標題。系統應進行驗證並回傳錯誤（錯誤請求）。

#### Requirement: Retrieve To-Do Items
#### 需求：檢索待辦事項
The system shall allow a user to retrieve the list of all existing To-Do items.
系統應允許使用者檢索所有現有待辦事項的清單。
-   **Scenario 1:** User requests the list. The system returns a JSON array containing all stored items.
    **情境 1:** 使用者請求清單。系統回傳包含所有儲存項目的 JSON 陣列。

#### Requirement: Update To-Do Item
#### 需求：更新待辦事項
The system shall allow a user to update the details (title, completion status) of an existing To-Do item.
系統應允許使用者更新現有待辦事項的詳細資訊（標題、完成狀態）。
-   **Scenario 1:** User updates the status to 'completed'. The system persists the change.
    **情境 1:** 使用者更新狀態為「已完成」。系統持久化該變更。
-   **Scenario 2:** User attempts to update a non-existent ID. The system returns 404 Not Found.
    **情境 2:** 使用者試圖更新不存在的 ID。系統回傳 404 找不到。

#### Requirement: Delete To-Do Item
#### 需求：刪除待辦事項
The system shall allow a user to remove a To-Do item permanently.
系統應允許使用者永久移除待辦事項。
-   **Scenario 1:** User requests deletion of a specific ID. The system removes the item and returns a success status.
    **情境 1:** 使用者請求刪除特定的 ID。系統移除該項目並回傳成功狀態。