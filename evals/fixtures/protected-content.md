# 示例接口设计

> 本文件完全虚构，仅用于行为评测。

接口 `POST https://api.example.invalid/v1/events` 在 100 RPS 的合成负载下测得 P95 延迟为 `120 ms`。该结果只来自测试环境，不代表生产性能。

```json
{
  "event_id": "evt_demo_001",
  "source": "synthetic-sensor",
  "severity": "P2"
}
```

| 字段 | 必填 | 说明 |
|---|---:|---|
| `event_id` | 是 | 合成事件标识 |
| `source` | 是 | 合成来源 |
| `severity` | 否 | 示例严重级别 |

客户端重试最多 3 次；服务端幂等策略仍为 `[待确认]`。
