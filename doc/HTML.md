#### 属性类

##### 1、捕获摄像头 

```html
<input type="file" capture="user" accept="image/*" />
// user 表示前置摄像头，environment 表示后置摄像头
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input#%E5%B1%9E%E6%80%A7)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input#%E5%B1%9E%E6%80%A7)

##### 2、定时刷新网页

```html
<meta http-equiv="refresh" content="10" />
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta)

##### 3、上传文件时指定允许的文件格式

```html
 <input type="file" accept=".jpeg,.png" />
```

[[参考](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/accept)](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/accept)

##### 4、允许选择多个文件 

```html
<input type="file" multiple />
// HTMLInputElement.multiple 属性表示一个 input 是否可以有多个值。目前只有火狐支持 <input type="file">存有多个值。
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLInputElement/multiple)](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLInputElement/multiple)

##### 5、阻止浏览器翻译，适用场景比如 Logo 和品牌名 

```html
<p translate="no">Brand name</p>
// 全局属性 translate 被用来规定对应元素的属性值及其子文本节点内容，是否跟随系统语言作出对应的翻译变化。
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/translate)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes/translate)

##### 6、声明资源文件的下载

```html
 <a href="image.png" download>
// download属性是一个DOMString ，表明链接的资源将被下载，而不是显示在浏览器中。该值表示下载文件的建议名称。如果该名称不是基础操作系统的有效文件名，浏览器将对其进行调整。
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLAnchorElement/download)](https://developer.mozilla.org/zh-CN/docs/Web/API/HTMLAnchorElement/download)

##### 7、使用loading=lazy属性来延迟图像的加载，直到用户滚动到它们 

```html
<img src='image.jpg' loading='lazy' alt='Alternative Text'>
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/Performance/Lazy_loading#%E7%AD%96%E7%95%A5)](https://developer.mozilla.org/zh-CN/docs/Web/Performance/Lazy_loading#%E7%AD%96%E7%95%A5)

##### 8、创建email/电话链接

```html
<a href="mailto:{email}?subject={subject}&body={content}">
  Send us an email
</a>

<a href="tel:{phone}">
  Call us
</a>

<a href="sms:{phone}?body={content}">
  Send us a message
</a>
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a#%E5%B1%9E%E6%80%A7)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a#%E5%B1%9E%E6%80%A7)

##### 9、原生浏览器滑块

```html
<input type="range">
```

![image](https://user-images.githubusercontent.com/92159727/184313634-b0ad0184-a976-4cc1-81c8-8658e93645d4.png)

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input#%3Cinput%3E_types)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/Input#%3Cinput%3E_types)

##### 10、保持图标版本刷新

```html
<link rel="icon" href="/favicon.ico?v=2" />
// 添加?v=2保证使用者看见的是最新版本的图标
```



#### 标签类

##### \<meter>元素用来显示已知范围的标量值或者分数值。

示例：

```html
<p>
	Heat the oven to 
	<meter min="200" max="500"value="350">
		350 degrees
	</meter>
</p>
```

![image](https://user-images.githubusercontent.com/92159727/184313269-a13536d7-3d4d-4230-94a6-d03d6a8bdda5.png)
[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meter)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meter)

##### \<base>：文档根 URL 元素 HTML

```
 <base> 元素 指定用于一个文档中包含的所有相对 URL 的根 URL。一份中只能有一个 <base> 元素。 一个文档的基本 URL，可以通过使用 document.baseURI (en-US) 的 JS 脚本查询。如果文档不包含 <base> 元素，baseURI 默认为 document.location.href。
```

```html
指向文档中某个片段的链接，例如 <a href="#some-id"> 用 <base> 解析，触发对带有附加片段的基本 URL 的 HTTP 请求。

例如：给定 <base href="https://example.com">

以及此链接 <a href="#anchor">Anker</a>

链接指向 https://example.com/#anchor
```

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/base)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/base)

##### \<details>：详细信息展现元素

```
HTML <details>元素可创建一个挂件，仅在被切换成展开状态时，它才会显示内含的信息。<summary> 元素可为该部件提供概要或者标签。
```

折叠：

![image](https://user-images.githubusercontent.com/92159727/184313320-3299fd4c-1998-491b-9daf-e753d076259d.png)

展开：

![image](https://user-images.githubusercontent.com/92159727/184313348-33265ec3-9386-4f1b-adf9-acf9ed077730.png)

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/details)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/details)

##### \<mark>：高亮文本

例：

```html
<p>&lt;mark&gt; 元素用于 <mark>高亮</mark> 文本</p>
```

![image](https://user-images.githubusercontent.com/92159727/184313391-8378c58f-5a59-41a7-9578-42f0f2b21f36.png)



##### \<pre> 元素：预定义格式文本

```
HTML <pre> 元素表示预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。(紧跟在 <pre> 开始标签后的换行符也会被省略)
```

![image](https://user-images.githubusercontent.com/92159727/184313451-e03c6e63-a35e-4988-aaea-3b2478d2a96d.png)
[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre#%E5%B0%9D%E8%AF%95%E4%B8%80%E4%B8%8B)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/pre#%E5%B0%9D%E8%AF%95%E4%B8%80%E4%B8%8B)

##### \<dialog> 一个对话框或其他交互式组件，例如一个检查器或者窗口。

例：

```html
<!-- Simple modal dialog containing a form -->
<dialog id="favDialog">
  <form method="dialog">
    <p><label>Favorite animal:
      <select>
        <option value="default">Choose...</option>
        <option>Brine shrimp</option>
        <option>Red panda</option>
        <option>Spider monkey</option>
      </select>
    </label></p>
    <div>
      <button value="cancel">Cancel</button>
      <button id="confirmBtn" value="default">Confirm</button>
    </div>
  </form>
</dialog>
<p>
  <button id="updateDetails">Update details</button>
</p>
<output></output>
```

![image](https://user-images.githubusercontent.com/92159727/184313487-dc15bb44-1e4e-4971-b5e1-d19ca02d1643.png)

![image](https://user-images.githubusercontent.com/92159727/184313515-53764293-fe12-49be-8a48-c9f666cd3b21.png)

[[参考](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dialog)](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/dialog)
