### Outline

Game theory (MWG Chapter 7,8,9)： Game theory basic concepts, Nash equilibrium, strategic-form game, extensive-form game, Bayesian game. 

Information economics (MWG Chapter 13, 14) Incomplete information game, adverse selection, moral hazard. 

Mechanism design (MWG Chapter 23) Mechanism design theory, auction and revenue maximizing mechanism. (the most challenging part!) 

Social choice (MWG Chapter 21) Social choice theory, collective decision and welfare.

# 1. Basic Element

The players, the rules, the outcomes, the payoffs

## 1.1 Type

Information about strategies and payoffs are **complete**: both prisoners know the available strategies and payoffs of the other.

A game has **complete information** if the structure of the game tree (including the payoffs) is common knowledge among players.

A game is one of **perfect information** if each **information set** contains a single decision node. Otherwise, it is a game of **imperfect information**.

**Simultaneous-move Games**: Games where players choose actions simultaneously. 

**Sequential-move Games**: Games where players choose actions in a particular sequence.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513092731.png)

**information sets**:  信息集的集合是所有参与者决策结的分割

partition：完备事件组

Each partition element, i.e. one information set, contains one or some of this player’s decision nodes.

Each information set represents a possible distinguishable circumstance under which a player is called upon to move.

When the game has reached a non-singleton information set, the player being called upon to move is unable to differentiate between the decision nodes within this information set.

The construction of “information set” must satisfy the following two restrictions: 

1.  A player must have the same set of possible actions at every node within an information set.

2.  Perfect recall: a player (1) does not forget what she once knew, or (2) what she once have done.

## 1.2 strategy

The concept of a **strategy** is central to game theory. A strategy is a fully described behavioral disposition. A player’s strategy is a **Complete Contingent Plan**: 针对所有可能发生情况的行动方案

A strategy will always completely specify behavior, **even at contingencies that are ruled out by the strategy itself**.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513092859.png)

A winning strategy for the first mover: “After each round in which the other player moved his/her piece two cells forward, move its piece one cell forward. Otherwise, move its piece two cells forward.”

Similarly, in any games with a multiple of 3 cells, the second mover has a win-for-sure strategy for the game: Second-mover advantage However, in any games with not-multiple-of-3 cells, the first mover has a win-for-sure strategy for the game: First-mover advantage

## 1.3 Game tree / Extension Form

consists of 

1. An initial node (in our example the node marked with Chance). 

2. Decision nodes (in our example the nodes at which player A or B faces strategy choices). 

3. Terminal nodes (the nodes with no succeeding decision nodes; associated with payoff vectors). 

4. An assignment of players (in our example Chance, A and B) to decision nodes. 

5. Branches that start at decision nodes and which indicate the decisions available to the player acting at that node. 
6. An assignment of payoffs to players at each terminal node.

Extensive game form 

1 A finite set of nodes X , a finite set of possible actions A , and a finite set of players {1, . . . , I}. 

2 A function p : X → {X ∪ ∅} specifying a single immediate predecessor each node x. 

- Initial node is denoted as x0. 

- Successors are then $s(x) = p^{−1} (x)$; s(x) and p(x) are disjoint. 
- Set of terminal nodes is T = {x ∈ X : s(x) = ∅}. 
- X - T are called decision nodes. 
- Note: p(x) must be a function, not a correspondence. This is to exclude graphs in which some nodes without common predecessor.

A **function α** : $X - {x_0} → A$ 

- 1 giving the action that leads to any non-initial node x from its immediate predecessor p(x); 
- 2 satisfying the property that (same action cannot lead to two different nodes);

$$
\text { if } x^{\prime}, x^{\prime \prime} \in s(x) \text { and } x^{\prime} \neq x^{\prime \prime}, \text { then } \alpha\left(x^{\prime}\right) \neq \alpha\left(x^{\prime \prime}\right)
$$

- 3 the set of choices available at decision node x is  (actions that lead from x to s(x)).

$$
c(x)=\left\{a \in \mathscr{A}: a=\alpha\left(x^{\prime}\right) \text { for some } x^{\prime} \in s(x)\right)
$$

4 A collection of information sets H and a function $H : X - T → H $ assigning each decision node x to an information set H(x) ∈ H .

-  The information sets H form a partition of X \ T with the following two restrictions: 
    -  1 all decision nodes assigned to one information set have the same choices: c(x) = c(x 0 ) if H(x) = H(x 0 ) 
    -  2 perfect recall : a player (1) does not forget what she once knew, or (2) what she once have done.
- All choices available at an information set H: C(H) = {a ∈ A : a ∈ c(x) for x ∈ H}.

5 A function ι : H → {0, 1, . . . , I} assigning each information set to the player (including nature, player 0) who moves at the decision nodes in that set. 

- Player i’s collection of information sets is 

$$
\mathscr{H}_{i}=\{H \in \mathscr{H}: i=\iota(H)\}
$$

6 A function ρ : H0 × A → [0, 1] assigning probabilities to actions at information sets where nature moves 

- satisfying ρ(H, a) = 0 if a ∈/ C(H) and $\Sigma_{a \in C(H)} \rho(H, a)=1$ for all H ∈ H0

7 A collection of payoff functions u = {u1(·), . . . , uI(·)} assigning utilities to the players for each terminal node that can be reached, ui : T → R. ui is Bernoulli.

