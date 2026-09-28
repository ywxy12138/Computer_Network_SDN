# Computer_Network_SDN

SDN 课程实验环境（SDNHub Tutorial VM，VMware 虚拟机）的配置与脚本归档。

## 仓库内容

| 文件 | 说明 |
|---|---|
| `firewall_.py` | 防火墙实验脚本 |
| `sdn.vmx` / `sdn.vmxf` / `sdn.vmsd` | VMware 虚拟机配置 |
| `nvram` | 虚拟机 NVRAM |
| `sdn.scoreboard` / `sdn-0/1.scoreboard` | 虚拟机运行状态快照 |
| `vmware.log` / `vmware-0.log` / `vmware-1.log` | VMware 运行日志 |
| `*.baiduyun.uploading.cfg` | 大文件网盘上传状态 |

## 未纳入版本控制的大文件

以下两个文件**不在本仓库中**，原因见下：

| 文件 | 大小 |
|---|---|
| `sdn-disk1.vmdk` | 10.1 GB |
| `SDNHub_tutorial_VM_64-bit[NEW](可直接导入VMware).ova` | 5.85 GB |

### 为什么传不上 GitHub

1. **普通 Git**：单文件超过 100 MB 会被 GitHub 的 pre-receive hook 直接拒绝。
2. **Git LFS**：同样有单文件上限——Free/Pro 2 GB、Team 4 GB、Enterprise 5 GB。`sdn-disk1.vmdk` 的 10.1 GB 超过了**所有套餐的上限**，`ova` 的 5.85 GB 也超过 5 GB。这无法通过付费解决。
3. **仓库总配额**：即使分片绕过单文件限制，15.9 GB 也远超 Free 账户 1 GB 的 LFS 存储额度，需购买 Data Pack。

> 注：`.ova` 本身是完整虚拟机导出包，内部已包含虚拟磁盘，与 `.vmdk` 内容重复。归档时只需保留其中一个。

## 获取大文件

虚拟机镜像建议通过网盘分发，可在本地目录中找到对应的 `.baiduyun.uploading.cfg` 上传记录。
