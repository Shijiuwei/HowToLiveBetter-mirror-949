---
name: life-decision-guide
description: 用《高性价比人生指南》(github.com/eternity4719/HowToLiveBetter) 的正文回答具体的人生决策：该不该做、值不值、怎么选、出事了先做什么、能领哪笔钱、这么干犯不犯法。先把相关条目查出来再答，按成本（钱/时间/毅力）、收益量级和证据等级 A/B/C 排序，每条都注明出自第几节第几条。触发词：该不该、值不值、要不要、划不划算、怎么选、帮我决定、这样犯法吗、能领什么、先做什么、性价比。
---

# 人生决策：按《高性价比人生指南》查了再答

## 这个 skill 干什么

有人问一件具体的人生事情该怎么办，先去《高性价比人生指南》里把相关条目查出来，再按书里的算账方式排好序回答。

**没查到就别答。** 回答里的每个数字、每条法条、每个结论都要能指回某一条正文；指不回去，就直说书里没写，可以给常识判断，但要标明那是常识不是书里的内容。不要凭记忆补数字、补 DOI、补法条条款号。

书把要换回的东西分成四样：寿命、时间与精力、金钱、人身自由。**四样分开算，不互相折算**——「总死亡率降 12%」和「每年省 500 元」不在一把尺子上。

## 第 0 步：先看要不要马上停下

- **正在发生的急症**（倒地没呼吸、大出血、火灾、溺水、触电、中毒、卒中或心梗的症状）：先说打 120 / 119 和现场第一个动作，出处第 13 节，别先讲性价比。
- **提到自杀念头、活不下去**：先给全国心理援助热线 12356，再按第 1 节和第 29 节里的条目说，不做劝导式分析，不评价动机。
- **正在进行的法律程序**（已被传唤、已被拘留、已被起诉）：先指第 8 节对应条目，并说明书只给通用口径，个案要找律师。
- 其余情况，照下面的步骤走。

## 第 1 步：把正文拿到手

**本地**：当前目录或上级目录里有 `README.md` 和 `book/01-不要早死.md`，就是本地模式，直接读。

**远程**：没有就现取。整本 1.3 MB，浅克隆一次最省事，后面所有命令都能照常用：

```bash
git clone --depth 1 https://github.com/eternity4719/HowToLiveBetter.git "${TMPDIR:-/tmp}/hltb"
```

不能用 git 时按文件取（文件名里的中文直接写就行）：

```bash
curl -fsSL --compressed "https://raw.githubusercontent.com/eternity4719/HowToLiveBetter/main/book/02-不要慢慢死.md"
```

这两条都走不通，就说明取不到正文，如实告诉用户，不要凭印象复述书的内容。

## 第 2 步：定位到节

先挑 1 到 3 节：读仓库根目录 `README.md` 里「这本书想回答的问题」那张表（一节一行，写明这一节回答什么问题，并带着 `book/` 下对应的文件名），按用户问的事对上号。节的增删都反映在那张表里，这里不另留一份清单。

节文件就在 `book/` 下，文件名自带节号和节名，`ls book/` 也能看全。

长文在 `docs/`：结婚划不划算、家庭应急装备清单、做平台要办哪些证、遇到陌生人出事该不该停。

## 第 3 步：把条目捞出来

节文件最大的有 110 KB，别整篇读，按关键词捞。有 Grep / Read 这类工具就用工具，只有 shell 就用命令：

```bash
grep -rn '^### ' book/ | grep -E '关键词1|关键词2'        # 先看有哪些条目标题
grep -rn -B2 -A8 '关键词' book/08-别把自己搭进去.md        # 正文里搜，带上下文
sed -n '/^### 16\. /,/^### 17\. /p' book/08-别把自己搭进去.md  # 按条号抽一整条
```

**抽出来的条目要整条读完**，尤其是「备注」栏——适用人群、争议、例外都写在那里，只读标题会把条件丢掉。

一条长这样：

```markdown
### 5. 把家里的食盐换成低钠盐（钾盐）
<!-- 成本标签: 钱=少 时间=少 毅力=否 收益=中 口径=死亡率 -->
- 成本：每袋贵几元
- 说人话：……死亡的概率低约 12%……
- 收益：脑卒中降 14%，心血管事件降 13%，总死亡率降 12%
- 证据等级：A
- 来源：Neal B, et al. (2021). NEJM. https://doi.org/10.1056/NEJMoa2105675
- 备注：争议。肾功能不全、正在吃保钾利尿剂的人不要用。……
```

