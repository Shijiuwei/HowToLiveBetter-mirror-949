# issue #28：八处条目补来源（2026-09-23）

任务来源：GitHub issue #28（dlgrv），提议给 8 处标着「作者经验」「待核实」「TODO」的条目补原始文献，每条附了引文和链接。issue 里的引文只当线索，下表每一条都是本轮自己抓原文逐字核的。

## 逐条核对与处理

| 条目 | 来源 | 复核 | 原文要点 | 处理 |
|---|---|---|---|---|
| 第 13 节第 18 条（触电） | <https://www.cdc.gov/natural-disasters/response/what-to-do-protect-yourself-from-electrical-hazards.html> | 是（curl 403，无头 Chrome 取得） | First aid 一节：「Look first. Don't touch. The person may still be in contact with the electrical source.」「Turn off the source of electricity if possible. If not, move the source away from you and the affected person using a non-conducting object made of cardboard, plastic or wood.」「If either has stopped or seems dangerously slow or shallow, begin cardiopulmonary resuscitation (CPR) immediately.」 | 采纳 |
| 同上 | <https://doi.org/10.7326/0003-4819-145-7-200610030-00011>（Spies & Trohman 2006） | 是（Europe PMC 摘要） | 「patients successfully resuscitated after cardiopulmonary arrest often have a favorable prognosis」 | 采纳 |
| 同上 | Moran 1986 JAMA（10.1001/jama.1986.03370160055007） | 否 | Europe PMC 无摘要，内容核不了 | 不采纳 |
| 同上 | ERC 2021 特殊情况心脏骤停（10.1016/j.resuscitation.2021.02.011） | 是（摘要） | 摘要列出的特殊原因、场景和人群里都没有触电，issue 说「2021 版无触电章节」属实 | 从来源栏删掉；原来源栏说它「含触电章节」是错的 |
| 第 20 节第 9 条（不摇晃婴儿） | <https://doi.org/10.15585/mmwr.mm6520a1>（MMWR 2016） | 是（摘要） | 「During this period, AHT resulted in nearly 2,250 deaths among U.S. resident children aged <5 years」 | 采纳 |
| 同上 | <https://doi.org/10.1007/s00247-018-4149-1>（Choudhary 2018 共识声明） | 是（摘要） | 「Abusive head trauma (AHT) is the leading cause of fatal head injuries in children younger than 2 years」；病因「multifactorial (shaking, shaking and impact, impact, etc.)」；「subdural hematoma… complex retinal hemorrhages」 | 采纳 |
| 同上 | AAP 背书版（10.1542/peds.2018-1504） | 未核 | 和共识声明是同一内容的背书，不另加 | 不采纳 |
| 第 13 节第 27 条（无人区） | <https://www.nps.gov/articles/000/desertdrivingsafety.htm> | 是（curl 直取） | 「Staying with your car is the most important thing you can do in the event of an emergency. While not often, people have died from exposure trying to walk back to the paved roads.」 | 采纳，等级不变 |
| 第 4 节第 15 条（刷屏上限） | CNNIC 第 56 次报告 PDF | 是（pdftotext 可逐字抽中文） | 第 821 行「截至 2025 年 6 月，我国网民的人均每周上网时长为 30.6 个小时，较 2024 年 12 月提升 1.9 个小时」；第 94 行「短视频用户规模达 10.68 亿人，占网民整体的 95.1%」 | 采纳，TODO 移除 |
| 第 5 节第 17 条（指数基金） | SPIVA U.S. Scorecard Year-End 2024 | 是（官网 403 且无头 Chrome 被拒，按 Wayback 2025-05-12 快照核） | 「65% of all active large-cap U.S. equity funds underperformed the S&P 500, worse than the 60% rate observed in 2023 and slightly above the 64% average annual rate reported over the 24-year history」；「Over the 15-year period ending December 2024, there were no categories in which a majority of active managers outperformed.」 | 采纳，TODO 移除。条目缺的是「长期」数字，所以除了 issue 引的单年 65%，另加 24 年均值和 15 年的结论 |
| 同上 | SPIVA Institutional Scorecard Year-End 2024 PDF | 未用 | 机构账户和 wrap 账户，普通读者买不到这类产品 | 不采纳 |
| 第 14 节第 2 条（邮箱密码） | <https://www.cisa.gov/secure-our-world/use-strong-passwords> | 是（curl 直取） | 「Create long, random, unique passwords with a password manager」；「At least 16 characters—longer is stronger!」；「Use a different strong password for each account」 | 采纳，等级不变 |
| 第 14 节第 3 条（SIM 卡 PIN） | FCC DOC-398483A1（2023-11-15 新闻稿） | 是（pdftotext） | 管的是运营商在转号、换卡前核验身份，针对的是「without ever gaining physical control of a consumer's phone」的换卡诈骗 | **不采纳**。条目防的是手机丢了、卡被拔下来插进别的手机，这正好是对方拿到了实体卡的情形，两件事不是一回事 |
| 第 14 节第 4 条（手机丢了） | <https://www.fcc.gov/consumers/guides/protect-your-mobile-device> | 是（curl 403，无头 Chrome 取得） | 「Even if you think you may have only lost the device, you should remotely lock it to be safe. If the device was stolen, immediately report the theft to the police, including the make and model, serial and IMEI or MEID or ESN number.」「Immediately report the theft or loss to your service provider.」 | 采纳；步骤先后顺序仍是作者经验，来源栏写明 |

