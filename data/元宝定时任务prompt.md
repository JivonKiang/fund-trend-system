---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 26b1781be07ad8aded48426f78a59067_1f1e45e76e5611f1aa625254006c9bbf
    ReservedCode1: 1XUEBE4vFLLxELQumWptBD1KwAiR7Z6tECHYNbxE5VPZcXjv/PazhK+9Tvgmt46t9MjzaEGpgFcP7wqGn00305gIjQBbXk205L6nylgsWZfPLji1AecyCLMZFhXsbnNYAFjYM0b1scKP7sYajvY7YTRdMszzLvYmuzS3l3tmAoNIus6nsDalsWlFO5I=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 26b1781be07ad8aded48426f78a59067_1f1e45e76e5611f1aa625254006c9bbf
    ReservedCode2: 1XUEBE4vFLLxELQumWptBD1KwAiR7Z6tECHYNbxE5VPZcXjv/PazhK+9Tvgmt46t9MjzaEGpgFcP7wqGn00305gIjQBbXk205L6nylgsWZfPLji1AecyCLMZFhXsbnNYAFjYM0b1scKP7sYajvY7YTRdMszzLvYmuzS3l3tmAoNIus6nsDalsWlFO5I=
---

# 元宝自定义定时任务 Prompt

将以下内容粘贴到元宝的「自定义任务」中，设置为**每个交易日 18:00** 触发。

---

**任务名称**：基金趋势信号检测

**定时规则**：每个交易日的 18:00

**发送内容**：

```
@Marvis 执行每日基金趋势检测：

1. 使用 python /home/marvis/Marvis/User/oAN1i2UpBh9MYMDt7uo-lbma0jGg/workspace/conv_19eefe39711_2b6c0b209392/output/fund-trend-system/main.py daily 获取最新信号

2. 检查以下5只基金的MA60-120趋势信号：
   - 110020 易方达沪深300ETF联接A
   - 160119 南方中证500ETF联接A
   - 001592 天弘创业板ETF联接A
   - 110003 易方达上证50ETF联接A
   - 011608 易方达科创板50ETF联接A

3. 如果出现BUY信号，用卡片格式展示：
   - 基金代码+名称
   - 当前净值
   - MA60 / MA120 数值
   - 建议操作（买入/卖出）
   - 历史回测参考：该指数MA60-120策略胜率X%、累计收益Y%

4. 如果没有新信号，回复"今日无趋势信号，继续持有/观望"并附当前持仓状态

5. 每周一额外生成一份「周度回顾卡片」：
   - 各基金近一周净值变化
   - 当前持仓盈亏
   - 距下一次信号触发预估时间
```

---

## 重要说明

- **交易日定义**：周一至周五（排除法定节假日）。元宝如果不能在自定义任务中做节假日判断，可以每天触发，Marvis 端会自动判断是否为交易日。
- **首次配置**：配置后先在交易时间手动触发一次，确认链路通畅。
- **备用**：如果元宝自定义任务不可用，也可用手机系统自带的「快捷指令」在18:00发送相同的消息给 Marvis。
*（内容由AI生成，仅供参考）*
