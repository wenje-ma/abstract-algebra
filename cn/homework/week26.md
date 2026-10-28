# week26

> **基础知识: 特征 $p$ 下的弗罗贝尼乌斯映射**<br>设域 $F$ 的特征为素数 $p$, 则对任意 $a,b\in F$ 有 $\left(a+b\right)^p=a^p+b^p$. 因而对任意 $c\in F$, 若 $\alpha$ 是 $x^p-c$ 在某分裂域中的根 (即 $\alpha^p=c$), 则 $x^p-c=\left(x-\alpha\right)^p$, 即 $x^p-c$ 在其分裂域中只有一个 $p$ 重根.

---

## 4.4-5

设 $F$ 为域, $c\in F$, $\mathrm{char}\,F=p\ne0$. 求证: $x^p-c$ 在 $F\left[x\right]$ 中不可约当且仅当 $x^p-c$ 在 $F$ 中无根.

### 解答 4.4-5

**必要性.** 设 $x^p-c$ 在 $F$ 中有根 $\alpha$, 即 $\alpha^p=c$, $\alpha\in F$. 由**基础知识: 特征 $p$ 下的弗罗贝尼乌斯映射**, $x^p-c=x^p-\alpha^p=\left(x-\alpha\right)^p$. 因 $p\ge2$, 上式给出 $x^p-c$ 在 $F\left[x\right]$ 中的非平凡分解, 故 $x^p-c$ 可约. 因而不可约必有根的反面成立, 即不可约推出 $x^p-c$ 在 $F$ 中无根.

**充分性.** 反设 $x^p-c$ 在 $F$ 中无根, 但 $x^p-c$ 在 $F\left[x\right]$ 中可约, 即存在非常数首一多项式 $f\left(x\right),g\left(x\right)\in F\left[x\right]$ 使 $x^p-c=f\left(x\right)g\left(x\right)$, 其中 $1\le\deg f=k< p$.

设 $E$ 为 $x^p-c$ 的分裂域, $\alpha\in E$ 为其根. 由**基础知识: 特征 $p$ 下的弗罗贝尼乌斯映射**, 在 $E\left[x\right]$ 中有 $x^p-c=\left(x-\alpha\right)^p$. 因 $f$ 首一, 比较分解得 $f\left(x\right)=\left(x-\alpha\right)^k$.

$f\left(x\right)=\left(x-\alpha\right)^k$ 中 $x^{k-1}$ 的系数为 $-k\alpha$. 因 $f\in F\left[x\right]$, 该系数属于 $F$, 故 $k\alpha\in F$. 又 $1\le k< p$, 在特征 $p$ 域中 $k\ne0$, 因而 $k$ 在 $F$ 中可逆, 故 $\alpha=\left(k\alpha\right)\cdot k^{-1}\in F$.

于是 $\alpha^p=c$, 即 $\alpha$ 是 $x^p-c$ 在 $F$ 中的根, 与反设矛盾. 故 $x^p-c$ 在 $F$ 中无根时必不可约.

综上, $x^p-c$ 在 $F\left[x\right]$ 中不可约当且仅当它在 $F$ 中无根. $\blacksquare$
