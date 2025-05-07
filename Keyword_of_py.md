# Python 的關鍵字(Keyword)

---

## **0. 前言**
Python 是一種易學易用的程式語言，其關鍵字(Keyword)非常多，本文將介紹 Python 的關鍵字，並且以範例的方式展示其用法。

這些關鍵字構成了Python語言的基礎結構，每個都有特定的語法用途，**不能用作變量名或其他標識符**。
它們涵蓋了 Python 的核心功能，掌握它們可以讓你寫出更靈活、高效的代碼！ 🚀

---

## **1. 值常量 (Value constants)**
這些關鍵字代表 Python 中的固定值，通常用於布林判斷或表示空值。

### **(1) `False`**
- **語法**: `False`
- **功能**: 布林值的「假」，用於條件判斷或邏輯運算。
- **範例**:
  ```python
  x = False
  if x:
      print("True")
  else:
      print("False")  # 輸出：False
  ```

### **(2) `True`**
- **語法**: `True`
- **功能**: 布林值的「真」，與 `False` 相對。
- **範例**:
  ```python
  is_active = True
  if is_active:
      print("系統啟用")  # 輸出：系統啟用
  ```

### **(3) `None`**
- **語法**: `None`
- **功能**: 表示「空值」或「無值」，類似於其他語言的 `null` 或 `nil`。
- **範例**:
  ```python
  result = None
  if result is None:
      print("沒有結果")  # 輸出：沒有結果
  ```

---

## **2. 運算符 (Operators)**
這些關鍵字用於邏輯運算、成員檢查或身份比較。

### **(1) `and`**
- **語法**: `x and y`
- **功能**: 邏輯「與」運算，如果 `x` 和 `y` 都為 `True`，則返回 `True`，否則返回 `False`（短路運算：如果 `x` 為 `False`，就不會檢查 `y`）。
- **範例**:
  ```python
  x = True
  y = False
  print(x and y)  # 輸出：False
  ```

### **(2) `or`**
- **語法**: `x or y`
- **功能**: 邏輯「或」運算，如果 `x` 或 `y` 任一為 `True`，則返回 `True`（短路運算：如果 `x` 為 `True`，就不會檢查 `y`）。
- **範例**:
  ```python
  x = False
  y = True
  print(x or y)  # 輸出：True
  ```

### **(3) `not`**
- **語法**: `not x`
- **功能**: 邏輯「非」運算，反轉布林值（`True` 變 `False`，`False` 變 `True`）。
- **範例**:
  ```python
  x = True
  print(not x)  # 輸出：False
  ```

### **(4) `is`**
- **語法**: `x is y`
- **功能**: 檢查 `x` 和 `y` 是否是 **同一個對象**（記憶體位置相同），通常用於 `None` 比較。
- **範例**:
  ```python
  a = [1, 2, 3]
  b = a  # b 和 a 指向同一個列表
  print(a is b)  # 輸出：True

  c = [1, 2, 3]  # 新創建的列表，記憶體位置不同
  print(a is c)  # 輸出：False
  ```

### **(5) `in`**
- **語法**: `x in y`
- **功能**: 檢查 `x` 是否是 `y` 的成員（適用於 `list`、`tuple`、`dict`、`str` 等可迭代對象）。
- **範例**:
  ```python
  numbers = [1, 2, 3]
  print(2 in numbers)  # 輸出：True
  print(5 in numbers)  # 輸出：False

  word = "hello"
  print("h" in word)  # 輸出：True
  ```

---

## **3. 控制流程 (Control flow)**
這些關鍵字用於控制程式的執行順序，包括條件判斷、循環和流程跳轉。

### **(1) `if`**
- **語法**:  
  ```python
  if 條件:
      # 條件成立時執行的程式碼
  ```
- **功能**: 如果條件為 `True`，則執行對應的程式碼區塊。
- **範例**:
  ```python
  age = 18
  if age >= 18:
      print("已成年")  # 輸出：已成年
  ```

### **(2) `elif`**
- **語法**:  
  ```python
  if 條件1:
      # 條件1成立時執行
  elif 條件2:
      # 條件2成立時執行
  ```
