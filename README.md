# 使用到的网页代码
## 配置
- 自留地利用GitHub+Vercel+Typora搭建，域名是Vercel免费提供的二级域名`http://injfnovel.now.sh/`
- 
## 首页
主题是Typora的Whitey主题，懒得改css了···
## 长文
**目前1.0实现的功能有：**
1. 章节跳转
2. 一键返回顶部
3. 没得了</br>

**以后希望做到的功能有：**
- [ ] 隐藏菜单目录
## 代码
1. 长文网页的基本框架如下：
```
<!doctype html>
<html>
<head>
<link rel="stylesheet" href="https://injfnovel.now.sh/github.css">
<meta charset='UTF-8'><meta name='viewport' content='width=device-width initial-scale=1'>
<title>遗落之墟的龙与精灵</title>
</head>
<body class='typora-export os-windows' >

<!-- 回顶部 -->
<style>
.button1 {
	font-size: 16px;
	border: 1px solid #000000; 
	border-radius: 4px;
	background-color: #ffffff;
	color: black;
}

.button1:hover {
    background-color: #000000;
    color: white;
}
</style>

<a id="mback" style="position: fixed;bottom: 10px;right: 10px;" onclick="backTop()"><button class="button button1" >▲</button></a>

<script type="text/javascript">
function backTop() {
	    scrollTo(0, 0);
	}
</script>

//章节目录和正文内容（章节目录可能需要手动添加</br>

</body>
</html>
```
