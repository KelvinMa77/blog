# canvas

## 创建

html

```html
<canvas id="..."></canvas>
```

js

```js
var canvas = document.getElementById('...')
var ctx = canvas.getContext('2d')
```

以上，就创建一个2d 画布

## 基本方法

```js
ctx.beginPath() // 新建路径
ctx.moveTo(x, y) // 将画笔移动到某一位置
ctx.closePath() // 闭合路径
ctx.stroke() // 通过线条绘制轮廓
ctx.fill() // 填充路径的内容，如果路径没有闭合，那fill方法会自动闭合路径
ctx.fillRect(x, y, width, height) // 绘制一个实心的矩形
ctx.strokeRect(x, y, width, height) // 绘制一个空心的矩形
ctx.clearRect(x, y, width, height) // 清除指定区域的矩形
ctx.arc(x, y, r, startAngle, endAngle, anticlockwise)
// 以 x, y 为圆心，r为半径，从 startAngle（弧度） 到 endAngle（弧度） ，anticlockwise是时针方向，默认是false; true为逆时针，false为顺时针
// 0弧度是指 x轴正向
// 弧度是指 radius = (Math.PI/180)*degrees
ctx.arcTo(x1, y1, x2, y2, r)
// 参数1、2：控制点1坐标   参数3、4：控制点2坐标  参数4：圆弧半径
```

