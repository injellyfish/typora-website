# 配置
 `沉目的自留地`利用GitHub+Vercel+Typora进行搭建，网站采用了Typora的Han主题，域名是由Vercel免费提供的`http://injfnovel.now.sh/`
 </br></br>
 
# 目前1.0实现的功能
1. 可隐藏的章节目录
2. 一键返回顶部
3. 禁止选中文字复制
4. 不同主题模式切换（已有🌜🌞🌿）
5. 网页留言板实现
</br>

# 以后希望做到的功能有：
- [x] 隐藏菜单目录
- [x] 不同主题模式切换（可能不是很必要）（已有🌜🌞🌿）
- [x] 留言板
</br>

# 代码

1. 中篇小说的网页基本框架如下：

```
<!doctype html>
<html>
<head>
<meta charset='UTF-8'>
<meta name='viewport' content='width=device-width initial-scale=1'>
<link rel="shortcut icon" href="https://i.loli.net/2020/07/24/oDBEbyOd6RIu2xT.png">
<link rel="stylesheet" type="text/css" id="han" href="https://injfn.now.sh/css/han.css">
<title>遗落之墟的龙与精灵</title><style type='text/css'>
</head>

<!-- style -->
<style></style>

<p>&nbsp;</p><div id='write'  class = ''>	
	
<!-- 禁止复制 -->
<body class='typora-export os-windows' leftmargin=0 topmargin=0 oncontextmenu='return false' ondragstart='return false' onselectstart ='return false' onselect='document.selection.empty()' oncopy='document.selection.empty()' onbeforecopy='return false' onmouseup='document.selection.empty()'>

<!--网页提示-->
<body onload="javascript:window.alert('⚠️这是一篇不适合未成年人阅读的文章！\n您确定自己已年满十八周岁？')"></body>

<!-- 辅助功能 -->
<details><summary style="cursor:pointer">辅助功能</summary>
	<input type="button" value="返回首页🏠" onclick="location.href='https://injfn.now.sh/'" style="cursor:pointer">&nbsp;<input type="button" value="留言评论💬" onclick="location.href='https://injfn.now.sh/comments/isolde.html'" style="cursor:pointer">&nbsp;<input type="button" value="夜间模式🌜" onclick="javascript:document.getElementById('han').href='https://injfn.now.sh/css/handark.css'" style="cursor:pointer">&nbsp;<input type="button" value="日间模式🌞" onclick="javascript:document.getElementById('han').href='https://injfn.now.sh/css/han.css'" style="cursor:pointer">&nbsp;<input type="button" value="绿色模式🌿" onclick="javascript:document.getElementById('han').href='https://injfn.now.sh/css/hangreen.css'" style="cursor:pointer">
</details>

<!-- 折叠目录 -->
<details><summary style="cursor:pointer">章节目录</summary>
	<a href="#第一章">第一章</a></br>
</details>


<!-- 正文部分 -->
<h2><a name="第一章" class="md-header-anchor"></a><span>第一章</span></h2>

<p>&nbsp;</p>



</div><footer><font size="3" color=grey><center>
	©2020 沉目. All rights reserved.</br>Powered by <a href="https://vercel.com/" target="_blank">Vercel</a> | Theme <a href="http://theme.typora.io/theme/Han/" target="_blank">Han</a> from <a href="https://typora.io/" target="_blank">Typora</a>.
	<p>&nbsp;</p>
	</center></font></footer>

<!-- 回到顶部 -->
<style>
.button2 {
	background-color: transparent;
	cursor:pointer; 
}
</style>

<a id="mback" style="position: fixed;bottom: 10px;right: 10px;" onclick="backTop()"><button class="button2"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M13 7.828V20h-2V7.828l-5.364 5.364-1.414-1.414L12 4l7.778 7.778-1.414 1.414L13 7.828z"/></svg></a>

<script type="text/javascript">
function backTop() {
	    scrollTo(0, 0);
	}
</script>

</body>
</html>

```
