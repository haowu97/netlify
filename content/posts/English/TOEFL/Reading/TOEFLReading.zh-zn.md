---
title: "托福阅读"
date: 2022-03-31T21:17:53+08:00
draft: true

description: ""
upd: ""

tags: ['笔记', 'TOEFL']
categories: ['TOEFL笔记']
---

<!--more-->

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220331220545258.png)

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220417001322470.png)

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220714204337149.png)

生命科学类占比最大，历史类其次，社会类和考古类最次

# 1. 结构阅读法

TOEFL阅读文章的**线性思维原则**：

- 先论点，后论据
- 先总括，后分类
- 先抽象，后具体

Skimming >> scanning，考试中略读为主，精读为辅。

结构式阅读法的要点：

- **首段：每句都看**
  - 议论文：论点
  - 说明文：专业背景
- **其余段落首句精读，中间部分略读**（弄清句间关系即可）
- **顺逻辑加速阅读**：当段落出现顺承(then)，并列and，举例(for example)，递进(further)，因果(because)，分类(123)，定义/解释(be)等表示顺方向含义词汇时候，说明段落后方内容与前方一致，可以加速阅读。
- **逆逻辑慢速阅读**：当段落出现转折(but), 否定(not), 让步(though), 对比(contrast)等表示逆方向含义词汇时候说明段落后方与前方内容有出入，需要放慢速度，如果出现多个表示逆方向词汇时，需要以最后一个逆方向词汇后的含义为准；
- 段落逻辑：
  - 顺逻辑先验证最易验证的细节；
  - 逆逻辑先验证最后的细节；
  - 多个顺逆逻辑结合：先验证最后一个逆逻辑的最好验证的细节

**结构式阅读方法的伪代码**：

```
define function 结构式阅读法(P){
    if(P是首段){
    read.scan(P); /*如果是首段需要精读*/
    }
    else{
        read.scan(P.首句)； /*不是首段则精读首句*/
        read.skim(P.余下句)； /*识别句间顺逆逻辑词*/

    case多顺逻辑：最短/最简单->次短/次简单->难/长；
    case多逆逻辑：最后逆->倒数2逆->倒数3逆…；
    case多顺逻辑+多逆逻辑：最后逆->最短/最简单->次短/次简单->难/长；
    }
}
```

**二分递归结构式阅读法**（针对嵌套逻辑）：二分递归是将大篇幅的内容化成结构相同的小篇幅内容，从待寻找结构的文章出发，一直分解到已经已知答案的最小问题为止，然后再逐级返回，从而得到大篇幅文章结构的解决。

```
function 二分递归结式构阅读法(P1){
    if（无子结构存在）{
        invoke function结构式阅读法(P1)
        return;
    }
    else{
        invoke function 二分递归结式构阅读法(P1.1);
        invoke function 二分递归结式构阅读法(P1.2);
    }
}
```

**一篇阅读的整体做题步骤伪代码**：

```
invoke function结构式阅读法(p1);
read.solve(P1.Q1);
read.solve(P1.Q2);
read.solve(P1.Q3)...

invoke function结构式阅读法(P2);
read.solve(P2.Q1);
read.solve(P2.Q2);
read.solve(P2.Q3)...

invoke function结构式阅读法(P3);
read.solve(P3.Q1);
read.solve(P3.Q2);
read.solve(P3.Q3)...

invoke function结构式阅读法(P4)…
```

注：**读完一个段落做当前段落的题目**即可。

建议做一些简单的笔记，参考GRE或者Fiona。

# 2. 题型及对应解题方法

## 2.1 词汇题：Vocabulary questions

*Vocabulary questions* ask you to identify the meanings of words or phrases as they are used in a reading passage.

**Word or phrase highlighted in the reading passage**. Question like,

1. The word X in the passage **is closest in meaning to**
2. The phrase X in the passage **is closest in meaning to**
3. In stating X, the author **means that**

解题技巧：

- 词根词缀
- 借助句内、句间逻辑，和GRE类似（一般不需要，词汇一般很简单）

词性对应一般准则：

- 名词优先对应名词
- 动词优先对应动词
- 形容词副词优先对应形容词副词

## 2.2 事实信息题/ 细节题：Factual Information questions

*Factual Information questions* ask you to recognize information explicitly stated in the text. This information can include:

- Major ideas
- Supporting details
- Definitions