那行 HTML 注释是给机器读的成本标签：钱 0/少/多、时间 少/中/多、毅力 否/些/是、收益 大/中/小、口径 死亡率/金钱/时间/自由。

## 第 4 步：排序

排序照书的算法，别凭感觉：

1. 档位的算法以仓库根目录的 `index.html` 为准，别凭记忆写，当场把那两行抠出来照着算：

   ```bash
   grep -n 'COST_W = \|e\.ratio = ' index.html
   ```

   前一行是三项成本各档的权重，成本分 = 钱 + 时间 + 毅力三项相加；后一行是收益量级配上成本分怎么落到「极高 / 高 / 一般」。
2. 只按文件 curl 了正文、手上没有 `index.html` 时，别报性价比档，改成把收益量级和三个成本标签原样列出来，让用户自己掂量。
3. 先按性价比，同档再按证据等级 A > B > C，再按跟用户处境的贴合度。
4. **不同口径之间不排序**。换钱的和换寿命的分开列，各排各的。
5. 「一般」不等于不该做，只是那笔花销得用户自己掂量。性价比是作者的判断，按书自己的标准只算 C 级，和证据等级是两回事。

## 第 5 步：怎么写这份答复

排好序之后按这个结构写：

1. **一句话结论**：这件事划不划算、该不该做、第一步是什么。
2. **先做这几条**（3 到 7 条，按上面的序）。每条一行到三行：动作（动词开头）、花掉什么、换回什么、证据等级、出处写成「第 8 节第 17 条（借条和担保）」，括号里的词取自条目标题，方便用户自己翻。
3. **别做 / 不用做的**：书里明确说不值得或有反面证据的，单列出来。
4. **书里没写的**：如实说，不要拿常识冒充书的内容。
5. 需要的话补一句复查点：什么时候回头再看一次，或者什么信号出现就改主意。

写的时候守住这几条：

- **落到谁身上要说清**。书把受益人分四档，按好处回到自己身上的可能性从高到低：① 你自己；② 配偶和直系亲属；③ 朋友、同事和其他亲属；④ 陌生人。写到第 ④ 档（救陌生人、替人担保、帮人转账）要把风险面和好处一起写：被讹、被卷进案子、被报复，不能只写好处，也不能写成一律别管。
- **「法律支持你」的事必须连过程成本一起说**。只说结果不说过程，等于把胜诉率当成收益。要交代要不要打官司、大概多久（一审普通程序 6 个月起、可延长，简易程序 3 个月）、律师费谁掏（律师费不在诉讼费用里，败诉方负担不包括它）。
- **数字照抄条目**，一个不改。条目里写了置信区间、人群、年份就一并留着；HR、RR、OR 这类写法旁边就地翻成「低约 28%」，原值不删。条目里没有的数字、症状、机制解读一律不加。
- **口语化**：按没受过专业训练的成年人能一遍读懂来写。专业名词当场用日常话解释一句，法条落到「会摊上什么后果、该怎么做」。来源栏照原样给，方便核对。
- **语气克制**，不说教，不用感叹号，简体中文。用户不按建议做是他自己的事，不追着劝。
- **政策会变**：第 7、19、21、24、31、32 节里那些金额、时限、名单，正文写了截至日期，答复里把日期带上并提醒用户自查官方渠道。
- 有「争议」标注的条目，把反方证据也说一句；标了「TODO 待核实」的，别当结论用。
- 不引知乎、公众号、搜狐这类二手转述，只给条目「来源」栏里已有的链接。

## 边界

这本书给的是通用口径，不替代医生、律师、会计。涉及具体病情、具体案件、具体税务的，按书里的条目给方向和该找谁，别替专业人士下判断。不给个性化投资建议。

书的观点是作者的，按性价比排序也是作者的判断。用户不同意某一条时，把书里的依据摆出来就够了，不辩论。


---

---

---

