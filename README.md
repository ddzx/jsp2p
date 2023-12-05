jsp2p为JavaScript开发,适用后h5浏览器加速m3u8影片,达到秒播和减少带宽使用的目的！

本项目参考cdnbye收费版开发，各项性能优于cdnbye,免费开源使用

采用国内大厂(斗鱼，抖音，腾讯，哔哩哔哩)开放的turn服务器桥接p2p,成功率和速度均优于使用国外服务器

魔改hls可设置视频缓存线程数(播放源速度不佳时建议不要超过3线程)
  注：修改js的maxHttpThread（默认为2线程）
  
魔改hls加入备用反代线路（默认为当前播放线路速度无法满足正常播放则会自动调用，缓存满足正常播放后则返回使用原始线路节省流量）
  注：修改js的mirrors:[{url:"",type:I.QUERY,fast:!0}]   反代格式为https://www.www.com/demo.ts?u=
  
可接入turnserver服务器，用户之前如果无法直接p2p打通则可以使用turnserver服务器进行中转互连

节点端:暂时只支持linux系统，启动后相当于万能节点，会根据设置缓存下载ts并24小时做种上传

本项目js端开源开放免费使用,代码无任何后门，免费配套wss桥接服务器，如有朋友需要定制需求欢迎联系

普通站长快速上手:
    dplayer:参考demo代码dplayer.html，并保存使用项目中的hls.js即可
    hls原生播放器:参考demo代码hls.html，并保存使用项目中的hls.js即可