Accordingly, a game in extensive form is specified by the collection $\Gamma_{E}=\{\mathscr{X}, \mathscr{A}, l, p(\cdot), \alpha(\cdot), \mathscr{H}(\cdot), \iota(\cdot), \rho(\cdot), u\}$

## 1.4 Normal form

### strategy

Let $\mathscr{H}_{i}$ denote the collection of player i's information sets, $\mathscr{A} /$ the set of possible actions in the game, and $C(H) \subset \mathscr{A}$ the set of actions possible at information set $H .$ 

A strategy for player $i$ is a function $s_{i}: \mathscr{H}_{i} \rightarrow \mathscr{A}$ such that $s_{i}(H) \in C(H)$ for all $H \in \mathscr{H}_{l}$

Profile of strategies:$s=\left(s_{1}, \ldots, s_{l}\right)$ for each player i

### normal form 

For a game with $/$ players, the normal form representation $\Gamma_{N}$ specifies for each player i a set of strategies $S_{i}$ and a payoff function $u_{i}\left(s_{1}, \ldots, s_{i}\right)$ giving the von Neumann-Morgenstern utility levels associated with the (possibly random) outcome arising from strategies $\left(s_{1}, \ldots, s_{l}\right)$ Formally, $\Gamma_{N}=\left[l,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$

每一个策略轮廓都直接指向一个收益，使用这种一一对应可以描述一个博弈，即博弈标准型。

混合策略：$\sigma _i:S_i \rightarrow[0,1]$，assigns to each pure strategy $s_i \in S_i$ a probability number σi(si) ≥ 0 which si will be played, where $\sum_{s_i∈S_i} σ_i(s_i) = 1$.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513093158.png)

期望收益
$$
E_\sigma[U_i(s)] = \sum_{s \in S}[\sigma_1(s_1)\times \dots \times \sigma_i(s_i)\times \dots \times \sigma_I(s_I) ]u_i(s_1,\dots,s_i\ldots,s_I)
$$
where $S = S_1 \times\dots\times S_I$

要求参与者的策略概率分布之间相互独立

从而标准型被表示为$\Gamma_{N}=\left[l,\left\{\Delta (S_{i})\right\},\left\{u_{i}(\cdot)\right\}\right]$

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513093233.png)

显然（注意需要满足前述对信息集的限制条件），行为策略总可以导致一个（或多个）与之结果等价的混合策略（概率的乘法法则）；反过来，混合策略也总可以找到一个（或多个）与之结果等价的行为策略。

结果等价：$O(\sigma)$表示最终收益的概率分布等价，$\sigma=(\sigma_i)_{i \in I}$ is the probability distribution over terminal nodes that results when each player i follows the precepts of $\sigma_i$ .

# 2. Simultaneous Move Games

## 2.1 严格占优策略

