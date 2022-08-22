---
title: "解密 GRE 逻辑题"
date: 2022-08-21T15:48:42+08:00
draft: false

description: "系统性剖析 GRE 逻辑题相关的所有知识点 + 11 类逻辑题型的解题方法，来自炜神《解密GRE系列课程-逻辑题》的 Bilibili 课程，炜神 YYDS！"
upd: "系统性剖析 GRE 逻辑题相关的所有知识点 + 11 类逻辑题型的解题方法，来自炜神《解密GRE系列课程-逻辑题》的 Bilibili 课程，炜神 YYDS！"

tags: ["笔记"]
categories: ["GRE"]
---

## 1. 论证(Argument)

**Argument**: a set of propositions(命题) in which one of the propositions is supported by the others.

**Conclusion**: the supported proposition.

**Premises**: the supporting propositions.

判断以下例子是不是论证：

- 万蜀黍很努力，所以他得以成功的。(explanation)
- 万蜀黍很努力，所以他**一定会**成功。(argument)
- 万蜀黍很不健康，因为他吃得特别多。(explanation)
- 万蜀黍**肯定**不健康，你看他吃得那么多。(argument)

<!--more-->

### 1.2 论证的分类

A. **演绎推理 (Deductive Arguments)**: an argument in which the arguer intends to give **complete** support to the conclusion (assuming the truthfulness of premises).

B. **归纳推理 (Inductive Arguments)**: an argument in which the arguer intends to give **strong** support to the conclusion(assuming the truthfulness of premises)

演绎推理范例：

1. 万蜀黍是英语老师。英语老师都很龌龊。所以，万蜀黍很龌龊。
2. 7+x=12 ∴ x=5
3. 万蜀黍喜欢吃桃子。青山学堂没有前途。所以，万蜀黍喜欢吃桃子且青山学堂没有前途。
4. 埃菲尔铁塔在巴黎。所以，埃菲尔铁塔在巴黎或万炜是世界足球先生。


**演绎推理的直观感受：可以符号化**

- 论证形式的理解重于话题内容日常意义的理解。
- 如果某个形式严谨，则符合所有这个形式的论证都是严谨的。

**演绎推理符号化**：

1. 万蜀黍是英语老师。英语老师都很龌龊。所以，万蜀黍很龌龊。

```
万蜀黍是英语老师。=> x is a T.
英语老师都很龌龊。=> All Ts are W.
所以，万炜很龌龊。=> So,x is W.
```
2. 7+x=12 ∴ x=5

```
7+x=12
∴ X=5
```

3. 万蜀黍喜欢吃桃子。青山学堂没有前途。所以，万蜀黍喜欢吃桃子且青山学堂没有前途。

```
万蜀黍喜欢吃桃子。=> p
青山学堂没有前途。=> q
所以，万蜀黍喜欢吃桃子且青山学堂没有前途。=>So, p·q
```
4. 埃菲尔铁塔在巴黎。所以，埃菲尔铁塔在巴黎或万炜是世界足球先生。

```
埃菲尔铁塔在巴黎。=> p
所以，埃菲尔铁塔在巴黎或万炜是世界足球先生。=> P V q
```

**归纳推理范例**：

1. 今早吃多了，然后这会儿肚子不舒服。估计是吃多导致肚子不舒服的。—— Causal Argument
2. 从人类记事起，太阳每天都是从东边升起。这说明，太阳一定是从东边升起。—— Analogical Argument
3. 青山学堂老师负责，专业知识过硬，而且课程廉价时间灵活，所以对于要考GRE的同学，青山学堂是他们的理想选择。一 Evaluative Argument

**归纳推理的直观感受：论证合理性的评价必须考虑内容的日常意义**。

演绎推理的评价方式：是否有效 (**validity**)

归纳推理的评价术语：有多强 (**strength**)

**论证类型与逻辑题型**：

