##### 生成随机字符串
```js
const randomString = () => Math.random().toString(36).slice(2);
随机数=>转36进制显示(正好覆盖a-z)=>删除字段串前两个字符(0.)
```

##### 从字符串中删除 HTML
```js
此方法用于从字符串中删除 HTML 元素。
const stripHtml = html => (new DOMParser().parseFromString(html, 'text/html')).body.textContent || '';
```

##### 随机选择一种十六进制颜色
```js
此方法用于获取随机的十六进制颜色值。
const randomHex = () => `#${Math.floor(Math.random() * 0xffffff).toString(16).padEnd(6, "0")}`;
randomHex();
```

##### 将内容复制到剪贴板
```js
此方法使用 navigator.clipboard.writeText 将文本复制到剪贴板。
const copyToClipboard = (text) => navigator.clipboard.writeText(text);
copyToClipboard("Hello World");
```

##### 删除所有cookies
```js
该方法使用 document.cookie 访问 cookie 并清除网页上存储的所有 cookie。
const clearCookies = document.cookie.split(';').forEach(cookie => document.cookie = cookie.replace(/^ +/, '').replace(/=.*/, `=;expires=${new Date(0).toUTCString()};path=/`));
```

##### 检索选择的文本
```js
该方法通过内置的 getSelection 属性获取用户选择的文本。
const getSelectedText = () => window.getSelection().toString();
getSelectedText();
```

##### 判断是否处于暗模式
```js
该方法用于检测当前环境是否处于暗模式，它是一个布尔值。
const isDarkMode = window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches
console.log(isDarkMode)
```

##### 导航到页面顶部
```js
此方法用于返回页面顶部。
const goToTop = () => window.scrollTo(0, 0);
goToTop();
```

##### 确定当前选项卡是否处于活动状态
```js
此方法用于检查当前选项卡是否处于活动状态。
const isTabInView = () => !document.hidden;
```

##### 打开浏览器打印框
```js
该方法用于打开浏览器的打印框。
const showPrintDialog = () => window.print()
```

##### 千分位格式化
```js
Number.prototype.toLocaleString
例：
let num = 12323421412.3213;
num.toLocaleString();
// '12,323,421,412.321'
```

##### 解析链接参数
```js
Object.fromEntries((new URLSearchParams(location.search)).entries())
```

##### 解构数组位置
```js
const array = [1,2,3,4,5,6];
// ✅ Different ways of accessing the third position
const {3: third} = array; // third = 4
array.at(3) // 4
array[3] // 4
```

##### RegExp.prototype.exec()
```js
exec() 方法在一个指定字符串中执行一个搜索匹配。返回一个结果数组或 null。
const regex1 = RegExp('foo*', 'g');
const str1 = 'table football, foosball';
let array1;

while ((array1 = regex1.exec(str1)) !== null) {
  console.log(`Found ${array1[0]}. Next starts at ${regex1.lastIndex}.`);
  // expected output: "Found foo. Next starts at 9."
  // expected output: "Found foo. Next starts at 19."
}
```

##### Number.prototype.toString()
```js
toString() 方法返回指定 Number 对象的字符串表示形式。
进制转换
numObj.toString([radix])
radix
指定要用于数字到字符串的转换的基数 (从 2 到 36)。如果未指定 radix 参数，则默认值为 10。
```

##### js对象二层解构
```js
const { data: { taxIds, url } } = res;
```

##### 监听非标准事件，以修改localStorage为例
```js
var event = new Event('setItem'); // 新建一个事件类型为setItem的事件
const setItem = localStorage.setItem; // 重写setItem方法
localStorage.setItem = function (name, value){
  setItem.apply(this, arguments);
  event.key = name;
  event.value = value;
  window.dispatchEvent(event); // 通知浏览器这个事件触发了，此时会触发下面的addEventListener
}
// 页面使用
window.addEventListener('setItem', function (e) {             document.querySelector('.view').innerText = `${e.key}： ${e.value}`
})
```

##### 深复制webApi
```js
structuredClone() // 兼容一般
```

##### 在对象中使用运算符

```js
{
    others,
    ...(yes === 2
        ? {
            bonus,
          }
        : {
            other,
        }),
}
```

##### 对象属性跟随变量切换
{
    [item === 1 ? 'name' : 'names'] : value,
}

##### 兼容replaceAll

```js
replaceAll只兼容到谷歌85版本。
可使用replace(/str1/g, str2)代替
```
