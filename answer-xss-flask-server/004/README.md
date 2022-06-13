# Answer: SQL inject

## 請先閱讀:
- 請先閱讀 [章節](https://github.com/yillkid/ntc-white-hat/blob/master/answer-xss-flask-server/003/README.md)

## 運作原理

## 解決方案

#### 基本原則:
你有非常多種作法，這邊我不會限制大家的想像，原則上：
1. 使用 ORM (Object Relational Mapping) 框架
2. 轉譯特殊字元
3. 或其他作法...

#### 轉譯引號:
- username = username.replace("'", "''")
- 上下文如下

```python3=
username = request.values["username"]
username = username.replace("'", "''")
```

#### 效果:
- 將所有的 ' 轉譯為 ''，這樣可以有助於 user 插入 SQL 語句
- Before
  - '; select true; --

- After
  - ''; select true; --
