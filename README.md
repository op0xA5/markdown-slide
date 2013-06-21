markdown-slide
==============

使用markdown书写幻灯片

-------

使用方法：

1. 使用markdown编写幻灯片内容，特别的，幻灯分页使用 `--- 页号或单词 ---` 分割开，保存为document.md文件。
2. 编写css文件控制幻灯样式。
3. html页面中引入slider.js，写一段脚本：

	window.onload= function(){
		new Slider(document.body, {fullScreen:true, width:640, height:480}).show('document.md?'+new Date());
	};

4. 将幻灯片内容、样式表、以及html文件上传到服务器，打开页面即可播放幻灯片。

原理：

- markdown文本中使用左右各不少于3个 - 作为页分割，中间可以写页码或单词，播放时中间的文本作为播放容器的class，故可以通过该单词来控制每页的样式。
- 播放容器大小可以通过config中的width及height来控制，以方便控制样式，实际播放是利用CSS3的transform特性进行缩放以适应窗口大小。

-----

该代码是我在单位内部交流时临时写的，目前还在更新中。在重视内容而非华丽表现力的场合使用很方便。编写幻灯片内容很惬意，思路流畅，不受“新建幻灯片”之类操作的打断，不论调整各页内容还是纵观全局都很方便。