*Factual Information* questions like:

1. According to the paragraph, ...
2. Paragraph X answers which of the following?

Tips:

1. Don't select an answer just because it contains words or phrases from the paragraph. Evaluate each option to determine if it is correct
2. For negative factual information questions, answer is either not in the paragraph, or it contradicts information in the paragraph

解题方法：

- 先对段落进行结构式阅读
- 阅读题干，然后带入文章，一目三行，定位词定位
- 关键词匹配信息：逻辑+主干
  - 注意**逻辑分割原则**：仅在当前逻辑段落进行匹配

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220713213243227.png)

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220713204503445.png)

### 定位词（3+1+1原则）

**定位词**：出现在题干中，是寻找答案的工具，通常不唯一。根据题干中的**定位词**进行题目定位：

- 定位词所在句和之后内容为定位词所统辖范围（有指代词除外）；
- 如果同个定位词段落中出现多次，从第一次出现位置所在句往后看。

**定位的时候，快速略读，一目三行，目的只是找到选项的位置**。

精读：段落中定位词和定位词之后的内容，多定位词取交集。

**定位词选择原则（3+1原则）**：以下是定位词选择的优先级：

1. 人名、**地名**、数字、**年份**、大写、括号/引号、黑体/斜体、专业词汇
2. 实意名词
3. 特殊形容词、动词
4. 最后选择：切记不只使用和文章标题/段落主旨相关的词汇！段首句、段第二句的定位词，能不用尽量不用，实在不行最后再用（需要其他佐证）。

从选项入手**（1原则）**：完成定位后，可以利用选项的虚假逻辑帮助排除选项。

- 虚假绝对逻辑

- 虚假否定逻辑

- 虚假比较逻辑

- 虚假上下逻辑

- 虚假因果逻辑

- 虚假转折逻辑

- 虚假并列逻辑

### 关键词

**关键词**：题目的核心考点，通常唯一；题干中出现的逻辑关系词，是选项的考点。

**八大关键词**：

1. 转折
   1. 转折：however, rather than, instead of, but, yet, on the other hand, unfortunately, whereas, while, in fact...
   2. 让步：although, after all, in spite of..., despite, even if, even though, though, admittedly, whatever may happen…
2. 对比: by contrast, on the contrary, contradict, while, whereas, on the other hand, unlike, instead, but, conversely, different from, however, nevertheless, otherwise, unlike, yet, in contrast.
3. 因果
   1. 表原因: for this reason, due to, thanks to, because, because of, as, since, by, out of, when/whenever
   2. 表结果: evidently, effect, as a result, thus, hence, so, so that, therefore, accordingly, consequently, as consequence
   3. 表结尾: therefore, as a result, then, consequently, accordingly, thus, etc.
   4. 下结论: in a word, in conclusion, therefore, in short, to sum up, etc.
4. 观点态度词
   1. 正面：emphasize, illustrate, acknowledge, explain, account for.…
   2. 负面：question, argue against, refute, disagree.…
   3. 中性：present/pose, introduce, indicate, suggest, conclude, reveal.…
5. 顺序词汇：1,2,3..（时间紧就抓住每个列举的首句）：第一、三、三... (for one thing, put it another way, first of all) ；总结概述性词汇
6. 判断(肯定否定/支持反对)：
   1. 系动词：be, remain
   2. 情态动词：can, cannot, must
   3. 自由褒贬词：对某人态度、观点、行为褒贬的形容词, (un)convincing, untenable, useful, effective, successfully
   4. 表示评价的实义动词：fail to, underestimate, overestimate, exaggerate, ignore, misrepresent, overlook, miss point
7. 比较选择：（注意和文中的动词替换现象）
   1. not A(x), but rather B(v);
   2. less A(x) than B(v);
   3. more A(v) than B(x);
   4. A(v) rather than B(x);
   5. no longer/not A(x)but B(V).
   6. not A(x), instead B(v).
8. 上升下降，绝对词：
   1. increase/decrease...
   2. 常见绝对词
      1. 表示频率：always never impossible must
      2. 表示范围：all any only no/none
      3. 表示程度：completely entirely alone

**错误选项优先级原则**：这几个逻辑出现的时候大概率是错的，因此留在最后验证：绝对 < 比较 < 上升/下降 

错误选项特征：

