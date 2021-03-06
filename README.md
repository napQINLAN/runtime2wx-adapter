# Cocos Runtime JavaScript API for WX

Cocos Runtime 为基于 JavaScript 虚拟机的脚本运行环境，为了方便适配微信平台的游戏在 Runtime 上运行，这里提供了一些游戏常用的微信标准的 JavaScript API，这类 API 在 Runtime 上的使用方式和微信环境中保持一致。主要有：

- wx.createInnerAudioContext()

##  InnerAudioContext APIs

Runtime 的音频接口是 AudioEngine，与微信的 InnerAudioContext 音频接口不一样，在此通过 Adapter 的方式模拟实现了 InnerAudioContext API 以方便微信游戏适配，具体实现详见 runtime2wx-adapter 的 adapter 目录，微信官方API请查看 [InnerAudioContext API 参考文档](https://developers.weixin.qq.com/minigame/dev/api/media/audio/InnerAudioContext.html)。


### 不支持的API
- number startTime
- boolean obeyMuteSwitch
- number buffered
- InnerAudioContext.onTimeUpdate(function callback)
- InnerAudioContext.offTimeUpdate(function callback)

### 编译说明
- 进入到 runtime2wx-adapter 目录下，先执行 npm install，然后再执行 gulp，会生成 rt-wx-adapter.js 放置在 runtime2wx-adapter/test/assets/Adapter 目录下
- nodejs 版本：v8.9.4
- gulp 版本：v3.9.1






