# Python 支援 JSON

## **前言**

Python **內建 支援 JSON（JavaScript Object Notation），主要透過 `json` 模組來 **解析（讀取）**、**處理（操作）** 和 **產生（寫入）** JSON 檔案。

---

## **1. 解析（讀取）JSON**

### **(1) 解析 JSON 字串**

如果你有一個 JSON 格式的字串，Python 可以將它轉換為對應的資料結構（通常是字典 `dict` 或列表 `list`）。

```python
import json

json_str = '{"name": "Alice", "age": 25, "city": "Taipei"}'
data = json.loads(json_str)  # 將 JSON 字串轉換成 Python 字典
print(data)       # {'name': 'Alice', 'age': 25, 'city': 'Taipei'}
print(data["age"])  # 25
```

---

### **(2) 讀取 JSON 檔案**

如果 JSON 儲存在 `.json` 檔案中，可以這樣讀取：

```python
import json

with open("data.json", "r", encoding="utf-8") as file:
    data = json.load(file)  # 讀取 JSON 檔案並轉成 Python 物件
print(data)
```

🔹 `json.load(file)` 會把 JSON 內容轉換成 Python 的字典或列表。

---

## **2. 產生（寫入）JSON**

### **(1) 轉換 Python 物件為 JSON 字串**

```python
import json

data = {"name": "Alice", "age": 25, "city": "Taipei"}
json_str = json.dumps(data)  # 轉換為 JSON 格式的字串
print(json_str)  # {"name": "Alice", "age": 25, "city": "Taipei"}
```

---

### **(2) 將 JSON 儲存為 `.json` 檔案**

```python
import json

data = {"name": "Alice", "age": 25, "city": "Taipei"}

with open("data.json", "w", encoding="utf-8") as file:
    json.dump(data, file, ensure_ascii=False, indent=4)  # 寫入 JSON 檔案，格式化輸出
```

🔹 `ensure_ascii=False`：確保中文字不被轉換為 Unicode 轉義序列。
🔹 `indent=4`：讓 JSON 內容更易讀（縮排 4 格）。

---

## **3. JSON 格式與 Python 物件的對應**

| **JSON 類型**           | **Python 類型** |
| --------------------- | ------------- |
| `{"key": "value"}`    | `dict`（字典）    |
| `["apple", "banana"]` | `list`（列表）    |
| `"hello"`             | `str`（字串）     |
| `123`                 | `int`（整數）     |
| `12.34`               | `float`（浮點數）  |
| `true`                | `True`（布林值）   |
| `false`               | `False`（布林值）  |
| `null`                | `None`（空值）    |

---

## **4. JSON 格式化輸出**

如果要讓 JSON 更易讀，可以使用 `indent` 參數：

```python
import json

data = {"name": "Alice", "age": 25, "city": "Taipei"}

print(json.dumps(data, indent=4, ensure_ascii=False))
```

輸出：

```json
{
    "name": "Alice",
    "age": 25,
    "city": "Taipei"
}
```

---

### **結論**

Python 提供 `json` 模組來處理 JSON，能夠：
✅ 解析（讀取）JSON
✅ 處理（操作）JSON
✅ 產生（寫入）JSON

這讓 Python 很容易與其他語言（如 JavaScript）或 API 進行資料交換！
