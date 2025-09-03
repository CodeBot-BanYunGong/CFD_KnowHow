
> ### Stefan-Boltzmann 定律（单向）：
> $$ [ Q_\text{rad}= \varepsilon , \sigma , A,(T_\text{hot}^4 - T_\text{sur}^4) ] $$
>* ε（0–1）：发射率，黑哑漆≈0.95，镜面铝≈0.05；
>* σ：5.67 × 10⁻⁸ W·m⁻²·K⁻⁴；
>* 四次方 → 温差越大、温度越高，辐射量暴涨。

> ### 牛顿冷却定律：
>$$ [ Q_\text{conv}= h , A,(T_\text{s} - T_\infty) ]  $$
>* h：对流换热系数，取决于流速、方向、流体种类；
>  * 自然对流：2–10 W·m⁻²·K⁻¹
>  * 风扇吹：50–200 W·m⁻²·K⁻¹ 
>  * 水冷喷：500–10 000 W·m⁻²·K⁻¹
>* A：接触面积；差值就是表面温度减环境温度。

> ### 流体能量方程:
>$$ [ \rho c_p\underbrace{\mathbf{u}\cdot\nabla T}_{\text{convective term}} ] $$
> ### 能量方程里以一个源项 q̇rad
>$$ [ \rho c_p,\mathbf{u}\cdot\nabla T = k\nabla^2T + \dot{q}_{\text{rad}} + \ldots ] $$
$$[ h_r = 4\varepsilon\sigma T_m^3 ]$$

---
### 第 i 段排气外壁需要的等效热通量 ( q''_i )。常用 3 种精度梯度——

#### 1. 能量守恒法（最粗略，1 根数就完）
$$[ q''{avg} = \frac{\dot m ,c_p,(T{in}-T_{out})}{A_{tot}} ]$$ 
* $( T_{in},T_{out} )$ 为排气管初末端气体温度
* $( A_{tot} = \pi D L )$ 全管外表面积  
整根管 q'' 一刀切，1 分钟估完。误差 20–30%，但足够做 A/B 方案对比。

#### 2. 段均匀法（推荐）
- 先算单段总热量
$$[ Q_i = \dot m ,c_p,(T_{g,i}-T_{g,i+1}) ]$$
- 再折算成壁面热通量
$$[ q''_i=\frac{Q_i}{A_i}, \quad A_i=\pi D_i L_i ]$$
* 典型分段：前催化器、下游管、膨胀室、消声器。
* 能反映“前高后低”分布，误差 10–15%。

#### 3. 内对流＋辐射线性化法（段/点级，最细）
$$[ q''i = h{int,i}(T_{g,i}-T_{wall,i})+\varepsilon\sigma(T_{g,i}^4-T_{wall,i}^4) ]$$
* $( h_{int,i} )$ 出自 1D or 经验 Nu 公式
* $( T_{wall,i} )$ 先假设 1 层薄壁导热平衡或用试验测得
* 将第二项辐射化简为等效对流 $( h_{rad,i}(T_{g,i}-T_{wall,i}) )$ 也行  
适合排气前段、催化器包热处易出现 400–600 °C hotspot 的精细估计。
---

![Conjugate Heat Transfer (CHT)](img.png)