- 无：选项内容没有提及
- 反：相关信息与原文不符合
- 混：选项将原文内容混搭
- 偏：以偏概全，将内容无端引申
- 满：**内容过于绝对**(做题时间不够了可以直接选)

### 黄金阅读八步法

细节题的**基本解题方法**，从文章入手解题，适用于题目定位词多且明显，文章简单，选项友善的情况。

invoke function 结构式阅读法

1. 详细阅读题目
2. 利用定位词两大原则（3+1+1原则）确定**定位词**
3. 利用定位词定位对应段落细节（多定位词联动原则）
4. 利用**关键词**八大原则筛选题目中的关键词
5. 找到文中的对应关键词
6. 根据文中关键词附近信息对照所有选项
7. 主干+逻辑匹配得出正确答案
8. 分类错误答案（PS: 无反混偏满）

### 逻辑细节分割原则

细节题的*辅助解题方法*，从选项入手解题，适用于文章崩溃，选项恶心，段落结构清楚，选项定位词明显的情况。

invoke function 结构式阅读法

如果存在以下情况：

- A *并列*逻辑关联词 B(时间，地点)
- A *转折*逻辑关联词 B
- A *递进*逻辑关联词 B

则：如果细节题考察的是A，但凡有选项涉及到B，该选项应当优先排除。

理由：当两个细节被分割，则两者极有可能是张冠李戴关系。

适用于*细节题，推断题，修辞目的题*。

**法不责众原则**：文章中并列逻辑(as well as等)的并列对象同时出现在两个或以上的选项中时，则这些选项都时错误的。（少用，但出现时能帮助快速排除选项）

## 2.3 否定事实信息题：Negative factual Information

In a *Negative Factual question,* 3 out of 4 answers are correct and only one answer choice is incorrect.

*Negative factual Information* questions like:

1. According to the paragraph which of the following is **NOT** true?
2. The author mentions all of the following **EXCEPT**

题目特点：

- 对应原文某一处描述，通常是**举例、列举逻辑**；
- 对应原文两处或两处以上描述，并且通常是**分散举例或排比**（未被选择的选项应和原文构成一一对应）
- 一般来讲，**选项会按照顺序来出**

解答技巧：结合笔记，以**选项**为切入点定位

- 先结构化阅读对应段落
- 一次性找出题干与四个选项的定位词；全部记录纸上；
- 每浏览段落的1-2句话，交叉对比四个选项的定位词与题干定位词
- 一旦一个选项锁定，留意附近的其他选项；

## 2.4 推理题：Inference question

An *Inference question* could ask you to identify information that is not explicitly stated. Like,

1. Which of the following can be **inferred** from paragraph 1 about X?
2. The author of the paragraph **implies** that X
3. Paragraph X **suggests** which of the following about Y?

**解题方法与事实信息题一致**，区别在于加入了适当的推理。

题目分类

- 细节题等同题（解题方法与细节题相同，占推理题的60%）
- 细节题+正向推断（正推题目相对较少）
- 细节题+反向推断（反推题目相对较多）

反向推理4大信号词：转折词，否定词，反义词，时间地点词(when)

- 出现4类信号词，优选从反推入手
- 优先选择带有主干信息和否定/反义逻辑的选项

找到定位词对应信息之后优先看并列

- 若有并列则多信息取反(并列中的某一信息取反即可)
- 若无并列则单信息取反

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220713204503445.png)

## 2.5 句子简化题：Sentence Simplification Questions

ID: 文中一个长句子被阴影标识出来。

问题: Which of the sentences below **best** expresses the **essential information** in the highlighted sentence in the passage? Incorrect choices change the meaning in important ways or leave out essential information.

**解题步骤**：依次对选项进行以下判断

1. 首先：逻辑词判断
   1. 否定、因果、比较、最高级/绝对化
   2. 通过逻辑可以排除掉一些选项
2. 其次：内容判断
   1. 主干内容判断
   2. 次要内容判断

**句中原则**：当句中出现多个逻辑词的时候，从最靠近句子中部位置的逻辑词入手。

## 2.6 指代题：Reference Questions

ID: The word X in the passage refers to

解题技巧：

1. **语法原则**：单复数一致，人称一致；（基本所有题目的选项都符合语法原则）
2. **前指原则**：正确答案必在所考代词之前；
3. **主语原则**：**优先主语，其次最近信息-主干信息**
4. **句内原则**：*正确答案与所考代词通常在同一句内*，除非代词位于句首或出现指代传递现象（此时一般是在前一句内）。
5. 语义原则：代入并译成中文进行**验证**；（指代词后面信息可以作为验证使用）

