# Introduction #

一些用js编写的网页小工具。


# Details #

### 破解网页禁止复制类 ###
  * 删除网页限制（禁止右键限制，禁止右键菜单，禁止复制，禁止选择）
```
javascript:(function(){var element=document.createElement('script'); element.setAttribute('src','https://xdc.googlecode.com/files/delete-page-limit.js'); document.body.appendChild(element);})();void(0);
```
  * 破解网页禁止复制
```
javascript:alert(document.onselectstart = document.oncontextmenu= document.onmousedown = document.onkeydown= function(){return true;});
```

### 浏览器工具类 ###
  * 显示password
```
javascript:(function(){var IN,F;IN=document.getElementsByTagName(‘input’);for(var i=0;i<IN.length;i  ){F=IN[i];if(F.type.toLowerCase()==’password’){try{F.type=’text’}catch(r){var n,Fa;n=document.createElement(‘input’);Fa=F.attributes;for(var ii=0;ii<Fa.length;ii  ){var k,knn,knv;k=Fa[ii];knn=k.nodeName;knv=k.nodeValue;if(knn.toLowerCase()!=’type’){if(knn!=’height’&&knn!=’width’&!!knv)n[knn]=knv}};F.parentNode.replaceChild(n,F)}}}})()
```
  * 修改cookie
```
javascript:(function(){var name=prompt("请输入要设置的cookie","cookie");if(name!=null&&name!="cookie"){var arrCookie=name.split("; ");for(var i=0;i<arrCookie.length;i++){document.cookie=arrCookie[i];}location.replace(location.href);}})();void(0);
```

### 网页应用类 ###
  * 豆瓣FM显示歌词 ynm3000
```
javascript:(function() {if ($('div#dui-dialog-lyric').length > 0) {return;}var s=FM.getCurrentSongInfo();$.getJSON('http://dblyrics.ynm3000.com/frame/?callback=?',{},function(data){var new_e = document.createElement('div');new_e.innerHTML=data.response;$('body').append(new_e);});})();
```
  * 优酷html5播放器 zhuyi
```
javascript:(function(){var l = document.createElement('link');l.setAttribute('rel','stylesheet');l.setAttribute('media','all');l.setAttribute('href','http://zythum.sinaapp.com/youkuhtml5playerbookmark/youkuhtml5playerbookmark2.css');document.body.appendChild(l);var s = document.createElement('script');s.setAttribute('src','http://zythum.sinaapp.com/youkuhtml5playerbookmark/youkuhtml5playerbookmark2.js');document.body.appendChild(s);})();
```
  * Let it snow! by zhuyi
```
javascript:void(function(){var%20d%20=%20document,a%20=%20'setAttribute',s%20=%20d.createElement('script');s[a]('tyle','text/javascript');s[a]('src','http://zythum.free.bg/googlesnow/forg.js');d.head.appendChild(s);})();
```