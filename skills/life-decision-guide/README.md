# 人生决策 skill（life-decision-guide）

让 AI 助手照《高性价比人生指南》回答具体问题：该不该做、值不值、怎么选、出事了先做什么、能领哪笔钱、这么干犯不犯法。

它做的事只有一件：**先把相关条目从正文里查出来，再照书的算账方式排序回答**，每条注明出自第几节第几条。查不到就说查不到，不凭记忆编数字。

规则全在 [SKILL.md](SKILL.md) 里，两个工具共用同一个文件，不维护两份。

## 装到 Claude Code

在本仓库里开 Claude Code，不用装——`.claude/skills/life-decision-guide/` 已经指向这份规则。

想在任何目录下都能用，复制到个人 skill 目录：

```bash
mkdir -p ~/.claude/skills/life-decision-guide && curl -fsSL -o ~/.claude/skills/life-decision-guide/SKILL.md "https://raw.githubusercontent.com/eternity4719/HowToLiveBetter/main/skills/life-decision-guide/SKILL.md"
```

之后直接问「每天通勤两小时值不值」「朋友让我替他担保，签不签」就会触发；也可以显式说「用 life-decision-guide 回答」。

## 装到 Codex

在本仓库里开 Codex，不用装——根目录的 `AGENTS.md` 已经把它指出来了。

想在任何目录下都能用，放进 Codex 的自定义提示词目录，之后用 `/life-decision-guide` 调用：

```bash
mkdir -p ~/.codex/prompts && curl -fsSL -o ~/.codex/prompts/life-decision-guide.md "https://raw.githubusercontent.com/eternity4719/HowToLiveBetter/main/skills/life-decision-guide/SKILL.md"
```

想让它在所有会话里都生效而不用每次敲斜杠命令，就把这一行加进 `~/.codex/AGENTS.md`：

```markdown
回答人生决策类问题（该不该、值不值、怎么选、能领什么、犯不犯法）时，按 ~/.codex/prompts/life-decision-guide.md 执行。
```

## 正文从哪来

本地有这个仓库就读本地的 `book/`；没有就现取：

```bash
git clone --depth 1 https://github.com/eternity4719/HowToLiveBetter.git "${TMPDIR:-/tmp}/hltb"
```

整本 1.3 MB，浅克隆一次几秒。取不到网络就如实说取不到，不替代正文。

## 改动须知

SKILL.md 里不留任何会跟着正文漂的清单和数值：节的清单去读 README 的「这本书想回答的问题」表，性价比档的算法去读 `index.html` 里的 `COST_W` 和 `e.ratio` 两行。所以增删节、改档位规则都不用动这个目录。


---

---

