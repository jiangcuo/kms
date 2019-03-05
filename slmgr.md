# Windows Script Host

> 命令  **`slmgr`** 

> 命令参数的组合无效。

> Windows 软件授权管理工具

用法: `slmgr.vbs [MachineName [User Password]] [<Option>]`

       MachineName: 远程计算机的名称(默认为本地计算机)

       User: 远程计算机上具有所需特权的帐户

       Password: 前面帐号的密码

----------

### 全局选项:

`/ipk <Product Key>`    安装产品密钥(替换现有密钥)

`/ato [Activation ID]`  激活 Windows 

`/dli [Activation ID | All]`    显示许可证信息(默认: 当前许可证)

`/dlv [Activation ID | All]`    显示详细的许可证信息(默认: 当前许可证)

`/xpr [Activation ID]`  当前许可证状态的截止日期

----------

### 高级选项:

`/cpky` 从注册表中清除产品密钥(防止泄露引起的攻击)

`/ilc <License file>`   安装许可证

`/rilc` 重新安装系统许可证文件

`/rearm`    重置计算机的授权状态

`/rearm-app <应用程序 ID>`  重置给定应用的授权状态

`/rearm-sku <Activation ID>`    重置给定 SKU 的授权状态

`/upk [Activation ID]`  卸载产品密钥

`/dti [Activation ID]`  显示安装 ID 以进行脱机激活

`/atp <Confirmation ID> [Activation ID]`    使用用户提供的确认 ID 激活产品

----------

### 批量许可: 密钥管理服务(KMS)客户端选项:

`/skms <Name[:Port] | : port> [Activation ID]`  设置 KMS 计算机名称和/或端口。IPv6 地址必须以“[计算机名]:端口”的格式指定

`/ckms [Activation ID]` 清除所使用的 KMS 计算机名称(将其端口设置为默认值)

`/skms-domain <FQDN> [Activation ID]`   设置可在其中找到所有 KMS SRV 记录的特定 DNS 域。如果特定的单 KMS 主机通过 /skms 选项进行设置，则此设置无效。

`/ckms-domain [Activation ID]`  清除可在其中找到所有 KMS SRV 记录的特定 DNS 域。如果特定的 KMS 主机通过 /skms 进行设置，则将使用该 KMS 主机。否则，将使用默认的 KMS 自动发现。

`/skhc` 启用 KMS 主机缓存

`/ckhc` 禁用 KMS 主机缓存

----------

### 批量许可: 基于令牌的激活选项:

`/lil`  列出安装的基于令牌的激活颁发许可证

`/ril <ILID> <ILvID>`   删除安装的基于令牌的激活颁发许可证

`/ltc`  列出基于令牌的激活证书

`/fta <证书指纹> [<PIN>]`   强制进行基于令牌的激活

----------

### 批量许可: 密钥管理服务(KMS)选项:

`/sprt <Port>`  设置 KMS 用于与客户端进行通信的 TCP 端口

`/sai <Activation Interval>`    设置未激活的客户端尝试连接 KMS 的时间间隔(分钟)。虽然建议了默认时间(2 小时)，但是激活间隔必须介于 15 分钟(最小值)到 30 天(最大值)之间。

`/sri <Renewal Interval>`   设置激活的客户端尝试连接 KMS 的续订时间间隔(分钟)。虽然建议了默认时间(7 天)，但是续订时间间隔必须介于 15 分钟(最小值)和 30 天(最大值)之间。

`/sdns` 启用通过 KMS 进行的 DNS 发布(默认)

`/cdns` 禁用通过 KMS 进行的 DNS 发布

`/spri` 将 KMS 优先级设置为普通(默认)

`/cpri` 将 KMS 优先级设置为低

`/act-type [激活类型] [Activation ID]`  将激活类型设置为 1 (针对 AD)或 2 (针对 KMS)或 3 (针对 Token)或 0 (针对全部)。

----------

### 批量许可: Active Directory (AD)激活选项:

`/ad-activation-online <Product Key> [激活对象名称]`    通过用户提供的产品密钥激活 AD (Active Directory)林。

`/ad-activation-get-iid <Product Key>`  显示 AD (Active Directory)林的安装 ID

`/ad-activation-apply-cid <Product Key> <Confirmation ID> [激活对象名称]`   通过用户提供的产品密钥和确认 ID 激活 AD (Active Directory)林

`/ao-list`  显示 AD (Active Directory)中的激活对象

`/del-ao <Activation Object DN | Activation Object RDN>`    针对用户提供的激活对象，删除 AD (Active Directory)中的激活对象