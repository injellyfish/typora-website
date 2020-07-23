# 配置
 `沉目的自留地`利用GitHub+Vercel+Typora进行搭建，网站采用了Typora的Han主题，域名是由Vercel免费提供的`http://injfnovel.now.sh/`
 </br>
 
# 目前1.0实现的功能
1. 可隐藏的章节目录
2. 一键返回顶部
</br>

# 以后希望做到的功能有：
- [x] 隐藏菜单目录
- [x] 不同主题模式切换（可能不是很必要）（已有🌜🌞🌿）
- [ ] 添加评论区/留言板（或许可以用Lof代替）
</br>

# 代码

1. 中篇小说的网页基本框架如下：

```
<!doctype html>
<html>
<head>
<meta charset='UTF-8'>
<meta name='viewport' content='width=device-width initial-scale=1'>
<link rel="stylesheet" type="text/css" id="github" href="https://injfnovel.now.sh/han.css">
<title>小说标题</title><style type='text/css'>
</head>

<!-- 返回顶部 -->
<style>
.button2 {
	border: none; 
	font-size: 10px;
    	text-align: center;
   	text-decoration: none;
	background-color: #ffffff;
	color: #000000;
}

.button2:hover {
    background-color: #ffffff;
    color: white;
}
</style>
<a id="mback" style="position: fixed;bottom: 10px;right: 10px;" onclick="backTop()"><button class="button2"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 10.828l-4.95 4.95-1.414-1.414L12 8l6.364 6.364-1.414 1.414z"/></svg></button></a>

<script type="text/javascript">
function backTop() {
	    scrollTo(0, 0);
	}
</script>

<!-- 禁止复制 -->
<body class='typora-export os-windows' leftmargin=0 topmargin=0 oncontextmenu='return false' ondragstart='return false' onselectstart ='return false' onselect='document.selection.empty()' oncopy='document.selection.empty()' onbeforecopy='return false' onmouseup='document.selection.empty()'>
<p>&nbsp;</p><div id='write'  class = ''>

<!--网页提示-->
<body onload="javascript:window.alert('⚠️这是一篇不适合未成年人阅读的文章！\n您确定自己已年满十八周岁？')"></body>

<!-- 辅助功能 -->
<details><summary><strong><span>辅助功能</span></strong></summary>
	<input type="button" value="返回首页🏠" onclick="location.href='http://injfnovel.now.sh'"> | <input type="button" value="夜间模式🌜" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/handark.css'"> | <input type="button" value="日间模式🌞" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/han.css'"> | <input type="button" value="绿色模式🌿" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/hangreen.css'">
</details>

<!-- 折叠目录 -->
<details><summary><strong><span>章节目录（点击展开）</span></strong></summary>
	<a href="#第一章">第一章</a></br>
</details>
<p><ul class="markdownIt-TOC"></p>

<!-- 正文部分【章节标题要用如下的形式】 -->
<h2><a name="章节标题" class="md-header-anchor"></a><span>章节标题</span></h2>

</div><footer><font size="3" color=grey><p class="copyright"><center>
	©2020 沉目. All rights reserved.</br>Powered by <a href="https://vercel.com/" target="_blank">Vercel</a> | Theme <a href="http://theme.typora.io/theme/Han/" target="_blank">Han</a> from <a href="https://typora.io/" target="_blank">Typora</a>.
	<p>&nbsp;</p>
	</center></p></font></footer>
</body>
</html>
```

2. 短篇小说的网页基本框架如下：
*（取消了章节目录的功能）*

```
<!doctype html>
<html>
<head>
<meta charset='UTF-8'>
<meta name='viewport' content='width=device-width initial-scale=1'>
<link rel="stylesheet" type="text/css" id="github" href="https://injfnovel.now.sh/han.css">
<title>小说标题</title><style type='text/css'>
</head>

<!-- 返回顶部 -->
<style>
.button2 {
	border: none; 
	font-size: 10px;
    	text-align: center;
   	text-decoration: none;
	background-color: #ffffff;
	color: #000000;
}

.button2:hover {
    background-color: #ffffff;
    color: white;
}
</style>
<a id="mback" style="position: fixed;bottom: 10px;right: 10px;" onclick="backTop()"><button class="button2"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 10.828l-4.95 4.95-1.414-1.414L12 8l6.364 6.364-1.414 1.414z"/></svg></button></a>

<script type="text/javascript">
function backTop() {
	    scrollTo(0, 0);
	}
</script>

<!-- 禁止复制 -->
<body class='typora-export os-windows' leftmargin=0 topmargin=0 oncontextmenu='return false' ondragstart='return false' onselectstart ='return false' onselect='document.selection.empty()' oncopy='document.selection.empty()' onbeforecopy='return false' onmouseup='document.selection.empty()'>
<p>&nbsp;</p><div id='write'  class = ''>

<!--网页提示-->
<body onload="javascript:window.alert('⚠️这是一篇不适合未成年人阅读的文章！\n您确定自己已年满十八周岁？')"></body>

<!-- 辅助功能 -->
<details><summary><strong><span>辅助功能</span></strong></summary>
	<input type="button" value="返回首页🏠" onclick="location.href='http://injfnovel.now.sh'"> | <input type="button" value="夜间模式🌜" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/handark.css'"> | <input type="button" value="日间模式🌞" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/han.css'"> | <input type="button" value="绿色模式🌿" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/hangreen.css'">
</details>

<p><ul class="markdownIt-TOC"></p>

<!-- 正文部分 -->

</div><footer><font size="3" color=grey><p class="copyright"><center>
	©2020 沉目. All rights reserved.</br>Powered by <a href="https://vercel.com/" target="_blank">Vercel</a> | Theme <a href="http://theme.typora.io/theme/Han/" target="_blank">Han</a> from <a href="https://typora.io/" target="_blank">Typora</a>.
	<p>&nbsp;</p>
	</center></p></font></footer>
</body>
</html>
```