- **功能**: 當前面的 `if` 或 `elif` 條件不成立時，檢查 `elif` 的條件（可有多個 `elif`）。
- **範例**:
  ```python
  score = 85
  if score >= 90:
      print("A")
  elif score >= 80:
      print("B")  # 輸出：B
  elif score >= 70:
      print("C")
  ```

### **(3) `else`**
- **語法**:  
  ```python
  if 條件:
      # 條件成立時執行
  else:
      # 條件不成立時執行
  ```
- **功能**: 當 `if` 或 `elif` 的所有條件都不成立時，執行 `else` 區塊（只能有一個 `else`）。
- **範例**:
  ```python
  age = 15
  if age >= 18:
      print("已成年")
  else:
      print("未成年")  # 輸出：未成年
  ```

### **(4) `for`**
- **語法**:  
  ```python
  for 變數 in 可迭代對象:
      # 循環執行的程式碼
  ```
- **功能**: 遍歷可迭代對象（如 `list`、`tuple`、`str`、`dict` 等），每次迭代將元素賦值給變數。
- **範例**:
  ```python
  fruits = ["apple", "banana", "cherry"]
  for fruit in fruits:
      print(fruit)
  # 輸出：
  # apple
  # banana
  # cherry
  ```

### **(5) `while`**
- **語法**:  
  ```python
  while 條件:
      # 條件成立時重複執行
  ```
- **功能**: 只要條件為 `True`，就重複執行區塊內的程式碼（需注意避免無限循環）。
- **範例**:
  ```python
  count = 0
  while count < 3:
      print(count)
      count += 1
  # 輸出：
  # 0
  # 1
  # 2
  ```

### **(6) `break`**
- **語法**:  
  ```python
  break
  ```
- **功能**: 強制退出當前所在的 `for` 或 `while` 循環，不再執行後續迭代。
- **範例**:
  ```python
  for num in [1, 2, 3, 4, 5]:
      if num == 3:
          break  # 當 num=3 時終止循環
      print(num)
  # 輸出：
  # 1
  # 2
  ```

### **(7) `continue`**
- **語法**:  
  ```python
  continue
  ```
- **功能**: 跳過當前迭代，直接進入下一次循環（`for` 或 `while`）。
- **範例**:
  ```python
  for num in [1, 2, 3, 4, 5]:
      if num == 3:
          continue  # 跳過 3，繼續下一輪
      print(num)
  # 輸出：
  # 1
  # 2
  # 4
  # 5
  ```

### **(8) `pass`**
- **語法**:  
  ```python
  pass
  ```
- **功能**: 空操作，什麼也不做，常用於佔位（避免語法錯誤）。
- **範例**:
  ```python
  if x > 10:
      pass  # 暫時不做任何事，但程式不會報錯
  else:
      print("x <= 10")
  ```

---

## **4. 函數與類 (Functions & Classes)**
這些關鍵字用於定義函數、類別以及控制返回值。

### **(1) `def`**
- **語法**:  
  ```python
  def 函數名稱(參數):
      # 函數內容
  ```
- **功能**: 定義一個函數。
- **範例**:
  ```python
  def greet(name):
      print(f"Hello, {name}!")
  
  greet("Alice")  # 輸出：Hello, Alice!
  ```

### **(2) `return`**
- **語法**:  
  ```python
  return [表達式]  # 可選，不寫則返回 None
  ```
- **功能**: 從函數中返回值，並結束函數執行。
- **範例**:
  ```python
  def add(a, b):
      return a + b
  
  result = add(3, 5)  # result = 8
  ```

### **(3) `lambda`**
- **語法**:  
  ```python
  lambda 參數: 表達式
  ```
- **功能**: 創建匿名函數（一次性小函數）。
- **範例**:
  ```python
  square = lambda x: x ** 2
  print(square(4))  # 輸出：16
  ```

### **(4) `class`**
- **語法**:  
  ```python
  class 類別名稱:
      # 類別內容
  ```
- **功能**: 定義一個類別（面向對象編程的基礎）。
- **範例**:
  ```python
  class Dog:
      def __init__(self, name):
          self.name = name
      
      def bark(self):
          print("Woof!")
  
  my_dog = Dog("Buddy")
  my_dog.bark()  # 輸出：Woof!
  ```

