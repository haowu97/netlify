---
title: "解密 GRE 逻辑题"
date: 2022-08-21T15:48:42+08:00
draft: false

description: ""
upd: "来自炜神《解密GRE系列课程-逻辑题》的 Bilibili 课程，炜神 YYDS！"

tags: ["笔记"]
categories: ["GRE"]
---

<!--more-->

## 1. 论证(Argument)

**Argument**: a set of propositions(命题) in which one of the propositions is supported by the others.

**Conclusion**: the supported proposition.

**Premises**: the supporting propositions.

判断以下例子是不是论证：

- 万蜀黍很努力，所以他得以成功的。(explanation)
- 万蜀黍很努力，所以他**一定会**成功。(argument)
- 万蜀黍很不健康，因为他吃得特别多。(explanation)
- 万蜀黍**肯定**不健康，你看他吃得那么多。(argument)

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

The information given, if accurate, most strongly supports which of the following hypotheses?

Which of the following conclusions is best supported by the information?

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