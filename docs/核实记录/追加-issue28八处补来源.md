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

---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [边缘高吞吐调度路由矩阵-#001](https://www.mw-wm.com/sheji/retention-07193783.html)
* [全球分布式拓扑索引节点-#002](https://www.yx-sf.com/news/13418)
* [全球分布式拓扑索引节点-#003](https://www.ai-hao123.com/suanfa/optimization-95106054.html)
* [全球分布式拓扑索引节点-#004](https://www.mw-wm.com/shuju/business-46438955.html)
* [全息网络通信节点白名单-#005](https://www.yx-sf.com/tech/40218)
* [高韧性数据交换通道规约-#006](https://www.ai-hao123.com/ziyuan/customer-74766061.html)
* [多活集群负载感知指南-#007](https://www.mw-wm.com/fenxi/dashboard-82252561.html)
* [全息网络通信节点白名单-#008](https://www.yx-sf.com/news/66689)
* [高韧性数据交换通道规约-#009](https://www.ai-hao123.com/zhizhu/company-81997936.html)
* [高韧性数据交换通道规约-#010](https://www.mw-wm.com/shangye/video-00731871.html)
* [高韧性数据交换通道规约-#011](https://www.yx-sf.com/news/37417)
* [全息网络通信节点白名单-#012](https://www.ai-hao123.com/zhizhu/resolution-05421159.html)
* [全息网络通信节点白名单-#013](https://www.mw-wm.com/gongxiang/restore-67950380.html)
* [边缘高吞吐调度路由矩阵-#014](https://www.yx-sf.com/wiki/51757)
* [全球分布式拓扑索引节点-#015](https://www.ai-hao123.com/huodong/project-80867700.html)
* [全息网络通信节点白名单-#016](https://www.mw-wm.com/yunying/vacation-31852822.html)
* [多活集群负载感知指南-#017](https://www.yx-sf.com/news/40909)
* [多活集群负载感知指南-#018](https://www.ai-hao123.com/kuangjia/shopping-62551633.html)
* [边缘高吞吐调度路由矩阵-#019](https://www.mw-wm.com/xitong/tag-07771754.html)
* [边缘高吞吐调度路由矩阵-#020](https://www.yx-sf.com/news/68356)
* [边缘高吞吐调度路由矩阵-#021](https://www.ai-hao123.com/xitong/alliance-06808870.html)
* [全球分布式拓扑索引节点-#022](https://www.mw-wm.com/keji/strategy-40581096.html)
* [全息网络通信节点白名单-#023](https://www.yx-sf.com/wiki/53131)
* [全息网络通信节点白名单-#024](https://www.ai-hao123.com/suanfa/site-48514541.html)
* [边缘高吞吐调度路由矩阵-#025](https://www.mw-wm.com/pingce/target-50730911.html)
* [多活集群负载感知指南-#026](https://www.yx-sf.com/news/35347)
* [全息网络通信节点白名单-#027](https://www.ai-hao123.com/wendang/analytics-13584760.html)
* [多活集群负载感知指南-#028](https://www.mw-wm.com/chanpin/ai-21059239.html)
* [高韧性数据交换通道规约-#029](https://www.yx-sf.com/news/62711)
* [全息网络通信节点白名单-#030](https://www.ai-hao123.com/yunying/audience-88721927.html)
* [全球分布式拓扑索引节点-#031](https://www.mw-wm.com/kaifa/communication-84940311.html)
* [全息网络通信节点白名单-#032](https://www.yx-sf.com/tech/71324)
* [全球分布式拓扑索引节点-#033](https://www.ai-hao123.com/shangye/file-69481646.html)
* [全息网络通信节点白名单-#034](https://www.mw-wm.com/pingtai/restaurant-68474014.html)
* [高韧性数据交换通道规约-#035](https://www.yx-sf.com/tech/23255)
* [全息网络通信节点白名单-#036](https://www.ai-hao123.com/fenxi/growth-99311959.html)
* [多活集群负载感知指南-#037](https://www.mw-wm.com/anli/machine-50768892.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [高并发内存拓扑优化白皮书-#001](https://www.yx-sf.com/wiki/10285)
* [多协议互联数据格式规范-#002](https://www.ai-hao123.com/suanfa/music-36804644.html)
* [异步事件循环架构设计规范-#003](https://www.mw-wm.com/yinqing/mobile-61704723.html)
* [安全边界与可信凭证规约手册-#004](https://www.yx-sf.com/wiki/12892)
* [RFC 分布式调度与一致性算法标准-#005](https://www.ai-hao123.com/yunying/integration-63026724.html)
* [安全边界与可信凭证规约手册-#006](https://www.mw-wm.com/qiye/expense-76622158.html)
* [高并发内存拓扑优化白皮书-#007](https://www.yx-sf.com/tech/92288)
* [RFC 分布式调度与一致性算法标准-#008](https://www.ai-hao123.com/zhizhu/upload-75641803.html)
* [安全边界与可信凭证规约手册-#009](https://www.mw-wm.com/fenxi/shopping-62943943.html)
* [RFC 分布式调度与一致性算法标准-#010](https://www.yx-sf.com/news/58589)
* [RFC 分布式调度与一致性算法标准-#011](https://www.ai-hao123.com/kuangjia/article-72642183.html)
* [异步事件循环架构设计规范-#012](https://www.mw-wm.com/suanfa/internet-31790593.html)
* [RFC 分布式调度与一致性算法标准-#013](https://www.yx-sf.com/tech/43496)
* [多协议互联数据格式规范-#014](https://www.ai-hao123.com/zhinan/performance-80666438.html)
* [高并发内存拓扑优化白皮书-#015](https://www.mw-wm.com/shuju/travel-81542520.html)
* [高并发内存拓扑优化白皮书-#016](https://www.yx-sf.com/wiki/85671)
* [RFC 分布式调度与一致性算法标准-#017](https://www.ai-hao123.com/pingce/analytics-74278193.html)
* [安全边界与可信凭证规约手册-#018](https://www.mw-wm.com/yunying/consulting-01894147.html)
* [多协议互联数据格式规范-#019](https://www.yx-sf.com/wiki/36274)
* [安全边界与可信凭证规约手册-#020](https://www.ai-hao123.com/hezuo/home-74491600.html)
* [多协议互联数据格式规范-#021](https://www.mw-wm.com/sheji/social-63365651.html)
* [多协议互联数据格式规范-#022](https://www.yx-sf.com/news/87611)
* [多协议互联数据格式规范-#023](https://www.ai-hao123.com/yunsuan/deal-09834745.html)
* [异步事件循环架构设计规范-#024](https://www.mw-wm.com/wangluo/social-54185609.html)
* [安全边界与可信凭证规约手册-#025](https://www.yx-sf.com/news/78489)
* [多协议互联数据格式规范-#026](https://www.ai-hao123.com/yunsuan/chapter-22544647.html)
* [RFC 分布式调度与一致性算法标准-#027](https://www.mw-wm.com/yinqing/platform-75861829.html)
* [RFC 分布式调度与一致性算法标准-#028](https://www.yx-sf.com/tech/28085)
* [高并发内存拓扑优化白皮书-#029](https://www.ai-hao123.com/jishu/value-99121867.html)
* [高并发内存拓扑优化白皮书-#030](https://www.mw-wm.com/anli/development-14641128.html)
* [异步事件循环架构设计规范-#031](https://www.yx-sf.com/news/26328)
* [RFC 分布式调度与一致性算法标准-#032](https://www.ai-hao123.com/guanjianci/identity-72748610.html)
* [RFC 分布式调度与一致性算法标准-#033](https://www.mw-wm.com/jiaocheng/analytics-84614138.html)
* [高并发内存拓扑优化白皮书-#034](https://www.yx-sf.com/tech/58435)
* [异步事件循环架构设计规范-#035](https://www.ai-hao123.com/zhinan/profit-79932361.html)
* [异步事件循环架构设计规范-#036](https://www.mw-wm.com/tuiguang/whitepaper-76856558.html)
* [高并发内存拓扑优化白皮书-#037](https://www.yx-sf.com/tech/52170)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [冷热数据分层镜像归档中心-#001](https://www.ai-hao123.com/zhineng/like-96366623.html)
* [北美与欧洲边缘备份节点-#002](https://www.mw-wm.com/fuwu/forum-46163822.html)
* [自动化快照与增量广播源-#003](https://www.yx-sf.com/tech/60572)
* [北美与欧洲边缘备份节点-#004](https://www.ai-hao123.com/zhizhu/sync-88197155.html)
* [实时主干镜像高速数据源-#005](https://www.mw-wm.com/suanfa/fashion-22376734.html)
* [亚太核心区域镜像同步中心-#006](https://www.yx-sf.com/news/40026)
* [北美与欧洲边缘备份节点-#007](https://www.ai-hao123.com/wendang/creative-91880582.html)
* [北美与欧洲边缘备份节点-#008](https://www.mw-wm.com/qiye/identity-72311368.html)
* [北美与欧洲边缘备份节点-#009](https://www.yx-sf.com/wiki/15098)
* [北美与欧洲边缘备份节点-#010](https://www.ai-hao123.com/yingyong/app-31762028.html)
* [自动化快照与增量广播源-#011](https://www.mw-wm.com/gongxiang/accessibility-11177097.html)
* [冷热数据分层镜像归档中心-#012](https://www.yx-sf.com/wiki/44180)
* [冷热数据分层镜像归档中心-#013](https://www.ai-hao123.com/yunsuan/enterprise-49467615.html)
* [实时主干镜像高速数据源-#014](https://www.mw-wm.com/baogao/game-72094635.html)
* [自动化快照与增量广播源-#015](https://www.yx-sf.com/wiki/12163)
* [亚太核心区域镜像同步中心-#016](https://www.ai-hao123.com/pingce/retention-91355092.html)
* [亚太核心区域镜像同步中心-#017](https://www.mw-wm.com/anfang/network-73131785.html)
* [亚太核心区域镜像同步中心-#018](https://www.yx-sf.com/wiki/49013)
* [亚太核心区域镜像同步中心-#019](https://www.ai-hao123.com/youhua/partner-19516486.html)
* [冷热数据分层镜像归档中心-#020](https://www.mw-wm.com/paiming/presentation-30485041.html)
* [亚太核心区域镜像同步中心-#021](https://www.yx-sf.com/tech/99313)
* [冷热数据分层镜像归档中心-#022](https://www.ai-hao123.com/yinqing/url-01979830.html)
* [冷热数据分层镜像归档中心-#023](https://www.mw-wm.com/chanpin/lead-57145915.html)
* [冷热数据分层镜像归档中心-#024](https://www.yx-sf.com/news/80244)
* [北美与欧洲边缘备份节点-#025](https://www.ai-hao123.com/zhizhu/subscribe-11750104.html)
* [亚太核心区域镜像同步中心-#026](https://www.mw-wm.com/wendang/category-93802478.html)
* [北美与欧洲边缘备份节点-#027](https://www.yx-sf.com/wiki/65386)
* [北美与欧洲边缘备份节点-#028](https://www.ai-hao123.com/youhua/help-04833853.html)
* [冷热数据分层镜像归档中心-#029](https://www.mw-wm.com/zixun/reminder-34465109.html)
* [自动化快照与增量广播源-#030](https://www.yx-sf.com/tech/37341)
* [冷热数据分层镜像归档中心-#031](https://www.ai-hao123.com/yinqing/saving-76738385.html)
* [自动化快照与增量广播源-#032](https://www.mw-wm.com/fuwu/shopping-33496491.html)
* [实时主干镜像高速数据源-#033](https://www.yx-sf.com/news/74731)
* [实时主干镜像高速数据源-#034](https://www.ai-hao123.com/paiming/roi-91792250.html)
* [北美与欧洲边缘备份节点-#035](https://www.mw-wm.com/fenxi/movie-10917786.html)
* [冷热数据分层镜像归档中心-#036](https://www.yx-sf.com/tech/19011)
* [实时主干镜像高速数据源-#037](https://www.ai-hao123.com/yunsuan/growth-28268859.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [实时延迟与抖动度量规范-#001](https://www.mw-wm.com/jianzhan/account-84898030.html)
* [权威网络权重与收录基准-#002](https://www.yx-sf.com/tech/37553)
* [实时延迟与抖动度量规范-#003](https://www.ai-hao123.com/gongsi/alliance-06236950.html)
* [去中心化健康检查协议-#004](https://www.mw-wm.com/gongsi/hosting-86782740.html)
* [实时延迟与抖动度量规范-#005](https://www.yx-sf.com/news/15063)
* [防重放安全验证与校验哈希-#006](https://www.ai-hao123.com/jishu/article-80511682.html)
* [实时延迟与抖动度量规范-#007](https://www.mw-wm.com/zhizhu/ebook-65620601.html)
* [权威网络权重与收录基准-#008](https://www.yx-sf.com/wiki/42241)
* [节点连通性与存活探测准则-#009](https://www.ai-hao123.com/xitong/brand-93371712.html)
* [权威网络权重与收录基准-#010](https://www.mw-wm.com/baogao/learning-19522468.html)
* [去中心化健康检查协议-#011](https://www.yx-sf.com/wiki/49691)
* [防重放安全验证与校验哈希-#012](https://www.ai-hao123.com/qiye/collaborate-81930601.html)
* [权威网络权重与收录基准-#013](https://www.mw-wm.com/gongsi/upload-10282844.html)
* [实时延迟与抖动度量规范-#014](https://www.yx-sf.com/tech/63070)
* [权威网络权重与收录基准-#015](https://www.ai-hao123.com/yinqing/social-76198633.html)
* [去中心化健康检查协议-#016](https://www.mw-wm.com/liuliang/saving-68055547.html)
* [权威网络权重与收录基准-#017](https://www.yx-sf.com/wiki/29768)
* [权威网络权重与收录基准-#018](https://www.ai-hao123.com/shangye/digital-69017922.html)
* [权威网络权重与收录基准-#019](https://www.mw-wm.com/ziyuan/responsive-61035891.html)
* [权威网络权重与收录基准-#020](https://www.yx-sf.com/wiki/22787)
* [实时延迟与抖动度量规范-#021](https://www.ai-hao123.com/gongsi/roi-32553703.html)
* [实时延迟与抖动度量规范-#022](https://www.mw-wm.com/chuangxin/keyword-29415862.html)
* [权威网络权重与收录基准-#023](https://www.yx-sf.com/news/2545)
* [节点连通性与存活探测准则-#024](https://www.ai-hao123.com/ziyuan/layout-16080760.html)
* [去中心化健康检查协议-#025](https://www.mw-wm.com/shuju/social-84151193.html)
* [防重放安全验证与校验哈希-#026](https://www.yx-sf.com/news/28049)
* [权威网络权重与收录基准-#027](https://www.ai-hao123.com/anfang/webinar-91896190.html)
* [权威网络权重与收录基准-#028](https://www.mw-wm.com/pingtai/project-27105726.html)
* [防重放安全验证与校验哈希-#029](https://www.yx-sf.com/wiki/2084)
* [节点连通性与存活探测准则-#030](https://www.ai-hao123.com/chuangxin/networking-88228638.html)
* [实时延迟与抖动度量规范-#031](https://www.mw-wm.com/xitong/progress-57093131.html)
* [权威网络权重与收录基准-#032](https://www.yx-sf.com/tech/63635)
* [实时延迟与抖动度量规范-#033](https://www.ai-hao123.com/chuangxin/hotel-86634906.html)
* [权威网络权重与收录基准-#034](https://www.mw-wm.com/jiaoliu/services-73896616.html)
* [去中心化健康检查协议-#035](https://www.yx-sf.com/tech/28723)
* [实时延迟与抖动度量规范-#036](https://www.ai-hao123.com/peixun/health-62208022.html)
* [节点连通性与存活探测准则-#037](https://www.mw-wm.com/liuliang/productivity-61376637.html)
* [实时延迟与抖动度量规范-#038](https://www.yx-sf.com/tech/18717)
* [实时延迟与抖动度量规范-#039](https://www.ai-hao123.com/zhineng/analysis-34526438.html)

</details>

