# 使用
点击左上角的 Fork，加入到你的仓库中~然后改名字。
## 文章列表
建议在`index.html`里使用以下格式列出文章列表：
```html
<!-- 在href的双引号里添加“/文件夹名称/名称.html” -->
<li><a href="">文章名称</a></li>

<!-- 如果您希望在新标签页打开文章 -->
<li><a href="" target="_blank">文章名称</a></li>
```
## 文章模板
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width, minimal-ui">
  
<!-- 这里是您网页的css样式 -->
<link rel="stylesheet" id="typo-font" href="/css/typo-font.css"/>
	
<!-- 这里是网页图标，在href的双引号里添加图片的url地址即可使用（默认不显示，如需显示请去掉这一行
<link rel="shortcut icon" href="">
如需显示，这一行也请去掉-->
	
<!-- 您可以在这里设置是否调用Boxicons CSS（默认不调用，如需使用请去掉这一行
<link href='https://cdn.jsdelivr.net/npm/boxicons@2.0.5/css/boxicons.min.css' rel='stylesheet'>
如需使用，这一行也请去掉-->

<!-- 这里是您的网页显示标题，请自己修改名称（将“标题”替换为其他名称）👈 -->
<title>标题</title>
</head>
<body>
<a href="\">返回首页</a>
	<p><br></p>
  
<!-- 在这里粘贴您的文章的HTML格式👋 -->
  
</body>
</html>
```
