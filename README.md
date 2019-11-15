
## 图片压缩策略


#### 1.该项目不包含实质性代码，仅提供Android端 微博，微信朋友圈 图片上传压缩策略
#### 2.图片上传压缩数据实验对比

|  原图尺寸   | 体积  | 微信   | 体积  |  微博   | 体积  |
|  ----  | ----  |  ----  | ----  |  ----  | ----  |
|30000x15232|	23m	|2127x1080|	142kb	|2127 × 1080	|239kb|
|5407x5580	|5.3m	|1080x1114	|86.44kb	|1080 × 1114	|135kb
|14400x9600	|19.3m	|1620x1080	|262kb	|1620 × 1080	|431kb
|13758x6114	|14.84m	|4524x2011	|1.3m	|2430 × 1080	|593 KB
|9039x9231	|8.3m	|1080x1102	|69kb	|1080 × 1102	|83kb
|1137x14751	|3.8m	|854x11076	|701kb	|771 × 10000	|885 KB
|1944x6833	|8.4m	|1577x5541	|455kb	|1080 × 3794	|384kb
|19765x1977	|5.77m	|9594x960	|0.97m	|10000 × 1000	|1.8m
|800x28959	|10.9m	|531x19188	|714kb	|276 × 10000	|429 KB

### 仅靠数据得出大致结论，仅供参考，不一定代表真实情况 

#### 微信：
* 压缩门槛： 宽x高 总像素 > 1024w px
* 宽高 > 1080 && 宽高比 < 2 短边压到1080px 等比压缩
* 其他等比压缩到 1024w px以内


#### 微博：
* 宽高最小值小于1080，最大值小于10800，图片尺寸大小保持不变。
* 宽高比小于10，宽高最小值大于1080，，取较小值等于1080，较大值等比例压缩。
* 宽高比大于10，取较大值等于10800，较大值等比例压缩。
