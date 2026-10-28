# week16

> **基础知识: 主理想与整除**<br>设 $R$ 为整环, $p\in R$. 则 $a\in\left(p\right)$ 当且仅当 $p\mid a$, 即存在 $r\in R$ 使 $a=pr$.

> **基础知识: 整环的消去律**<br>整环无零因子; 故若 $p\ne0$ 且 $pa=pb$, 则 $a=b$.

> **定义 2.5.6 (不可约元素)**<br>设 $R$ 为整环, $\alpha\in R^{*}\setminus U$ (即非零且非单位). 如果 $\alpha$ 不存在非平凡因子, 则称 $\alpha$ 为不可约元素.

> **定理 2.5.15 (唯一分解整环的等价条件)**<br>整环 $R$ 为唯一分解整环当且仅当 $R$ 满足因子链条件与素条件; 特别地, 在唯一分解整环中每个不可约元素都是素元素, 即 $p\mid ab$ 可推出 $p\mid a$ 或 $p\mid b$.

> **定义 2.6.1 (素理想)**<br>设 $I$ 为环 $R$ 的理想, $I\ne R$. 如果由 $ab\in I$ 可以推出 $a\in I$ 或 $b\in I$, 则称 $I$ 为 $R$ 的一个素理想.

---

## 2.6-13

设 $R$ 为唯一分解整环, $p\in R^{*}$. 证明: $p$ 为不可约元素当且仅当主理想 $\left(p\right)$ 为素理想.

### 解答 2.6-13

设 $p\in R^{*}\setminus U$ (若 $p$ 为零元或单位, 结论平凡, 不作讨论).

**必要性**: 设 $p$ 为不可约元素. 因 $R$ 是唯一分解整环, 由**定理 2.5.15 (唯一分解整环的等价条件)**, $p$ 是素元素, 即 $p\mid ab$ 可推出 $p\mid a$ 或 $p\mid b$. 由**基础知识: 主理想与整除**, $ab\in\left(p\right)$ 等价于 $p\mid ab$, $a\in\left(p\right)$ 等价于 $p\mid a$, $b\in\left(p\right)$ 等价于 $p\mid b$. 故 $ab\in\left(p\right)$ 可推出 $a\in\left(p\right)$ 或 $b\in\left(p\right)$. 又 $p$ 非单位, 由**基础知识: 主理想与整除**, $1\notin\left(p\right)$ (否则 $p\mid1$, $p$ 为单位), 故 $\left(p\right)\ne R$. 由**定义 2.6.1 (素理想)**, $\left(p\right)$ 是素理想.

**充分性**: 设 $\left(p\right)$ 为素理想. 反设 $p$ 可约, 即存在 $a,b\in R$, 二者均非单位, 使 $p=ab$. 因 $ab=p\in\left(p\right)$, 由**定义 2.6.1 (素理想)**, $a\in\left(p\right)$ 或 $b\in\left(p\right)$. 若 $a\in\left(p\right)$, 由**基础知识: 主理想与整除**, 存在 $r\in R$ 使 $a=pr$; 于是 $p=ab=prb$. 因 $p\ne0$ (由 $p\in R^{*}$) 且 $R$ 为整环, 由**基础知识: 整环的消去律** 消去 $p$, 得 $1=rb$, 故 $b$ 为单位, 与 $b$ 非单位矛盾. 若 $b\in\left(p\right)$, 同理存在 $r\in R$ 使 $b=pr$, 于是 $p=ab=ap r$, 消去 $p$ 得 $1=ar$, 故 $a$ 为单位, 亦矛盾.

故 $p$ 为不可约元素. $\blacksquare$