## 2.7 修辞目的题：Rhetorical Purpose Question

三大类：

1. 考察句子和句子之间的逻辑关联
2. 考察段落和句子（段落从属句）之间的逻辑关联
3. 考察段落和段落之间的逻辑关联

![](C:\Users\Wuhao\AppData\Roaming\Typora\typora-user-images\image-20220715114229665.png)

### 句-句逻辑关系

句句关系占修辞目的题的85%，**对具体信息目的的提问**，出题形式通常是：

- The author discuss X in order to..?
- Why does the author mention X?
- The author uses X as an example of..?

在这种形式下，一般都是作者举了例子，题目问作者为什么要举这个例子。

句-句逻辑关系题目包含以下两种：

- **论点论据逻辑关系（85%）**：正确答案通常会包含论点，论据，以及论点论据之间的支持/反对关系；
- **原因结果逻辑关系（15%）**：解法同细节题，不再赘述。
  - 题干：xxx in order to explain why

**论点论据核心功能性词汇**：

- 正/中性: to emphasize, to illustrate, to suggest, to provide an example, to cite evidence, to acknowledge...
- 负性: to question, argue against, differentiate/distinguish, compare, contrast, refute, digress, contradict...

#### 解题方法

识别文章中修辞目的题的**界面/接口**构成：

1. 逻辑关键词: and, but
2. 功能性关键词：for instance/ example, include, testify
3. 逻辑+功能性关键词

界面/接口完备功能性：

1. 确定论点论据的角色
2. 确定论点论据正负逻辑

**隐形例证原则**：当信息具体（具体人物，具体地点，具体时间，具体数据）即使界面不完善，可以判定为**论据**。

**线性思维原则**：

- 先论点，后论据
- 先总括，后分类
- 先抽象，后具体

**就近原则**：论点论据之间不可存在大量无关细节。

### 句-段逻辑关系

第二种修辞目的题的形式是对段落目的的提问，出题形式：

- What is the purpose of paragraph X?
- What is the structure of paragraph X?
- What is the main point of paragraph X?

这种情况就是问段落的主要目的是什么，**其实是在问段落的主旨是什么**。

**解题方法**：调用**结构式阅读法**厘清段落结构即可解决问题。

**段落逻辑分类**：

- 问题解决型 (To solve this problem.../There are two answers)
  - Suggesting an answer to a theoretical question
  - Discussing a problem with two possible solutions
- 现象解释型 (There are two explanations.…)
  - A phenomenon is described and an interpretation presented and rejected
  - Discussing a possible explanation for ...
- 新老观点对比型 (Now/Today/Currently/Recently/However)
  - Showing that a certain interpretation is better supported by the evidence
  - Recommending a *different approach*
  - Describe an *alternative hypothesis*

### 段-段逻辑关系

最后一种修辞目的题的形式就是对**段间关系**的提问，考对段落之间关系和联系的把握和理解。它的出题形式

- How is the paragraph X related to other parts of the passage?

题目一般就是在问某一段和其他段的关系是什么，或者这一段在全文中有什么作用。

那我们在做题的时候就要注意**段落之间的衔接**，不能只看一段的内容，还要看看这一段与前后文是又怎样的关系(注意TS)。

**解题方法**：**着重阅读各个段落的首末句**，厘清段落间的逻辑关系。

## 2.8 句子插入题：Insert Text Questions

题目ID：小黑方块

插入文本题考查的主要是**衔接手段**（cohesion）的把握。要使一个段落内容统一和连贯，句子与句子之间必须有相应的衔接手段。这些衔接手段包括**语言线索**和**内容线索**，其中语言线索包括：

- 词汇衔接手段

- 逻辑衔接手段

- 语法衔接手段

这些衔接手段作为线索，有助于找到插入句子的最佳位置。它们或出现于原文方块前后的句子中，或者就存在于待插入的句子中。反之，如果上下句之间关系紧密，没有跳跃，就不能在它们之间插入句子。

### 词汇衔接手段