---

## **5. 異常處理 (Exceptions)**
這些關鍵字用於處理程式運行時的錯誤或異常情況。

### **(1) `try` / `except`**
- **語法**:  
  ```python
  try:
      # 可能引發異常的代碼
  except 異常類型 [as 變數]:
      # 異常處理代碼
  ```
- **功能**: 嘗試執行代碼，捕獲並處理異常。
- **範例**:
  ```python
  try:
      result = 10 / 0
  except ZeroDivisionError:
      print("不能除以零！")  # 輸出：不能除以零！
  ```

### **(2) `raise`**
- **語法**:  
  ```python
  raise [異常類型(錯誤訊息)]
  ```
- **功能**: 主動引發異常（手動觸發錯誤）。
- **範例**:
  ```python
  if age < 0:
      raise ValueError("年齡不能為負數！")
  ```

### **(3) `finally`**
- **語法**:  
  ```python
  try:
      # 嘗試執行的代碼
  finally:
      # 無論是否發生異常都會執行的代碼
  ```
- **功能**: 確保代碼塊一定會執行（常用於資源清理）。
- **範例**:
  ```python
  try:
      file = open("test.txt", "r")
      print(file.read())
  finally:
      file.close()  # 確保文件一定會關閉
  ```

### **(4) `assert`**
- **語法**:  
  ```python
  assert 條件 [, 錯誤訊息]
  ```
- **功能**: 斷言條件為 `True`，否則引發 `AssertionError`（常用於調試）。
- **範例**:
  ```python
  x = 5
  assert x > 0, "x 必須是正數"  # 條件成立，無錯誤
  assert x == 0, "x 必須等於 0"  # 引發 AssertionError
  ```

---

## **6. 上下文管理 (Context managers)**
這個關鍵字用於管理資源（如文件、數據庫連接）的生命週期，確保資源正確釋放。

### **(1) `with`**
- **語法**:  
  ```python
  with 上下文管理器 as 變數:
      # 代碼塊
  ```
- **功能**: 自動管理資源的取得和釋放（例如自動關閉文件）。
- **範例**:
  ```python
  with open("test.txt", "r") as file:
      print(file.read())  # 文件會在代碼塊結束後自動關閉
  ```

---

## **7. 變量作用域 (Variable scope)**
這些關鍵字用於控制變量的作用範圍（全局、局部或嵌套函數中的變量）。

### **(1) `global`**
- **語法**:  
  ```python
  global 變量名
  ```
- **功能**: 在函數內部聲明一個變量為 **全局變量**（避免創建局部變量）。
- **範例**:
  ```python
  x = 10  # 全局變量

  def modify():
      global x
      x = 20  # 修改全局變量 x

  modify()
  print(x)  # 輸出：20
  ```

### **(2) `nonlocal`**
- **語法**:  
  ```python
  nonlocal 變量名
  ```
- **功能**: 在嵌套函數中聲明一個變量為 **非局部變量**（修改閉包作用域中的變量，非全局）。
- **範例**:
  ```python
  def outer():
      x = 10
      def inner():
          nonlocal x  # 引用 outer 函數中的 x
          x = 20
      inner()
      print(x)  # 輸出：20（outer 的 x 被修改）

  outer()
  ```

---

## **8. 導入模組 (Importing)**
這些關鍵字用於導入其他模組或庫中的代碼。

### **(1) `import`**
- **語法**:  
  ```python
  import 模組名 [as 別名]
  ```
- **功能**: 導入整個模組，並可選用別名簡化引用。
- **範例**:
  ```python
  import math
  print(math.sqrt(16))  # 輸出：4.0

  import numpy as np  # 使用別名
  ```

### **(2) `from`**
- **語法**:  
  ```python
  from 模組名 import 名稱 [as 別名]
  ```
- **功能**: 從模組中導入特定函數、類或變量（避免寫完整模組名）。
- **範例**:
  ```python
  from math import sqrt, pi
  print(sqrt(9))  # 輸出：3.0
  print(pi)       # 輸出：3.141592653589793
  ```

### **(3) `as`**
- **語法**:  
  ```python
  import 模組名 as 別名
  或
  from 模組名 import 名稱 as 別名
  ```