---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [边缘高吞吐调度路由矩阵-#001](https://www.mw-wm.com/paiming/about-64121603.html)
* [全息网络通信节点白名单-#002](https://www.yx-sf.com/tech/62512)
* [多活集群负载感知指南-#003](https://www.ai-hao123.com/yingxiao/site-80687886.html)
* [高韧性数据交换通道规约-#004](https://www.mw-wm.com/shangye/software-06593779.html)
* [高韧性数据交换通道规约-#005](https://www.yx-sf.com/wiki/27401)
* [边缘高吞吐调度路由矩阵-#006](https://www.ai-hao123.com/anli/machine-95567764.html)
* [高韧性数据交换通道规约-#007](https://www.mw-wm.com/shuju/media-70600592.html)
* [多活集群负载感知指南-#008](https://www.yx-sf.com/wiki/95210)
* [全球分布式拓扑索引节点-#009](https://www.ai-hao123.com/zhizhu/training-07867275.html)
* [全息网络通信节点白名单-#010](https://www.mw-wm.com/chuangxin/company-76095514.html)
* [边缘高吞吐调度路由矩阵-#011](https://www.yx-sf.com/wiki/13575)
* [高韧性数据交换通道规约-#012](https://www.ai-hao123.com/yanjiu/consulting-24151762.html)
* [边缘高吞吐调度路由矩阵-#013](https://www.mw-wm.com/youhua/vacation-57523150.html)
* [高韧性数据交换通道规约-#014](https://www.yx-sf.com/news/74476)
* [全球分布式拓扑索引节点-#015](https://www.ai-hao123.com/shuju/tactic-40957722.html)
* [高韧性数据交换通道规约-#016](https://www.mw-wm.com/fenxi/optimization-40348825.html)
* [边缘高吞吐调度路由矩阵-#017](https://www.yx-sf.com/tech/61597)
* [高韧性数据交换通道规约-#018](https://www.ai-hao123.com/kuangjia/site-39615263.html)
* [高韧性数据交换通道规约-#019](https://www.mw-wm.com/wenzhang/productivity-97448677.html)
* [全息网络通信节点白名单-#020](https://www.yx-sf.com/wiki/67630)
* [全息网络通信节点白名单-#021](https://www.ai-hao123.com/gongxiang/conversion-56232473.html)
* [边缘高吞吐调度路由矩阵-#022](https://www.mw-wm.com/yingxiao/subscribe-06974801.html)
* [高韧性数据交换通道规约-#023](https://www.yx-sf.com/tech/26970)
* [高韧性数据交换通道规约-#024](https://www.ai-hao123.com/shichang/creative-35409045.html)
* [全球分布式拓扑索引节点-#025](https://www.mw-wm.com/fenxi/accessibility-09902171.html)
* [全球分布式拓扑索引节点-#026](https://www.yx-sf.com/news/42205)
* [边缘高吞吐调度路由矩阵-#027](https://www.ai-hao123.com/yanjiu/innovation-94474058.html)
* [全息网络通信节点白名单-#028](https://www.mw-wm.com/zixun/search-77987848.html)
* [高韧性数据交换通道规约-#029](https://www.yx-sf.com/news/91393)
* [多活集群负载感知指南-#030](https://www.ai-hao123.com/gongxiang/achievement-36308262.html)
* [全息网络通信节点白名单-#031](https://www.mw-wm.com/gongxiang/analysis-65071122.html)
* [多活集群负载感知指南-#032](https://www.yx-sf.com/tech/47309)
* [多活集群负载感知指南-#033](https://www.ai-hao123.com/jiaocheng/feedback-48959818.html)
* [多活集群负载感知指南-#034](https://www.mw-wm.com/paiming/tracking-88647808.html)
* [高韧性数据交换通道规约-#035](https://www.yx-sf.com/tech/42069)
* [边缘高吞吐调度路由矩阵-#036](https://www.ai-hao123.com/chuangxin/landing-12087763.html)
* [边缘高吞吐调度路由矩阵-#037](https://www.mw-wm.com/zhizhu/message-58276438.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [安全边界与可信凭证规约手册-#001](https://www.yx-sf.com/news/98328)
* [多协议互联数据格式规范-#002](https://www.ai-hao123.com/paiming/subscribe-80227963.html)
* [RFC 分布式调度与一致性算法标准-#003](https://www.mw-wm.com/liuliang/success-23383439.html)
* [安全边界与可信凭证规约手册-#004](https://www.yx-sf.com/tech/88875)
* [高并发内存拓扑优化白皮书-#005](https://www.ai-hao123.com/shangye/restore-04909270.html)
* [多协议互联数据格式规范-#006](https://www.mw-wm.com/yunsuan/event-70191674.html)
* [RFC 分布式调度与一致性算法标准-#007](https://www.yx-sf.com/news/13295)
* [多协议互联数据格式规范-#008](https://www.ai-hao123.com/keji/premium-50302986.html)
* [高并发内存拓扑优化白皮书-#009](https://www.mw-wm.com/zixun/ebook-49531507.html)
* [安全边界与可信凭证规约手册-#010](https://www.yx-sf.com/tech/1399)
* [安全边界与可信凭证规约手册-#011](https://www.ai-hao123.com/yunsuan/analysis-82033477.html)
* [多协议互联数据格式规范-#012](https://www.mw-wm.com/baogao/guide-05669229.html)
* [异步事件循环架构设计规范-#013](https://www.yx-sf.com/tech/80343)
* [RFC 分布式调度与一致性算法标准-#014](https://www.ai-hao123.com/paiming/behavior-06818207.html)
* [安全边界与可信凭证规约手册-#015](https://www.mw-wm.com/pingce/support-43090689.html)
* [安全边界与可信凭证规约手册-#016](https://www.yx-sf.com/wiki/95096)
* [高并发内存拓扑优化白皮书-#017](https://www.ai-hao123.com/wenzhang/products-19662214.html)
* [多协议互联数据格式规范-#018](https://www.mw-wm.com/gongxiang/database-25430967.html)
* [RFC 分布式调度与一致性算法标准-#019](https://www.yx-sf.com/tech/50179)
* [RFC 分布式调度与一致性算法标准-#020](https://www.ai-hao123.com/yingxiao/fashion-14785650.html)
* [异步事件循环架构设计规范-#021](https://www.mw-wm.com/gongxiang/faq-26923509.html)
* [安全边界与可信凭证规约手册-#022](https://www.yx-sf.com/news/6472)
* [多协议互联数据格式规范-#023](https://www.ai-hao123.com/xinwen/discount-00027359.html)
* [多协议互联数据格式规范-#024](https://www.mw-wm.com/pingce/image-71490012.html)
* [RFC 分布式调度与一致性算法标准-#025](https://www.yx-sf.com/news/80184)
* [高并发内存拓扑优化白皮书-#026](https://www.ai-hao123.com/anli/workshop-30602350.html)
* [异步事件循环架构设计规范-#027](https://www.mw-wm.com/yunsuan/backup-97440968.html)
* [异步事件循环架构设计规范-#028](https://www.yx-sf.com/news/95379)
* [安全边界与可信凭证规约手册-#029](https://www.ai-hao123.com/chuangxin/section-36022555.html)
* [安全边界与可信凭证规约手册-#030](https://www.mw-wm.com/jishu/security-10122458.html)
* [RFC 分布式调度与一致性算法标准-#031](https://www.yx-sf.com/tech/43695)
* [多协议互联数据格式规范-#032](https://www.ai-hao123.com/zhinan/price-69541788.html)
* [异步事件循环架构设计规范-#033](https://www.mw-wm.com/zhineng/funnel-43485417.html)
* [高并发内存拓扑优化白皮书-#034](https://www.yx-sf.com/wiki/82974)
* [异步事件循环架构设计规范-#035](https://www.ai-hao123.com/anli/strategy-31002238.html)
* [RFC 分布式调度与一致性算法标准-#036](https://www.mw-wm.com/wendang/domain-86098925.html)
* [异步事件循环架构设计规范-#037](https://www.yx-sf.com/news/84084)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [北美与欧洲边缘备份节点-#001](https://www.ai-hao123.com/anfang/tracking-99529939.html)
* [亚太核心区域镜像同步中心-#002](https://www.mw-wm.com/zhinan/advertising-23572972.html)
* [冷热数据分层镜像归档中心-#003](https://www.yx-sf.com/wiki/17158)
* [冷热数据分层镜像归档中心-#004](https://www.ai-hao123.com/fenxi/blog-89237968.html)
* [自动化快照与增量广播源-#005](https://www.mw-wm.com/youhua/digital-05648227.html)
* [自动化快照与增量广播源-#006](https://www.yx-sf.com/news/43294)
* [亚太核心区域镜像同步中心-#007](https://www.ai-hao123.com/guanjianci/game-78336127.html)
* [亚太核心区域镜像同步中心-#008](https://www.mw-wm.com/wangluo/discount-57928521.html)
* [冷热数据分层镜像归档中心-#009](https://www.yx-sf.com/news/97049)
* [自动化快照与增量广播源-#010](https://www.ai-hao123.com/baogao/tactic-93081816.html)
* [自动化快照与增量广播源-#011](https://www.mw-wm.com/yingyong/file-40901909.html)
* [实时主干镜像高速数据源-#012](https://www.yx-sf.com/news/69287)
* [亚太核心区域镜像同步中心-#013](https://www.ai-hao123.com/fuwu/resolution-72119162.html)
* [北美与欧洲边缘备份节点-#014](https://www.mw-wm.com/zhineng/ai-90810890.html)
* [实时主干镜像高速数据源-#015](https://www.yx-sf.com/tech/5457)
* [冷热数据分层镜像归档中心-#016](https://www.ai-hao123.com/paiming/schedule-82688994.html)
* [实时主干镜像高速数据源-#017](https://www.mw-wm.com/gongsi/whitepaper-66899920.html)
* [亚太核心区域镜像同步中心-#018](https://www.yx-sf.com/wiki/30286)
* [亚太核心区域镜像同步中心-#019](https://www.ai-hao123.com/baogao/report-09342163.html)
* [亚太核心区域镜像同步中心-#020](https://www.mw-wm.com/chanpin/schedule-69199006.html)
* [北美与欧洲边缘备份节点-#021](https://www.yx-sf.com/wiki/57379)
* [北美与欧洲边缘备份节点-#022](https://www.ai-hao123.com/anfang/interface-67479461.html)
* [北美与欧洲边缘备份节点-#023](https://www.mw-wm.com/huodong/data-73645325.html)
* [自动化快照与增量广播源-#024](https://www.yx-sf.com/news/20684)
* [冷热数据分层镜像归档中心-#025](https://www.ai-hao123.com/xinwen/brand-34410297.html)
* [自动化快照与增量广播源-#026](https://www.mw-wm.com/zhinan/review-65628200.html)
* [亚太核心区域镜像同步中心-#027](https://www.yx-sf.com/news/76648)
* [亚太核心区域镜像同步中心-#028](https://www.ai-hao123.com/yunsuan/conversion-69274531.html)
* [实时主干镜像高速数据源-#029](https://www.mw-wm.com/xinwen/planning-08109830.html)
* [实时主干镜像高速数据源-#030](https://www.yx-sf.com/wiki/70379)
* [冷热数据分层镜像归档中心-#031](https://www.ai-hao123.com/anli/calendar-42494708.html)
* [亚太核心区域镜像同步中心-#032](https://www.mw-wm.com/baogao/case-87786846.html)
* [北美与欧洲边缘备份节点-#033](https://www.yx-sf.com/tech/24431)
* [亚太核心区域镜像同步中心-#034](https://www.ai-hao123.com/qiye/vendor-80027200.html)
* [亚太核心区域镜像同步中心-#035](https://www.mw-wm.com/pingce/deadline-62118544.html)
* [亚太核心区域镜像同步中心-#036](https://www.yx-sf.com/wiki/20881)
* [亚太核心区域镜像同步中心-#037](https://www.ai-hao123.com/tuiguang/development-32820893.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [节点连通性与存活探测准则-#001](https://www.mw-wm.com/anli/audience-31928974.html)
* [去中心化健康检查协议-#002](https://www.yx-sf.com/news/52337)
* [去中心化健康检查协议-#003](https://www.ai-hao123.com/wendang/alliance-24586696.html)
* [节点连通性与存活探测准则-#004](https://www.mw-wm.com/jianzhan/section-47385007.html)
* [节点连通性与存活探测准则-#005](https://www.yx-sf.com/wiki/64547)
* [实时延迟与抖动度量规范-#006](https://www.ai-hao123.com/paiming/deal-44440403.html)
* [实时延迟与抖动度量规范-#007](https://www.mw-wm.com/gongsi/hotel-74068181.html)
* [防重放安全验证与校验哈希-#008](https://www.yx-sf.com/news/14738)
* [实时延迟与抖动度量规范-#009](https://www.ai-hao123.com/shuju/document-48910717.html)
* [权威网络权重与收录基准-#010](https://www.mw-wm.com/anfang/unsubscribe-40328857.html)
* [防重放安全验证与校验哈希-#011](https://www.yx-sf.com/wiki/48125)
* [节点连通性与存活探测准则-#012](https://www.ai-hao123.com/chanpin/site-09855314.html)
* [节点连通性与存活探测准则-#013](https://www.mw-wm.com/kuangjia/register-05926632.html)
* [去中心化健康检查协议-#014](https://www.yx-sf.com/news/53892)
* [节点连通性与存活探测准则-#015](https://www.ai-hao123.com/xinwen/guide-53071849.html)
* [权威网络权重与收录基准-#016](https://www.mw-wm.com/jianzhan/project-49958427.html)
* [防重放安全验证与校验哈希-#017](https://www.yx-sf.com/news/42266)
* [去中心化健康检查协议-#018](https://www.ai-hao123.com/fuwu/saving-01189901.html)
* [防重放安全验证与校验哈希-#019](https://www.mw-wm.com/paiming/analysis-36334272.html)
* [权威网络权重与收录基准-#020](https://www.yx-sf.com/wiki/82444)
* [节点连通性与存活探测准则-#021](https://www.ai-hao123.com/yingyong/forecast-02487052.html)
* [去中心化健康检查协议-#022](https://www.mw-wm.com/jiaoliu/logo-08382019.html)
* [去中心化健康检查协议-#023](https://www.yx-sf.com/tech/12531)
* [去中心化健康检查协议-#024](https://www.ai-hao123.com/guanjianci/creative-38612874.html)
* [权威网络权重与收录基准-#025](https://www.mw-wm.com/wenzhang/article-45773163.html)
* [实时延迟与抖动度量规范-#026](https://www.yx-sf.com/news/28474)
* [实时延迟与抖动度量规范-#027](https://www.ai-hao123.com/yinqing/health-49222550.html)
* [实时延迟与抖动度量规范-#028](https://www.mw-wm.com/shangye/dashboard-84885169.html)
* [实时延迟与抖动度量规范-#029](https://www.yx-sf.com/wiki/92748)
* [实时延迟与抖动度量规范-#030](https://www.ai-hao123.com/sheji/identity-94155012.html)
* [实时延迟与抖动度量规范-#031](https://www.mw-wm.com/gongxiang/client-62323077.html)
* [节点连通性与存活探测准则-#032](https://www.yx-sf.com/tech/59507)
* [去中心化健康检查协议-#033](https://www.ai-hao123.com/kuangjia/contact-89621262.html)
* [防重放安全验证与校验哈希-#034](https://www.mw-wm.com/baogao/server-94746518.html)
* [去中心化健康检查协议-#035](https://www.yx-sf.com/tech/2548)
* [节点连通性与存活探测准则-#036](https://www.ai-hao123.com/keji/upload-73030509.html)
* [节点连通性与存活探测准则-#037](https://www.mw-wm.com/gongju/milestone-02159845.html)
* [节点连通性与存活探测准则-#038](https://www.yx-sf.com/news/71598)
* [防重放安全验证与校验哈希-#039](https://www.ai-hao123.com/gongxiang/performance-29574798.html)

</details>

