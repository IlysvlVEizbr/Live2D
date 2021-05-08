# Live2D
&emsp;&emsp;为安卓端Chrome内核浏览器适配的Live2D看板娘插件，可应用于[via](https://viayoo.com/zh-cn/)等可调用js插件或编辑首页Html的浏览器。
- 源码基于 [live2d_demo / ©fghrsh / GPL v2.0](https://github.com/fghrsh/live2d_demo) 修改
- 所有资源和库文件封装到一个js，牺牲了部分定制性，换取更快的加载速度以及更稳定的体验。

*<p align="right">Customized by Sky.</p>*

------------

# 使用说明——以via浏览器为例
## 输入脚本代码：
```javascript
/*
 * @name: 看板娘
 * @Author: Sky
 * @version: 1.9
 * @description: 愿你每天好心情
 * @include: *
 * @createTime: 2020-5-9 21:00
 * @updateTime: 2021-4-2 0:30
 */
(function(){const w = window,
/*以下参数可修改，=null表示恢复默认值*/
onlyWifi=true; /*仅在Wifi环境运行*/
w.kbn_setting0=6; /*人物ID*/
w.kbn_setting1=19; /*衣服ID*/
w.kbn_setting2=true; /*是否显示关闭按钮*/
w.kbn_setting3='180x170'; /*看板娘大小*/
w.kbn_setting4='right:10'; /*停靠侧:到侧边距离*/
w.kbn_setting5='160x50'; /*提示框大小*/
w.kbn_setting6='14px'; /*提示框字体大小*/
w.kbn_setting7='-13px'; /*提示框Y轴偏移*/
w.kbn_setting8='18px'; /*工具栏图标大小*/
w.kbn_setting9='36px'; /*工具栏行高*/
w.kbn_setting10=null; /*一言API可选'fghrsh.net', 'hitokoto.cn', 'jinrishici.com'(古诗词)*/
/*－－－－以下勿改－－－－*/
const key=encodeURIComponent('看板娘:执行判断');if(w[key]||(onlyWifi&&navigator.connection.type!='wifi')){return;}try{w[key]=true;const lib=document.createElement('script');lib.src='https://cdn.jsdelivr.net/gh/IlysvlVEizbr/Live2D@1.9/kbn.js';lib.defer=true;document.body.append(lib);}catch(err){console.log('看板娘：',err);}})();
```
## 脚本作用：
&emsp;&emsp;纯粹娱乐向的一个脚本——在您浏览的网页添加一个**看板娘**~ 为您的浏览体验增加一分乐趣！（现在，您可以在脚本代码中的指定区域对个性化参数进行修改！）
## 何时作用：
&emsp;&emsp;由于看板娘的维持和背后的库文件都需要不少流量，因此设定为仅在使用wifi时生效，应当注意某些网页（比如百度系网站）禁用了跨域资源调用，因此在这些网站上可能不生效或功能异常。
## 测试链接：
[点击进入测试页面](https://m.bilibili.com/bangumi/play/ss530)
- 跨域调用资源速度较慢，请耐心等待，安装完脚本最好先刷新一遍。
## 使用效果：
<img src="https://i.loli.net/2020/05/09/9eCqx7MHbohdfJ8.jpg"  alt="使用效果" height="600"></img>
## 更多玩法：
&emsp;&emsp;您可以在 via设置-定制-Logo-Html代码 中，填入<br>
`<script src="https://cdn.jsdelivr.net/gh/IlysvlVEizbr/Live2D@1.9/kbn.js" defer></script>`<br>
然后，看板娘就能在via首页中陪伴您了~（或者可以把整段脚本代码复制到`<script> </script>`之间填入，这样既可以对参数进行个性化定制，又能使之仅在使用wifi时生效以节省流量）  <br>
<img src="https://i.loli.net/2020/05/10/FWcanCAZbRE2kjd.jpg"  alt="首页看板娘" height="600"></img>
## 可能存在的BUG：
&emsp;&emsp;点击"关闭看板娘"按钮后，可能会导致**浏览器卡死**！暂时未探明原因，若遇到该问题建议通过删除脚本并刷新的方式关闭。
## 免责声明：
- 此插件仅适用于个人技术研究学习，请勿商用。
- 出现任何法律纠纷，与作者无关。