- **功能**: 為導入的模組或名稱指定別名（簡化代碼或避免命名衝突）。
- **範例**:
  ```python
  from datetime import datetime as dt
  print(dt.now())  # 輸出當前時間
  ```

---

## **9. 異步編程 (Async programming)**
這些關鍵字用於編寫非同步（協程）代碼，提高 I/O 密集型任務的效率。

### **(1) `async`**
- **語法**:  
  ```python
  async def 函數名():
      # 異步函數內容
  ```
- **功能**: 定義一個 **協程函數**（coroutine），該函數可被 `await` 調用。
- **範例**:
  ```python
  async def fetch_data():
      print("開始獲取數據")
      await asyncio.sleep(2)  # 模擬 I/O 操作
      print("數據獲取完成")

  # 需在事件循環中運行：asyncio.run(fetch_data())
  ```

### **(2) `await`**
- **語法**:  
  ```python
  await 協程或異步操作
  ```
- **功能**: 暫停當前協程，等待異步操作完成（只能在 `async def` 函數中使用）。
- **範例**:
  ```python
  async def main():
      await fetch_data()  # 等待 fetch_data() 完成
      print("所有任務完成")
  ```

---

## **10. 其他 (Others)**
這些關鍵字不屬於上述分類，但有獨特用途。

### **(1) `del`**
- **語法**:  
  ```python
  del 變量名
  或
  del 列表[索引]
  ```
- **功能**: 刪除變量、列表元素或對象屬性（釋放資源）。
- **範例**:
  ```python
  x = 10
  del x  # 刪除變量 x
  # print(x)  # 會報錯：NameError

  nums = [1, 2, 3]
  del nums[1]  # 刪除索引 1 的元素
  print(nums)  # 輸出：[1, 3]
  ```

### **(2) `yield`**
- **語法**:  
  ```python
  yield 值
  ```
- **功能**: 在生成器函數中返回一個值，並暫停函數執行（下次從暫停處繼續）。
- **範例**:
  ```python
  def count_up_to(n):
      i = 1
      while i <= n:
          yield i  # 每次迭代返回 i，並暫停
          i += 1

  for num in count_up_to(3):
      print(num)  # 輸出：1, 2, 3
  ```

---

## **總結**

### 1. 值常量(Value constants)
- `False` - 布林值的假值
- `True` - 布林值的真值
- `None` - 表示空值或無值的特殊常數

### 2. 運算符(Operators)
- `and` - 邏輯與運算
- `or` - 邏輯或運算
- `not` - 邏輯非運算
- `is` - 身份運算(檢查是否為同一對象)
- `in` - 成員運算(檢查是否包含在序列中)

### 3. 控制流程(Control flow)
- `if` - 條件語句開始
- `elif` - 前一個條件不滿足時檢查的條件
- `else` - 所有條件不滿足時執行的代碼
- `for` - 迭代循環
- `while` - 條件循環
- `break` - 跳出循環
- `continue` - 跳過當前循環迭代
- `pass` - 空操作，什麼也不做(佔位符)

### 4. 函數與類(Functions & Classes)
- `def` - 定義函數
- `return` - 從函數返回值
- `lambda` - 創建匿名函數
- `class` - 定義類

### 5. 異常處理(Exceptions)
- `try` - 嘗試執行可能引發異常的代碼塊
- `except` - 捕獲並處理異常
- `raise` - 引發異常
- `finally` - 無論是否發生異常都會執行的代碼塊
- `assert` - 斷言，用於調試

### 6. 上下文管理(Context managers)
- `with` - 上下文管理器，用於資源管理

### 7. 變量作用域(Variable scope)
- `global` - 聲明全局變量
- `nonlocal` - 聲明非局部變量(用於嵌套函數)

### 8. 導入模組(Importing)
- `import` - 導入模組
- `from` - 與import一起使用，從模組導入特定內容
- `as` - 與import一起使用，為導入的模組或變量創建別名

### 9. 異步編程(Async programming)
- `async` - 定義異步函數
- `await` - 等待異步函數執行完成

### 10. 其他(Others)
- `del` - 刪除變量或對象屬性
- `yield` - 從生成器函數返回值(用於創建迭代器)
