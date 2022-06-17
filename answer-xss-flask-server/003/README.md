# Answer: SQL inject

## 原理:
- HTTP get parameter 完全沒有校對
- 因此, 可透過在 http parameter 中注入 SQL 語法來偽造 true 的 response

## 重製 - 觸發 response true:

#### 注入語法:
- '; select true; --

#### Flask 後端會收到:
- select admin from users where username = ''; select true; --'

#### 注入語法解析:
- ;
  - 中止查詢 
  - 透過中止查詢的 ; 記號
  - 結束 select admin from users where username = ''; 這段表示式
- select true;
  - 直接在第二個表示式上加入新的規則
  - 亦即： select true;
  - 代表始終返回 True
- `--`
  - 註釋符號
  - 代表之後所有的內容全部註釋

## 觸發:
- http://127.0.0.1:5566/is_admin?username='; select true; --
