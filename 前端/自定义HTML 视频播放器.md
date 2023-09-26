## 自定义HTML5 播放器控件

为什么要自定义HTML5 播放器？





videojs官网：videojs.com

中文文档：https://gitcode.gitcode.host/docs-cn/video.js-docs-cn/index.html

### Video.js 

#### 简介

Video.js 是一个围绕原生视频元素的可扩展框架/库

- 提供插件 API，以便将不同类型的视频传递给原生视频元素（例如HLS、HTML5 视频等）
- video.js 支持降级成 flash 播放
- 跨浏览器统一原生视频 API（如有必要，对功能进行 polyfill 支持）
- 提供可扩展和可主题化的 UI
- 兼容移动端和PC端
- video.js 通过插件的方式支持播放 HLS、DASH、360 视角、直播以及全景
- 其他特性：全屏、字幕、第三方播放器的支持（TouTube、QuickTime）



#### 安装

加载 Video 的方法：

1、CDN直接引入

~~~html
<link href="//vjs.zencdn.net/7.10.2/video-js.min.css" rel="stylesheet">
<script src="//vjs.zencdn.net/7.10.2/video.min.js"></script>
~~~

2、NPM 安装

~~~shell
npm install --save-dev video.js
~~~

> 注意
>
> 较早版本的 Video.js (6或更早版本)中，在 vjs.zencdn.net CDN 托管版本中，包含一个Google Analytics pixel收集用户信息分析。想要禁用分析，可以包含下面脚本
>
> `<script>window.HELP_IMPROVE_VIDEOJS = false;</script>`
>
> 或者，您可以通过从 npm 获取 Video.js，从 GitHub 发布版本下载，或者通过 unpkg 或另一个 JavaScript CDN (如 CDNjs)包含 Video.js。这些版本根本不包括谷歌分析跟踪



#### 快速使用

**自动设置**

加载完成 Video.js 后，就可以初始化播放器，初始化有两种方法

直接在video的HTML标签中初始化，默认情况下，当你的网页完成加载，Video.js 将扫描具有该`data-setup`属性的媒体元素。该`data-setup`属性用于将选项传递给 Video.js

~~~html
<video
    id="my-player"
    class="video-js"
    controls
    preload="auto"
    poster="//vjs.zencdn.net/v/oceans.png"
    data-setup='{}'>
  <source src="//vjs.zencdn.net/v/oceans.mp4" type="video/mp4"></source>
  <source src="//vjs.zencdn.net/v/oceans.webm" type="video/webm"></source>
  <source src="//vjs.zencdn.net/v/oceans.ogv" type="video/ogg"></source>
  <p class="vjs-no-js">
    To view this video please enable JavaScript, and consider upgrading to a
    web browser that
    <a href="https://videojs.com/html5-video-support/" target="_blank">
      supports HTML5 video
    </a>
  </p>
</video>
~~~

> 注意：必须在数据设置中使用单引号，因为预计它将包含 JSON

**手动设置**

如果不想自动启动播放器，可以移除video标签上的data-setup属性，然后使用js代码启动。

~~~html
<video id="my-player" class="video-js">
	<source src="//vjs.zencdn.net/v/oceans.mp4" type="video/mp4">
	<source src="//vjs.zencdn.net/v/oceans.webm" type="video/webm">
</video>
~~~

~~~js
let options = {};

let player = videojs('my-player', options, function onPlayerReady() {
  	videojs.log('播放器准备好了!');

  // In this context, `this` is the player that was created by Video.js.
  	this.play();

  	this.on('ended', function() {
    	videojs.log('播放结束!');
  	});
});
~~~



有三种方法向 Video.js 传递 option，

因为 Video.js 装饰了一个 HTML5 < video > 元素，所以许多可用的选项当作属性一样

~~~html
<video id="my-player" class="video-js" controls autoplay>
~~~

用 data-setup 属性将选项作为 JSON 传递。这也是为 < video > 元素设置非标准选项的方法:

~~~html
<video data-setup='{"controls": true, "autoplay": false, "preload": "auto"}'...>
~~~

如果没有使用 data-setup 属性来触发播放器设置，那么可以将播放器选项的options对象作为第二个参数传递给 video js 函数

