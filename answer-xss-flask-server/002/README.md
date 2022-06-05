# Answer

#### 原理:
- HTTP get parameter 完全沒有校對
- 即便 parameter 是相對位置也一樣


#### 觸發:
- `http://127.0.0.1:5566/inject?path=../secret/config`

#### 修補:
```path=
if (".." in path):
    return "invalid path"
```
