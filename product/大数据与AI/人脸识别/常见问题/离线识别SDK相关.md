### 离线识别 SDK 和 API 文档中提供的各类 SDK 区别是什么？
- API 文档中提供的各类 SDK，即 Tencent Cloud SDK 3.0 for Python/Java/PHP/Go/NodeJS/.Net 等，是为了方便您通过不同的开发语言快速使用我们的在线 API 服务。
- 离线识别 SDK，是将我们的人脸识别服务集成到一个离线的 SDK 中，您无需联网，可以在设备端本地化进行实时处理。
- 目前我们的离线识别 SDK 仅支持 Android 操作系统，我们建议您使用离线识别 SDK 中的人脸检测、活体检测功能，从设备中获取用于人脸识别的图片，传输到云端进行完整的人脸识别。

### 离线识别 SDK 支持哪些操作系统？
目前离线识别 SDK 仅支持 Android 操作系统，Linux 和 iOS 系统暂不支持。

### 离线识别 SDK 支持几路并发？
目前离线识别 SDK 仅支持 Android 操作系统，目前不支持并发，只能单路。

### 离线识别 SDK 的性能如何？
离线识别 SDK 的性能表现需要看具体的设备情况，建议测试方法：因为相同的人脸不干扰性能，所以对同一张图循环操作 N 次求平均值即可获得性能数据。

### 人脸截图尺寸固定吗?
没有固定值，从输入帧中截取人脸范围部分，脸越大，截图越大。

### 为什么人脸跟踪多次检测同一张图片得到的关键点不一致？
track 对象请每次创建（new），不要重复使用。

### 能否判断光照?
暂时不支持。

### 是否有质量分影响因素以及权重？
因素有运动模糊、光线、面部遮挡，目前没有显式的权重。


### 离线识别 SDK 有没有推荐的硬件设备？
芯片支持RK3288、RK3399、RK3368，双目摄像头建议金晟芯D046，3D 结构光摄像头建议华捷艾米/艾芯/PICO，内存建议大于2GB。


### 如何查询设备的授权时间？
SDK 初始化时候会回调授权结果, 其中包含日期，Android Logcat 日志过滤 "授权" 字样可以看到。


### 离线识别 SDK 需要哪些系统授权？
READ_PHONE_STATE、CAMERA 为必需，ACCESS_COARSE_LOCATION，ACCESS_FINE_LOCATION 用于帮助授权，READ_EXTERNAL_STORAGE、 WRITE_EXTERNAL_STORAGE 用于预留给日志文件读写。如无特殊原因建议保留。


