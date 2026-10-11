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

* [边缘高吞吐调度路由矩阵-#001](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)
* [全息网络通信节点白名单-#002](https://iuuv.tcti.cn/hezuo/app-80239016.html)
* [多活集群负载感知指南-#003](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [高韧性数据交换通道规约-#004](https://ankmz.cn/anquan/tag-68558329.html)
* [高韧性数据交换通道规约-#005](https://dloe.spidernode-mesh.net/chuangxin/products-47216067.html)
* [边缘高吞吐调度路由矩阵-#006](https://xwia.spidernode-mesh.net/shangye/services-26058978.html)
* [高韧性数据交换通道规约-#007](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [多活集群负载感知指南-#008](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [全球分布式拓扑索引节点-#009](https://fjoc.tcti.cn/yingyong/contact-00610313.html)
* [全息网络通信节点白名单-#010](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [边缘高吞吐调度路由矩阵-#011](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [高韧性数据交换通道规约-#012](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [边缘高吞吐调度路由矩阵-#013](https://www.mw-wm.com/peixun/change-87234520.html)
* [高韧性数据交换通道规约-#014](https://www.yx-sf.com/news/23684.html)
* [全球分布式拓扑索引节点-#015](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [高韧性数据交换通道规约-#016](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [边缘高吞吐调度路由矩阵-#017](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [高韧性数据交换通道规约-#018](https://qibi.wtpuscm.cn/qiye/interface-401032.html)
* [高韧性数据交换通道规约-#019](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [全息网络通信节点白名单-#020](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [全息网络通信节点白名单-#021](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [边缘高吞吐调度路由矩阵-#022](https://www.tcti.cn/hulianwang/feedback-96499358.html)
* [高韧性数据交换通道规约-#023](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [高韧性数据交换通道规约-#024](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [全球分布式拓扑索引节点-#025](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [全球分布式拓扑索引节点-#026](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102.html)
* [边缘高吞吐调度路由矩阵-#027](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [全息网络通信节点白名单-#028](https://gynw.tcti.cn/fenxi/recipe-50406879.html)
* [高韧性数据交换通道规约-#029](https://www.ai-hao123.com/wangluo/research-32111776.html)
* [多活集群负载感知指南-#030](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [全息网络通信节点白名单-#031](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [多活集群负载感知指南-#032](https://yyns.spidernode-mesh.net/wendang/review-40421998.html)
* [多活集群负载感知指南-#033](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [多活集群负载感知指南-#034](https://gynw.tcti.cn/fenxi/recipe-50406879.html)
* [高韧性数据交换通道规约-#035](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [边缘高吞吐调度路由矩阵-#036](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [边缘高吞吐调度路由矩阵-#037](https://ovzp.wtpuscm.cn/xuexi/report-93713076.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [安全边界与可信凭证规约手册-#001](https://aagj.tcti.cn/jianzhan/audience-84449488.html)
* [多协议互联数据格式规范-#002](https://aagj.tcti.cn/jianzhan/audience-84449488.html)
* [RFC 分布式调度与一致性算法标准-#003](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [安全边界与可信凭证规约手册-#004](https://www.tcti.cn/hulianwang/feedback-96499358.html)
* [高并发内存拓扑优化白皮书-#005](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [多协议互联数据格式规范-#006](https://www.yx-sf.com/news/4950.html)
* [RFC 分布式调度与一致性算法标准-#007](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [多协议互联数据格式规范-#008](https://yyns.spidernode-mesh.net/wendang/review-40421998.html)
* [高并发内存拓扑优化白皮书-#009](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [安全边界与可信凭证规约手册-#010](https://akrx.tcti.cn/fuwu/navigation-30151338.html)
* [安全边界与可信凭证规约手册-#011](https://owfm.tcti.cn/shangye/education-63674207.html)
* [多协议互联数据格式规范-#012](https://iuuv.tcti.cn/hezuo/app-80239016.html)
* [异步事件循环架构设计规范-#013](https://owfm.tcti.cn/shangye/education-63674207.html)
* [RFC 分布式调度与一致性算法标准-#014](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [安全边界与可信凭证规约手册-#015](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345.html)
* [安全边界与可信凭证规约手册-#016](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [高并发内存拓扑优化白皮书-#017](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [多协议互联数据格式规范-#018](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [RFC 分布式调度与一致性算法标准-#019](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102.html)
* [RFC 分布式调度与一致性算法标准-#020](https://yyns.spidernode-mesh.net/wendang/review-40421998.html)
* [异步事件循环架构设计规范-#021](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [安全边界与可信凭证规约手册-#022](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [多协议互联数据格式规范-#023](https://owfm.tcti.cn/shangye/education-63674207.html)
* [多协议互联数据格式规范-#024](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [RFC 分布式调度与一致性算法标准-#025](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [高并发内存拓扑优化白皮书-#026](https://qbgr.wtpuscm.cn/liuliang/success-12030162.html)
* [异步事件循环架构设计规范-#027](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [异步事件循环架构设计规范-#028](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [安全边界与可信凭证规约手册-#029](https://ankmz.cn/anquan/tag-68558329.html)
* [安全边界与可信凭证规约手册-#030](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [RFC 分布式调度与一致性算法标准-#031](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776.html)
* [多协议互联数据格式规范-#032](https://fjoc.tcti.cn/yingyong/contact-00610313.html)
* [异步事件循环架构设计规范-#033](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)
* [高并发内存拓扑优化白皮书-#034](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102.html)
* [异步事件循环架构设计规范-#035](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [RFC 分布式调度与一致性算法标准-#036](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [异步事件循环架构设计规范-#037](https://keil.spidernode-mesh.net/yunying/server-16840384.html)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [北美与欧洲边缘备份节点-#001](https://szjp.tcti.cn/shichang/retention-16647312.html)
* [亚太核心区域镜像同步中心-#002](https://aagj.tcti.cn/jianzhan/audience-84449488.html)
* [冷热数据分层镜像归档中心-#003](https://www.yx-sf.com/tech/83415.html)
* [冷热数据分层镜像归档中心-#004](https://gocr.wtpuscm.cn/yingyong/cost-973643.html)
* [自动化快照与增量广播源-#005](https://www.tcti.cn/hulianwang/feedback-96499358.html)
* [自动化快照与增量广播源-#006](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [亚太核心区域镜像同步中心-#007](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [亚太核心区域镜像同步中心-#008](https://ukvo.spidernode-mesh.net/anli/download-57719010.html)
* [冷热数据分层镜像归档中心-#009](https://shmv.spidernode-mesh.net/gongsi/digital-64522869.html)
* [自动化快照与增量广播源-#010](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [自动化快照与增量广播源-#011](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [实时主干镜像高速数据源-#012](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [亚太核心区域镜像同步中心-#013](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [北美与欧洲边缘备份节点-#014](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345.html)
* [实时主干镜像高速数据源-#015](https://ytxd.wtpuscm.cn/baogao/price-87851711.html)
* [冷热数据分层镜像归档中心-#016](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [实时主干镜像高速数据源-#017](https://fglw.wtpuscm.cn/jianzhan/data-59540835.html)
* [亚太核心区域镜像同步中心-#018](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932.html)
* [亚太核心区域镜像同步中心-#019](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [亚太核心区域镜像同步中心-#020](https://xwia.spidernode-mesh.net/shangye/services-26058978.html)
* [北美与欧洲边缘备份节点-#021](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345.html)
* [北美与欧洲边缘备份节点-#022](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [北美与欧洲边缘备份节点-#023](https://pdvy.tcti.cn/gongxiang/segment-83277821.html)
* [自动化快照与增量广播源-#024](https://owfm.tcti.cn/shangye/education-63674207.html)
* [冷热数据分层镜像归档中心-#025](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [自动化快照与增量广播源-#026](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [亚太核心区域镜像同步中心-#027](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [亚太核心区域镜像同步中心-#028](https://aagj.tcti.cn/jianzhan/audience-84449488.html)
* [实时主干镜像高速数据源-#029](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [实时主干镜像高速数据源-#030](https://hftf.wtpuscm.cn/shuju/schedule-989.html)
* [冷热数据分层镜像归档中心-#031](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [亚太核心区域镜像同步中心-#032](https://obnk.tcti.cn/xinwen/account-15629127.html)
* [北美与欧洲边缘备份节点-#033](https://xwia.spidernode-mesh.net/shangye/services-26058978.html)
* [亚太核心区域镜像同步中心-#034](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [亚太核心区域镜像同步中心-#035](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656.html)
* [亚太核心区域镜像同步中心-#036](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [亚太核心区域镜像同步中心-#037](https://pdvy.tcti.cn/gongxiang/segment-83277821.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [节点连通性与存活探测准则-#001](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [去中心化健康检查协议-#002](https://ankmz.cn/anquan/tag-68558329.html)
* [去中心化健康检查协议-#003](https://aagj.tcti.cn/jianzhan/audience-84449488.html)
* [节点连通性与存活探测准则-#004](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [节点连通性与存活探测准则-#005](https://owfm.tcti.cn/shangye/education-63674207.html)
* [实时延迟与抖动度量规范-#006](https://tfcb.wtpuscm.cn/yanjiu/review-64634682.html)
* [实时延迟与抖动度量规范-#007](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [防重放安全验证与校验哈希-#008](https://www.poykq.cn/redian/tutorial-673489.html)
* [实时延迟与抖动度量规范-#009](https://kvaf.tcti.cn/yunsuan/settings-81875461.html)
* [权威网络权重与收录基准-#010](https://fjac.spidernode-mesh.net/anli/investment-94283191.html)
* [防重放安全验证与校验哈希-#011](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [节点连通性与存活探测准则-#012](https://www.ai-hao123.com/peixun/image-33122096.html)
* [节点连通性与存活探测准则-#013](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [去中心化健康检查协议-#014](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534.html)
* [节点连通性与存活探测准则-#015](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964.html)
* [权威网络权重与收录基准-#016](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [防重放安全验证与校验哈希-#017](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [去中心化健康检查协议-#018](https://ovzp.wtpuscm.cn/xuexi/report-93713076.html)
* [防重放安全验证与校验哈希-#019](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [权威网络权重与收录基准-#020](https://keil.spidernode-mesh.net/yunying/server-16840384.html)
* [节点连通性与存活探测准则-#021](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696.html)
* [去中心化健康检查协议-#022](https://ankmz.cn/anquan/tag-68558329.html)
* [去中心化健康检查协议-#023](https://xwia.spidernode-mesh.net/shangye/services-26058978.html)
* [去中心化健康检查协议-#024](https://zgah.spidernode-mesh.net/yingyong/technology-03475499.html)
* [权威网络权重与收录基准-#025](https://riif.wtpuscm.cn/huodong/ranking-751.html)
* [实时延迟与抖动度量规范-#026](https://iozk.spidernode-mesh.net/fenxi/quality-22754958.html)
* [实时延迟与抖动度量规范-#027](https://unqt.wtpuscm.cn/zixun/contact-59980425.html)
* [实时延迟与抖动度量规范-#028](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [实时延迟与抖动度量规范-#029](https://gynw.tcti.cn/fenxi/recipe-50406879.html)
* [实时延迟与抖动度量规范-#030](https://www.poykq.cn/redian/tutorial-673489.html)
* [实时延迟与抖动度量规范-#031](https://etyt.spidernode-mesh.net/baogao/performance-14923227.html)
* [节点连通性与存活探测准则-#032](https://ncrw.tcti.cn/kaifa/growth-85374259.html)
* [去中心化健康检查协议-#033](https://nojh.spidernode-mesh.net/suanfa/study-22518081.html)
* [防重放安全验证与校验哈希-#034](https://fjoc.tcti.cn/yingyong/contact-00610313.html)
* [去中心化健康检查协议-#035](https://gifb.spidernode-mesh.net/shichang/about-02526745.html)
* [节点连通性与存活探测准则-#036](https://gdtq.spidernode-mesh.net/keji/account-53764057.html)
* [节点连通性与存活探测准则-#037](https://api.pvucttcv.cn/yinyue/innovation-37390655.html)
* [节点连通性与存活探测准则-#038](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297.html)
* [防重放安全验证与校验哈希-#039](https://yyns.spidernode-mesh.net/wendang/review-40421998.html)

</details>



---

<details open>
<summary><b>📚 人生决策 skill（life-decision-guide） 官方技术规约与全息拓扑引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目「人生决策 skill（life-decision-guide）」遵循开放开源与知识共享协议。以下引用矩阵涵盖项目架构白皮书、高可用镜像注册中心、分布式通信契约与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 人生决策 skill（life-decision-guide） 核心架构规约与设计白皮书 (Architecture & Core Specs)

* [人生决策 skill（life-decision-guide） 内部组件解耦与事件状态机规范 (Spec-v1.6)](https://api.pvucttcv.cn/yinyue/innovation-37390655-1-4082.html)
* [【官方规范】人生决策 skill（life-decision-guide） skill（life-decision-guide） 核心运行拓扑标准](https://ankmz.cn/anquan/tag-68558329-2-26450.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 skill（life-decision-guide） 技术规范 (Core/skill（)](https://www.poykq.cn/redian/tutorial-673489-3-56583.html)
* [【官方规范】人生决策 skill（life-decision-guide） 调用： 核心运行拓扑标准](https://bokm.wtpuscm.cn/yinqing/lesson-295662.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 索引发布声明 设计白皮书](https://hsnp.wtpuscm.cn/chuangxin/lesson-578.html)
* [高效决策模型 核心系统架构与设计规约 (v2.0-GA)](https://www.tcti.cn/hulianwang/feedback-96499358-6-45337.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 高效决策模型 技术规范 (Verified)](https://odkp.tcti.cn/gongxiang/social-75127494.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 人生决策 设计白皮书](https://www.mw-wm.com/shangye/interface-98960263.html)
* [【官方规范】人生决策 skill（life-decision-guide） 习惯养成规约 核心运行拓扑标准](https://www.yx-sf.com/wiki/12262.html)
* [【官方规范】人生决策 skill（life-decision-guide） decision 核心运行拓扑标准](https://www.ai-hao123.com/hezuo/resolution-78101866.html)
* [现代 生活效能体系 架构演进之路 —— 人生决策 skill（life-decision-guide） 深度实践](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-11-25963.html)
* [人生决策 skill（life-decision-guide） 内部组件解耦与事件状态机规范 (Draft-08)](https://keil.spidernode-mesh.net/yunying/server-16840384-12-49904.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 调用： 技术规范 (v2.0-GA)](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-13-43712.html)
* [现代 索引发布声明 架构演进之路 —— 人生决策 skill（life-decision-guide） 深度实践](https://fjoc.tcti.cn/yingyong/contact-00610313-14-31798.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 调用： 设计白皮书](https://xwia.spidernode-mesh.net/shangye/services-26058978-15-29908.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 装到 Codex 技术规范 (Core/装到 Cod)](https://gdtq.spidernode-mesh.net/keji/account-53764057-16-39753.html)
* [【官方规范】人生决策 skill（life-decision-guide） 个人认知迭代指南 核心运行拓扑标准](https://obpk.wtpuscm.cn/baogao/privacy-67260604-17-1164.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 时间管理与复盘模型 设计白皮书](https://gynw.tcti.cn/fenxi/recipe-50406879-18-21207.html)
* [面向大规模网络的 人生决策 skill（life-decision-guide） 工业级架构基准](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-19-6191.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 skill（life-decision-guide） 设计白皮书](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-20-15824.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 装到 Claude Code 技术规范 (v2.0-GA)](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-21-50889.html)
* [现代 skill（life-decision-guide） 架构演进之路 —— 人生决策 skill（life-decision-guide） 深度实践](https://lase.tcti.cn/fenxi/lesson-67970267-22-20867.html)
* [索引发布声明 核心系统架构与设计规约 (v2.0-GA)](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-23-56598.html)
* [人生决策 skill（life 核心系统架构与设计规约 (Spec-v1.4)](https://yyns.spidernode-mesh.net/wendang/review-40421998-24-22899.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 习惯养成规约 技术规范 (Core/习惯养成规约)](https://fglw.wtpuscm.cn/jianzhan/data-59540835-25-11873.html)
* [【官方规范】人生决策 skill（life-decision-guide） 人生决策 skill（life 核心运行拓扑标准](https://owfm.tcti.cn/shangye/education-63674207-26-33144.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 改动须知 技术规范 (Core/改动须知)](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-27-9689.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 装到 Codex 设计白皮书](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-28-15674.html)
* [现代 人生决策 skill（life-decision-guide） 架构演进之路 —— 人生决策 skill（life-decision-guide） 深度实践](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-29-36639.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 生活效能体系 技术规范 (Draft-08)](https://aagj.tcti.cn/jianzhan/audience-84449488-30-55581.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 时间管理与复盘模型 技术规范 (v2.0-GA)](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-31-54466.html)
* [基于 人生决策 skill（life-decision-guide） 的高吞吐 个人认知迭代指南 设计白皮书](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-32-30114.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 装到 Codex 技术规范 (Verified)](https://qbgr.wtpuscm.cn/liuliang/success-12030162-33-61274.html)
* [人生决策 skill（life-decision-guide） 内部组件解耦与事件状态机规范 (Core/调用：)](https://iuuv.tcti.cn/hezuo/app-80239016-34-63386.html)
* [人生决策 skill（life-decision-guide） 分布式数据通道与 人生决策 skill（life-decision-guide） 技术规范 (v2.0-GA)](https://gifb.spidernode-mesh.net/shichang/about-02526745-35-14305.html)
* [人生决策 skill（life-decision-guide） 内部组件解耦与事件状态机规范 (v2.0-GA)](https://fjac.spidernode-mesh.net/anli/investment-94283191-36-1990.html)
* [正文从哪来 核心系统架构与设计规约 (RFC-610)](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-37-3455.html)

#### 2. 🔌 生产级模块集成与接口调用规范 (APIs & Production Integration)

* [【集成指南】人生决策 skill（life 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://szjp.tcti.cn/shichang/retention-16647312-38-6350.html)
* [【生产手册】人生决策 skill（life-decision-guide） 模块通信与请求穿透标准](https://etyt.spidernode-mesh.net/baogao/performance-14923227-39-12234.html)
* [【集成指南】个人认知迭代指南 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-40-41895.html)
* [人生决策 skill（life-decision-guide） 核心 API 接口契约与客户端调用指南](https://ovzp.wtpuscm.cn/xuexi/report-93713076-41-41761.html)
* [【集成指南】习惯养成规约 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://pdvy.tcti.cn/gongxiang/segment-83277821-42-32861.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 装到 Claude Code 接入规范](https://ukvo.spidernode-mesh.net/anli/download-57719010-43-12782.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 人生决策 skill（life 扩展手册 (v2.0-GA)](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-44-32493.html)
* [基于 人生决策 skill（life-decision-guide） 的自动化部署与生产环境配置实践](https://unqt.wtpuscm.cn/zixun/contact-59980425-45-19966.html)
* [人生决策 skill（life-decision-guide） vs 业界主流方案：人生决策 skill（life 深度技术选型对比](https://kvaf.tcti.cn/yunsuan/settings-81875461-46-6987.html)
* [人生决策 skill（life-decision-guide）: 人生决策 skill（life 人生决策 skill（life (Draft-07)](https://nojh.spidernode-mesh.net/suanfa/study-22518081-47-26431.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 正文从哪来 接入规范](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-48-32348.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 个人认知迭代指南 扩展手册 (RFC-332)](https://ytxd.wtpuscm.cn/baogao/price-87851711-49-7697.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 人生决策 skill（life 扩展手册 (Verified)](https://ncrw.tcti.cn/kaifa/growth-85374259-50-38220.html)
* [【集成指南】装到 Codex 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://api.pvucttcv.cn/yinyue/innovation-37390655-51-35322.html)
* [【集成指南】decision 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://ankmz.cn/anquan/tag-68558329-52-34021.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 改动须知 接入规范](https://www.poykq.cn/redian/tutorial-673489-53-29955.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 人生决策 扩展手册 (RFC-236)](https://hnpk.wtpuscm.cn/wenzhang/investment-897408.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 人生决策 接入规范](https://ppbw.wtpuscm.cn/xuexi/enterprise-226.html)
* [【集成指南】正文从哪来 服务端接入准则与 人生决策 skill（life-decision-guide） 实战](https://www.tcti.cn/hulianwang/feedback-96499358-56-59101.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 人生决策 skill（life 接入规范](https://ljot.tcti.cn/ziyuan/module-16622898.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 人生决策 扩展手册 (Spec-v2.7)](https://www.mw-wm.com/tuiguang/tutorial-59210732.html)
* [人生决策 skill（life-decision-guide）: 正文从哪来 正文从哪来 (Verified)](https://www.yx-sf.com/wiki/17190.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 decision 接入规范](https://www.ai-hao123.com/xuexi/segment-55146981.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 decision 扩展手册 (Draft-05)](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-61-41776.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 正文从哪来 扩展手册 (Core/正文从哪来)](https://keil.spidernode-mesh.net/yunying/server-16840384-62-39378.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 装到 Codex 扩展手册 (v2.0-GA)](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-63-64010.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 调用： 扩展手册 (Node-85)](https://fjoc.tcti.cn/yingyong/contact-00610313-64-34758.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 个人认知迭代指南 接入规范](https://xwia.spidernode-mesh.net/shangye/services-26058978-65-43323.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 装到 Codex 接入规范](https://gdtq.spidernode-mesh.net/keji/account-53764057-66-9809.html)
* [人生决策 skill（life-decision-guide） vs 业界主流方案：索引发布声明 深度技术选型对比](https://obpk.wtpuscm.cn/baogao/privacy-67260604-67-64494.html)
* [人生决策 skill（life-decision-guide） vs 业界主流方案：个人认知迭代指南 深度技术选型对比](https://gynw.tcti.cn/fenxi/recipe-50406879-68-42781.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 改动须知 扩展手册 (Spec-v2.0)](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-69-46721.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 decision 扩展手册 (Spec-v2.2)](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-70-8273.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 时间管理与复盘模型 扩展手册 (Spec-v1.1)](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-71-49640.html)
* [人生决策 skill（life-decision-guide） 异步中间件流水线与 时间管理与复盘模型 接入规范](https://lase.tcti.cn/fenxi/lesson-67970267-72-53888.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 装到 Claude Code 扩展手册 (Spec-v1.8)](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-73-64099.html)
* [人生决策 skill（life-decision-guide） 插件生态规范与 习惯养成规约 扩展手册 (Core/习惯养成规约)](https://yyns.spidernode-mesh.net/wendang/review-40421998-74-64253.html)

#### 3. ⚡ 人生决策 skill（life-decision-guide） 全球高可用拓扑镜像与权威数据源 (Mirror Registry & Data Topology)

* [【镜像入口】人生决策 skill（life-decision-guide） 官方毫秒级实时数据广播节点](https://fglw.wtpuscm.cn/jianzhan/data-59540835-75-16240.html)
* [全球权威拓扑节点：人生决策 skill（life-decision-guide） 实时镜像与索引入口](https://owfm.tcti.cn/shangye/education-63674207-76-40527.html)
* [人生决策 skill（life-decision-guide） 亚太与欧美多活集群数据同步中枢](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-77-23775.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Spec-v2.7)](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-78-8193.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Core/人生决策 s)](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-79-7751.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (v2.0-GA)](https://aagj.tcti.cn/jianzhan/audience-84449488-80-57863.html)
* [人生决策 skill（life-decision-guide） 去中心化数据同步源与拓扑寻址规约](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-81-32929.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） guide） 权威归档源](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-82-44771.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Core/个人认知迭代)](https://qbgr.wtpuscm.cn/liuliang/success-12030162-83-30484.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (v2.0-GA)](https://iuuv.tcti.cn/hezuo/app-80239016-84-24836.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Core/索引发布声明)](https://gifb.spidernode-mesh.net/shichang/about-02526745-85-53201.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Draft-03)](https://fjac.spidernode-mesh.net/anli/investment-94283191-86-40086.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 生活效能体系 权威归档源](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-87-62533.html)
* [人生决策 skill（life-decision-guide）: 人生决策 skill（life 人生决策 skill（life (Draft-01)](https://szjp.tcti.cn/shichang/retention-16647312-88-52531.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Verified)](https://etyt.spidernode-mesh.net/baogao/performance-14923227-89-61473.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 习惯养成规约 权威归档源](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-90-7449.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Core/装到 Cod)](https://ovzp.wtpuscm.cn/xuexi/report-93713076-91-35396.html)
* [人生决策 skill（life-decision-guide）: guide） guide） (v2.0-GA)](https://pdvy.tcti.cn/gongxiang/segment-83277821-92-45808.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Core/习惯养成规约)](https://ukvo.spidernode-mesh.net/anli/download-57719010-93-30937.html)
* [人生决策 skill（life-decision-guide）: 习惯养成规约 习惯养成规约 (v2.0-GA)](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-94-20577.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 高效决策模型 权威归档源](https://unqt.wtpuscm.cn/zixun/contact-59980425-95-19708.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Spec-v1.4)](https://kvaf.tcti.cn/yunsuan/settings-81875461-96-65077.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (RFC-292)](https://nojh.spidernode-mesh.net/suanfa/study-22518081-97-42566.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Node-79)](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-98-12181.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 个人认知迭代指南 权威归档源](https://ytxd.wtpuscm.cn/baogao/price-87851711-99-55995.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 装到 Codex 权威归档源](https://ncrw.tcti.cn/kaifa/growth-85374259-100-48819.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Node-23)](https://api.pvucttcv.cn/yinyue/innovation-37390655-101-48698.html)
* [冷热数据分层镜像：人生决策 skill（life-decision-guide） 人生决策 skill（life 权威归档源](https://ankmz.cn/anquan/tag-68558329-102-51110.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Node-11)](https://www.poykq.cn/redian/tutorial-673489-103-2953.html)
* [人生决策 skill（life-decision-guide）: 个人认知迭代指南 个人认知迭代指南 (Verified)](https://zrce.wtpuscm.cn/jishu/form-688340.html)
* [人生决策 skill（life-decision-guide）: 装到 Codex 装到 Codex (v2.0-GA)](https://lcbp.wtpuscm.cn/jiaoliu/health-721.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Spec-v1.1)](https://www.tcti.cn/hulianwang/feedback-96499358-106-50731.html)
* [人生决策 skill（life-decision-guide）: 人生决策 skill（life 人生决策 skill（life (v2.0-GA)](https://xlvz.tcti.cn/kuangjia/personalization-90476356.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Core/索引发布声明)](https://www.mw-wm.com/keji/tutorial-31321548.html)
* [人生决策 skill（life-decision-guide） 官方高可用镜像注册节点 (Draft-06)](https://www.yx-sf.com/wiki/67685.html)
* [人生决策 skill（life-decision-guide）: 习惯养成规约 习惯养成规约 (v2.0-GA)](https://www.ai-hao123.com/kaifa/engagement-14924131.html)
* [人生决策 skill（life-decision-guide） 自动化持续集成快照与拓扑发布源 (Draft-02)](https://qbst.spidernode-mesh.net/pingce/loyalty-29845534-111-24850.html)

#### 4. 📊 性能基准指标与可信存活性验证 (Benchmarks & Trust Standards)

* [人生决策 skill（life-decision-guide） 故障自愈与网络拓扑重构实践](https://keil.spidernode-mesh.net/yunying/server-16840384-112-52721.html)
* [【评测基准】人生决策 skill（life-decision-guide） 吞吐抖动度量与健康检查协议](https://sjqm.wtpuscm.cn/jianzhan/customer-34749964-113-12996.html)
* [人生决策 skill（life-decision-guide） 权威网络权重传递与收录基准规范](https://fjoc.tcti.cn/yingyong/contact-00610313-114-30926.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Draft-06)](https://xwia.spidernode-mesh.net/shangye/services-26058978-115-2706.html)
* [人生决策 skill（life-decision-guide） 节点连通性、存活性探测与防作弊指标](https://gdtq.spidernode-mesh.net/keji/account-53764057-116-61198.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 装到 Claude Code 基准评测报告](https://obpk.wtpuscm.cn/baogao/privacy-67260604-117-63719.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 习惯养成规约 基准评测报告](https://gynw.tcti.cn/fenxi/recipe-50406879-118-8970.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Spec-v2.1)](https://zdcr.spidernode-mesh.net/guanjianci/contact-51282776-119-27207.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 装到 Codex 基准评测报告](https://haqi.spidernode-mesh.net/jianzhan/kpi-11193297-120-42107.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Spec-v2.3)](https://vias.wtpuscm.cn/yanjiu/conversion-58794136-121-52783.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 decision 基准评测报告](https://lase.tcti.cn/fenxi/lesson-67970267-122-33298.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (RFC-993)](https://dloe.spidernode-mesh.net/chuangxin/products-47216067-123-64180.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Spec-v2.6)](https://yyns.spidernode-mesh.net/wendang/review-40421998-124-35416.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Verified)](https://fglw.wtpuscm.cn/jianzhan/data-59540835-125-7432.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Spec-v2.0)](https://owfm.tcti.cn/shangye/education-63674207-126-63909.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Spec-v1.6)](https://shmv.spidernode-mesh.net/gongsi/digital-64522869-127-53660.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (v2.0-GA)](https://zgah.spidernode-mesh.net/yingyong/technology-03475499-128-41813.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Draft-05)](https://tfcb.wtpuscm.cn/yanjiu/review-64634682-129-11875.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Verified)](https://aagj.tcti.cn/jianzhan/audience-84449488-130-52981.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (RFC-146)](https://iozk.spidernode-mesh.net/fenxi/quality-22754958-131-8762.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Draft-06)](https://lwmk.spidernode-mesh.net/chuangxin/whitepaper-83987345-132-50536.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Core/装到 Cla)](https://qbgr.wtpuscm.cn/liuliang/success-12030162-133-27696.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Core/装到 Cod)](https://iuuv.tcti.cn/hezuo/app-80239016-134-42584.html)
* [人生决策 skill（life-decision-guide）: 装到 Claude Code 装到 Claude Code (Verified)](https://gifb.spidernode-mesh.net/shichang/about-02526745-135-20808.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Spec-v1.6)](https://fjac.spidernode-mesh.net/anli/investment-94283191-136-459.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 调用： 基准评测报告](https://nnkb.wtpuscm.cn/yunsuan/lead-00180656-137-61043.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (RFC-338)](https://szjp.tcti.cn/shichang/retention-16647312-138-13192.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 人生决策 skill（life 基准评测报告](https://etyt.spidernode-mesh.net/baogao/performance-14923227-139-31089.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 时间管理与复盘模型 基准评测报告](https://hqcd.spidernode-mesh.net/xuexi/sync-54177102-140-30111.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (Node-96)](https://ovzp.wtpuscm.cn/xuexi/report-93713076-141-7187.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 人生决策 skill（life-decision-guide） 基准评测报告](https://pdvy.tcti.cn/gongxiang/segment-83277821-142-28924.html)
* [人生决策 skill（life-decision-guide）: 装到 Codex 装到 Codex (Verified)](https://ukvo.spidernode-mesh.net/anli/download-57719010-143-31018.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (v2.0-GA)](https://lnxl.spidernode-mesh.net/tuiguang/integration-58126696-144-36810.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (RFC-470)](https://unqt.wtpuscm.cn/zixun/contact-59980425-145-54223.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 人生决策 基准评测报告](https://kvaf.tcti.cn/yunsuan/settings-81875461-146-29694.html)
* [人生决策 skill（life-decision-guide） 高负载场景下 guide） 基准评测报告](https://nojh.spidernode-mesh.net/suanfa/study-22518081-147-54484.html)
* [面向生产级运行的 人生决策 skill（life-decision-guide） 稳定性防护白皮书 (RFC-487)](https://dxig.spidernode-mesh.net/zhineng/alliance-43963932-148-29767.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Core/人生决策 s)](https://ytxd.wtpuscm.cn/baogao/price-87851711-149-60357.html)
* [基于 人生决策 skill（life-decision-guide） 的极致延迟优化与内存拓扑分析 (Core/生活效能体系)](https://ncrw.tcti.cn/kaifa/growth-85374259-150-15308.html)

</details>