注意: 不要同时使用`data-setup`和`options`。

~~~js
videojs('my-player', {
  	controls: true,
  	autoplay: false,
	preload: 'auto'
});
~~~



三种异步调用的方法

第一种：将回调函数作为第三个参数传递给`videojs()`函数，

~~~js
videojs('my-player', null, function() {
  this.addClass('my-example');
});
~~~

第二种：

~~~js
var player = videojs('my-player');

player.ready(function() {
  this.addClass('my-example');
});
~~~

第三种

~~~js
var player = videojs('my-player');

player.on('ready', function() {
  this.addClass('my-example');
});
~~~



#### 配置

初始化播放器的时候，video标签的data-setup属性和videojs函数的第二个参数，都可以传一个对象, 用来初始化播放器的一些配置信息

##### 常用基础配置

###### autoplay（自动播放）

> 注意：
> 1、自动播放属性和选项并不能保证视频会自动播放，浏览器对自动播放的支持不同，永远不要假设自动播放会起作用
> 2、如果在video标签上设置了autoplay，options上的设置就会失效
> 3、通过该player.play()方法进行程序化自动播放，避免使用autoplay属性/选项
>
> 4、使用`muted`属性/选项将提高自动播放成功的机会

~~~js
// type：string|boolean
autoplay:false|true|muted|play|any
~~~

- true:：开启自动播放
- false：关闭自动播放
- muted：将会把播放器设置成静音，然后调用play() 实现自动播放
- play：将会调用play()实现自动播放。
- any：将会调用play实现自动播放，如果不能播放，则会把播放器设置成静音状态，再调用play()

> CND方式引入无论设置什么值都不能实现自动播放，使用npm包引入video.js，设置autoplay为’muted’或者’any’可以实现自动播放。

###### controls（显示控件）

~~~js
controls:true | false
~~~

###### height（高度）/ width（宽度）

设置播放器的高度和宽度，单位是px。

~~~js
// string|munber
height: "900",
width: "1600"
~~~

###### loop（循环播放）

~~~js
// type: boolean
loop: true
~~~

###### muted（静音）

~~~js
// type: boolean
muted: true
~~~

###### poster

视频播放前显示的图片

~~~js
// type:string
poster: "https://vjs.zencdn.net/v/oceans.png"
~~~

###### preload（预加载）

向浏览器建议是否应该在 <video> 元素加载后立即开始下载视频数据

~~~js
// type: string
preloas: "auto"
~~~

- auto：立即开始加载视频（如果浏览器支持的话）一些移动设备不会预先加载视频，以保护其用户的带宽 / 数据使用。（推荐）
- metadata：只加载视频的元数据，其中包括视频的持续时间和尺寸等信息。有时，元数据将通过下载几帧视频来加载
- none：不要预装任何数据。浏览器将等待，直到用户点击“播放”开始下载

###### src（视频源地址）

要嵌入的视频源的源 URL

~~~js
// type:string
src: "https://vjs.zencdn.net/v/oceans.mp4"
~~~



##### Specific Options

除非另有说明，否则默认情况下每个选项都是未定义的

###### aspectRatio（宽高比）

设置aspectRatio后，播放器大小将不再是固定的值，播放器大小会根据aspectRatio的值动态计算得到。aspectRatio的值为一个比例，如4:3或者16:9

你也可以通过给video设置特定的class，如vjs-16-9, vjs-9-16, vjs-4-3，vjs-1-1来实现同样的效果。

设置了aspectRatio后，设置width和height就不起作用了

~~~js
// type:string
aspectRatio: "4:3"
~~~

###### audioOnlyMode（音频模式）

设置位`true`，隐藏跟视频有关的组件

~~~js
// type: boolean
audioOnlyMode: true
~~~

###### audioPosterMode

设置为`true`，会一直持续显示poster图像

~~~js
// type: boolean
audioPosterMode: true
~~~

###### autoSetup

是否允许使用video的data-setup属性启动播放器

这必须在加载 videojs 时使用 videojs.options.autoSetup = false 全局设置才能生效。

~~~js
// 加载video前设置
videojs.options.autoSetup = false
~~~

###### breakpoints

响应式设备时，通过设置breakpoints，实现播放器使用那个class，根据播放器的大小调整ui样式