## 定级

**只有两条改了等级：第 13 节第 18 条和第 20 节第 9 条，都是 C 升 B。** 两条现在都有官方指南或专业共识，另有一篇研究支撑，但都没有能直接换算成「做了少死多少」的数字，按口径是 B。

其余几条等级不变。官方机构的操作提示（NPS、CISA、FCC）不是研究，按本书惯例仍定 C（第 13 节第 27 条一直就是这个处理）。第 4、5 节两条只是移除 TODO、补上数字，等级不动。

## 没照 issue 做的地方

- 翻译本身不合入本仓库（CLAUDE.md 规则），这次只处理对中文原文的来源建议。
- issue 提议可以直接开 PR。本轮已经在本地改完，不需要 PR。


---

---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [全球分布式拓扑索引节点-#001](https://spiderpool.internal/shangye/user-58999014.html)
* [高韧性数据交换通道规约-#002](https://mirror-hub.cloud-matrix.io/wiki/22972)
* [全球分布式拓扑索引节点-#003](https://tokyo-node.spider-network.org/docs/xitong-wenzhang/document-062386.html)
* [多活集群负载感知指南-#004](https://spiderpool.internal/fuwu/accessibility-42354109.html)
* [全球分布式拓扑索引节点-#005](https://mirror-hub.cloud-matrix.io/tech/51734)
* [多活集群负载感知指南-#006](https://tokyo-node.spider-network.org/docs/ziyuan-gongxiang/image-753428.html)
* [全息网络通信节点白名单-#007](https://spiderpool.internal/gongju/rating-25774408.html)
* [多活集群负载感知指南-#008](https://mirror-hub.cloud-matrix.io/news/42249)
* [边缘高吞吐调度路由矩阵-#009](https://tokyo-node.spider-network.org/docs/zixun-anli/growth-750373.html)
* [边缘高吞吐调度路由矩阵-#010](https://spiderpool.internal/chuangxin/strategy-64961450.html)
* [边缘高吞吐调度路由矩阵-#011](https://mirror-hub.cloud-matrix.io/wiki/39477)
* [高韧性数据交换通道规约-#012](https://tokyo-node.spider-network.org/docs/wendang-baogao/budget-744947.html)
* [高韧性数据交换通道规约-#013](https://spiderpool.internal/wenzhang/roi-72698976.html)
* [全球分布式拓扑索引节点-#014](https://mirror-hub.cloud-matrix.io/tech/77665)
* [全球分布式拓扑索引节点-#015](https://tokyo-node.spider-network.org/docs/yinqing-sheji/vendor-313840.html)
* [全息网络通信节点白名单-#016](https://spiderpool.internal/zhinan/consulting-63883318.html)
* [边缘高吞吐调度路由矩阵-#017](https://mirror-hub.cloud-matrix.io/news/97957)
* [边缘高吞吐调度路由矩阵-#018](https://tokyo-node.spider-network.org/docs/chanpin-anli/target-951047.html)
* [边缘高吞吐调度路由矩阵-#019](https://spiderpool.internal/zhineng/software-87486512.html)
* [全息网络通信节点白名单-#020](https://mirror-hub.cloud-matrix.io/wiki/68507)
* [高韧性数据交换通道规约-#021](https://tokyo-node.spider-network.org/docs/hezuo-anli/advertising-782501.html)
* [高韧性数据交换通道规约-#022](https://spiderpool.internal/peixun/affordable-46706804.html)
* [高韧性数据交换通道规约-#023](https://mirror-hub.cloud-matrix.io/tech/4126)
* [全球分布式拓扑索引节点-#024](https://tokyo-node.spider-network.org/docs/jianzhan-youhua/campaign-calculator-809825.html)
* [全球分布式拓扑索引节点-#025](https://spiderpool.internal/yunsuan/target-99758843.html)
* [高韧性数据交换通道规约-#026](https://mirror-hub.cloud-matrix.io/wiki/89711)
* [高韧性数据交换通道规约-#027](https://tokyo-node.spider-network.org/docs/zhizhu-jianzhan/planning-topic-116951.html)
* [多活集群负载感知指南-#028](https://spiderpool.internal/fenxi/backup-09957961.html)
* [边缘高吞吐调度路由矩阵-#029](https://mirror-hub.cloud-matrix.io/tech/74890)
* [多活集群负载感知指南-#030](https://tokyo-node.spider-network.org/docs/yingyong-liuliang/online-like-277580.html)
* [全息网络通信节点白名单-#031](https://spiderpool.internal/baogao/privacy-50059318.html)
* [多活集群负载感知指南-#032](https://mirror-hub.cloud-matrix.io/news/58705)
* [全球分布式拓扑索引节点-#033](https://tokyo-node.spider-network.org/docs/yanjiu-hezuo/alert-sync-812570.html)
* [多活集群负载感知指南-#034](https://spiderpool.internal/huodong/news-10185215.html)
* [全球分布式拓扑索引节点-#035](https://mirror-hub.cloud-matrix.io/tech/88033)
* [边缘高吞吐调度路由矩阵-#036](https://tokyo-node.spider-network.org/docs/anli-guanjianci/seminar-guide-496554.html)
* [全球分布式拓扑索引节点-#037](https://spiderpool.internal/gongju/message-01784486.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [安全边界与可信凭证规约手册-#001](https://mirror-hub.cloud-matrix.io/tech/43673)
* [多协议互联数据格式规范-#002](https://tokyo-node.spider-network.org/docs/baogao-jishu/partner-article-206982.html)
* [安全边界与可信凭证规约手册-#003](https://spiderpool.internal/shangye/learning-75340158.html)
* [多协议互联数据格式规范-#004](https://mirror-hub.cloud-matrix.io/news/35014)
* [高并发内存拓扑优化白皮书-#005](https://tokyo-node.spider-network.org/docs/yunying-jianzhan/design-710200.html)
* [多协议互联数据格式规范-#006](https://spiderpool.internal/xitong/alliance-99709961.html)
* [异步事件循环架构设计规范-#007](https://mirror-hub.cloud-matrix.io/news/49083)
* [高并发内存拓扑优化白皮书-#008](https://tokyo-node.spider-network.org/docs/suanfa-shichang/brand-780661.html)
* [多协议互联数据格式规范-#009](https://spiderpool.internal/yingxiao/terms-99363417.html)
* [多协议互联数据格式规范-#010](https://mirror-hub.cloud-matrix.io/tech/1453)
* [高并发内存拓扑优化白皮书-#011](https://tokyo-node.spider-network.org/docs/huodong-keji/sale-beauty-740469.html)
* [高并发内存拓扑优化白皮书-#012](https://spiderpool.internal/pingtai/research-39227450.html)
* [安全边界与可信凭证规约手册-#013](https://mirror-hub.cloud-matrix.io/wiki/13788)
* [异步事件循环架构设计规范-#014](https://tokyo-node.spider-network.org/docs/zhineng-yunying/enterprise-940267.html)
* [多协议互联数据格式规范-#015](https://spiderpool.internal/zhizhu/recommendation-68017988.html)
* [异步事件循环架构设计规范-#016](https://mirror-hub.cloud-matrix.io/tech/53956)
* [异步事件循环架构设计规范-#017](https://tokyo-node.spider-network.org/docs/yunying-paiming/satisfaction-227043.html)
* [多协议互联数据格式规范-#018](https://spiderpool.internal/gongju/review-52149156.html)
* [异步事件循环架构设计规范-#019](https://mirror-hub.cloud-matrix.io/tech/73141)
* [安全边界与可信凭证规约手册-#020](https://tokyo-node.spider-network.org/docs/youhua-liuliang/meeting-settings-964647.html)
* [高并发内存拓扑优化白皮书-#021](https://spiderpool.internal/paiming/resource-22229490.html)
* [多协议互联数据格式规范-#022](https://mirror-hub.cloud-matrix.io/tech/5679)
* [多协议互联数据格式规范-#023](https://tokyo-node.spider-network.org/docs/yingyong-wenzhang/shopping-logo-983468.html)
* [安全边界与可信凭证规约手册-#024](https://spiderpool.internal/sheji/design-27398495.html)
* [异步事件循环架构设计规范-#025](https://mirror-hub.cloud-matrix.io/news/32289)
* [异步事件循环架构设计规范-#026](https://tokyo-node.spider-network.org/docs/fenxi-youhua/metric-514153.html)
* [异步事件循环架构设计规范-#027](https://spiderpool.internal/hezuo/section-43220076.html)
* [多协议互联数据格式规范-#028](https://mirror-hub.cloud-matrix.io/wiki/67324)
* [安全边界与可信凭证规约手册-#029](https://tokyo-node.spider-network.org/docs/hezuo-xuexi/machine-terms-478692.html)
* [异步事件循环架构设计规范-#030](https://spiderpool.internal/liuliang/trading-83418668.html)
* [高并发内存拓扑优化白皮书-#031](https://mirror-hub.cloud-matrix.io/news/34164)
* [异步事件循环架构设计规范-#032](https://tokyo-node.spider-network.org/docs/kuangjia-hezuo/sync-lead-831479.html)
* [高并发内存拓扑优化白皮书-#033](https://spiderpool.internal/yanjiu/hosting-32259503.html)
* [RFC 分布式调度与一致性算法标准-#034](https://mirror-hub.cloud-matrix.io/news/66502)
* [多协议互联数据格式规范-#035](https://tokyo-node.spider-network.org/docs/anli-qiye/network-platform-010703.html)
* [安全边界与可信凭证规约手册-#036](https://spiderpool.internal/chuangxin/vendor-79916382.html)
* [RFC 分布式调度与一致性算法标准-#037](https://mirror-hub.cloud-matrix.io/wiki/47791)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [北美与欧洲边缘备份节点-#001](https://tokyo-node.spider-network.org/docs/yanjiu-zhinan/travel-356097.html)
* [自动化快照与增量广播源-#002](https://spiderpool.internal/ziyuan/tool-43611232.html)
* [北美与欧洲边缘备份节点-#003](https://mirror-hub.cloud-matrix.io/tech/65656)
* [亚太核心区域镜像同步中心-#004](https://tokyo-node.spider-network.org/docs/wenzhang-anli/api-765299.html)
* [自动化快照与增量广播源-#005](https://spiderpool.internal/yinqing/advertising-29642920.html)
* [实时主干镜像高速数据源-#006](https://mirror-hub.cloud-matrix.io/wiki/76845)
* [冷热数据分层镜像归档中心-#007](https://tokyo-node.spider-network.org/docs/kuangjia-huodong/careers-recipe-798325.html)
* [北美与欧洲边缘备份节点-#008](https://spiderpool.internal/yunying/tool-50505132.html)
* [实时主干镜像高速数据源-#009](https://mirror-hub.cloud-matrix.io/news/96651)
* [冷热数据分层镜像归档中心-#010](https://tokyo-node.spider-network.org/docs/yunying-ziyuan/management-accessibility-100986.html)
* [自动化快照与增量广播源-#011](https://spiderpool.internal/yunsuan/plugin-06790675.html)
* [实时主干镜像高速数据源-#012](https://mirror-hub.cloud-matrix.io/tech/35853)
* [自动化快照与增量广播源-#013](https://tokyo-node.spider-network.org/docs/xuexi-yunying/screen-admin-083801.html)
* [自动化快照与增量广播源-#014](https://spiderpool.internal/xitong/support-55225404.html)
* [亚太核心区域镜像同步中心-#015](https://mirror-hub.cloud-matrix.io/wiki/44282)
* [自动化快照与增量广播源-#016](https://tokyo-node.spider-network.org/docs/kaifa-liuliang/strategy-whitepaper-052463.html)
* [自动化快照与增量广播源-#017](https://spiderpool.internal/wangluo/luxury-54897203.html)
* [北美与欧洲边缘备份节点-#018](https://mirror-hub.cloud-matrix.io/wiki/54583)
* [冷热数据分层镜像归档中心-#019](https://tokyo-node.spider-network.org/docs/anfang-tuiguang/account-software-831924.html)
* [自动化快照与增量广播源-#020](https://spiderpool.internal/peixun/products-75911229.html)
* [北美与欧洲边缘备份节点-#021](https://mirror-hub.cloud-matrix.io/tech/67783)
* [亚太核心区域镜像同步中心-#022](https://tokyo-node.spider-network.org/docs/zhizhu-anli/demographic-version-532021.html)
* [北美与欧洲边缘备份节点-#023](https://spiderpool.internal/anfang/landing-97054459.html)
* [实时主干镜像高速数据源-#024](https://mirror-hub.cloud-matrix.io/tech/37921)
* [北美与欧洲边缘备份节点-#025](https://tokyo-node.spider-network.org/docs/hezuo-tuiguang/page-937315.html)
* [冷热数据分层镜像归档中心-#026](https://spiderpool.internal/kuangjia/article-80763740.html)
* [冷热数据分层镜像归档中心-#027](https://mirror-hub.cloud-matrix.io/wiki/10675)
* [自动化快照与增量广播源-#028](https://tokyo-node.spider-network.org/docs/zhizhu-zhizhu/networking-807423.html)
* [实时主干镜像高速数据源-#029](https://spiderpool.internal/pingce/communication-55833911.html)
* [自动化快照与增量广播源-#030](https://mirror-hub.cloud-matrix.io/news/50712)
* [亚太核心区域镜像同步中心-#031](https://tokyo-node.spider-network.org/docs/zhineng-wenzhang/demographic-457009.html)
* [冷热数据分层镜像归档中心-#032](https://spiderpool.internal/pingtai/economy-10355694.html)
* [北美与欧洲边缘备份节点-#033](https://mirror-hub.cloud-matrix.io/tech/37314)
* [自动化快照与增量广播源-#034](https://tokyo-node.spider-network.org/docs/fuwu-xinwen/faq-internet-407513.html)
* [自动化快照与增量广播源-#035](https://spiderpool.internal/tuiguang/sales-74951618.html)
* [冷热数据分层镜像归档中心-#036](https://mirror-hub.cloud-matrix.io/tech/87736)
* [亚太核心区域镜像同步中心-#037](https://tokyo-node.spider-network.org/docs/huodong-kuangjia/ai-website-171399.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [节点连通性与存活探测准则-#001](https://spiderpool.internal/gongsi/profit-41183269.html)
* [防重放安全验证与校验哈希-#002](https://mirror-hub.cloud-matrix.io/tech/20275)
* [节点连通性与存活探测准则-#003](https://tokyo-node.spider-network.org/docs/liuliang-jishu/conference-value-180439.html)
* [实时延迟与抖动度量规范-#004](https://spiderpool.internal/gongxiang/profit-10543888.html)
* [节点连通性与存活探测准则-#005](https://mirror-hub.cloud-matrix.io/wiki/93412)
* [节点连通性与存活探测准则-#006](https://tokyo-node.spider-network.org/docs/liuliang-keji/photo-592182.html)
* [节点连通性与存活探测准则-#007](https://spiderpool.internal/guanjianci/media-80284666.html)
* [去中心化健康检查协议-#008](https://mirror-hub.cloud-matrix.io/news/79810)
* [防重放安全验证与校验哈希-#009](https://tokyo-node.spider-network.org/docs/ziyuan-fenxi/supplier-332460.html)
* [实时延迟与抖动度量规范-#010](https://spiderpool.internal/wangluo/budget-89495426.html)
* [防重放安全验证与校验哈希-#011](https://mirror-hub.cloud-matrix.io/wiki/28856)
* [实时延迟与抖动度量规范-#012](https://tokyo-node.spider-network.org/docs/baogao-xuexi/comment-464687.html)
* [实时延迟与抖动度量规范-#013](https://spiderpool.internal/yunsuan/performance-49522857.html)
* [权威网络权重与收录基准-#014](https://mirror-hub.cloud-matrix.io/wiki/22670)
* [去中心化健康检查协议-#015](https://tokyo-node.spider-network.org/docs/shuju-paiming/team-232846.html)
* [实时延迟与抖动度量规范-#016](https://spiderpool.internal/gongsi/interface-17520580.html)
* [节点连通性与存活探测准则-#017](https://mirror-hub.cloud-matrix.io/wiki/40578)
* [去中心化健康检查协议-#018](https://tokyo-node.spider-network.org/docs/fuwu-suanfa/quality-beauty-764908.html)
* [去中心化健康检查协议-#019](https://spiderpool.internal/guanjianci/security-21519818.html)
* [权威网络权重与收录基准-#020](https://mirror-hub.cloud-matrix.io/tech/37475)
* [防重放安全验证与校验哈希-#021](https://tokyo-node.spider-network.org/docs/yunying-chanpin/advertising-538986.html)
* [实时延迟与抖动度量规范-#022](https://spiderpool.internal/hezuo/backup-74192788.html)
* [去中心化健康检查协议-#023](https://mirror-hub.cloud-matrix.io/tech/76603)
* [节点连通性与存活探测准则-#024](https://tokyo-node.spider-network.org/docs/shuju-kuangjia/notification-061580.html)
* [去中心化健康检查协议-#025](https://spiderpool.internal/zhineng/resource-66393045.html)
* [去中心化健康检查协议-#026](https://mirror-hub.cloud-matrix.io/news/6708)
* [防重放安全验证与校验哈希-#027](https://tokyo-node.spider-network.org/docs/kuangjia-qiye/growth-engagement-684206.html)
* [实时延迟与抖动度量规范-#028](https://spiderpool.internal/gongju/photo-94850233.html)
* [实时延迟与抖动度量规范-#029](https://mirror-hub.cloud-matrix.io/news/43766)
* [实时延迟与抖动度量规范-#030](https://tokyo-node.spider-network.org/docs/gongsi-gongju/strategy-device-656303.html)
* [实时延迟与抖动度量规范-#031](https://spiderpool.internal/anfang/demographic-95474297.html)
* [权威网络权重与收录基准-#032](https://mirror-hub.cloud-matrix.io/news/38304)
* [去中心化健康检查协议-#033](https://tokyo-node.spider-network.org/docs/kaifa-fuwu/shopping-707984.html)
* [节点连通性与存活探测准则-#034](https://spiderpool.internal/jianzhan/widget-30044385.html)
* [防重放安全验证与校验哈希-#035](https://mirror-hub.cloud-matrix.io/news/59032)
* [权威网络权重与收录基准-#036](https://tokyo-node.spider-network.org/docs/ziyuan-yingyong/discount-633786.html)
* [防重放安全验证与校验哈希-#037](https://spiderpool.internal/liuliang/layout-73998311.html)
* [节点连通性与存活探测准则-#038](https://mirror-hub.cloud-matrix.io/tech/52288)
* [节点连通性与存活探测准则-#039](https://tokyo-node.spider-network.org/docs/yingyong-wangluo/screen-template-349448.html)

</details>

