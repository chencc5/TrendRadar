# TrendRadar 可用数据源平台列表

## 当前配置的平台（11个）

以下是在 `main.py` 中默认配置的数据源：

1. **今日头条** (`toutiao`)
2. **百度热搜** (`baidu`)
3. **华尔街见闻** (`wallstreetcn-hot`)
4. **澎湃新闻** (`thepaper`)
5. **bilibili 热搜** (`bilibili-hot-search`)
6. **财联社热门** (`cls-hot`)
7. **凤凰网** (`ifeng`)
8. **百度贴吧** (`tieba`)
9. **微博** (`weibo`)
10. **抖音** (`douyin`)
11. **知乎** (`zhihu`)

## 所有可用平台（38个）

基于 newsnow 项目支持的所有数据源：

### 新闻媒体类
1. **36氪** (`_36kr`) - 科技创业资讯
2. **参考消息** (`cankaoxiaoxi`) - 国际新闻
3. **凤凰网** (`ifeng`) - 综合新闻
4. **澎湃新闻** (`thepaper`) - 时政新闻
5. **俄罗斯卫星通讯社** (`sputniknewscn`) - 国际新闻
6. **联合早报** (`zaobao`) - 新加坡华文媒体

### 财经金融类
7. **华尔街见闻** (`wallstreetcn`) - 金融资讯
8. **财联社** (`cls`) - 财经快讯
9. **金十数据** (`jin10`) - 财经数据
10. **雪球** (`xueqiu`) - 投资社区
11. **格隆汇** (`gelonghui`) - 港股资讯
12. **Fastbull** (`fastbull`) - 财经资讯

### 科技社区类
13. **GitHub** (`github`) - 开源项目趋势
14. **Hacker News** (`hackernews`) - 科技新闻
15. **掘金** (`juejin`) - 开发者社区
16. **V2EX** (`v2ex`) - 创意工作者社区
17. **IT之家** (`ithome`) - IT资讯
18. **少数派** (`sspai`) - 效率工具
19. **Product Hunt** (`producthunt`) - 产品发现
20. **Solidot** (`solidot`) - 科技资讯
21. **Linux.do** (`linuxdo`) - Linux社区
22. **PC Beta** (`pcbeta`) - 电脑硬件社区
23. **牛客网** (`nowcoder`) - 程序员社区

### 社交媒体类
24. **微博** (`weibo`) - 微博热搜
25. **百度贴吧** (`tieba`) - 贴吧热议
26. **知乎** (`zhihu`) - 知乎热榜
27. **抖音** (`douyin`) - 抖音热点
28. **快手** (`kuaishou`) - 快手热榜
29. **今日头条** (`toutiao`) - 头条热榜
30. **百度** (`baidu`) - 百度热搜

### 视频平台类
31. **bilibili** (`bilibili`) - B站热搜

### 购物社区类
32. **什么值得买** (`smzdm`) - 购物推荐
33. **酷安** (`coolapk`) - 应用社区

### 体育娱乐类
34. **虎扑** (`hupu`) - 体育社区

### 其他类
35. **虫部落** (`chongbuluo`) - 资源分享
36. **共享信息** (`ghxi`) - 信息分享
37. **靠谱** (`kaopu`) - 信息平台
38. **MKT新闻** (`mktnews`) - 营销资讯

## 如何添加新的数据源

要添加新的数据源，需要修改 `main.py` 文件中的 `ids` 列表（第 2587-2599 行）。

### 配置格式

数据源可以使用两种格式配置：

1. **简单格式**：直接使用平台 ID
   ```python
   "github"
   ```

2. **完整格式**：包含 ID 和显示名称
   ```python
   ("github", "GitHub 趋势")
   ```

### 注意事项

- 某些平台可能有多个子类别（如 `wallstreetcn-hot`、`bilibili-hot-search`、`cls-hot`）
- 具体的子类别需要查看 newsnow 项目的源代码来确认
- 添加新数据源后，需要重新运行程序才能生效

### 示例：添加更多数据源

```python
ids = [
    # 现有配置...
    ("toutiao", "今日头条"),
    ("baidu", "百度热搜"),
    
    # 添加新的数据源
    ("github", "GitHub 趋势"),
    ("v2ex", "V2EX 热议"),
    ("_36kr", "36氪快讯"),
    ("ithome", "IT之家"),
    ("juejin", "掘金热榜"),
    ("smzdm", "什么值得买"),
    ("xueqiu", "雪球热帖"),
    # ... 更多数据源
]
```

## 更新时间

文档更新于：2025年1月11日