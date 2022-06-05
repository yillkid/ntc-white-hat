# Answer

#### 原理:
```python=
@app.route('/xss-attack-1', methods=['GET'])
def XSS_attack():
    return f'Hello {request.values["code"]}'
```
- backend 接收到 request 完全沒有做檢查，馬上 response
- 即便 request 是 jsvascript code 也一樣


#### 觸發:
- `http://127.0.0.1:5566/XSS-attack?code=<script>alert('XSS%20test')</script>`

#### 修補:
- https://pypi.org/project/MarkupSafe/

```python=
from markupsafe import escape
    return f'Hello {escape(request.values["code"])}'
```
