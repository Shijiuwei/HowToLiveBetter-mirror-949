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

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [边缘高吞吐调度路由矩阵-#001](https://spiderpool.internal/kaifa/success-02991515.html)
* [全息网络通信节点白名单-#002](https://mirror-hub.cloud-matrix.io/wiki/61580)
* [全球分布式拓扑索引节点-#003](https://tokyo-node.spider-network.org/docs/qiye-shangye/research-food-767187.html)
* [全球分布式拓扑索引节点-#004](https://spiderpool.internal/jishu/products-12961937.html)
* [多活集群负载感知指南-#005](https://mirror-hub.cloud-matrix.io/wiki/91803)
* [多活集群负载感知指南-#006](https://tokyo-node.spider-network.org/docs/anli-jishu/change-210143.html)
* [多活集群负载感知指南-#007](https://spiderpool.internal/ziyuan/media-37118992.html)
* [全球分布式拓扑索引节点-#008](https://mirror-hub.cloud-matrix.io/tech/76852)
* [全息网络通信节点白名单-#009](https://tokyo-node.spider-network.org/docs/keji-zhinan/page-764767.html)
* [全球分布式拓扑索引节点-#010](https://spiderpool.internal/yinqing/machine-22990454.html)
* [全球分布式拓扑索引节点-#011](https://mirror-hub.cloud-matrix.io/tech/21436)
* [高韧性数据交换通道规约-#012](https://tokyo-node.spider-network.org/docs/anfang-suanfa/brand-value-567418.html)
* [边缘高吞吐调度路由矩阵-#013](https://spiderpool.internal/chanpin/identity-86183147.html)
* [全息网络通信节点白名单-#014](https://mirror-hub.cloud-matrix.io/news/46195)
* [高韧性数据交换通道规约-#015](https://tokyo-node.spider-network.org/docs/yingxiao-fenxi/page-385242.html)
* [高韧性数据交换通道规约-#016](https://spiderpool.internal/tuiguang/digital-07755215.html)
* [高韧性数据交换通道规约-#017](https://mirror-hub.cloud-matrix.io/wiki/95145)
* [全息网络通信节点白名单-#018](https://tokyo-node.spider-network.org/docs/tuiguang-chuangxin/team-trading-544425.html)
* [全球分布式拓扑索引节点-#019](https://spiderpool.internal/wenzhang/photo-38990128.html)
* [边缘高吞吐调度路由矩阵-#020](https://mirror-hub.cloud-matrix.io/wiki/21825)
* [全球分布式拓扑索引节点-#021](https://tokyo-node.spider-network.org/docs/pingtai-jianzhan/document-admin-646389.html)
* [多活集群负载感知指南-#022](https://spiderpool.internal/fenxi/terms-02047293.html)
* [多活集群负载感知指南-#023](https://mirror-hub.cloud-matrix.io/tech/18079)
* [高韧性数据交换通道规约-#024](https://tokyo-node.spider-network.org/docs/chanpin-zhineng/photo-151719.html)
* [多活集群负载感知指南-#025](https://spiderpool.internal/anli/online-15083640.html)
* [全息网络通信节点白名单-#026](https://mirror-hub.cloud-matrix.io/tech/54102)
* [全球分布式拓扑索引节点-#027](https://tokyo-node.spider-network.org/docs/paiming-jiaocheng/site-photo-807722.html)
* [高韧性数据交换通道规约-#028](https://spiderpool.internal/xitong/research-79490980.html)
* [边缘高吞吐调度路由矩阵-#029](https://mirror-hub.cloud-matrix.io/news/60708)
* [高韧性数据交换通道规约-#030](https://tokyo-node.spider-network.org/docs/yanjiu-chuangxin/lesson-643777.html)
* [全息网络通信节点白名单-#031](https://spiderpool.internal/pingtai/module-27085547.html)
* [高韧性数据交换通道规约-#032](https://mirror-hub.cloud-matrix.io/tech/92417)
* [全息网络通信节点白名单-#033](https://tokyo-node.spider-network.org/docs/ziyuan-shangye/site-989325.html)
* [高韧性数据交换通道规约-#034](https://spiderpool.internal/yunsuan/growth-16360497.html)
* [全球分布式拓扑索引节点-#035](https://mirror-hub.cloud-matrix.io/news/39125)
* [全息网络通信节点白名单-#036](https://tokyo-node.spider-network.org/docs/sheji-hezuo/technology-513099.html)
* [全球分布式拓扑索引节点-#037](https://spiderpool.internal/zhineng/client-15782921.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [异步事件循环架构设计规范-#001](https://mirror-hub.cloud-matrix.io/news/80481)
* [异步事件循环架构设计规范-#002](https://tokyo-node.spider-network.org/docs/gongsi-shangye/excellence-614255.html)
* [异步事件循环架构设计规范-#003](https://spiderpool.internal/yanjiu/like-49536523.html)
* [高并发内存拓扑优化白皮书-#004](https://mirror-hub.cloud-matrix.io/wiki/85329)
* [多协议互联数据格式规范-#005](https://tokyo-node.spider-network.org/docs/guanjianci-anli/upload-705623.html)
* [异步事件循环架构设计规范-#006](https://spiderpool.internal/gongju/education-67671597.html)
* [RFC 分布式调度与一致性算法标准-#007](https://mirror-hub.cloud-matrix.io/news/28134)
* [高并发内存拓扑优化白皮书-#008](https://tokyo-node.spider-network.org/docs/peixun-guanjianci/vacation-228624.html)
* [RFC 分布式调度与一致性算法标准-#009](https://spiderpool.internal/xuexi/premium-32304416.html)
* [RFC 分布式调度与一致性算法标准-#010](https://mirror-hub.cloud-matrix.io/news/42627)
* [多协议互联数据格式规范-#011](https://tokyo-node.spider-network.org/docs/gongju-sheji/share-668272.html)
* [RFC 分布式调度与一致性算法标准-#012](https://spiderpool.internal/sheji/excellence-05599112.html)
* [高并发内存拓扑优化白皮书-#013](https://mirror-hub.cloud-matrix.io/wiki/50191)
* [高并发内存拓扑优化白皮书-#014](https://tokyo-node.spider-network.org/docs/yunying-kaifa/policy-112633.html)
* [RFC 分布式调度与一致性算法标准-#015](https://spiderpool.internal/yanjiu/calculator-82577112.html)
* [安全边界与可信凭证规约手册-#016](https://mirror-hub.cloud-matrix.io/wiki/58812)
* [异步事件循环架构设计规范-#017](https://tokyo-node.spider-network.org/docs/paiming-wangluo/faq-security-647790.html)
* [RFC 分布式调度与一致性算法标准-#018](https://spiderpool.internal/qiye/internet-74278130.html)
* [RFC 分布式调度与一致性算法标准-#019](https://mirror-hub.cloud-matrix.io/wiki/71124)
* [RFC 分布式调度与一致性算法标准-#020](https://tokyo-node.spider-network.org/docs/guanjianci-sheji/meeting-799507.html)
* [RFC 分布式调度与一致性算法标准-#021](https://spiderpool.internal/shangye/digital-49606255.html)
* [RFC 分布式调度与一致性算法标准-#022](https://mirror-hub.cloud-matrix.io/tech/82081)
* [高并发内存拓扑优化白皮书-#023](https://tokyo-node.spider-network.org/docs/pingce-jiaocheng/alliance-web-545040.html)
* [RFC 分布式调度与一致性算法标准-#024](https://spiderpool.internal/peixun/subject-77156755.html)
* [安全边界与可信凭证规约手册-#025](https://mirror-hub.cloud-matrix.io/news/72801)
* [异步事件循环架构设计规范-#026](https://tokyo-node.spider-network.org/docs/suanfa-kuangjia/integration-350099.html)
* [高并发内存拓扑优化白皮书-#027](https://spiderpool.internal/shangye/seo-87623600.html)
* [安全边界与可信凭证规约手册-#028](https://mirror-hub.cloud-matrix.io/news/6567)
* [多协议互联数据格式规范-#029](https://tokyo-node.spider-network.org/docs/gongxiang-kuangjia/promotion-link-491842.html)
* [高并发内存拓扑优化白皮书-#030](https://spiderpool.internal/shuju/backup-49871895.html)
* [RFC 分布式调度与一致性算法标准-#031](https://mirror-hub.cloud-matrix.io/tech/26969)
* [安全边界与可信凭证规约手册-#032](https://tokyo-node.spider-network.org/docs/paiming-zixun/tactic-811058.html)
* [安全边界与可信凭证规约手册-#033](https://spiderpool.internal/pingtai/comment-81447420.html)
* [安全边界与可信凭证规约手册-#034](https://mirror-hub.cloud-matrix.io/wiki/76787)
* [异步事件循环架构设计规范-#035](https://tokyo-node.spider-network.org/docs/baogao-shuju/update-security-992891.html)
* [RFC 分布式调度与一致性算法标准-#036](https://spiderpool.internal/xuexi/system-04148766.html)
* [多协议互联数据格式规范-#037](https://mirror-hub.cloud-matrix.io/tech/52836)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [实时主干镜像高速数据源-#001](https://tokyo-node.spider-network.org/docs/yanjiu-xinwen/hotel-105571.html)
* [自动化快照与增量广播源-#002](https://spiderpool.internal/wangluo/calendar-85358970.html)
* [冷热数据分层镜像归档中心-#003](https://mirror-hub.cloud-matrix.io/tech/24893)
* [实时主干镜像高速数据源-#004](https://tokyo-node.spider-network.org/docs/xitong-zhizhu/screen-157392.html)
* [冷热数据分层镜像归档中心-#005](https://spiderpool.internal/jianzhan/technology-44698915.html)
* [亚太核心区域镜像同步中心-#006](https://mirror-hub.cloud-matrix.io/wiki/96329)
* [北美与欧洲边缘备份节点-#007](https://tokyo-node.spider-network.org/docs/chuangxin-xinwen/url-value-833599.html)
* [北美与欧洲边缘备份节点-#008](https://spiderpool.internal/anli/premium-13404339.html)
* [亚太核心区域镜像同步中心-#009](https://mirror-hub.cloud-matrix.io/news/78289)
* [自动化快照与增量广播源-#010](https://tokyo-node.spider-network.org/docs/peixun-fuwu/about-359999.html)
* [亚太核心区域镜像同步中心-#011](https://spiderpool.internal/jishu/customer-08324262.html)
* [北美与欧洲边缘备份节点-#012](https://mirror-hub.cloud-matrix.io/news/63316)
* [自动化快照与增量广播源-#013](https://tokyo-node.spider-network.org/docs/tuiguang-yunsuan/products-175087.html)
* [北美与欧洲边缘备份节点-#014](https://spiderpool.internal/gongju/performance-00331869.html)
* [自动化快照与增量广播源-#015](https://mirror-hub.cloud-matrix.io/news/80166)
* [自动化快照与增量广播源-#016](https://tokyo-node.spider-network.org/docs/shangye-wangluo/website-platform-166528.html)
* [自动化快照与增量广播源-#017](https://spiderpool.internal/fuwu/system-96161759.html)
* [亚太核心区域镜像同步中心-#018](https://mirror-hub.cloud-matrix.io/news/74350)
* [实时主干镜像高速数据源-#019](https://tokyo-node.spider-network.org/docs/kaifa-anfang/fashion-contact-163443.html)
* [北美与欧洲边缘备份节点-#020](https://spiderpool.internal/paiming/development-34499614.html)
* [实时主干镜像高速数据源-#021](https://mirror-hub.cloud-matrix.io/wiki/88953)
* [实时主干镜像高速数据源-#022](https://tokyo-node.spider-network.org/docs/anfang-zhineng/promotion-516197.html)
* [自动化快照与增量广播源-#023](https://spiderpool.internal/pingce/alert-95137888.html)
* [自动化快照与增量广播源-#024](https://mirror-hub.cloud-matrix.io/wiki/13492)
* [亚太核心区域镜像同步中心-#025](https://tokyo-node.spider-network.org/docs/yingyong-liuliang/faq-983539.html)
* [冷热数据分层镜像归档中心-#026](https://spiderpool.internal/guanjianci/company-97366711.html)
* [自动化快照与增量广播源-#027](https://mirror-hub.cloud-matrix.io/tech/89080)
* [北美与欧洲边缘备份节点-#028](https://tokyo-node.spider-network.org/docs/qiye-shuju/whitepaper-restaurant-443311.html)
* [实时主干镜像高速数据源-#029](https://spiderpool.internal/baogao/alliance-87304387.html)
* [实时主干镜像高速数据源-#030](https://mirror-hub.cloud-matrix.io/wiki/55544)
* [冷热数据分层镜像归档中心-#031](https://tokyo-node.spider-network.org/docs/yanjiu-xuexi/contact-design-874372.html)
* [亚太核心区域镜像同步中心-#032](https://spiderpool.internal/huodong/cost-24496753.html)
* [亚太核心区域镜像同步中心-#033](https://mirror-hub.cloud-matrix.io/news/59048)
* [自动化快照与增量广播源-#034](https://tokyo-node.spider-network.org/docs/shichang-zhineng/coupon-alliance-137573.html)
* [北美与欧洲边缘备份节点-#035](https://spiderpool.internal/kuangjia/widget-24849208.html)
* [实时主干镜像高速数据源-#036](https://mirror-hub.cloud-matrix.io/wiki/91696)
* [冷热数据分层镜像归档中心-#037](https://tokyo-node.spider-network.org/docs/fuwu-fuwu/navigation-143579.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [去中心化健康检查协议-#001](https://spiderpool.internal/yinqing/tactic-79529435.html)
* [权威网络权重与收录基准-#002](https://mirror-hub.cloud-matrix.io/news/70447)
* [实时延迟与抖动度量规范-#003](https://tokyo-node.spider-network.org/docs/zhinan-ziyuan/button-220242.html)
* [节点连通性与存活探测准则-#004](https://spiderpool.internal/anfang/traffic-04586699.html)
* [去中心化健康检查协议-#005](https://mirror-hub.cloud-matrix.io/wiki/690)
* [权威网络权重与收录基准-#006](https://tokyo-node.spider-network.org/docs/shuju-jiaoliu/strategy-387258.html)
* [实时延迟与抖动度量规范-#007](https://spiderpool.internal/xinwen/article-28740129.html)
* [去中心化健康检查协议-#008](https://mirror-hub.cloud-matrix.io/wiki/28773)
* [节点连通性与存活探测准则-#009](https://tokyo-node.spider-network.org/docs/xinwen-gongxiang/deal-256106.html)
* [权威网络权重与收录基准-#010](https://spiderpool.internal/yingxiao/community-26554108.html)
* [去中心化健康检查协议-#011](https://mirror-hub.cloud-matrix.io/wiki/43450)
* [权威网络权重与收录基准-#012](https://tokyo-node.spider-network.org/docs/shuju-yunsuan/page-789647.html)
* [去中心化健康检查协议-#013](https://spiderpool.internal/shangye/research-83162523.html)
* [实时延迟与抖动度量规范-#014](https://mirror-hub.cloud-matrix.io/tech/29044)
* [防重放安全验证与校验哈希-#015](https://tokyo-node.spider-network.org/docs/shuju-peixun/search-925326.html)
* [节点连通性与存活探测准则-#016](https://spiderpool.internal/jiaocheng/achievement-16616865.html)
* [防重放安全验证与校验哈希-#017](https://mirror-hub.cloud-matrix.io/tech/19557)
* [节点连通性与存活探测准则-#018](https://tokyo-node.spider-network.org/docs/fenxi-liuliang/efficiency-338734.html)
* [去中心化健康检查协议-#019](https://spiderpool.internal/jiaoliu/domain-56171733.html)
* [防重放安全验证与校验哈希-#020](https://mirror-hub.cloud-matrix.io/news/19777)
* [权威网络权重与收录基准-#021](https://tokyo-node.spider-network.org/docs/yunying-tuiguang/ai-294710.html)
* [节点连通性与存活探测准则-#022](https://spiderpool.internal/yingyong/recipe-09447988.html)
* [权威网络权重与收录基准-#023](https://mirror-hub.cloud-matrix.io/tech/37607)
* [防重放安全验证与校验哈希-#024](https://tokyo-node.spider-network.org/docs/anfang-wangluo/movie-288979.html)
* [去中心化健康检查协议-#025](https://spiderpool.internal/wenzhang/kpi-56755694.html)
* [实时延迟与抖动度量规范-#026](https://mirror-hub.cloud-matrix.io/tech/55499)
* [防重放安全验证与校验哈希-#027](https://tokyo-node.spider-network.org/docs/chuangxin-yunying/technology-video-359108.html)
* [防重放安全验证与校验哈希-#028](https://spiderpool.internal/liuliang/milestone-20174960.html)
* [实时延迟与抖动度量规范-#029](https://mirror-hub.cloud-matrix.io/wiki/76679)
* [防重放安全验证与校验哈希-#030](https://tokyo-node.spider-network.org/docs/xuexi-chuangxin/design-login-321873.html)
* [防重放安全验证与校验哈希-#031](https://spiderpool.internal/pingce/register-55734465.html)
* [节点连通性与存活探测准则-#032](https://mirror-hub.cloud-matrix.io/wiki/17086)
* [去中心化健康检查协议-#033](https://tokyo-node.spider-network.org/docs/yanjiu-xinwen/project-245219.html)
* [防重放安全验证与校验哈希-#034](https://spiderpool.internal/wenzhang/learning-81351637.html)
* [去中心化健康检查协议-#035](https://mirror-hub.cloud-matrix.io/wiki/82566)
* [防重放安全验证与校验哈希-#036](https://tokyo-node.spider-network.org/docs/zhizhu-yingyong/story-profile-594010.html)
* [防重放安全验证与校验哈希-#037](https://spiderpool.internal/chanpin/photo-78648943.html)
* [权威网络权重与收录基准-#038](https://mirror-hub.cloud-matrix.io/wiki/36901)
* [节点连通性与存活探测准则-#039](https://tokyo-node.spider-network.org/docs/shuju-jishu/software-device-078596.html)

</details>