A strategy $s_{i} \in S_{i}$ is a **strictly dominant strategy** for player $i$ in game $\Gamma_{N}=\left[l,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$ if **for all** $s_{i}^{\prime} \neq s_{i},$ we have $u_{i}\left(s_{i}, s_{-i}\right)>u_{i}\left(s_{i}^{\prime}, s_{-i}\right)$ for all $s_{-i} \in S_{-i}$

严优策略一定会被采用，好于其他所有策略

## 2.2 严劣策略

### 2.2.1 纯策略

A strategy $s_{i} \in S_{i}$ is **strictly dominated** for player $i$ in game $\Gamma_{N}=\left[I,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$ if there **exists** another strategy $s_{i}^{\prime} \in S_{i}$ such that for all $s_{-i} \in S_{-i}, u_{i}\left(s_{i}^{\prime}, s_{-i}\right)>u_{i}\left(s_{i}, s_{-i}\right)$. In this case, we say that strategy $s_{i}^{\prime}$ strictly dominates $s_{i}$

至少有一个策略好于该策略，严劣策略一定不会被选择。

### 2.2.2 混合策略

A strategy $\sigma_{i} \in \Delta\left(S_{i}\right)$ is strictly dominated for player $i$ in a normal-form game $\Gamma_{N}=\left[I,\left\{\Delta\left(S_{i}\right)\right\},\left\{u_{i}(\cdot)\right\}\right]$ if there exists another strategy $\sigma_{i}^{\prime} \in \Delta\left(S_{i}\right)$ such that for all $\sigma_{-i} \in \prod_{j \neq i} \Delta\left(S_{j}\right), u_{i}\left(\sigma_{i}^{\prime}, \sigma_{-i}\right)>u_{i}\left(\sigma_{i}, \sigma_{-i}\right)$

$$\begin{aligned}
&\text { Note that } u_{i}\left(\sigma_{i}^{\prime}, \sigma_{-i}\right)-u_{i}\left(\sigma_{i}, \sigma_{-i}\right)\\
&=\sum_{s_{-i} \in S_{-i}}\left[\prod_{k \neq i} \sigma_{k}\left(s_{k}\right)\right]\left[u_{i}\left(\sigma_{i}^{\prime}, s_{-i}\right)-u_{i}\left(\sigma_{i}, s_{-i}\right)\right]
\end{aligned}$$

Iterated Deletion of Strictly Dominated Strategies

![](https://upload-images.jianshu.io/upload_images/20447423-58f0b16fe45115eb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**A reasoning process**, the logic of which depends on each player being rational, knowing his/her opponent being rational, knowing that his/her opponent knows that oneself being rational, ..., and so on.

## 2.3 劣策略

A strategy $s_{i} \in S_{i}$ is **weakly dominated** for player $i$ in game $\Gamma_{N}=\left[I,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$ if there exists another strategy $s_{i}^{\prime} \in S_{i}$ such that for all $s_{-i} \in S_{-i}, u_{i}\left(s_{i}^{\prime}, s_{-i}\right) \geq u_{i}\left(s_{i}, s_{-i}\right)$ **with strict inequality for some** $s_{-i}$. In this case, we say that strategy $s^{\prime}_i$ weakly dominates $s_i$ . 

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200512174225.png)

A strategy is a **weakly dominant strategy** if it weakly dominates every other strategy in Si

if players believe that any strategies of their rivals will be played with some positive probabilities, a weakly dominated strategy can be dismissed.

 **Order** does not matter in iterated deletion of strictly dominated strategies, but it does matter for iterated deletion of weakly dominated strategies. An example.(因此并不建议采用)

![](https://upload-images.jianshu.io/upload_images/20447423-ea9e94f077e98ad6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 2.4 纳什均衡

In game $\Gamma_{N}=\left[I,\left\{\Delta\left(S_{i}\right)\right\},\left\{u_{i}(\cdot)\right\}\right],$ strategy $\sigma_{i}$ is a **best response** for player $i$ to his rivals' strategies $\sigma_{-i}$ if $u_{i}\left(\sigma_{i}, \sigma_{-i}\right) \geq u_{i}\left(\sigma_{i}^{\prime}, \sigma_{-i}\right)$ for all $\sigma_{i}^{\prime} \in \Delta\left(S_{i}\right)$
Strategy $\sigma_{i}$ is **never a best response** if there is no $\sigma_{-i}$ for which $\sigma_{i}$ is a best response.

### 纯策略

A strategy profile $s=\left(s_{1}, \ldots, s_{l}\right)$ constitutes a Nash equilibrium of game $\Gamma_{N}=\left[l,\left\{\mathcal{S}_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$ if for every $i=1, \ldots, l, u_{i}\left(s_{i}, s_{-i}\right) \geq u_{i}\left(s_{i}^{\prime}, s_{-i}\right)$ for all $s_{i}^{\prime} \in S_{i}$

Mutually best response: nobody has any incentive to deviate to another strategy

纳什均衡不一定是帕累托最优

Nash equilibrium outcome coincide with the set that survives iterated elimination of strictly dominated strategies

pure strategy is played in a Nash equilibrium,  it may not survive the iterative elimination of weakly dominated strategies

Cell-by-cell inspection always works(划线法/Best Response法)

### 混合策略

A mixed strategy profile $\sigma=\left(\sigma_{1}, \ldots, \sigma_{l}\right)$ constitutes a (mixed-strategy) Nash equilibrium of game $\Gamma_{N}=\left[I,\left\{\Delta S_{i}\right\},\left\{u_{i}(\cdot)\right\}\right]$ if for every $i=1, \ldots, I$ $u_{i}\left(\sigma_{i}, \sigma_{-i}\right) \geq u_{i}\left(\sigma_{i}^{\prime}, \sigma_{-i}\right)$ for all $\sigma_{i}^{\prime} \in \Delta S_{i}$

纳什均衡的存在性, Nash (1950)

Every game $\Gamma_{N}=\left[I,\left\{\Delta\left(S_{i}\right)\right\},\left\{u_{i}(\cdot)\right\}\right]$ in which the sets $S_{1}, \ldots, S_{I}$ have a finite number of elements has a mixed strategy Nash equilibrium.

纳什均衡的充要条件

Let $S_{i}^{+} \subset S_{i}$ denote the set of pure strategies that player i plays with positive probability in mixed strategy profile $\sigma=\left(\sigma_{1}, \ldots, \sigma_{l}\right) .$ Strategy profile $\sigma$ is a Nash equilibrium of game $\Gamma_{N}=\left[I,\left\{\Delta\left(S_{i}\right)\right\},\left\{u_{i}(\cdot)\right\}\right]$ if and only if for all $i=1, \ldots, I$

1. $u_{i}\left(\boldsymbol{s}_{i}, \sigma_{-i}\right)=u_{i}\left(\boldsymbol{s}_{i}^{\prime}, \sigma_{-i}\right)$ for all $\boldsymbol{s}_{i}, \boldsymbol{s}_{i}^{\prime} \in S_{i}^{+}$
2. $u_{i}\left(\boldsymbol{s}_{i}, \sigma_{-i}\right) \geq u_{i}\left(\boldsymbol{s}_{i}^{\prime}, \sigma_{-i}\right)$ for all $s_{i} \in S_{i}^{+}$ and all $s_{i}^{\prime} \notin S_{i}^{+}$

条件1是求解混合策略纳什均衡的方法

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200512174925.png)

还可以通过画图求解

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513093427.png)

定理

A strictly dominated pure strategy is not used with positive probability in any mixed strategy Nash equilibrium.（对劣策略不成立）

![](https://upload-images.jianshu.io/upload_images/20447423-01d3f71726731af9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/20447423-a6679c890b2f0e61.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513095506.png)

## 2.5 连续博弈/无限策略博弈

Game Matrixes ⇒ Profit Functions 

Best response sets ⇒ Best-response functions 

Nash equilibrium: Mutual best responses

### 2.5.1 古诺模型

A game where two firms (duopoly) compete in terms of the quantity sold (market share) of a homogeneous good is referred to as a Cournot game after the French economist who first studied it. 

#### Duopoly

Two firms, i ∈ {1, 2}, produce the same good at the same marginal cost c. Let their outputs be q1 and q2. Let Q = q1 + q2 be the total output. The inverse demand function of the market is P(Q) = a − Q if Q < a; otherwise P(Q) = 0.
$$
\begin{aligned}
\pi_{i}\left(q_{i}, q_{j}\right) &=P(Q) \cdot q_{i}-c \cdot q_{i} \\
&=\left\{\begin{array}{ll}
\left(a-q_{1}-q_{2}-c\right) \cdot q_{i}, & \text { if } q_{1}+q_{2}<a \\
-c \cdot q_{i} & \text { otherwise }
\end{array}\right.
\end{aligned}
$$
First we study how firm 1 would respond given the output $q_{2}$ of firm 2.
Firms 1 chooses $q_{1}$ to solve: $\max _{q_{1}} \pi_{1}\left(q_{1}, q_{2}\right)$
Solving the F.O.C. gives the best response function of firm 1:
$$
b_{1}\left(q_{2}\right)=\left\{\begin{array}{ll}
\frac{1}{2}\left(a-c-q_{2}\right), & \text { if } q_{2}<a-c \\
0, & \text { otherwise }
\end{array}\right.
$$
Similarly, firm 2 's best response function $b_{2}\left(q_{1}\right)$ takes the same form.

Solving $q_{1}=b_{1}\left(q_{2}\right)$ and $q_{2}=b_{2}\left(q_{1}\right),$ we have
$$
q_{1}^{*}=q_{2}^{*}=\frac{a-c}{3}
$$
**Once a collusion is formed**, each produces half of the monopolistic quantity q1 = q2 = Qm/2 and earns half of the monopolistic profit πm/2.

Now the optimization for the collusion becomes:
$$
\max _{Q}(a-Q) \cdot Q-c \cdot Q
$$
F.O.C. gives
$$
\begin{aligned}
& a-Q-c-Q=0 \\
\Rightarrow \quad Q_{m}^{*}=& \frac{a-c}{2}
\end{aligned}
$$
Each firm produces half of it: $q_{1}^{m}=q_{2}^{m}=\frac{a-c}{4}$

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513114650.png)

#### Oligopoly

Now let's generalize the number of the firms to $J$
Each firm has identical costs: $C\left(q^{j}\right)=c \cdot q^{j}, c \geq 0$
Let inverse market demand be
$$
p=a-b \cdot \sum_{j=1}^{J} q^{j}, a>0, b>0 \text { and } a>c
$$
The profit for firm $j$ is
$$
\Pi^{j}\left(q^{1}, \ldots, q^{J}\right)=\left(a-b \cdot \sum_{k=1}^{J} q^{k}\right) \cdot q^{j}-c \cdot q^{j}
$$
The best response of firm $j$ when firms $k \neq j$ produce $q^{k}$.
The profit function can be rewritten as
$$
\Pi^{j}\left(q^{1}, \ldots, q^{J}\right)=\left(a-b \cdot q^{j}-b \cdot \sum_{k \neq j} q^{k}\right) \cdot q^{j}-c \cdot q^{j}
$$
The first-order condition is
$$
a-b q^{j}-b \sum_{k \neq j} q^{k}-b q^{j}-c=0
$$
This gives firm $j$ 's best response function:
$$
q^{j}=\frac{a-c}{2 b}-\frac{\sum_{k \neq j} q^{k}}{2}
$$
Solving $J$ simultaneous equations with $J$ unknowns.
A short-cut: Symmetric equilibrium: $q_{j}=q^{*}$ for all $j$
Then, we have
$$
q^{*}=\frac{a-c}{2 b}-\frac{(J-1) q^{*}}{2}
$$
Thus, we have
$$
q^{*}=\frac{a-c}{b(J+1)}
$$
Insert back, the market price is
$$
p^{*}=a-\frac{J(a-c)}{J+1}
$$
Remark: the Cournot price decreases (increases) as the number of firm increases (decreases)

- Consider the price-cost margin: $p^{*}-c=\frac{a-c}{J+1}$

- The price-cost margin is the highest when $J=1$ : a monopolistic market outcome.
- Also, $\lim _{J \rightarrow \infty}\left(p^{*}-c\right)=0:$ a perfectly competitive market outcome.

### 2.5.2 Bertrand competition

In the Bertrand competition of duopoly, firms compete over prices instead of quantities of outputs. Usually the price is a continuous variable.

Two firms $i, j,$ with identical marginal cost $c .$

The market demand function (assuming $a>c$ )
$$
D(p)=\left\{\begin{array}{ll}
a-p, & \text { if } p \leq a \\
0, & \text { if } p>a
\end{array}\right.
$$
The two firms' choices: $p_{i}, p_{j} \in \mathbb{R}$

Assume that the consumers only buy from the firm that offers lower price. Thus the demand for firm $i$ is:
$$
q_{i}\left(p_{i}, p_{j}\right)=\left\{\begin{array}{ll}
a-p_{i}, & \text { if } p_{i}<p_{j} \\
\frac{1}{2}\left(a-p_{i}\right), & \text { if } p_{i}=p_{j} \\
0, & \text { if } p_{i}>p_{j}
\end{array}\right.
$$
Notice the discontinuity in the demand function:

- If $p_{j}>c,$ firm $i$ has incentive to undercut by $p_{j}-\epsilon$ and wins the entire market.
- If firm $j$ charges $p_{j}=p_{i},$ each's sale changes to half of the market.
- If firm $j$ undercuts the price to $p_{j}<p_{i}$, firm $j$ can sell to the entire market while firm $i$ has 0 demand.

Firm i's profit is also a piecewise (discontinuous) function:
$$
\pi_{i}\left(p_{i}, p_{j}\right)=\left\{\begin{array}{ll}
\left(p_{i}-c\right)\left(a-p_{i}\right), & \text { if } p_{i}<p_{j} \\
\frac{1}{2}\left(p_{i}-c\right)\left(a-p_{i}\right), & \text { if } p_{i}=p_{j} \\
0, & \text { if } p_{i}>p_{j}
\end{array}\right.
$$
Instead of taking the f.o.c. directly, let's find the optimum manually this time (note that $(a+c) / 2$ is the maximizer of the quadratic function of $p_{i}$ ).

Depending on $p_{i}$ and $c, 4$ cases (where the B.R. is set-valued):
$$
B_{i}\left(p_{j}\right)=\left\{\begin{array}{ll}
\left\{p_{i} \in \mathbb{R}: p_{i}>p_{j}\right\}, & \text { if } p_{j}<c \\
\left\{p_{i} \in \mathbb{R}: p_{i} \geq p_{j}\right\}, & \text { if } p_{j}=c \\
\emptyset, & \text { if } c<p_{j} \leq \frac{a+c}{2} \\
\frac{a+c}{2}, & \text { if } p_{j}>\frac{a+c}{2}
\end{array}\right.
$$
Discontinuous functions with a “jump” of value may not have a maximum

Best-Response Correspondences and Equilibrium

![](https://upload-images.jianshu.io/upload_images/20447423-e81484df11ab0521.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 2.5.3 Hotelling’s Model

This is the Hotelling’s location game in both industrial organization theory and the electoral competition model in political science. 

Two parties: Left or Right. (Or two coffee shops: H and D.) 

The parties only differ in policy positions. (Two coffee shops only differ in locations – the price are the same.) x1, x2 ∈ [0, 1]. 

Voters (uniformly distributed over [0, 1]) will vote for the candidate whose policy position is closer. (Consumers will only go to wherever is nearby.) 

To illustrate the best responses and Nash equilibria, we need to look at best response correspondence instead of functions.

Majority rule makes the candidates' winning probabilities discontinuous:
"If Donald Trump attracts slightly more than $1 / 2$ of the voters, he wins the election with prob. 1.

Hillary and Donald resolves a tie with a coin flip, each's winning probability decreases to 0.5
Let's derive the parties' best-responses case-by-case:
$$
B_{1}\left(x_{2}\right)=\left\{\begin{array}{ll}
\left(x_{2}, 1-x_{2}\right), & \text { if } x_{2}<\frac{1}{2} \\
\frac{1}{2}, & \text { if } x_{2}=\frac{1}{2} \\
\left(1-x_{2}, x_{2}\right), & \text { if } x_{2}>\frac{1}{2}
\end{array}\right.
$$
![](https://upload-images.jianshu.io/upload_images/20447423-2c541b04ea8b065f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 2.6 Incomplete Information and Bayesian Nash Equilibrium

### 2.6.1 Incomplete Information

When players **do not know others’ payoffs**, the game is of incomplete information.

Harsanyi (1967-68) proposed an approach: 

- Each player’s payoffs are determined by the realization of a random variable. 
- The realization of the random variable is observed only by the player. We call it a player’s “type.” 
- The ex-ante probability is assumed to be common knowledge among all the players.

A **Bayesian game** as $\left[l,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}, \Theta, F(\cdot)\right]$

- Each player $i$ has a payoff function $u_{i}\left(s_{i}, s_{-i}, \theta_{i}\right),$ where $\theta_{i} \in \Theta_{i}$ is a random variable chosen by nature that is observed only by player $i$.

- Let $\Theta=\Theta_{1} \times \cdots \times \Theta_{I}$. The joint probability of the $\theta_{i}$ 's is given by $F\left(\theta_{1}, \ldots, \theta_{l}\right),$ which is common knowledge.

A pure strategy for player $i$ is a function $s_{i}\left(\theta_{i}\right),$ a decision rule, specifying for each realization of his type a strategy choice. That is, $s_{i}: \Theta_{i} \rightarrow S_{i} .$ We denote the collection of player i's pure strategies as $\mathscr{S}_{i}$ (a functional space).

- Player i's expected payoff given strategy profile $\left(s_{1}(\cdot), \ldots, s_{l}(\cdot)\right)$ is given by $\tilde{u}_{i}\left(s_{1}(\cdot), \ldots, s_{l}(\cdot)\right) \doteq E_{\theta}\left[u_{i}\left(s_{1}(\theta), \ldots, s_{l}(\theta), \theta_{i}\right)\right]$

Continuous Strategies: Cournot Competition Revisited

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513155021.png)

转换成如下形式

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513163349.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513163025.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200513163046.png)

### 2.6.2 Bayesian Nash equilibrium

A pure strategy Bayesian Nash equilibrium in this Bayesian game is a triple of actions, one for the woman and one for each type of man, with the no-deviation property as

- the action of woman is optimal given the actions of each type of man and the woman’s belief about the man’s types;
- the action of each type of man is optimal, given the woman’s action choice.

注意一下两种等价定义的区别

A pure strategy Bayesian Nash equilibrium for the Bayesian game $\left[I,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}, \Theta, F(\cdot)\right]$ is a profile of decision rules $\left(s_{1}(\cdot), \ldots, s_{l}(\cdot)\right)$ that constitutes a Nash equilibrium of game $\Gamma_{N}=\left[I,\left\{\mathscr{S}_{i}\right\},\left\{\tilde{u}_{i}(\cdot)\right\}\right]$ That is, for every $i=1, \ldots, l, \tilde{u}_{i}\left(s_{i}(\cdot), s_{-i}(\cdot)\right) \geq \tilde{u}_{i}\left(s_{i}^{\prime}(\cdot), s_{-i}(\cdot)\right)$ for all $s_{i}^{\prime}(\cdot) \in \mathscr{S}_{i}$

According to the definition earlier, the condition is equivalent to:
$$
E_{\theta}\left[u_{i}\left(s_{i}(\theta), s_{-i}(\theta), \theta_{i}\right)\right]>E_{\theta}\left[u_{i}\left(s_{i}^{\prime}(\theta), s_{-i}(\theta), \theta_{i}\right)\right]
$$
A profile of decision rules $\left(s_{1}(\cdot), \ldots, s_{l}(\cdot)\right)$ is a Bayesian Nash equilibrium in Bayesian game $\left.l,\left\{S_{i}\right\},\left\{u_{i}(\cdot)\right\}, \Theta, F(\cdot)\right]$ if and only if, for all $i$ and all $\bar{\theta}_{i} \in \Theta_{i}$ occurring with positive probability $E_{\theta_{-1}\left[U_{i}\left(s_{i}\left(\bar{\theta}_{i}\right), s_{-i}\left(\theta_{-i}\right), \bar{\theta}_{i}\right) | \bar{\theta}_{i}\right] \geq E_{\theta_{-1},}\left[u_{i}\left(s_{i}^{\prime}, s_{-i}\left(\theta_{-i}\right), \bar{\theta}_{i}\right) | \bar{\theta}_{i}\right] \text { for all } s_{i}^{\prime} \in S_{i}}$

Q: 这两种定义的等价，是表明即使每个决策者不知道自己的type，也能够达到和知道自己type情况下相同的贝叶斯纳什均衡嘛？

Q2

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200514204427.png)

可能会漏掉，女人混合策略，男人纯策略的均衡情况

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200514210545.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200514210636.png)

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200514211204.png)

# 3. Dynamic Games

标准型不能反映顺序信息。

## 3.1 Backward Induction (core)

Generalized **backward induction procedure**:

Start at the end of the game tree, and identify the Nash equilibria for each of the final subgames (i.e. those that have no other subgames nested within);

Select one Nash equilibrium in each of these final subgames, and derive the reduced extensive form game in which these final subgames are replaced by the payoffs that result in these subgames when players use these equilibrium strategies;

Repeat steps 1 and 2 for the reduced game. Continue the procedure until every move in $\Gamma_{E}$ is determined. This collection of moves at the various information sets of $\Gamma_{E}$ constitutes a profile of SPNE strategies.

If multiple equilibria are never encountered in any step of this process, this profile of strategies is the unique SPNE. If multiple equilibria are encountered, the full set of SPNEs is identified by repeating the procedure for each possible equilibrium that could occur for the subgames in question.

## 3.2 子博弈精炼纳什均衡

A **subgame** of an extensive form game $\Gamma_E$ is a subset of the game having the following properties: 

**It begins with an information set containing a single decision node**, contains all the decision nodes that are successors of this node, and contains only these nodes. 

If decision node x is in the subgame, then any $x ^\prime \in H(x)$ is also in the subgame.

The whole game is a subgame (of itself). Proper subgame (strict subset)

子博弈精炼纳什均衡(SPNE)

A strategy profile σ in extensive form game $\Gamma_E$ induces a Nash equilibrium in a particular subgame of $\Gamma_E$ if the moves specified in σ for information sets within the subgame constitute a Nash equilibrium when this subgame is considered in isolation.

A profile of strategies $\sigma = (\sigma_1, . . . , \sigma_I)$ in an extensive form game $\Gamma_E$ is a subgame perfect Nash equilibrium (SPNE) if it induces a Nash equilibrium in every subgame of $\Gamma_E$.

存在性

Subgame perfection and backward induction: for **finite games of perfect information**, the set of SPNEs coincides with the set of Nash equilibria that can derived through backward induction.

**Every finite game of perfect information** has a pure strategy subgame perfect Nash equilibrium.

Furthermore, if no player has the same payoffs at any two terminal nodes, then there is a **unique subgame perfect Nash equilibrium**.

![](https://upload-images.jianshu.io/upload_images/20447423-22736387d6e91b5a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 3.3 Application

### 3.3.1 Stackelberg Model Of Duopoly

动态的古诺模型

Firm 1 chooses a quantity $q_{1} \geq 0$ 

Firm 2 observes $q_{1}$ and chooses a quantity $q_{2} \geq 0$ The payoff to each firm is given by
$$
\Pi_{j}\left(q_{i}, q_{j}\right)=\left(a-\left(q_{j}+q_{i}\right)\right) q_{j}-c q_{j}
$$
Firm 2 's best response function is
$$
q_{2}=\frac{a-c}{2}-\frac{q_{1}}{2}
$$
Look at firm 1's problem. Firm 1 is to maximize by inserting the quantity $q_{2}$ into the profit function:
$$
\begin{aligned}
\Pi_{1}\left(q_{1}, q_{2}\right) &=\left(a-\left(q_{1}+q_{2}\right)\right) q_{1}-c q_{1} \\
&=\left(a-\left(q_{1}+\frac{a-c}{2}-\frac{q_{1}}{2}\right)\right) q_{1}-c q_{1}
\end{aligned}
$$
Solve the maximization problem, we have
$$
q^*_1 = \frac{1}{2}(a-c),q^*_2 = \frac{1}{4}(a-c)
$$

### 3.4 Ultimatum Bargaining

最后通牒博弈

Two players, 1 and 2.

Stage 1: Player 1 offers player 2 an amount of money x, $x \in  [0; 10]$.

Stage 2: Player 2 chooses between “Accept” and “Reject” player 1’s offer.

If the offered amount accepted, player 1 receives 10 - x while player 2 receives x. If rejected, then both receive 0.

![](https://cdn.jsdelivr.net/gh/Henrry-Wu/FigBed/Figs/20200514211324.png)

In an ultimatum game with continuous strategies described above, there exist **infinitely many Nash equilibria**. Any strategy profile involving player 2 adopting a “cutpoint strategy,” i.e. $\exist \bar{x}$ such that player 2 “accept if $x\geq \hat{x}$ and reject otherwise,” and player 1 offering an amount $\hat{x}$ to player 2 is an Nash equilibrium of the game.

The unique SPNE** strategies are player 1 chooses x = 0 while player 2 accept any offer amount.

#### Alternating Offers Bargaining

Player 1 begins in the first period by proposing to keep $x_{1}^{1}$. $M$ for herself and giving $\left(1-x_{1}^{1}\right) \cdot M$ to Player 2

If Player 2 accepts, the deal is struck. If Player 2 rejects, another bargaining period is played. In period $2,$ Player 2 proposes to keep $y_{2}^{2} \cdot M$ to himself, and giving $\left(1-y_{2}^{2}\right) \cdot M$ to player 1

If Player 1 accepts, the deal is struck; otherwise, it is period 3 and Player 1 gets to make another proposal.

Bargaining continues in this manner until a deal is struck or no agreement is reached when both players walk away with their disagreement values-a for Player 1 and $b$ for Player 2

**A shrinking pie and decreasing gains from trade**.

- Suppose there are 2 periods, Player 1 proposes a division of $M$ first, and Player 2 accepts/rejects.
- If accepted the proposal is implemented. If rejected, Player 2 gets to make a counter-proposal for how to split a reduced amount of pie $\lambda M,$ where $0<\lambda<1$ is the rate of decay.
- Player 1 can then accept or reject this final proposal. The bargaining game is then over with certainty.

Example: suppose that $M=12$ dollar and $\lambda=1 / 3, a=b=0 .$ What is the subgame perfect Nash equilibrium?

**Backward Induction**

Note that $M=12$ in period 1 but only 4 in period 2
Start from the second period. Player 2 knows he can get $4-\epsilon(\epsilon \geq 0)$ if the game moves to the second period, because player 1 will prefer getting $\epsilon$ to 0 at the end of period $2 .$ In the limit, player 1 will accept any second-period offer including $\epsilon=0$

Anticipating this, Player 1 must offer Player 2 an amount $12-x \geq 4$ in period $1,$ and keeping $x \leq 8(x=8 \text { when Player } 1$ maximizes) for herself. As Player 2 recognizes it as a weakly-better payoff than what could be gotten by waiting to period 2 , he accepts Player 1 's first period offer.

**Player 1 's first period offer to Player 2 thus equals the amount at stake at the start of the final round, $\lambda \cdot M$**

## 3.5 Repeated Games

### 3.5.1 Finitely Repeated Games

 A game being played repeated for a known and finite number of periods. 

let’s suppose the Prisoner’s dilemma will be played twice

![](https://upload-images.jianshu.io/upload_images/20447423-c6859aa44b65ae64.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/20447423-b81ac02ace8134a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

In sum, **the only SPNE** of this two-period repeated PD game is for both players to choose D in the first-period and choose D in the second period no matter which first-period outcome they observe.

**As long as there is a known, finite end, there will be no change in the equilibrium outcome of a game with a unique equilibrium.** Besides PD game, this is also true for zero/constant-sum games.

【Proposition】The same argument can be generalized to finite repetition of any stage-game which has a unique equilibrium. **Let $G$ be a finite static complete information game which has a unique Nash equilibrium**. Suppose $G$ is played $T$ times ( $T$ periods) and before each stage the outcomes of preceding play are perfectly observable. Let the repeated game be denoted by $G(T)$. There is **a unique subgame perfect Nash equilibrium for $G(T) :$** in which all players play the equilibrium action of the stage game, independent of the history of play that they observe.

**Rethink** the Prisoner’s Dilemma: even if players play it multiple times, they still cannot do any better than both defect: This is because the play of future periods are fixed at the unique N.E. – No flexibility to generate credible future punishments for the non-cooperation of the current period.

eg: **credible future punishments**

![](https://upload-images.jianshu.io/upload_images/20447423-7173658fa2916900.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

Intuition: since the stage-game has two Nash equilibria, one can use the worse one as punishment.it is indeed a SPNE

**Summary**

If a simultaneous move game has a unique Nash equilibrium, then this equilibrium is also the unique subgame perfect Nash equilibrium of the finitely repeated game.

If a simultaneous move game has multiple Nash equilibria, then there are many subgame perfect Nash equilibria of the finitely repeated game. Some of these involve the play of strategies that are collectively more profitable for players than the one-shot game Nash equilibria.

### 3.5.2 Infinitely Repeated Games

A game being played infinitely without end.  Since no one lives forever, we might call such games indefinitely repeated games. 

Possibly overlapping generations. e.g. the relationship with family members, friends, employer, or the community, who are expected to remain in our life for a while but of course, not forever.

Discount factor, $\delta = \frac{1}{1+r} \in [0: 1]$. $\delta$ can also be interpreted as the **probability that the two players will meet and play the game again tomorrow**. Indefinitely repeated games are common. We often don’t know whether a relationship will continue in the future or not.

【Average Payoff】The average payoff of player i in the infinite game is
$$
(1-\delta) u_{i}=(1-\delta) \sum_{t=0}^{\infty} \delta^{t} \pi_{t}
$$

For example, if the players cooperate in every period, $\pi_{t}=4$ for all $t$, we have
$$
\begin{aligned}
(1-\delta) u_{i} &=(1-\delta) \sum_{t=0}^{\infty} \delta^{t} \cdot 4 \\
&=(1-\delta) \cdot \frac{1}{1-\delta} \cdot 4=4
\end{aligned}
$$
【Proposition(Cooperation)】If $\delta$ is high enough, then there exists a subgame perfect Nash equilibrium such that $(C, C)$ is played in every period. 

Intuition: cooperation is possible now because the threat to play D is credible in each period, unlike in the finitely repeated games.

One way to maintain cooperation is to use **Trigger strategies**: A player using a trigger strategy plays cooperatively as long as her rival(s) do so, but any defection on their part “triggers” a period of punishment, of specified length, in which she plays non-cooperatively in response.

#### 3.5.2.1 Grim-trigger strategy

A **Grim-trigger strategy** prescribes the following choices at each possible history: play C in the first period. In later periods, keep playing C if the previous outcome is (C,C); otherwise, switch to playing D forever.

![](https://upload-images.jianshu.io/upload_images/20447423-c6859aa44b65ae64.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

If both players use the grim-trigger strategy, it's easy to check that both will cooperate forever as long as the discount factor $\delta$ is sufficiently large.

Check for deviations. Consider player $1 .$

Suppose player 1 is on the equilibrium path and does not deviate. Her total payoff starting from the current period is
$$
4+4 \cdot \delta+4 \cdot \delta^{2}+\ldots=\frac{4}{1-\delta}
$$
Now if player 1 deviates from the equilibrium path, i.e. she plays $D$ instead of $\mathrm{C}$ in the current period. Then her total payoff is
$$
5+1 \cdot \delta+1 \cdot \delta^{2}+\ldots=5+\frac{\delta}{1-\delta}
$$
To ensure no deviation we require player 1 's total payoff from the equilibrium path being greater than that from deviation:
$$
\begin{aligned}
\frac{4}{1-\delta} & \geq 5+\frac{\delta}{1-\delta} \\
& \Leftrightarrow \delta \geq \frac{1}{4}
\end{aligned}
$$
As long as $\delta \in(1 / 4,1)$ - player 1 is sufficiently patient-she will have no incentive to deviate from the equilibrium path, i.e. the cooperation phase.

#### 3.5.2.2 Tit-for-Tat strategy

There are "nicer" strategies that will also support (C,C) in every period as an SPNE outcome.

A **Tit-for-Tat strategy** prescribes the following choices at each possible history: play $C$ in the first period. In later periods, keep playing $C$ if the opponent plays C. Switch to play D if the opponent plays D in the previous period. Return to playing $C$ if the opponent switch back to playing $C$; otherwise keep on playing $D$. 

Now if player 1 deviates from the equilibrium path, i.e. she plays D instead of $\mathrm{C}$ in the current period. Then her total payoff is
$$
5+1 \cdot \delta+0 \cdot \delta^{2}+4 \cdot \delta^{3}+\ldots=5+\delta+\frac{4 \cdot \delta^{3}}{1-\delta}
$$
The only different is the next three periods if the players back to the cooperation phase after 4 periods.

To ensure no deviation we require player 1 's total payoff from the equilibrium path being greater than that from deviation:
$$
\begin{aligned}
\frac{4}{1-\delta} & \geq 5+\delta+\frac{4 \cdot \delta^{3}}{1-\delta} \\
& \Leftrightarrow \delta \geq \frac{1}{4}
\end{aligned}
$$
As long as $\delta \in(1 / 4,1)$ - player 1 is sufficiently patient - she will have no incentive to deviate from the equilibrium path, i.e. the cooperation phase.

#### 3.5.2.3 Folk Theorem

**Any outcome** that on average yields the mutual defection payoff or better for both players can be sustained as a subgame perfect Nash equilibrium of the infinitely repeated Prisoner’s Dilemma game.

![](https://upload-images.jianshu.io/upload_images/20447423-735f91c78208be57.png?imageMogr2/auto-orient/strip|imageView2/2/w/1240)