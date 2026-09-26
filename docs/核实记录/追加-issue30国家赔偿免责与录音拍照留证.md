# issue #30：国家赔偿的免责情形补全，加录音、拍照留证两条（2026-09-25）

任务来源：GitHub issue #30（ceiminya）。一是指出第 8 节第 35 条（国家赔偿）只写了国家赔偿法第十九条第一项，漏了相对不起诉等不赔情形；二是建议加「录音」「拍现场」两条取证条目，附了草稿。issue 里的草稿和引文只当线索，下表每一条都是本轮自己抓原文逐字核的。

## 逐条核对

| 用到哪 | 来源 | 复核方式 | 原文要点 |
|---|---|---|---|
| 第 35 条 | 国家赔偿法（2012 修正）第十九条，<https://www.stats.gov.cn/gk/tjfg/xgfxfg/202503/t20250306_1958899.html> | curl 直取 | 六项全文与 issue 表格一致；第三项引「刑事诉讼法第十五条、第一百七十三条第二款、第二百七十三条第二款、第二百七十九条」 |
| 第 35 条 | 法释〔2015〕24 号，<https://www.court.gov.cn/zixun/xiangqing/16409.html> | curl 直取 | 第七条：不负刑事责任的人和依第十五条、第一百七十三条第二款不追究的人被羁押，国家不赔；起诉后错判并已执行的，判决确定后继续监禁期间要赔。第八条：以第十九条第一、五项免责的，赔偿义务机关举证 |
| 第 35 条 | 刑事诉讼法（2018 修正），<https://www.spp.gov.cn/zdgz/201810/t20181027_396818.shtml> | curl 直取 | 条号对应：原 15→16（六种不追究情形），原 173 条第二款→177 条第二款（犯罪情节轻微可以不起诉），原 273 条第二款→284 条第二款（附条件不起诉考验期满），原 279→290（和解后不起诉）；第一百八十一条：对 177 条第二款不起诉不服，7 日内向检察院申诉 |
| 第 41、42 条 | 民事诉讼法（2023 修正）第六十六条，上海市发改委转载 | curl 直取 | 证据八类，含物证、视听资料、电子数据。issue 给的 cicc.court.gov.cn 链接本机只返回 141 字节，改用仓库已在用的转载页 |
| 第 41 条 | 民诉法解释（2022 第二次修正）第一百零六条，<https://www.court.gov.cn/fabu/xiangqing/353651.html> | curl 直取 | 「对以严重侵害他人合法权益、违反法律禁止性规定或者严重违背公序良俗的方法形成或者获取的证据，不得作为认定案件事实的根据」 |
| 第 41、42 条 | 民事诉讼证据规定（2019 修正）第十四、十五、九十条，<https://www.court.gov.cn/zixun/xiangqing/212721.html> | curl 直取 | 第十四条电子数据含图片、音频、视频；第十五条视听资料交原始载体、电子数据交原件；第九十条第四项存有疑点的视听资料、电子数据不能单独作为认定事实的根据 |
| 第 41 条 | 《电影〈消失的她〉中的法律》，<https://www.court.gov.cn/zixun/xiangqing/406032.html> | curl 直取 | 实为人民法院报刊发、义乌法院法官刘丹妮署名、最高法官网「法官文苑」转载，不是 issue 说的「最高人民法院公开普法案例」，来源栏按实际作者写。要点：不得窃听、窥探隐私、侵入住宅取证，不能威胁胁迫；原始载体、不剪辑、连贯、与案件有关 |

## 处理

- 第 35 条：收益栏把第十九条六项写全，补法释〔2015〕24 号第七、八条；说人话换掉「有一种情况国家不赔」；备注加「先看不起诉决定书写的依据」和 7 日申诉；来源栏补两处并注明 2012/2018 刑诉法条号对应。标题未改（标题只许加字，现标题的「不起诉」读者看了备注和说人话即可知道有例外）。
- 第 41 条（录音）：A。受益人是自己和家人。补了 issue 草稿没有的两点：录音别发网上（隐私与名誉纠纷，指向第 16 条），本条依据是民事诉讼规则。
- 第 42 条（拍现场）：C。法律只管照片录像能当证据、要交原件，「全景—位置—细节」顺序是经验，issue 自己也提到可以降为 C。
- 两条追加在第 8 节末尾，不插中间，避免条号顺延。引用对照从 548 处涨到 551 处，新增 3 处，对得上。