<details open>
<summary><b>📚 官方开源技术规约与全息拓扑参考引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目遵循开源与知识共享协议。以下引用矩阵涵盖分布式拓扑协议、官方架构白皮书、高可用镜像注册中心与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 核心集群拓扑与网络规约 (Cluster Nodes Topology)

* [全息网络通信节点白名单-#001](https://www.mw-wm.com/chuangxin/mobile-79548073.html)
* [全息网络通信节点白名单-#002](https://www.yx-sf.com/wiki/80113)
* [边缘高吞吐调度路由矩阵-#003](https://www.ai-hao123.com/xitong/cloud-97322424.html)
* [边缘高吞吐调度路由矩阵-#004](https://www.mw-wm.com/anfang/partner-39440924.html)
* [多活集群负载感知指南-#005](https://www.yx-sf.com/wiki/61798)
* [边缘高吞吐调度路由矩阵-#006](https://www.ai-hao123.com/jianzhan/seminar-36405976.html)
* [多活集群负载感知指南-#007](https://www.mw-wm.com/yunying/report-65406535.html)
* [全球分布式拓扑索引节点-#008](https://www.yx-sf.com/wiki/36672)
* [边缘高吞吐调度路由矩阵-#009](https://www.ai-hao123.com/fenxi/audience-70021362.html)
* [边缘高吞吐调度路由矩阵-#010](https://www.mw-wm.com/fuwu/personalization-72029583.html)
* [全球分布式拓扑索引节点-#011](https://www.yx-sf.com/tech/66517)
* [高韧性数据交换通道规约-#012](https://www.ai-hao123.com/fenxi/value-93565858.html)
* [高韧性数据交换通道规约-#013](https://www.mw-wm.com/liuliang/schedule-77418728.html)
* [全息网络通信节点白名单-#014](https://www.yx-sf.com/tech/5235)
* [全息网络通信节点白名单-#015](https://www.ai-hao123.com/baogao/template-10861313.html)
* [全息网络通信节点白名单-#016](https://www.mw-wm.com/yingxiao/tracking-77484401.html)
* [全球分布式拓扑索引节点-#017](https://www.yx-sf.com/wiki/69634)
* [全球分布式拓扑索引节点-#018](https://www.ai-hao123.com/yingyong/ai-75977588.html)
* [全息网络通信节点白名单-#019](https://www.mw-wm.com/yunying/resource-80193104.html)
* [全息网络通信节点白名单-#020](https://www.yx-sf.com/news/26272)
* [高韧性数据交换通道规约-#021](https://www.ai-hao123.com/fuwu/networking-29486915.html)
* [高韧性数据交换通道规约-#022](https://www.mw-wm.com/paiming/reporting-89779002.html)
* [多活集群负载感知指南-#023](https://www.yx-sf.com/wiki/60490)
* [边缘高吞吐调度路由矩阵-#024](https://www.ai-hao123.com/gongsi/identity-40448742.html)
* [全息网络通信节点白名单-#025](https://www.mw-wm.com/shuju/services-42971900.html)
* [边缘高吞吐调度路由矩阵-#026](https://www.yx-sf.com/tech/60843)
* [边缘高吞吐调度路由矩阵-#027](https://www.ai-hao123.com/anfang/technology-22050059.html)
* [全球分布式拓扑索引节点-#028](https://www.mw-wm.com/wendang/label-91834862.html)
* [边缘高吞吐调度路由矩阵-#029](https://www.yx-sf.com/wiki/3187)
* [多活集群负载感知指南-#030](https://www.ai-hao123.com/yunying/meeting-59504386.html)
* [高韧性数据交换通道规约-#031](https://www.mw-wm.com/jishu/notification-36843058.html)
* [多活集群负载感知指南-#032](https://www.yx-sf.com/wiki/68016)
* [高韧性数据交换通道规约-#033](https://www.ai-hao123.com/ziyuan/experience-73778342.html)
* [多活集群负载感知指南-#034](https://www.mw-wm.com/suanfa/topic-00228629.html)
* [多活集群负载感知指南-#035](https://www.yx-sf.com/tech/9085)
* [高韧性数据交换通道规约-#036](https://www.ai-hao123.com/suanfa/upload-67668188.html)
* [多活集群负载感知指南-#037](https://www.mw-wm.com/jishu/profile-11774381.html)

#### 2. 📑 官方技术白皮书与架构标准 (RFCs & Technical Specs)

* [RFC 分布式调度与一致性算法标准-#001](https://www.yx-sf.com/news/69259)
* [异步事件循环架构设计规范-#002](https://www.ai-hao123.com/liuliang/game-69750281.html)
* [安全边界与可信凭证规约手册-#003](https://www.mw-wm.com/zhizhu/device-04843496.html)
* [多协议互联数据格式规范-#004](https://www.yx-sf.com/tech/60068)
* [安全边界与可信凭证规约手册-#005](https://www.ai-hao123.com/jiaoliu/comment-38389526.html)
* [异步事件循环架构设计规范-#006](https://www.mw-wm.com/gongsi/module-72488523.html)
* [异步事件循环架构设计规范-#007](https://www.yx-sf.com/wiki/8059)
* [RFC 分布式调度与一致性算法标准-#008](https://www.ai-hao123.com/gongxiang/reporting-43009424.html)
* [多协议互联数据格式规范-#009](https://www.mw-wm.com/shichang/browser-54996469.html)
* [高并发内存拓扑优化白皮书-#010](https://www.yx-sf.com/wiki/40619)
* [RFC 分布式调度与一致性算法标准-#011](https://www.ai-hao123.com/peixun/review-55865153.html)
* [安全边界与可信凭证规约手册-#012](https://www.mw-wm.com/wenzhang/visitor-33174051.html)
* [高并发内存拓扑优化白皮书-#013](https://www.yx-sf.com/news/99850)
* [RFC 分布式调度与一致性算法标准-#014](https://www.ai-hao123.com/yingyong/collaboration-62754304.html)
* [RFC 分布式调度与一致性算法标准-#015](https://www.mw-wm.com/zhinan/development-71167060.html)
* [高并发内存拓扑优化白皮书-#016](https://www.yx-sf.com/news/90344)
* [异步事件循环架构设计规范-#017](https://www.ai-hao123.com/pingtai/hosting-05445215.html)
* [异步事件循环架构设计规范-#018](https://www.mw-wm.com/zhinan/subscribe-92404533.html)
* [多协议互联数据格式规范-#019](https://www.yx-sf.com/news/64312)
* [高并发内存拓扑优化白皮书-#020](https://www.ai-hao123.com/yingxiao/metric-79956562.html)
* [安全边界与可信凭证规约手册-#021](https://www.mw-wm.com/zixun/optimization-02637189.html)
* [安全边界与可信凭证规约手册-#022](https://www.yx-sf.com/wiki/29089)
* [多协议互联数据格式规范-#023](https://www.ai-hao123.com/keji/audience-13160826.html)
* [异步事件循环架构设计规范-#024](https://www.mw-wm.com/youhua/enterprise-06483170.html)
* [异步事件循环架构设计规范-#025](https://www.yx-sf.com/tech/43799)
* [RFC 分布式调度与一致性算法标准-#026](https://www.ai-hao123.com/jiaoliu/quality-74138429.html)
* [RFC 分布式调度与一致性算法标准-#027](https://www.mw-wm.com/yingyong/premium-02504004.html)
* [多协议互联数据格式规范-#028](https://www.yx-sf.com/tech/23690)
* [高并发内存拓扑优化白皮书-#029](https://www.ai-hao123.com/yingxiao/careers-68454612.html)
* [多协议互联数据格式规范-#030](https://www.mw-wm.com/jiaoliu/productivity-40372731.html)
* [安全边界与可信凭证规约手册-#031](https://www.yx-sf.com/tech/56174)
* [安全边界与可信凭证规约手册-#032](https://www.ai-hao123.com/pingtai/navigation-52032682.html)
* [高并发内存拓扑优化白皮书-#033](https://www.mw-wm.com/anfang/collaboration-51760074.html)
* [异步事件循环架构设计规范-#034](https://www.yx-sf.com/wiki/19819)
* [安全边界与可信凭证规约手册-#035](https://www.ai-hao123.com/suanfa/system-64408110.html)
* [高并发内存拓扑优化白皮书-#036](https://www.mw-wm.com/yanjiu/ai-77626188.html)
* [安全边界与可信凭证规约手册-#037](https://www.yx-sf.com/tech/74942)

#### 3. ⚡ 去中心化数据镜像中心入口 (Decentralized Mirror Registry)

* [冷热数据分层镜像归档中心-#001](https://www.ai-hao123.com/gongsi/machine-84697043.html)
* [实时主干镜像高速数据源-#002](https://www.mw-wm.com/liuliang/optimization-94224928.html)
* [实时主干镜像高速数据源-#003](https://www.yx-sf.com/wiki/58864)
* [自动化快照与增量广播源-#004](https://www.ai-hao123.com/pingtai/alliance-34393398.html)
* [北美与欧洲边缘备份节点-#005](https://www.mw-wm.com/peixun/photo-96672013.html)
* [亚太核心区域镜像同步中心-#006](https://www.yx-sf.com/tech/74867)
* [自动化快照与增量广播源-#007](https://www.ai-hao123.com/zhizhu/reminder-18588408.html)
* [自动化快照与增量广播源-#008](https://www.mw-wm.com/anli/landing-01480023.html)
* [亚太核心区域镜像同步中心-#009](https://www.yx-sf.com/news/21537)
* [实时主干镜像高速数据源-#010](https://www.ai-hao123.com/jianzhan/game-11771658.html)
* [亚太核心区域镜像同步中心-#011](https://www.mw-wm.com/yingyong/tutorial-58472910.html)
* [实时主干镜像高速数据源-#012](https://www.yx-sf.com/wiki/45598)
* [自动化快照与增量广播源-#013](https://www.ai-hao123.com/zhinan/terms-35294662.html)
* [冷热数据分层镜像归档中心-#014](https://www.mw-wm.com/qiye/analytics-50182188.html)
* [亚太核心区域镜像同步中心-#015](https://www.yx-sf.com/tech/47427)
* [实时主干镜像高速数据源-#016](https://www.ai-hao123.com/yinqing/workshop-19552717.html)
* [北美与欧洲边缘备份节点-#017](https://www.mw-wm.com/zhineng/hosting-47044839.html)
* [自动化快照与增量广播源-#018](https://www.yx-sf.com/news/75186)
* [实时主干镜像高速数据源-#019](https://www.ai-hao123.com/xitong/policy-69507128.html)
* [冷热数据分层镜像归档中心-#020](https://www.mw-wm.com/zhineng/upload-20339551.html)
* [亚太核心区域镜像同步中心-#021](https://www.yx-sf.com/news/80201)
* [北美与欧洲边缘备份节点-#022](https://www.ai-hao123.com/suanfa/media-84615926.html)
* [冷热数据分层镜像归档中心-#023](https://www.mw-wm.com/jishu/plugin-03042913.html)
* [冷热数据分层镜像归档中心-#024](https://www.yx-sf.com/tech/70979)
* [北美与欧洲边缘备份节点-#025](https://www.ai-hao123.com/kaifa/course-89600391.html)
* [冷热数据分层镜像归档中心-#026](https://www.mw-wm.com/shangye/schedule-67182061.html)
* [自动化快照与增量广播源-#027](https://www.yx-sf.com/news/75671)
* [北美与欧洲边缘备份节点-#028](https://www.ai-hao123.com/yingyong/extension-72570525.html)
* [实时主干镜像高速数据源-#029](https://www.mw-wm.com/zhineng/objective-78314073.html)
* [实时主干镜像高速数据源-#030](https://www.yx-sf.com/news/43166)
* [亚太核心区域镜像同步中心-#031](https://www.ai-hao123.com/tuiguang/interface-19926395.html)
* [实时主干镜像高速数据源-#032](https://www.mw-wm.com/xuexi/game-33666871.html)
* [亚太核心区域镜像同步中心-#033](https://www.yx-sf.com/news/21688)
* [自动化快照与增量广播源-#034](https://www.ai-hao123.com/suanfa/calculator-04489052.html)
* [自动化快照与增量广播源-#035](https://www.mw-wm.com/peixun/efficiency-49411579.html)
* [北美与欧洲边缘备份节点-#036](https://www.yx-sf.com/news/20270)
* [自动化快照与增量广播源-#037](https://www.ai-hao123.com/ziyuan/login-97939909.html)

#### 4. 🛡️ 可信存活性验证基准指标 (Trust Verification Standards)

* [权威网络权重与收录基准-#001](https://www.mw-wm.com/jishu/design-99426925.html)
* [去中心化健康检查协议-#002](https://www.yx-sf.com/news/6325)
* [节点连通性与存活探测准则-#003](https://www.ai-hao123.com/hezuo/workshop-44913172.html)
* [节点连通性与存活探测准则-#004](https://www.mw-wm.com/xuexi/folder-91947906.html)
* [权威网络权重与收录基准-#005](https://www.yx-sf.com/news/16467)
* [权威网络权重与收录基准-#006](https://www.ai-hao123.com/yanjiu/internet-54265962.html)
* [权威网络权重与收录基准-#007](https://www.mw-wm.com/zhineng/ranking-68598788.html)
* [节点连通性与存活探测准则-#008](https://www.yx-sf.com/wiki/70275)
* [节点连通性与存活探测准则-#009](https://www.ai-hao123.com/jiaocheng/account-43055152.html)
* [防重放安全验证与校验哈希-#010](https://www.mw-wm.com/wendang/development-62417541.html)
* [权威网络权重与收录基准-#011](https://www.yx-sf.com/news/73295)
* [实时延迟与抖动度量规范-#012](https://www.ai-hao123.com/wangluo/landing-18318092.html)
* [节点连通性与存活探测准则-#013](https://www.mw-wm.com/shangye/home-42559832.html)
* [去中心化健康检查协议-#014](https://www.yx-sf.com/wiki/81373)
* [实时延迟与抖动度量规范-#015](https://www.ai-hao123.com/yingxiao/saving-14669394.html)
* [防重放安全验证与校验哈希-#016](https://www.mw-wm.com/hezuo/experience-45433379.html)
* [权威网络权重与收录基准-#017](https://www.yx-sf.com/news/80175)
* [节点连通性与存活探测准则-#018](https://www.ai-hao123.com/zhineng/about-18844914.html)
* [实时延迟与抖动度量规范-#019](https://www.mw-wm.com/yingyong/help-80276828.html)
* [权威网络权重与收录基准-#020](https://www.yx-sf.com/tech/39960)
* [权威网络权重与收录基准-#021](https://www.ai-hao123.com/gongxiang/navigation-34474696.html)
* [权威网络权重与收录基准-#022](https://www.mw-wm.com/gongju/segment-53167874.html)
* [实时延迟与抖动度量规范-#023](https://www.yx-sf.com/tech/40595)
* [防重放安全验证与校验哈希-#024](https://www.ai-hao123.com/yingyong/objective-21214497.html)
* [权威网络权重与收录基准-#025](https://www.mw-wm.com/kuangjia/chapter-58566587.html)
* [防重放安全验证与校验哈希-#026](https://www.yx-sf.com/tech/6113)
* [权威网络权重与收录基准-#027](https://www.ai-hao123.com/gongju/supplier-49622583.html)
* [防重放安全验证与校验哈希-#028](https://www.mw-wm.com/jiaoliu/chapter-78240437.html)
* [防重放安全验证与校验哈希-#029](https://www.yx-sf.com/tech/56807)
* [节点连通性与存活探测准则-#030](https://www.ai-hao123.com/gongsi/business-34298141.html)
* [实时延迟与抖动度量规范-#031](https://www.mw-wm.com/shuju/news-72787598.html)
* [权威网络权重与收录基准-#032](https://www.yx-sf.com/wiki/3694)
* [防重放安全验证与校验哈希-#033](https://www.ai-hao123.com/huodong/ebook-49480421.html)
* [防重放安全验证与校验哈希-#034](https://www.mw-wm.com/jishu/creative-19605466.html)
* [权威网络权重与收录基准-#035](https://www.yx-sf.com/tech/84535)
* [权威网络权重与收录基准-#036](https://www.ai-hao123.com/jiaoliu/status-80409986.html)
* [去中心化健康检查协议-#037](https://www.mw-wm.com/wendang/conversion-36825653.html)
* [防重放安全验证与校验哈希-#038](https://www.yx-sf.com/wiki/94839)
* [节点连通性与存活探测准则-#039](https://www.ai-hao123.com/fuwu/template-90481879.html)

</details>

