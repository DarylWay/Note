#### 修改字体配置 

plt.rcParams["font.sans-serif"]

字体说明：

| 中文字体   | 说明     |
| ---------- | -------- |
| ‘SimHei’   | 中文黑体 |
| ‘Kaiti’    | 中文楷体 |
| ‘LiSu’     | 中文隶书 |
| ‘FangSong’ | 中文仿宋 |
| ‘YouYuan’  | 中文幼圆 |
| STSong     | 华文宋体 |

临时设置

```
# 使用中文需要进行配置信息的设置
plt.rcParams['font.sans-serif'] = ["FangSong"]
```

设置了中文字体后, 负数无法正常显示, 此时还需要添加负号编码的设置

```
# 解决方式: 修改轴中的负号编码
plt.rcParams['axes.unicode_minus'] = False
```