- 如果题干涉及建立绝对严谨的论证——演绎体系
- 如果题干涉及论证的强弱性——归纳体系
- Otherwise——均有可能

范例：

- If the statements in the passage are true,then which of the following **must** on the basis of them be true? - Must Be True (Deduction)
- Which of the following conclusions is **best** supported by the information? - Most Strongly Supported (Induction)
- Which of the following, if true, most seriously **weakens** the argument? - Weaken (Induction)
- The conclusion is properly drawn if which of the following is assumed? - **Sufficient** Assumption (Deduction)
- Which of the following, if true, provides the **strongest** additional support for the argument? Strengthen (Induction)

### 1.2 归纳推理论证体系

GRE 重点考察归纳推理，几乎不考察演绎推理。

A. **解释型论证**：己知一个事件的发生，目标是探索其发生的原因（果 推 因）

例：

- 万蜀黍最近胖了。他肯定是吃得比以前多了。
- 万蜀黍最近吃得比以前多了，然后他果然变胖了。说明一定是吃多让他变胖的。
- 万蜀黍最近比以前吃得多了许多，所以一定是吃多让他变得那么胖的。

B. **预测型论证**：已知一个事件的发生，推测它将产生的结果（因 推 果）

例：万蜀黍最近吃得比以前多了许多，所以他之后一定会变胖的。

C. **类比型论证**：相似对象 S 与 S' 之间，基于 S 具有特点 P，推断 S' 也会具有特点 P。

例：万蜀黍几年前狂吃了一阵子，后来胖了很多。最近他又在狂吃，他之后肯定又会发胖。

D. **建议型论证**：目标是提出建议，支持某种行动

例：万蜀黍教得好，课程还便宜。所以，考GRE一定要找万蜀黍的课。

### 1.3 演绎推理规则体系

演绎推理体系晦涩且庞大，在 GRE 考试中占比极低，下面仅做粗略介绍。

**Symbolic Logic**

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208211706091.png)

The three "Laws of Thought" （逻辑学基本公理）

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208211717720.png)

Inference rule(单项推理)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208211725826.png)

Equivalence rule(可以单项推理)

