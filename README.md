# 配置
 `沉目的自留地`利用GitHub+Vercel+Typora进行搭建，网站采用了Typora的Han主题，域名是由Vercel免费提供的`http://injfnovel.now.sh/`
 </br></br>
 
# 目前1.0实现的功能
1. 可隐藏的章节目录
2. 一键返回顶部
3. 禁止选中文字复制
4. 不同主题模式切换（已有🌜🌞🌿）
</br>

# 以后希望做到的功能有：
- [x] 隐藏菜单目录
- [x] 不同主题模式切换（可能不是很必要）（已有🌜🌞🌿）
</br>

# 代码

1. 中篇小说的网页基本框架如下：

```
<!doctype html>
<html>
<head>
<meta charset='UTF-8'>
<meta name='viewport' content='width=device-width initial-scale=1'>
<link rel="stylesheet" type="text/css" id="han" href="https://injfnovel.now.sh/css/han.css">
<title>小说名字</title><style type='text/css'>
</head>

<!-- 禁止复制 -->
<body class='typora-export os-windows' leftmargin=0 topmargin=0 oncontextmenu='return false' ondragstart='return false' onselectstart ='return false' onselect='document.selection.empty()' oncopy='document.selection.empty()' onbeforecopy='return false' onmouseup='document.selection.empty()'>

<!-- style -->
<style></style>

<p>&nbsp;</p><div id='write'  class = ''>

<!--网页提示-->
<body onload="javascript:window.alert('⚠️这是一篇不适合未成年人阅读的文章！\n您确定自己已年满十八周岁？')"></body>

<!-- 辅助功能 -->
<details><summary><strong><span>辅助功能</span></strong></summary>
	<input type="button" value="返回首页🏠" onclick="location.href='http://injfnovel.now.sh'"> | <input type="button" value="夜间模式🌜" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/css/handark.css'"> | <input type="button" value="日间模式🌞" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/css/han.css'"> | <input type="button" value="绿色模式🌿" onclick="javascript:document.getElementById('han').href='https://injfnovel.now.sh/css/hangreen.css'">
</details>

<!-- 折叠目录 -->
<details><summary><strong><span>章节目录</span></strong></summary>
	<a href="#章节标题">章节标题</a></br>
</details>


<!-- 正文部分 -->
<h2><a name="章节标题" class="md-header-anchor"></a><span>章节标题</span></h2>

<p>&nbsp;</p>



</div><footer><font size="3" color=grey><p class="copyright"><center>
	©2020 沉目. All rights reserved.</br>Powered by <a href="https://vercel.com/" target="_blank">Vercel</a> | Theme <a href="http://theme.typora.io/theme/Han/" target="_blank">Han</a> from <a href="https://typora.io/" target="_blank">Typora</a>.
	<p>&nbsp;</p>
	</center></p></font></footer>

<!-- 回到顶部 -->
<style>
.button2 {
	border: none; 
	border-radius: 8px;
	font-size: 20px;
	padding: 5px 5px;
    	text-align: center;
   	text-decoration: none;
	background-color: #f5f5f5;
	color: #000000;
}

.button2:hover {
    background-color: #000000;
    color: white;
}
</style>

<a id="mback" style="position: fixed;bottom: 10px;right: 10px;" onclick="backTop()"><button class="button2">⇪</button></a>

<script type="text/javascript">
function backTop() {
	    scrollTo(0, 0);
	}
</script>

</body>
</html>

```