词汇衔接手段就是以**核心词的重复**使前后句连贯起来，其中词类可能发生变化，如原文中使用了形容词，而待插入句中有同一形容词的名词形式。或者原文中使用了形容词，而待插入句中有该形容词的副词形式。不管词类如何变化，两句话中的两个句或词组的意思是一样的，因此将前后句衔接起来。词类衔接的主要形式有：

1. **重复核心词**：就是待插入的句子中与方块前的句子拥有相同的核心词，使得前后连贯。

2. 使用**同义词或反义词**：就是待插入的句子中的核心词与方块前的句子中的核心词成同义词或反义词。

### 逻辑衔接手段

完整参考逻辑词汇表：

1. 因果过渡词：because, therefore, thus, consequently, so, as a result;

2. 对比过渡词：however, on the contrary, nevertheless, unlike, in contrast, while, although, but

3. 结构配对词：on the one hand… on the other hand, some...others

4. 比较过渡词：similarly, likewise, like

5. 举例过渡词：for example, for instance, including, such as

6. 递进过渡词：furthermore, also, as well, too, other, in addition, moreover, besides, even, additionally

7. 序列过渡词：first, second, after that, afterwards, next, then, finally

### 语法衔接手段

1. 指示代词：this, these, it, such, another, that, these, those

2. 人称代词：he, she, one, they, his, her, one's, their

3. 定冠词：the

### 前技巧调用

细节题/推断题：逻辑分割原则

- 有时插入句就是逻辑分割点

原则指代题：指代词原则

修辞目的题：线性思维原则

- 帮助对句子进行排序

## 2.9 主旨题：Prose Summary Questions

ID: 位置最后一道题，黑体字的介绍句如下

Directions: An introductory sentence for a brief summary of the passage is provided below. Complete the summary by selecting the THREE answer choices that express the most important ideas in the passage. Some answer choices do not belong in the summary because they express ideas that are **not presented **in the passage or are **minor ideas** in the passage. This question is worth 2 points.

PS: 选中3个得到2分，选中2个得到1分。

**正确答案组成**：

1. 全文主题
2. 一个或多个段落概述

注意：正确答案多为**概括性描述**，可能找不到对应的原文某句话

**错误选项**分析：

1. 与原文矛盾
2. 原文未明确提及
3. 原文正确信息但与介绍句无关的原文细节

黑体字的**介绍句**(introductory sentence)分析：

1. 绝大部分为文章主题
2. 极少数是对文章的话题topic下定义

**解题步骤**：

- 只剩下**10秒钟**蒙的时间：选择最长的3个句子（句子太短无法进行概述）

- **1min-2min**时间：**精读介绍句**，筛选关键词（筛选标准：介绍句的**主干**，**标题**，或文章中**高频**出现的表达），匹配与关键词语义相等的选项，排除与介绍句无关的选项。

- 剩下**3min**或以上的时间：精读介绍句，点**review text**,.用1min左右时间，结合之前记录每段主题句（首尾句）中的要点，选择表达了文章主旨与段落概述（记录要点）一致的选项。

- **具有区分度的题目，不要死磕！**

**排除技巧**：

1. 排除带有**解释修饰成分**的且修饰对象和修饰内容为不重要信息的选项

2. 排除**主语为细节**的选项

3. 排除**小举例**(只提到过一次，未展开，或连续列举的举例)，不能排除对大段举例主题的概述

| 主要细节      | 次要细节          |
| --------- | ------------- |
| 直接支持主题    | 支持主要细节        |
| 对理解文章必不可少 | 删除后并不影响理解文章主题 |

## 2.10 配对题：Fill in a Table Questions

ID: 位置最后一道题，出题形式是表格（相对少考）。

Directions: Complete the table below by selecting three answer choices that are characteristics of primary groups and two answer choices that are characteristics of secondary groups. This question is worth 3 points.

**Each reading passage will have one Prose summary question, or one Fill In A Table Question, but not both**.

PS: 选对得3分，错一个扣一分，以此类推。

**正确选项**要同时满足两个条件

1. 原文明确提及正确信息

2. 与引导词对应

注意：正确答案可以是**段落概述**，也可以是段落中**细节的同义改写**。

**错误选项**分析：矛盾/未提及/与引导词无关。

**解题步骤**

1. 匹配与引导词语义相等的选项，排除与引导词无关的选项

2. 若引导词与选项中没有语义对应，则判断**引导词所在大区间(通常为1-3个自然段)**，然后再进行配对

注意：同一个表格中不可能出现相反两个含义的选项
