# DNS-Splitter 
## HTTP代理模式下的DNS分流器
> 当前项目仅提供使用说明与版本下载地址

什么是dns-splitter: dns-splitter是一个代理工具,对请求代理实现分流上网功能.
关键词：
1. DNS分流
2. DNS分流器
3. DNS分流上网
4. 基于DNS的分流方案
5. 解决switchhosts分流场景
6. 自定义DNS分流规则

* 流程图
> 分流所实现的功能
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_F001.png)


> 浏览器插件将流量转发到 DNS-Splitter
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_F002.png)



1. 启动 DNS-Splitter / DNS分流器
> 分流列表

![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0002.png)

2. 修改或新增DNS分流配置
> 设置【监听端口】

![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0003.png)

3. 修改或新增分流规则
> 多个匹配规则，使用分号;或,分隔（英文符号;,)

![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/dns-splitter-v1.png)

4. 浏览器安装 SplitterOmega 代理插件
* 提供3种安装方式

> a) 谷歌插件应用市场下载
```
https://chromewebstore.google.com/detail/splitteromega/ploedkalbbpgnejmmdoejdhjapflbhkd
```

> b) 在设置中,为浏览器初始化代理插件

![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0000.png)

> c) 手动为浏览器安装压缩包里的crx插件

5. 配置【SplitterOmega代理插件】情景模式
> 点击【DNS分流器设置】下的【同步方案】,自动将DNS-Splitter中设置的代理方案同步到浏览器插件.(避免用户关注端口)

![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0001.png)

6. 解析域名的规则由 【DNS-Splitter / DNS分流器】接管
> 应用程序可以配置多个分流配置,结合【SplitterOmega代理插件】多个情景模式.

#### 更新日志
- 1.2.0.2
1. 增加https代理的支持.
2. 增加浏览器启动自动获取dns-splitter的分流方案
3. 修复splitterOmega插件升级导致分流方案丢失.
4. 优化分流配置里面的规则按优先级排序.


- 1.2.0.1
1. 支持用户自定义规则列表
2. 支持用户设置规则的优先级
3. 支持设置走系统dns
4. 支持设置是否为黑名单,匹配后则丢弃请求
5. 区分chrome与edge的crx
6. 兼容1.0版本的配置文件


- 1.0.2.3
1. 增加[复制方案]功能
2. 优化为浏览器初始化SplitterOmega插件.
3. 升级浏览器插件,移除默认proxy代理方案.

- 1.0.2.2
1. 增加浏览器插件:SplitterOmega.
2. 程序为chrome与edge安装浏览器插件.
3. 方便通过浏览器插件获取DNS分流方案.

- 1.0.2.1
1. 增加SplitterHosts用于与浏览器通讯使用


- 1.0.2.0
1. 编辑[方案]后,勾选[启用]后,则需要开启监听模式.
2. 设置中新增[内存优化]选项,用于优化进程内存耗用.


- 1.0.1.9
1. 修复大文件传输中断问题.
2. 启用状态的方案,在删除的时候强制停止.
3. 界面显示当前连接数.
4. 右键菜单增加[停止所有]
5. 调整[连接列表]显示内容.


- 1.0.1.8
1. 将dll组件打包到exe内部.
2. [粘贴方案]之后,如果规则为[启用]状态,且端口未占用,则启动监听.

- 1.0.1.7
1. 修复内存泄露.
2. 增加显示连接列表，展示当前建立的连接信息.

- 1.0.1.6
1. 方案列表,右键菜单增加[复制方案列表][粘贴方案列表]功能，方便将选中的方案一次性复制出来，应用到其他主机。

- 1.0.1.5
1. 屏蔽F1快捷键,可能系统F1是截图功能.

- 1.0.1.4
1. 增加设置[允许保存日志],将请求日志写入本地磁盘文件,取消需要重启应用程序.
2. 增加设置[启用调试模式],将记录更多日志.

- 1.0.1.3
1. 优化任务栏右下角,鼠标[右键]弹出后失去焦点自动关闭菜单.

- 1.0.1.2
1. 增加默认公网dns.
2. 优化界面突出模式: [DNS分流]与[TCP转发].

- 1.0.1.1
1. 支持TCP端口转发.

- 1.0.1.0
1. 支持多语言切换 (简体中文/英文).

- 1.0.0.9
1. 修复线程与内存泄露.

- 1.0.0.8
1. 优化系统explorer进程崩溃的情况,状态栏右下角图标丢失.

- 1.0.0.7
1. 优化编译组件dll的参数,提升性能.

- 1.0.0.6 
1. 增加参数设置 [规则未匹配,则使用操作系统的DNS解析], 未勾选的情况下如果未匹配规则,则直接终止解析与请求.

- 1.0.0.5
1. 支持按规则指定dns解析域名.
2. 支持按规则指定DoH解析域名.
3. 支持按规则使用HTTP代理.
4. 支持设置开机启动.
5. 支持为浏览器初始化 ZeroOmega 扩展插件.

- 1.0.0.2
1. 修复ip映射关系解析规则.

- 1.0.0.1
1. 初始化版本.


#### 解析规则
1. 首先,查询域名与ip映射关系
    - 1.查找 单个域名与ip的匹配
    - 2.根据 模糊匹配进行查找
2. 其次,根据匹配条件,使用指定DNS进行解析
3. 最后,使用操作系统的DNS进行解析


#### 分流列表
> 可以配置多条解析规则,使用不同的【监听端口】来隔离

#### 分流配置
1. 方案名称, 用于区分规则名称
2. 监听端口, 用于隔离浏览接管
3. 域名IP映射关系, 可以实现ip与域名直接映射 
> 类似修改操作系统的 hosts 文件
4. 指定DNS解析
> 在[域名与IP映射关系]中未找到域名对应的IP后则使用指定DNS来解析
* 匹配条件, * 所匹配的域名将使用 [指定DNS] 进行解析,
- 匹配条件[*],代表所有域名
- 匹配条件[*abc001.com],代表所有abc001.com域名
- 匹配条件[*abc001.com;*abc002.com],代表所有abc001.com以及abc002.com域名
如果不满足匹配条件的,则使用操作系统的默认DNS进行解析


#### 域名IP映射关系 规则说明 

1. 注释行
```
#这是注释
192.168.100.51 www.abc001.com  #行内尾部写注释
```

2. 单个域名与ip匹配
> 解析 www.abc111.com 的 ip 为 192.168.100.51
```
192.168.100.51  www.abc111.com
```

3. 多个域名与ip匹配, 多个域名之间使用分号或逗号分隔
> 解析 www.abc111.com 和 www.abc112.com 的 ip 为 192.168.100.51
```
192.168.100.51  www.abc111.com;www.abc112.com
```

3. 单个模糊匹配
> 所有 abc112.com 后缀域名的 ip 为 192.168.100.52
```
192.168.100.52  *abc112.com
```

4. 多个模糊匹配, 多个匹配规则使用分号或逗号分隔
> 所有 abc112.com 和 abc113.com 后缀域名的 ip 为 192.168.100.52
```
192.168.100.52  *abc112.com;*abc113.com
```

#### DNS列表
> 可以预设多条DNS服务器地址

#### 关于



