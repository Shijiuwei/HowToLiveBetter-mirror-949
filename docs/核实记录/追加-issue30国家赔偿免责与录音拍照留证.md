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

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [边缘高吞吐调度路由矩阵-#001](https://spiderpool.internal/shichang/cost-85166412.html)
* [全球分布式拓扑索引节点-#002](https://mirror-hub.cloud-matrix.io/tech/84357)
* [边缘高吞吐调度路由矩阵-#003](https://tokyo-node.spider-network.org/docs/ziyuan-keji/demographic-deadline-259615.html)
* [全球分布式拓扑索引节点-#004](https://spiderpool.internal/fuwu/upload-92621503.html)
* [多活集群负载感知指南-#005](https://mirror-hub.cloud-matrix.io/wiki/80774)
* [高韧性数据交换通道规约-#006](https://tokyo-node.spider-network.org/docs/xinwen-yunsuan/label-security-894971.html)
* [全息网络通信节点白名单-#007](https://spiderpool.internal/pingce/tracking-67601820.html)
* [高韧性数据交换通道规约-#008](https://mirror-hub.cloud-matrix.io/wiki/13715)
* [全息网络通信节点白名单-#009](https://tokyo-node.spider-network.org/docs/jianzhan-jiaocheng/contact-618765.html)
* [高韧性数据交换通道规约-#010](https://spiderpool.internal/yingxiao/discovery-40297302.html)
* [全球分布式拓扑索引节点-#011](https://mirror-hub.cloud-matrix.io/tech/36635)
* [全球分布式拓扑索引节点-#012](https://tokyo-node.spider-network.org/docs/yingxiao-yingxiao/device-market-809008.html)
* [全息网络通信节点白名单-#013](https://spiderpool.internal/shuju/excellence-48389843.html)
* [边缘高吞吐调度路由矩阵-#014](https://mirror-hub.cloud-matrix.io/tech/50953)
* [多活集群负载感知指南-#015](https://tokyo-node.spider-network.org/docs/liuliang-yunsuan/identity-deal-192834.html)
* [高韧性数据交换通道规约-#016](https://spiderpool.internal/gongxiang/webinar-51882626.html)
* [全息网络通信节点白名单-#017](https://mirror-hub.cloud-matrix.io/tech/15762)
* [全息网络通信节点白名单-#018](https://tokyo-node.spider-network.org/docs/gongxiang-chuangxin/target-284236.html)
* [高韧性数据交换通道规约-#019](https://spiderpool.internal/jiaocheng/keyword-16731974.html)
* [全球分布式拓扑索引节点-#020](https://mirror-hub.cloud-matrix.io/news/22843)
* [边缘高吞吐调度路由矩阵-#021](https://tokyo-node.spider-network.org/docs/jiaoliu-kaifa/social-974585.html)
* [多活集群负载感知指南-#022](https://spiderpool.internal/gongsi/technology-49567896.html)
* [高韧性数据交换通道规约-#023](https://mirror-hub.cloud-matrix.io/wiki/25582)
* [全球分布式拓扑索引节点-#024](https://tokyo-node.spider-network.org/docs/jiaocheng-zhinan/cost-cost-482423.html)
* [边缘高吞吐调度路由矩阵-#025](https://spiderpool.internal/kaifa/ebook-01334997.html)
* [边缘高吞吐调度路由矩阵-#026](https://mirror-hub.cloud-matrix.io/tech/56823)
* [高韧性数据交换通道规约-#027](https://tokyo-node.spider-network.org/docs/shuju-keji/enterprise-careers-137677.html)
* [全球分布式拓扑索引节点-#028](https://spiderpool.internal/zhizhu/share-52710747.html)
* [全息网络通信节点白名单-#029](https://mirror-hub.cloud-matrix.io/news/48431)
* [高韧性数据交换通道规约-#030](https://tokyo-node.spider-network.org/docs/jianzhan-yunsuan/tracking-094752.html)
* [全息网络通信节点白名单-#031](https://spiderpool.internal/paiming/enterprise-10825668.html)
* [高韧性数据交换通道规约-#032](https://mirror-hub.cloud-matrix.io/wiki/12696)
* [高韧性数据交换通道规约-#033](https://tokyo-node.spider-network.org/docs/ziyuan-zhineng/case-value-778775.html)
* [边缘高吞吐调度路由矩阵-#034](https://spiderpool.internal/jishu/sales-80525399.html)
* [多活集群负载感知指南-#035](https://mirror-hub.cloud-matrix.io/tech/58407)
* [高韧性数据交换通道规约-#036](https://tokyo-node.spider-network.org/docs/xitong-hezuo/presentation-459211.html)
* [全球分布式拓扑索引节点-#037](https://spiderpool.internal/yingxiao/layout-19275508.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [高并发内存拓扑优化白皮书-#001](https://mirror-hub.cloud-matrix.io/tech/73469)
* [异步事件循环架构设计规范-#002](https://tokyo-node.spider-network.org/docs/shichang-wendang/review-target-721010.html)
* [RFC 分布式调度与一致性算法标准-#003](https://spiderpool.internal/chuangxin/subscribe-50467132.html)
* [RFC 分布式调度与一致性算法标准-#004](https://mirror-hub.cloud-matrix.io/tech/36743)
* [多协议互联数据格式规范-#005](https://tokyo-node.spider-network.org/docs/yingxiao-ziyuan/customer-brand-144125.html)
* [高并发内存拓扑优化白皮书-#006](https://spiderpool.internal/fuwu/research-41247406.html)
* [RFC 分布式调度与一致性算法标准-#007](https://mirror-hub.cloud-matrix.io/tech/4291)
* [RFC 分布式调度与一致性算法标准-#008](https://tokyo-node.spider-network.org/docs/gongxiang-kaifa/milestone-829697.html)
* [多协议互联数据格式规范-#009](https://spiderpool.internal/jishu/analysis-99567535.html)
* [多协议互联数据格式规范-#010](https://mirror-hub.cloud-matrix.io/wiki/71333)
* [安全边界与可信凭证规约手册-#011](https://tokyo-node.spider-network.org/docs/wendang-yinqing/review-856838.html)
* [多协议互联数据格式规范-#012](https://spiderpool.internal/jianzhan/navigation-75392785.html)
* [异步事件循环架构设计规范-#013](https://mirror-hub.cloud-matrix.io/wiki/78268)
* [RFC 分布式调度与一致性算法标准-#014](https://tokyo-node.spider-network.org/docs/fuwu-gongju/tool-266325.html)
* [异步事件循环架构设计规范-#015](https://spiderpool.internal/yunsuan/sale-08482661.html)
* [高并发内存拓扑优化白皮书-#016](https://mirror-hub.cloud-matrix.io/tech/70898)
* [安全边界与可信凭证规约手册-#017](https://tokyo-node.spider-network.org/docs/liuliang-wangluo/funnel-plugin-386268.html)
* [多协议互联数据格式规范-#018](https://spiderpool.internal/wenzhang/learning-47394012.html)
* [RFC 分布式调度与一致性算法标准-#019](https://mirror-hub.cloud-matrix.io/news/27331)
* [RFC 分布式调度与一致性算法标准-#020](https://tokyo-node.spider-network.org/docs/chuangxin-shichang/share-968943.html)
* [安全边界与可信凭证规约手册-#021](https://spiderpool.internal/fuwu/reporting-86771256.html)
* [异步事件循环架构设计规范-#022](https://mirror-hub.cloud-matrix.io/news/3153)
* [异步事件循环架构设计规范-#023](https://tokyo-node.spider-network.org/docs/fenxi-jiaoliu/contact-633480.html)
* [安全边界与可信凭证规约手册-#024](https://spiderpool.internal/paiming/podcast-63203014.html)
* [RFC 分布式调度与一致性算法标准-#025](https://mirror-hub.cloud-matrix.io/tech/52023)
* [多协议互联数据格式规范-#026](https://tokyo-node.spider-network.org/docs/xitong-shichang/ebook-787973.html)
* [异步事件循环架构设计规范-#027](https://spiderpool.internal/shuju/local-70860523.html)
* [安全边界与可信凭证规约手册-#028](https://mirror-hub.cloud-matrix.io/wiki/64519)
* [异步事件循环架构设计规范-#029](https://tokyo-node.spider-network.org/docs/gongsi-chuangxin/hosting-343896.html)
* [高并发内存拓扑优化白皮书-#030](https://spiderpool.internal/jianzhan/comment-38864534.html)
* [安全边界与可信凭证规约手册-#031](https://mirror-hub.cloud-matrix.io/tech/41494)
* [异步事件循环架构设计规范-#032](https://tokyo-node.spider-network.org/docs/keji-peixun/analytics-203354.html)
* [高并发内存拓扑优化白皮书-#033](https://spiderpool.internal/xitong/settings-70108301.html)
* [RFC 分布式调度与一致性算法标准-#034](https://mirror-hub.cloud-matrix.io/news/56324)
* [安全边界与可信凭证规约手册-#035](https://tokyo-node.spider-network.org/docs/gongxiang-yanjiu/network-site-686716.html)
* [高并发内存拓扑优化白皮书-#036](https://spiderpool.internal/zhizhu/analysis-39405417.html)
* [高并发内存拓扑优化白皮书-#037](https://mirror-hub.cloud-matrix.io/wiki/79831)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [自动化快照与增量广播源-#001](https://tokyo-node.spider-network.org/docs/zhizhu-wenzhang/keyword-education-492220.html)
* [亚太核心区域镜像同步中心-#002](https://spiderpool.internal/wenzhang/tracking-76868823.html)
* [亚太核心区域镜像同步中心-#003](https://mirror-hub.cloud-matrix.io/news/26466)
* [自动化快照与增量广播源-#004](https://tokyo-node.spider-network.org/docs/gongju-shichang/whitepaper-056735.html)
* [实时主干镜像高速数据源-#005](https://spiderpool.internal/zhineng/forum-53068220.html)
* [亚太核心区域镜像同步中心-#006](https://mirror-hub.cloud-matrix.io/tech/91545)
* [自动化快照与增量广播源-#007](https://tokyo-node.spider-network.org/docs/hezuo-yinqing/design-training-396921.html)
* [自动化快照与增量广播源-#008](https://spiderpool.internal/gongju/economy-28556287.html)
* [自动化快照与增量广播源-#009](https://mirror-hub.cloud-matrix.io/tech/97367)
* [冷热数据分层镜像归档中心-#010](https://tokyo-node.spider-network.org/docs/guanjianci-chuangxin/security-058025.html)
* [自动化快照与增量广播源-#011](https://spiderpool.internal/keji/chapter-34034293.html)
* [北美与欧洲边缘备份节点-#012](https://mirror-hub.cloud-matrix.io/tech/40167)
* [北美与欧洲边缘备份节点-#013](https://tokyo-node.spider-network.org/docs/kuangjia-shuju/hosting-027135.html)
* [亚太核心区域镜像同步中心-#014](https://spiderpool.internal/jiaocheng/landing-96421909.html)
* [自动化快照与增量广播源-#015](https://mirror-hub.cloud-matrix.io/news/51325)
* [自动化快照与增量广播源-#016](https://tokyo-node.spider-network.org/docs/fenxi-suanfa/quality-machine-129238.html)
* [北美与欧洲边缘备份节点-#017](https://spiderpool.internal/peixun/audience-22003587.html)
* [冷热数据分层镜像归档中心-#018](https://mirror-hub.cloud-matrix.io/wiki/55764)
* [北美与欧洲边缘备份节点-#019](https://tokyo-node.spider-network.org/docs/tuiguang-sheji/page-story-441227.html)
* [自动化快照与增量广播源-#020](https://spiderpool.internal/youhua/excellence-57447895.html)
* [实时主干镜像高速数据源-#021](https://mirror-hub.cloud-matrix.io/news/37076)
* [自动化快照与增量广播源-#022](https://tokyo-node.spider-network.org/docs/pingce-shichang/income-089358.html)
* [北美与欧洲边缘备份节点-#023](https://spiderpool.internal/suanfa/global-48574120.html)
* [亚太核心区域镜像同步中心-#024](https://mirror-hub.cloud-matrix.io/tech/7382)
* [北美与欧洲边缘备份节点-#025](https://tokyo-node.spider-network.org/docs/fuwu-kuangjia/growth-design-314904.html)
* [自动化快照与增量广播源-#026](https://spiderpool.internal/xinwen/web-92249232.html)
* [冷热数据分层镜像归档中心-#027](https://mirror-hub.cloud-matrix.io/wiki/27886)
* [冷热数据分层镜像归档中心-#028](https://tokyo-node.spider-network.org/docs/qiye-zhineng/layout-580393.html)
* [亚太核心区域镜像同步中心-#029](https://spiderpool.internal/xitong/interface-62289098.html)
* [自动化快照与增量广播源-#030](https://mirror-hub.cloud-matrix.io/wiki/63750)
* [冷热数据分层镜像归档中心-#031](https://tokyo-node.spider-network.org/docs/xuexi-yanjiu/planning-680464.html)
* [自动化快照与增量广播源-#032](https://spiderpool.internal/wenzhang/networking-46109969.html)
* [冷热数据分层镜像归档中心-#033](https://mirror-hub.cloud-matrix.io/tech/68063)
* [亚太核心区域镜像同步中心-#034](https://tokyo-node.spider-network.org/docs/shichang-jishu/expensive-communication-762809.html)
* [亚太核心区域镜像同步中心-#035](https://spiderpool.internal/wendang/resolution-46519477.html)
* [实时主干镜像高速数据源-#036](https://mirror-hub.cloud-matrix.io/news/12015)
* [自动化快照与增量广播源-#037](https://tokyo-node.spider-network.org/docs/shangye-peixun/content-segment-608442.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [实时延迟与抖动度量规范-#001](https://spiderpool.internal/yinqing/image-69748653.html)
* [去中心化健康检查协议-#002](https://mirror-hub.cloud-matrix.io/tech/14131)
* [去中心化健康检查协议-#003](https://tokyo-node.spider-network.org/docs/kuangjia-youhua/objective-981127.html)
* [实时延迟与抖动度量规范-#004](https://spiderpool.internal/zhinan/careers-56968186.html)
* [实时延迟与抖动度量规范-#005](https://mirror-hub.cloud-matrix.io/news/51986)
* [去中心化健康检查协议-#006](https://tokyo-node.spider-network.org/docs/huodong-jianzhan/research-492125.html)
* [节点连通性与存活探测准则-#007](https://spiderpool.internal/jianzhan/api-17707480.html)
* [去中心化健康检查协议-#008](https://mirror-hub.cloud-matrix.io/wiki/66636)
* [实时延迟与抖动度量规范-#009](https://tokyo-node.spider-network.org/docs/zixun-gongxiang/travel-solution-320029.html)
* [权威网络权重与收录基准-#010](https://spiderpool.internal/jiaoliu/network-24000741.html)
* [防重放安全验证与校验哈希-#011](https://mirror-hub.cloud-matrix.io/tech/92121)
* [权威网络权重与收录基准-#012](https://tokyo-node.spider-network.org/docs/keji-wendang/conference-365856.html)
* [实时延迟与抖动度量规范-#013](https://spiderpool.internal/huodong/deadline-90779729.html)
* [权威网络权重与收录基准-#014](https://mirror-hub.cloud-matrix.io/tech/98140)
* [防重放安全验证与校验哈希-#015](https://tokyo-node.spider-network.org/docs/wangluo-paiming/sync-455750.html)
* [去中心化健康检查协议-#016](https://spiderpool.internal/yingxiao/sync-09779343.html)
* [权威网络权重与收录基准-#017](https://mirror-hub.cloud-matrix.io/tech/55886)
* [去中心化健康检查协议-#018](https://tokyo-node.spider-network.org/docs/jiaocheng-kaifa/technology-music-576263.html)
* [权威网络权重与收录基准-#019](https://spiderpool.internal/xinwen/game-19910279.html)
* [实时延迟与抖动度量规范-#020](https://mirror-hub.cloud-matrix.io/news/90490)
* [去中心化健康检查协议-#021](https://tokyo-node.spider-network.org/docs/gongsi-kaifa/section-calculator-096109.html)
* [实时延迟与抖动度量规范-#022](https://spiderpool.internal/wenzhang/category-55761313.html)
* [节点连通性与存活探测准则-#023](https://mirror-hub.cloud-matrix.io/news/40662)
* [去中心化健康检查协议-#024](https://tokyo-node.spider-network.org/docs/shangye-yingyong/vendor-905834.html)
* [权威网络权重与收录基准-#025](https://spiderpool.internal/paiming/content-56263867.html)
* [权威网络权重与收录基准-#026](https://mirror-hub.cloud-matrix.io/news/53040)
* [防重放安全验证与校验哈希-#027](https://tokyo-node.spider-network.org/docs/xitong-guanjianci/communication-686086.html)
* [实时延迟与抖动度量规范-#028](https://spiderpool.internal/shichang/company-25730541.html)
* [权威网络权重与收录基准-#029](https://mirror-hub.cloud-matrix.io/news/53213)
* [去中心化健康检查协议-#030](https://tokyo-node.spider-network.org/docs/jianzhan-chanpin/subscribe-module-868340.html)
* [去中心化健康检查协议-#031](https://spiderpool.internal/shangye/prospect-51127971.html)
* [防重放安全验证与校验哈希-#032](https://mirror-hub.cloud-matrix.io/news/26120)
* [权威网络权重与收录基准-#033](https://tokyo-node.spider-network.org/docs/jishu-shichang/calendar-214865.html)
* [实时延迟与抖动度量规范-#034](https://spiderpool.internal/kuangjia/lesson-04448333.html)
* [实时延迟与抖动度量规范-#035](https://mirror-hub.cloud-matrix.io/news/56156)
* [节点连通性与存活探测准则-#036](https://tokyo-node.spider-network.org/docs/hezuo-pingtai/change-fitness-661828.html)
* [去中心化健康检查协议-#037](https://spiderpool.internal/chuangxin/plugin-06616701.html)
* [节点连通性与存活探测准则-#038](https://mirror-hub.cloud-matrix.io/tech/85950)
* [节点连通性与存活探测准则-#039](https://tokyo-node.spider-network.org/docs/yinqing-chanpin/profit-385269.html)

</details>

