# Venom Button / 02 · 流光版

解压后用支持 WebGL 2 的浏览器打开 `index.html`。不需要联网、安装依赖或启动服务。

## 体验

- **靠近**：把鼠标移到黑胶边缘，等胶丝缠上手形光标。
- **拉远**：胶丝越拉越细，断开时甩出墨珠。蓝紫高光从连接点掠过胶丝。
- **点击**：点一下按钮，浅灰地面会泛起短暂的椭圆形波纹。
- **触屏**：靠近按钮边缘按住，等胶丝缠住后往外拖。
- **切换**：右下角「流光／经典」可关闭或开启本版新增效果，保留原来的拉丝交互。点「自动演示」看完整演示。参数可以调整文字、感应距离、粗细等。

`index.html?clean=1&demo=1` 打开无控件的自动演示；`index.html?mode=classic` 以经典模式打开。不支持 WebGL 2 时用静态按钮代替。系统开启减少动态效果时，页面停止胶丝、流光、墨珠及波纹。

## 拿去修改

`index.html` 内含 HTML、CSS、JavaScript、GLSL 和字体。`LABEL_TEXT` 是默认按钮文字。`VenomButton.setLabelText('你的文字')` 改文字；`VenomButton.setFlair(false)` 关闭附加视觉效果；`VenomButton.element.addEventListener('venom:activate', handler)` 接按钮点击与键盘激活。该演示未绑定导航地址。

## 渲染与来源

本版保留弹性胶丝模拟，以深度缓冲绘制胶丝、手形、黑胶底座和墨珠。演示为 1920×1080、30 fps 的原生逐帧渲染；导出采用浏览器生成的同一套 WebGL 绘制指令，在原生尺寸离屏绘制，未使用旧视频放大，也未使用原帖音轨或画面。

- 视觉参考：[Bear Liu 的 X 帖](https://x.com/bearliu/status/2125113196088373713)。
- 弹性模拟与部分着色改编自 [exteestudio / Venom Button](https://github.com/exteestudio/venom-button/tree/ca890bde95e81230c075879518bb70c1f2885c53)，保留 MIT 许可与署名，见 `LICENSE`。
- 内嵌 Geist 字体采用 SIL OFL 1.1，见 `Geist-OFL.txt`。手形及箭头为适配版重绘。
