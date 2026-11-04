# 状态图与简单类图

## 状态图
工单创建后进入 PENDING（待处理）。仅允许两个事件：
- 开始维修：PENDING → PROCESSING
- 完成维修：PROCESSING → COMPLETED

COMPLETED 为本次业务终态，不增加重新打开、取消、跳过处理中等状态。

```mermaid
stateDiagram-v2
    [*] --> PENDING
    PENDING --> PROCESSING: 开始维修
    PROCESSING --> COMPLETED: 完成维修
    COMPLETED --> [*]
