# 不活跃贡献者

问题：在特定时间段内有多少贡献者处于不活跃状态？


## 描述
该指标显示特定时间段内有多少贡献者停止了贡献。 贡献者被记为不活跃所需的时间可以由一个变量决定，此指标将显示在给定时间框架内被标记为不活跃贡献者的数量。

## 目标
确定有多少人停止了活跃贡献。 这可以让社区管理者高效确定关键成员是否将失去兴趣或准备休息。

## 实现
该指标将包含两个变量 - 时间段和时间间隔。 时间段将是显示不活跃成员数量的时间段。 例如，如果时间段 = 年，那么它将显示每年的不活跃贡献者数量。 时间间隔将决定贡献者被标记为不活跃所花费的时间。 如果贡献者没有做出贡献的时间超过时间间隔，即被视为不活跃。

指标运作方式：
1. 获取所有贡献者的列表
2. 检查最后的贡献日期
3. 如果最后一次贡献日期在截止日期之前，则将其添加到最后一次贡献所处时间段的不活跃计数中。
4. 创建不活跃贡献者列表

**聚合器：**
- 不活跃：不活跃贡献者数量

### 筛选条件
- 必要的最低活跃贡献者数量
- 确定不活跃的时间段
- 开始日期/结束日期
- 图形周期

### 数据收集策略
可以使用现有贡献者指标来收集贡献者列表。 要确定最后的贡献日期，可能需要新的代码。