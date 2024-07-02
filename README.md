# RandomBroadcast 随机广播
- 作者: 羽学
- 出处: 无
- 定时随机发送一条广播内容（支持指令）

## 配置注意事项

```
1.`触发概率`不能超过`1`，否则报错，如果只有`2组`内容，则`各写0.5`上去就不会有延迟，
如果只有`2组`你都写`0.1`，剩下的`80%`系统会算空就会有`延迟`。

2.`消息内容`含有 / 或者 .的会默认当服务器指令执行

3.`同发数量`要按实数填写，比如你有`2组`，
你想同时发送2组消息内容，同发就写`2`，
不要只有2组你同发数量写个`9999`，`刷屏`刷死你

4.`默认间隔`写整数，0.01`0.6秒`是羽学测试时不想等那么长时间才写上去的。
```

## 配置
> 配置文件位置：tshock/随机广播.json
```json
{
  "使用说明": "【触发概率】1为100%，【消息内容】含【/或.】的会当指令执行，【同发数量】会随机发多组内容",
  "开启插件": true,
  "同发数量": 1,
  "默认间隔/分钟": 30.0,
  "内容表": [
    {
      "触发概率": 0.5,
      "消息内容": [
        ".time 7:30",
        "我又来啦"
      ],
      "触发颜色": [
        255.0,
        234.0,
        115.0
      ]
    },
    {
      "触发概率": 0.5,
      "消息内容": [
        "/time 19:30",
        "我又走啦"
      ],
      "触发颜色": [
        190.0,
        233.0,
        250.0
      ]
    }
  ]
}
```
## 反馈
- 优先发issued -> 共同维护的插件库：https://github.com/Controllerdestiny/TShockPlugin
- 次优先：TShock官方群：816771079
- 大概率看不到但是也可以：国内社区trhub.cn ，bbstr.net , tr.monika.love
