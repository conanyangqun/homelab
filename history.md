## 此文件记录homelab发生的历史事件

### 2025-01-07断电

2025-01-07 11:50左右，群晖App报警：市电断开。（可能是UPS日常自检）2min后，群晖App再次报警：市电断开。此时，可以判断为正常的市电断开。

通过以下方式再次确认市电断开、断网：
- 米家app。联网设备离线。
- 乔安监控。监控头离线。

截止到2025-01-07 20:50，市电、网络仍然没有恢复。推测可能存在以下两种情况：
- 市电、网络都未恢复。需要人到现场排查市电问题。
- 市电恢复，但网络未恢复。**由于无网络，无法判断情况。但路由器每天定时重启，等待路由重启看网络是否恢复**。如果无法恢复，则需要人到现场排查。

想到2024-10-01期间，测试电、网恢复时的一个问题，市电断开一定时间，homelab启动断电关机进程。但在该进程执行过程中，市电恢复，则可能导致自动开机失效。这个问题当时没有处理，可能是此次问题的原因。

等确定原因，再考虑改进。目前可能的改进点有：
- 建立即时通讯方式，在市电断开后立即发送通知。
- 处理关机进程期间，市电恢复无法成功启动的bug。
- 建立网、电的冗余机制。

自2024-10-01更新homelab到现在，才运行了3个月，就遭遇了此等故障，耻辱啊……奇耻大辱。

**后续，现场排查问题，发现市电正常、UPS等处于关闭状态**。因此属于bug导致的自动开机失败，后续考虑完善。
