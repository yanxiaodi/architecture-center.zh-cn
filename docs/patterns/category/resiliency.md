---
title: "复原模式"
description: "复原是指系统能够在发生故障后进行恰当处理，然后恢复正常。 由于云托管的性质（应用程序通常是多租户的、使用共享平台服务、争用资源和带宽、通过 Internet 通信、在市售硬件上运行），出现暂时性故障和持久性故障的可能性增大。 快速高效检测故障并恢复是保持复原能力所必需的。"
keywords: "设计模式"
author: dragon119
ms.date: 06/23/2017
pnp.series.title: Cloud Design Patterns
ms.openlocfilehash: a3b9d72989e0de57c689bcec51e20653d0441d31
ms.sourcegitcommit: b0482d49aab0526be386837702e7724c61232c60
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2017
---
# <a name="resiliency-patterns"></a>复原模式

复原是指系统能够在发生故障后进行恰当处理，然后恢复正常。 由于云托管的性质（应用程序通常是多租户的、使用共享平台服务、争用资源和带宽、通过 Internet 通信、在市售硬件上运行），出现暂时性故障和持久性故障的可能性增大。 快速高效检测故障并恢复是保持复原能力所必需的。

| 模式 | 摘要 |
| ------- | ------- |
| [隔板](../bulkhead.md) | 将应用程序的元素隔离到池中，这样一来，如果一个元素出现故障，其他元素会继续工作。 |
| [断路器](../circuit-breaker.md) | 连接到远程服务或资源时处理故障，此类故障所需修复时间不定。 |
| [补偿事务](../compensating-transaction.md) | 撤销一系列会共同定义最终一致操作的工作。 |
| [运行状况终结点监视](../health-endpoint-monitoring.md) | 在应用程序中实施可让外部工具通过公开终结点定期访问的功能检查。 |
| [领导选择](../leader-election.md) | 通过选拔一个实例作为领导来负责管理其他实例，协调分布式应用程序中协作性任务实例集合所执行的操作。 |
| [基于队列的负载调节](../queue-based-load-leveling.md) | 使用队列在任务与所调用的服务之间充当缓冲，从而缓解间歇性负载过大现象。 |
| [重试](../retry.md) | 当应用程序尝试连接到服务或网络资源（通过明显重试先前失败的操作）时，启用应用程序以处理预期的临时故障。 |
| [计划程序代理监督程序](../scheduler-agent-supervisor.md) | 跨一组分布式服务和其他远程资源协调一组操作。 |