![](https://wuhao97.oss-cn-hangzhou.aliyuncs.com/202208211726397.png)

## 2. 题型与解法

### 2.1 题型1: Boldface

In the argument given, the two portions in boldface play which of the following roles?

考察句子的功能：观点、

例：有人说，嫁人就要嫁万蜀黍，因为他**又高，又富**，虽然可能不算很帅。但其实，**这个建议实在是太离谱了**。多方证据显示，万蜀黍其实是个大渣男，嫁给他只会被他辜负。

问：黑体字作用是什么？

答：第一处给出了作者所反对的观点背后所依据的理由；第二处是作者自己的观点。

Boldface题的做题建议：

1. **淡化文章内容语义，关注文章形式符号**
2. 基于符号判断黑体字到底是
   1. 论证的前提还是结论，观点还是事实；
   2. 作者认可的还是作者反对的论证的部分；
   3. (让步)
3. 如果发现选项仍然剩下2个难以区分：回头看一眼结论的逻辑类型，结合文章内容(解释；建议；预测)

例：

**有人说**，嫁人就要嫁万蜀黍，**因为**他又高，又富，**虽然**可能不算很帅。**但其实**，这个建议实在是太离谱了。**多方证据显示**，万蜀黍其实是个大渣男，嫁给他只会被他辜负。


【practice】Stylistic evidence and laboratory evidence strongly s*upport the claim that* [引用观点] the magnificent painting Garden of Eden is a work of the Flemish master van Eyck. Nevertheless [作者观点], **the painting must have been the work of someone else**, as anyone with a little historical and zoological knowledge can tell merely by looking at the painting [展开/证据]. **The animals in the painting are all vivid representations of actual animals, including armadillos**. Yet armadillos are native only to Americas, and van Eyck died decades before Europeans reached the Americas.

In the argument given, the two highlighted portions play which of the following roles?

A.The first is a position that the argument seeks to reject, the second is evidence that the argument uses against that position.

B.The first and the second are each pieces of evidence that have been used to support the position that the argument opposes.

C.The first presents the main conclusion of the argument; the second provides evidence in support of that conclusion.

D.The first is a judgment that serves as the basis for the main conclusion of the argument; the second states that main conclusion

E.The first is an intermediate conclusion drawn in order to support a further conclusion stated in the argument; the second provides evidence in support of that intermediate conclusion.

解析：选 C。

🔺【practice】In most coastal regions,the level of the sea is rising in relation to the land by one to two millimeters a year,and this trend [事实] would be explained by the hypothesis [作者观点] that at the North and South Poles,the amount of ice that melts during the summer now exceeds the amount forms during the winter.The hypothesis is not undermined by observations [排除一种可能的误解] that **sea levels are falling relative to the Scandinavian coast by four millimeters a yea**r. Much land in northern latitudes,including Scandinavia,is still rising in response to being freed of the enormous weight of the ice that used to cover it during the last ice age,and **in Scandinavia the land is now rising faster than the sea**. [事实/ 展开]

In the passage,the two highlighted portions play which of the following roles?

A.The first states observations the accuracy of which is challenged in the passage;the second is part of the ground on which that challenge is based.

B.The first states observations that, according to the passage, are incompatible with a certain hypothesis; the second is part of the grounds offered in support of a revision of that hypothesis.

C.The first states observations that, according to the passage,can be reconciled with a certain hypothesis;the second describes a phenomenon that is the factual basis of that reconciliation.

D.The first presents a phenomenon,two competing explanations of which are considered in the passage;the second is the explanation of the phenomenon that the passage argues is correct.

E.The first provides evidence against a position;the second is that position.

解析：事实永远不可能被质疑，选项 A 错误；选 C。

### 2.2 题型2: Must Be True

题干：If the statements in the passage are true, then which of the following must on the basis of them be true?

题干：From the information given, which of the following can properly be **concluded**? 

题干：Which of the following most logically follows from the passage?

Must Be True题的做题建议：

1. 考的是**演绎推理**，追求绝对的严谨性；
2. 不需要过分在意这种题型，**考频极低**

【practice】The manuscript of a previously unknown ragtime piano piece recently been discovered. The manuscript is unsigned and has the notation "New York City,1899"written on it. In 1899 Ben Harney was the New York musician most closely associated with ragtime.The style of the piece,however,is closer to that of Scott Joplin,but scholars believe that Joplin did not visit New York before 1906.

From the information given,which of the following can properly be concluded?

A.If Scott Joplin wrote the piece,either he did visit New York before 1906 or the notation on the manuscript does not reflect the place and date of composition of the piece.

B.Ben Harney was stylistically influenced by Scott Joplin's music before Joplin ever visited New York.

C.If Scott Joplin did not visit New York before 1906,then neither Ben Harney nor Scott Joplin composed the work.

D.The notation on the manuscript was intended to signify something other than the place and date of composition of the piece.

E.If the dating on the manuscript accurately reflects when and where the piece was composed,then Scott Joplin visited New York earlier than scholars have believed.

解析：选 A。

### 2.3 题型3: Most Strongly Supported

题干：The information given, if accurate, most strongly supports which of the following hypotheses?

题干：Which of the following conclusions is best supported by the information?

Most Strongly Supported题的做题建议：

1. 考的是**归纳推理**，所有正确选项都不是绝对严谨的推理结论，不要对文章进行符号化处理：
2. 我们做的是最**合理的推测**（比如：已知AB足够相似，则可以进行合理类比，己知XY有强因果关系，则有X就可以推Y，反之亦然）

🔺【practice】Normally, seeds of Emmenathe penduliflora stay dormant for years and germinate only when a fire burns through their habitat. Nitrogen dioxide in the smoke induces the seeds to germinate. Fires clear the **bush**, allowing germinating seeds to receive the sunlight they need to grow. The plants mature quickly, produce seeds, and then die. In areas with heavy automobile traffic, however, the seed germinates in the absence of fire, with automobile exhaust supplying the required nitrogen dioxide.

The information given, if accurate, **most strongly supports** which of the following hypotheses?

A. Fires in the habitat of E.penduliflora do not entirely destroy the plant's seeds even in the places where the fires burn most intensely.

B. The nitrogen dioxide in automobile exhaust cannot harm plants of E.penduliflora after germination.

C. If human intervention decreases the number of fires in the habitat of E.penduliflora, automobile exhaust can replicate the conditions the plant requires in order to thrive.

D. Within the habitat of E.penduliflora, natural fires are significantly more frequent in areas with heavy automobile traffic than they are in other areas.

E. Unless E.penduliflora seeds that have germinated can survive in the shade, automobile exhaust threatens the long-term survival of the plant in areas with heavy automobile traffic.

文章信息：germinate 需要 二氧化氮；grow 需要光。

解析：选项 AB 信息不足，无法判断；选项，thrive 还需要光；选 E，**unless = if not**。

【practice】Many musicians who would like to produce the rich sonorities of the double bass have been kept from doing so because the sheer length and bulk of the instrument require a tall player with long arms. A recently invented electric double bass produces the same tones as a traditional double bass but is significantly smaller. Most jobs for bassists, however, are with musical ensembles unwilling to forgo the visual appeal of the traditional double bass.

Which of the following is most strongly supported by the information given?

A. Most musicians who would be interested in playing the recently invented electric double bass currently play the traditional double bass.

B. Being tall and long-armed is unlikely to become irrelevant for a professional career as a bassist in the near future.

C. Many musical ensembles place a higher value on the visual appeal of an instrument than on the richness of the sounds that instrument can produce.

D. The number of musicians who are tall and have long arms is insufficient to meet the current demand for bass players.

E. Reducing the size of a musical instrument almost invariably reduces the visual appeal of the instrument.

解析：选 B；选项 C，重要性的比较是不成立的。

### 2.4 题型4: Paradox

题干：Which of the following, if true, would help resolve the apparent paradox presented above?

题干：Which of the following, if true, best reconciles the apparent discrepancy presented in the passage?

例：

万炜比上次考LSAT前更努力学习了，但是他的LSAT成绩却比之前更差了。

Which one of the following, if true, most helps to resolve the apparent paradox in the situation described above?

(A)题目难度比之前降低了。（反）

(B)除了努力之外，考试时的心态也对考试成绩有很大影响。（没说清楚，万炜可能心态变好，没得选的情况下可以选这个）

(C)万炜他们班都很努力，但是都考得很差。（重复怪事）

(D)180分的题他之前能拿160分，但现在只能答40分。（没有解释）

(E)万炜班里的其他学生比他更努力。（无关对比！）

(F)过分努力导致万炜神经衰弱，考试时无法集中注意力。

(G)LSAT成绩对于成功申请法学博士有着重要的作用。（完全无关）

解析：选 F。

Paradox 题的做题建议：

1. *文章通常暗含反常的两件事，某原因 A 发生的情况下，本该产生结果 B 的反面，结果却出现了 B*，正确选项一定可以导致 B 的发生，所以读题是一定要**判断出来哪件事情才是要解释的**；
2. **看清楚怪事所包含的对比点**，错误选项经常会引入无关对比点；
3. 只有对比才可以解释对比，**只有变化才可以解释变化**；
4. 正确选项会解释文中的怪事，**解释就是导致**，不是证明，不是体现，不是说明，更不是简单的方向一致。

评价：

- 简单，但是其他复杂逻辑题的基础
- 练习解题速度，**提前预判答案**

【practice】Despite a dramatic increase in the number of people riding bicycles for recreation in Parkville, a recent report by the Parkville Department of Transportation shows that the number of accidents involving bicycles has decreased for the third consecutive year.

Which of the following, if true during the last three years, best reconciles the apparent discrepancy in the facts?

A. The Parkville Department of Recreation confiscated abandoned bicycles and sold them at auction to any interested Parkville residents.

B. Increased automobile and bus traffic in Parkville had been the leading cause of the most recent increase in automobile accidents.

C. Because of the local increase in the number of people bicycling for recreation, many out-of-town bicyclists ride in the Parkville area.

D. The Parkville Police Department enforced traffic rules for bicycle riders much more vigorously and began requiring recreational riders to pass a bicycle safety course.

E. The Parkville Department of Transportation canceled a program that required all bicycles to be inspected and registered each year

解析：

- 骑车的人多了，但是事故少了（要解释为什么事故少）
- 答案预期：造成事故减少（不违背骑车人多的前提）
- 选 D

🔺【practice】Frog eggs quickly die if permitted to dry out. Yet frogs of some species increase their chances for reproductive success by depositing their eggs, not in large, relatively permanent ponds,but in small puddles that may evaporate before the eggs have hatched.

Which of the following, if true, most helps to resolve the apparent discrepancy?

A. Some types of frog give birth to live young.

B. If the water in a puddle where frog eggs have been deposited evaporates before the eggs have hatched, the entire clutch of eggs perishes.

C. Unlike ponds, small puddles cannot support the forms of aquatic life that typically **feed on** frog eggs.

D. The tadpoles that hatch from frog eggs develop into air breathing frogs more quickly in hot, wet tropical climates than elsewhere.

E. The eggs of most nontropical frog species are fertilized in the water.

解析：

- 干旱对青蛙卵的生存不利；但是在水容易蒸发的 puddles，里卵的存活率竟然还提高了。（要解释的怪事）
- 答案预期：给一个好的原因可以造成青蛙把卵产到容易蒸发的 puddles，里真的会存活率更高。
- 选 C，puddles 里缺少天敌。

### 2.5 题型5: Weaken

题干：Which of the following, if true, most seriously weakens the argument?

题干：Which of the following, if true, casts most doubt on the conclusion?

题干：Which of the following, if true, could best be used to counter the conclusion?

Weaken 题的做题建议：

1. 一般为**归纳推理**，必须区分论证类型！
2. 不同的论证类型，对答案方向将有完全不同的预判。

**解释型论证的削弱策略**：

1. **列举它因**（给出其它解释）
2. **无因有果**：没这个原因，该结果一样可以发生
3. （极小概率）直接攻击结论，仅在没有前两种选项存在时才要考虑

例：万蜀黍考试进步了，说明他努力了。（解释型论证）

- 削弱1：万蜀黍作弊了（列举它因）
- 削弱2：万蜀黍没努力的时候也有考试进步过（无因有果）

**非解释型论证的削弱策略**(预测型，类比型)：**直接破坏结论成立的可能性**。

例：万蜀黍最近很努力，相信他的成绩下次一定会提高。

- 削弱：过分努力让他精神衰弱，考试状态变得很差。

🔺【practice】There are many structural and thematic similarities between Piers Plowman by Langland (1330-1400) and House of Fame by Chaucer(1342-1400), two Middle English poems relating dream visions. Some critics have argued that because a number of the shared elements are uncommon in Middle English poetry, and because Langland's poem probably predates Chaucer's by a few years, Chaucer was most likely influenced by Piers Plowman when writing House of Fame.

Which of the following, if true, most seriously weakens the critics'argument?

A. Piers Plowman is one of Langland's major works, whereas House of Fame is a minor work of Chaucer's.

B. House of Fame survives in only three manuscript copies, substantially fewer than the number of manuscript copies that exist of Piers Plowman.

C. Because Piers Plowman became a well-known work in its day, it is likely that the similarities between it and House of Fame were detected by many of the people who read House of Fame soon after Chaucer wrote it.

D. Many of the themes and structures of Piers Plowman are also found in Latin, Italian, French works with which Chaucer could well have been familiar.

E. There is no evidence that Chaucer and Langland ever met or that they corresponded with each other about literary topics.

解析：

- 前提：两者有很多相似。
- 结论：后者学了前者。
- 论证类型：解释型论证(“学”导致“相似”)
- 🔺选项 E 看似能够直接能削弱结论，其实并没有。
- 列举他因：选 D。

【practice】The Rivera Art Museum recently began charging admission. The resulting decline in visitors has been far larger than at other local museums, which have also begun charging admission. The magnitude of the decline **might** be due to the Rivera's location near government offices. Because an admission charge is most discouraging to those who plan a short visit, it is likely that government workers who formerly made brief visits during lunch time and after work now do not.

Which of the following, if true, most seriously undermine the proposed explanation?

A. The fee for admission to the Rivera is no larger than that charged by other museums.

B. The Rivera does not keep track of how long individual visitors stay in the museum.

C. The decline in visitors to the Rivera has been no greater on workdays than it has been on nonworking days.

D. The museum with the smallest decline in visitors is the most popular with visitors from other countries.

E. In the period between the announcement that there would be an admissions charge and its' actual introduction, there was an increase in visitors at the Rivera.

解析：解释型论证，🔺周末的时候**无因有果**，选 C。

【practice】In commercial fishing, people compete for their catches with whatever other creatures naturally prey on the fish sought for human consumption. From a purely commercial point of view, therefore, it **would** make sense to kill off those other predator species in order to increase yields of the commercially desirable prey species.

Which of the following, if true about aquatic species, most seriously weakens the argument above?

A. There are many pairs of predator and prey species in which their species that is of commercial importance is the predator species.

B. There are species that are under little or no predatory pressure except that they are hunted by people.

C. Commercial fishing, unless carefully managed, can deplete certain species enough to threaten the associated predator species with extinction.

D. In comparison with the predator species associated with a given prey species, the prey species is generally the more numerous, but the ranges occupied by the two species usually coincide.

E. The presence of nonhuman predators tends to improve the survival chances prey species by selectively removing weak or sick individuals or reproductive age.

解析：预测型论证，答案预测：即使杀了 predator，也不会增加 prey的数量；选 E。

### 2.6 题型6: Necessary Assumption

**Necessary Assumption = 必要条件**：

- 题干：Which of the following is an assumption on which the argument relies?
- 题干：Which of the following is an assumption made in the argument?
- 题干：The argument assumes which of the following?

Necessary Assumption 题的做题建议：

1. Necessary Assumption 永远等于 **Weaken 的对立面**（没了就挂了）！所以简而言之——**取非削弱**；
2. 严格禁止直接看哪个选项对结论有利，因为对结论有利不等于论证所必须依赖的条件

🔺【practice】In 1995 earthquake along the Knowler fault caused some steel-framed buildings to collapse in Knowler, a city situated immediately over the fault. Existing steel-framed buildings meeting 1994 government minimum earthquake-safety standards for new construction, however, suffered negligible damage. Since seismologists predict that any earthquake affecting Knowler in the near future will be no stronger than the 1995, more stringent earthquake-safety standards for the construction of steel-framed buildings in Knowler are unnecessary.

Which of the following is an assumption on which the argument depends? 

A. Most steel-framed buildings that did not meet the 1994 government standards did collapse.

B. A city situated immediately over a fault typically suffers extensive damage in earthquakes along the fault.

C. There are government earthquake-safety standards for new construction of structures other than steel-framed buildings.

D. The steel-framed buildings that were not seriously damaged by the earthquake did not significantly exceed 1994 government minimum standards for earthquake safety.

E. More earthquakes are anticipated along the Knowler fault.

解析：预测型论证。

- 削弱题答案：如果不提高标准，未来的地震会让建筑受到损害。
- 把选项取非，判断是否能削弱
- 选 D

🔺【practice】The Thorvald epic was transmitted orally until the early 1300s, when it was written down. Three manuscripts of the epic survive from the 1300s. The latest of these manuscripts, made in the mid-1300s, has an episode that is not in the second manuscript, but that occurs in the earliest of the three manuscripts in virtually the same words. Therefore, the third manuscript was **probably** copied from the first or from a now lost copy of the first.

Which of the following is an assumption on which the argument relies?

A. Whoever produced the second manuscript did not deliberately omit the missing episode.

B. The earliest of the surviving manuscripts was not the first manuscript ever made of Thorvald.

C. The texts of the first and third surviving manuscripts do not derive from the text of a manuscript, now lost, that predates them both.

D. The first manuscript was copied at most once before the third manuscript was made.

E. The episode that is missing from the second manuscript was not invented by whoever produced the first manuscript.

解析：

- 前提：3rd = 1st
- 结论：3rd一定是抄了1st
- 解释型论证，选 C。

## 2.7 题型7: Sufficient Assumption

题干：The conclusion is properly drawn if which of the following is assumed?

题干：Which of the following, if true, would enable the conclusion of the argument to be properly drawn?

题干：Which of the following,if justifiably assumed,allows the conclusion to be properly drawn?

| Sufficient assumption | Necessary Assumption |
| --------------------- | -------------------- |
| 充分条件              | 必要条件             |
| 有了就行              | 没了不行             |

Sufficient Assumption 题的做题建议：

1. 考的是**演绎推理**，所以要**追求绝对严谨的论证**：
2. 正确选项和文章前提加在一起，能绝对保证结论的成立
3. 一定要留意和 Necessary Assumption 题的题干区别以及做法区别

| Must Be True | Sufficient Assumption |
| ------------ | --------------------- |
| 推结论       | 找条件                |

【practice】X-ray examination of a recently discovered painting-judged by some authorities to be a self-portrait by Vincent van Gogh-revealed an underimage of a woman's face.Either van Gogh or another painter covered the first painting with the portrait now seen on the surface of the canvas.Because the face of the woman in the underimage also appears on canvases van Gogh is known to have painted,the surface painting must be an authentic self-portrait by van Gogh.

The conclusion is properly drawn if which of the following is assumed?

A. If a canvas already bears a painted image produced by an artist,a second artist who uses thecanvas to produce a new painting tends to be influenced by the style of the first artist.

B. Many painted canvases that can be reliably attributed to van Gogh contain underimages ofsubjects that appear on at least one other canvas that van Gogh is known to have painted.

C.Any painted canvas incorrectly attributed to van Gogh would not contain an underimage ofa subject that appears in authentic paintings by that artist.

D.A painted canvas cannot be reliably attributed to an artist unless the authenticity of anyunderimage that painting might contain can be reliably attributed to the artist.

E.A painted canvas cannot be reliably attributed to a particular artist unless a reliable x-rayexamination of the painting is performed.

【practice】When on an airplane,Consuelo never enjoys movies that have been widely recommendedbecause the poor quality of the picture spoils her enjoyment.Since in no circumstances doesshe ever enjoy movies that have been widely derided,it follows that she never enjoys movieson airplanes.
Which of the following,if true,would enable the conclusion of the argument to be properlydrawn?

A.The only place where Consuelo enjoys widely recommended movies is a movie theater.

B.Widely recommended movies are never shown on airplane.

C.If a movie shown on an airplane is not widely derided,then it is invariable widelyrecommended.

D.If the picture quality of the movies shown on airplanes was better,Consuelo would enjoythe widely recommended movies.

E.Some movies are neither widely recommended nor widely derided.