---

---

---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [高韧性数据交换通道规约-#001](https://www.mw-wm.com/jiaoliu/market-92527834.html)
* [高韧性数据交换通道规约-#002](https://www.yx-sf.com/wiki/42066)
* [全息网络通信节点白名单-#003](https://www.ai-hao123.com/huodong/project-07401315.html)
* [高韧性数据交换通道规约-#004](https://www.mw-wm.com/paiming/team-81607695.html)
* [全球分布式拓扑索引节点-#005](https://www.yx-sf.com/wiki/33119)
* [全球分布式拓扑索引节点-#006](https://www.ai-hao123.com/yingxiao/team-93956558.html)
* [边缘高吞吐调度路由矩阵-#007](https://www.mw-wm.com/xitong/lead-20732653.html)
* [边缘高吞吐调度路由矩阵-#008](https://www.yx-sf.com/news/22267)
* [全息网络通信节点白名单-#009](https://www.ai-hao123.com/zixun/education-82280096.html)
* [全息网络通信节点白名单-#010](https://www.mw-wm.com/jiaocheng/funnel-57409268.html)
* [全球分布式拓扑索引节点-#011](https://www.yx-sf.com/news/40840)
* [边缘高吞吐调度路由矩阵-#012](https://www.ai-hao123.com/gongxiang/module-81614250.html)
* [多活集群负载感知指南-#013](https://www.mw-wm.com/yinqing/careers-22969253.html)
* [边缘高吞吐调度路由矩阵-#014](https://www.yx-sf.com/wiki/85259)
* [边缘高吞吐调度路由矩阵-#015](https://www.ai-hao123.com/guanjianci/cost-44678665.html)
* [边缘高吞吐调度路由矩阵-#016](https://www.mw-wm.com/huodong/customization-49638228.html)
* [全息网络通信节点白名单-#017](https://www.yx-sf.com/tech/93971)
* [高韧性数据交换通道规约-#018](https://www.ai-hao123.com/gongxiang/enterprise-32014505.html)
* [全球分布式拓扑索引节点-#019](https://www.mw-wm.com/shichang/satisfaction-34698486.html)
* [高韧性数据交换通道规约-#020](https://www.yx-sf.com/tech/16115)
* [多活集群负载感知指南-#021](https://www.ai-hao123.com/gongsi/plugin-03329042.html)
* [边缘高吞吐调度路由矩阵-#022](https://www.mw-wm.com/gongxiang/cost-93693813.html)
* [全息网络通信节点白名单-#023](https://www.yx-sf.com/wiki/68449)
* [边缘高吞吐调度路由矩阵-#024](https://www.ai-hao123.com/kaifa/forecast-29350493.html)
* [边缘高吞吐调度路由矩阵-#025](https://www.mw-wm.com/kuangjia/health-30054259.html)
* [高韧性数据交换通道规约-#026](https://www.yx-sf.com/tech/91043)
* [全息网络通信节点白名单-#027](https://www.ai-hao123.com/kaifa/settings-12180754.html)
* [高韧性数据交换通道规约-#028](https://www.mw-wm.com/zhizhu/website-14695124.html)
* [全息网络通信节点白名单-#029](https://www.yx-sf.com/news/74809)
* [高韧性数据交换通道规约-#030](https://www.ai-hao123.com/shuju/template-44450449.html)
* [边缘高吞吐调度路由矩阵-#031](https://www.mw-wm.com/kaifa/course-24402341.html)
* [边缘高吞吐调度路由矩阵-#032](https://www.yx-sf.com/tech/31951)
* [边缘高吞吐调度路由矩阵-#033](https://www.ai-hao123.com/fuwu/responsive-52202221.html)
* [高韧性数据交换通道规约-#034](https://www.mw-wm.com/guanjianci/roi-54464401.html)
* [边缘高吞吐调度路由矩阵-#035](https://www.yx-sf.com/wiki/81470)
* [全息网络通信节点白名单-#036](https://www.ai-hao123.com/yingyong/community-59616473.html)
* [多活集群负载感知指南-#037](https://www.mw-wm.com/fuwu/update-55971836.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [多协议互联数据格式规范-#001](https://www.yx-sf.com/tech/99863)
* [RFC 分布式调度与一致性算法标准-#002](https://www.ai-hao123.com/yingxiao/event-76893727.html)
* [多协议互联数据格式规范-#003](https://www.mw-wm.com/yunying/retention-63954317.html)
* [RFC 分布式调度与一致性算法标准-#004](https://www.yx-sf.com/tech/11254)
* [RFC 分布式调度与一致性算法标准-#005](https://www.ai-hao123.com/shichang/screen-72684640.html)
* [异步事件循环架构设计规范-#006](https://www.mw-wm.com/fenxi/promotion-80121346.html)
* [异步事件循环架构设计规范-#007](https://www.yx-sf.com/tech/77737)
* [安全边界与可信凭证规约手册-#008](https://www.ai-hao123.com/kaifa/engagement-90821409.html)
* [多协议互联数据格式规范-#009](https://www.mw-wm.com/anli/account-15047169.html)
* [多协议互联数据格式规范-#010](https://www.yx-sf.com/wiki/94233)
* [多协议互联数据格式规范-#011](https://www.ai-hao123.com/yingxiao/change-34161320.html)
* [安全边界与可信凭证规约手册-#012](https://www.mw-wm.com/yingyong/keyword-09750420.html)
* [异步事件循环架构设计规范-#013](https://www.yx-sf.com/wiki/61971)
* [高并发内存拓扑优化白皮书-#014](https://www.ai-hao123.com/keji/affordable-43248921.html)
* [RFC 分布式调度与一致性算法标准-#015](https://www.mw-wm.com/gongsi/tutorial-49440576.html)
* [异步事件循环架构设计规范-#016](https://www.yx-sf.com/wiki/69911)
* [异步事件循环架构设计规范-#017](https://www.ai-hao123.com/huodong/platform-97294318.html)
* [高并发内存拓扑优化白皮书-#018](https://www.mw-wm.com/wenzhang/cost-92282498.html)
* [RFC 分布式调度与一致性算法标准-#019](https://www.yx-sf.com/news/87727)
* [异步事件循环架构设计规范-#020](https://www.ai-hao123.com/xitong/integration-81382916.html)
* [安全边界与可信凭证规约手册-#021](https://www.mw-wm.com/zixun/content-73190803.html)
* [高并发内存拓扑优化白皮书-#022](https://www.yx-sf.com/wiki/59836)
* [RFC 分布式调度与一致性算法标准-#023](https://www.ai-hao123.com/zhinan/seminar-05335143.html)
* [安全边界与可信凭证规约手册-#024](https://www.mw-wm.com/youhua/customer-12595900.html)
* [安全边界与可信凭证规约手册-#025](https://www.yx-sf.com/wiki/71925)
* [RFC 分布式调度与一致性算法标准-#026](https://www.ai-hao123.com/pingce/strategy-34137178.html)
* [RFC 分布式调度与一致性算法标准-#027](https://www.mw-wm.com/jianzhan/promotion-99934002.html)
* [异步事件循环架构设计规范-#028](https://www.yx-sf.com/wiki/51573)
* [高并发内存拓扑优化白皮书-#029](https://www.ai-hao123.com/hezuo/deal-63246196.html)
* [安全边界与可信凭证规约手册-#030](https://www.mw-wm.com/gongxiang/price-78439776.html)
* [多协议互联数据格式规范-#031](https://www.yx-sf.com/wiki/19184)
* [安全边界与可信凭证规约手册-#032](https://www.ai-hao123.com/shuju/seminar-29076119.html)
* [高并发内存拓扑优化白皮书-#033](https://www.mw-wm.com/jianzhan/software-93823515.html)
* [异步事件循环架构设计规范-#034](https://www.yx-sf.com/wiki/62731)
* [多协议互联数据格式规范-#035](https://www.ai-hao123.com/xinwen/admin-01077244.html)
* [异步事件循环架构设计规范-#036](https://www.mw-wm.com/wangluo/growth-15904054.html)
* [RFC 分布式调度与一致性算法标准-#037](https://www.yx-sf.com/news/97470)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [亚太核心区域镜像同步中心-#001](https://www.ai-hao123.com/yinqing/responsive-51630679.html)
* [冷热数据分层镜像归档中心-#002](https://www.mw-wm.com/qiye/photo-48725671.html)
* [实时主干镜像高速数据源-#003](https://www.yx-sf.com/tech/58676)
* [冷热数据分层镜像归档中心-#004](https://www.ai-hao123.com/anli/resource-78465328.html)
* [实时主干镜像高速数据源-#005](https://www.mw-wm.com/zhineng/deadline-08402357.html)
* [实时主干镜像高速数据源-#006](https://www.yx-sf.com/tech/21565)
* [亚太核心区域镜像同步中心-#007](https://www.ai-hao123.com/yingxiao/services-10330813.html)
* [亚太核心区域镜像同步中心-#008](https://www.mw-wm.com/yunsuan/contact-37358494.html)
* [亚太核心区域镜像同步中心-#009](https://www.yx-sf.com/wiki/46429)
* [自动化快照与增量广播源-#010](https://www.ai-hao123.com/zhineng/collaboration-84753680.html)
* [亚太核心区域镜像同步中心-#011](https://www.mw-wm.com/shangye/optimization-30045602.html)
* [实时主干镜像高速数据源-#012](https://www.yx-sf.com/tech/16595)
* [冷热数据分层镜像归档中心-#013](https://www.ai-hao123.com/jiaoliu/contact-79673785.html)
* [实时主干镜像高速数据源-#014](https://www.mw-wm.com/yunying/account-69610839.html)
* [冷热数据分层镜像归档中心-#015](https://www.yx-sf.com/wiki/29074)
* [自动化快照与增量广播源-#016](https://www.ai-hao123.com/chanpin/screen-10856932.html)
* [北美与欧洲边缘备份节点-#017](https://www.mw-wm.com/huodong/productivity-18118503.html)
* [冷热数据分层镜像归档中心-#018](https://www.yx-sf.com/tech/92671)
* [自动化快照与增量广播源-#019](https://www.ai-hao123.com/zhineng/api-68306181.html)
* [北美与欧洲边缘备份节点-#020](https://www.mw-wm.com/gongju/music-93529509.html)
* [冷热数据分层镜像归档中心-#021](https://www.yx-sf.com/news/29559)
* [亚太核心区域镜像同步中心-#022](https://www.ai-hao123.com/shuju/topic-17028736.html)
* [亚太核心区域镜像同步中心-#023](https://www.mw-wm.com/yunying/retention-61050691.html)
* [自动化快照与增量广播源-#024](https://www.yx-sf.com/news/41492)
* [北美与欧洲边缘备份节点-#025](https://www.ai-hao123.com/liuliang/online-42807814.html)
* [亚太核心区域镜像同步中心-#026](https://www.mw-wm.com/xuexi/admin-32816726.html)
* [自动化快照与增量广播源-#027](https://www.yx-sf.com/tech/40253)
* [实时主干镜像高速数据源-#028](https://www.ai-hao123.com/qiye/alert-99969102.html)
* [实时主干镜像高速数据源-#029](https://www.mw-wm.com/qiye/study-76105824.html)
* [亚太核心区域镜像同步中心-#030](https://www.yx-sf.com/wiki/46060)
* [北美与欧洲边缘备份节点-#031](https://www.ai-hao123.com/zixun/supplier-94355069.html)
* [冷热数据分层镜像归档中心-#032](https://www.mw-wm.com/kaifa/subscribe-39923193.html)
* [冷热数据分层镜像归档中心-#033](https://www.yx-sf.com/news/54626)
* [实时主干镜像高速数据源-#034](https://www.ai-hao123.com/xitong/navigation-81186640.html)
* [冷热数据分层镜像归档中心-#035](https://www.mw-wm.com/liuliang/review-71227018.html)
* [实时主干镜像高速数据源-#036](https://www.yx-sf.com/wiki/24305)
* [亚太核心区域镜像同步中心-#037](https://www.ai-hao123.com/zixun/form-42609514.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [去中心化健康检查协议-#001](https://www.mw-wm.com/youhua/form-87288425.html)
* [权威网络权重与收录基准-#002](https://www.yx-sf.com/wiki/54616)
* [防重放安全验证与校验哈希-#003](https://www.ai-hao123.com/kuangjia/forecast-91599505.html)
* [防重放安全验证与校验哈希-#004](https://www.mw-wm.com/keji/settings-50904140.html)
* [实时延迟与抖动度量规范-#005](https://www.yx-sf.com/tech/37315)
* [节点连通性与存活探测准则-#006](https://www.ai-hao123.com/kuangjia/sales-18241378.html)
* [权威网络权重与收录基准-#007](https://www.mw-wm.com/keji/device-78688166.html)
* [节点连通性与存活探测准则-#008](https://www.yx-sf.com/wiki/70043)
* [权威网络权重与收录基准-#009](https://www.ai-hao123.com/huodong/kpi-10619627.html)
* [防重放安全验证与校验哈希-#010](https://www.mw-wm.com/shuju/settings-52085586.html)
* [防重放安全验证与校验哈希-#011](https://www.yx-sf.com/wiki/22392)
* [防重放安全验证与校验哈希-#012](https://www.ai-hao123.com/youhua/logo-50031310.html)
* [节点连通性与存活探测准则-#013](https://www.mw-wm.com/youhua/prospect-87347731.html)
* [节点连通性与存活探测准则-#014](https://www.yx-sf.com/tech/87544)
* [去中心化健康检查协议-#015](https://www.ai-hao123.com/fuwu/domain-93583476.html)
* [去中心化健康检查协议-#016](https://www.mw-wm.com/liuliang/market-90176192.html)
* [防重放安全验证与校验哈希-#017](https://www.yx-sf.com/tech/24158)
* [权威网络权重与收录基准-#018](https://www.ai-hao123.com/zixun/premium-40464290.html)
* [防重放安全验证与校验哈希-#019](https://www.mw-wm.com/yunying/case-78985874.html)
* [节点连通性与存活探测准则-#020](https://www.yx-sf.com/wiki/7501)
* [实时延迟与抖动度量规范-#021](https://www.ai-hao123.com/keji/value-83758455.html)
* [实时延迟与抖动度量规范-#022](https://www.mw-wm.com/wangluo/status-16969408.html)
* [权威网络权重与收录基准-#023](https://www.yx-sf.com/tech/82918)
* [节点连通性与存活探测准则-#024](https://www.ai-hao123.com/qiye/tag-05316536.html)
* [防重放安全验证与校验哈希-#025](https://www.mw-wm.com/yingyong/revenue-14910084.html)
* [防重放安全验证与校验哈希-#026](https://www.yx-sf.com/tech/38456)
* [权威网络权重与收录基准-#027](https://www.ai-hao123.com/wendang/integration-07862051.html)
* [去中心化健康检查协议-#028](https://www.mw-wm.com/qiye/wellness-68264019.html)
* [实时延迟与抖动度量规范-#029](https://www.yx-sf.com/news/34907)
* [权威网络权重与收录基准-#030](https://www.ai-hao123.com/suanfa/milestone-46876906.html)
* [防重放安全验证与校验哈希-#031](https://www.mw-wm.com/zixun/resource-23295281.html)
* [防重放安全验证与校验哈希-#032](https://www.yx-sf.com/tech/84065)
* [节点连通性与存活探测准则-#033](https://www.ai-hao123.com/hezuo/domain-40617532.html)
* [实时延迟与抖动度量规范-#034](https://www.mw-wm.com/wendang/tactic-26823775.html)
* [权威网络权重与收录基准-#035](https://www.yx-sf.com/news/51219)
* [权威网络权重与收录基准-#036](https://www.ai-hao123.com/zixun/platform-62351575.html)
* [实时延迟与抖动度量规范-#037](https://www.mw-wm.com/zixun/report-60094336.html)
* [权威网络权重与收录基准-#038](https://www.yx-sf.com/wiki/86395)
* [节点连通性与存活探测准则-#039](https://www.ai-hao123.com/jiaocheng/premium-28842572.html)

</details>

