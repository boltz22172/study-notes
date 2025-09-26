# A survey on gSPT and beyond

## 1. Overview and History

### 1.1 gSPT

It was first studied in [T. Scaffidi 2017](10.1103/PhysRevX.7.041048)。

Derived using **Decorated Defect Construction**

>**DDC**:
>
>- Start with a $G$ symmetric gapless system
>
>- Decorate its $G$-defect with $H$-gapped SPT
>
>- Get a $G\times H$ gSPT
>
>- Note:
>
>  - Such construction introduces a gapped sector, which both $G$ and $H$ acts.  $\Longrightarrow$ **Not pure**
>
>  - However, H doesn't act on the gapless sector, a.k.a `a part of symmetries only acting on gapped degrees of freedom`. 
>
>  >  *This might be understood as a key feature of 'gapped sector'*.
>
>  - Such Properties can be realized in $G\times H$ gapped SPT ( a.k.a  `gapped counterpart`)$\Longrightarrow$ **Not Intrinsic**

It exist at the **critical points/regime** between SSB phases and gapped SPT phases.

### 1.2 igSPT

It was first studied in [R. Thorngren 2021](10.1103/PhysRevB.104.075132.) 。

Consider **Group Expansion**: $1\rightarrow H \rightarrow \Gamma \rightarrow G\rightarrow 1$

>**Construction:** 
>
>- Start with a $G$ symmetric gapless system, with self-anomaly $\omega_G$
>- Stack an $H$ SPT on top of $G$-defects
>- Induced gapped sector has opposite anomaly $-\omega_G$, due to non-trivial group extension
>- Anomaly is cancelled in gapless sector, s.t. the $\Gamma$ symmetry is anomaly-free
>
>- Note that:
>  - igSPT also contains **a gapped sector** coming from the decorated defect construction $\Longrightarrow$ **Not Pure**
>  - Its topological features can not be realized in a $\Gamma$ gapped SPT (No gapped counterpart) $\Longrightarrow$ **Intrinsic**

==疑问：stacking和群扩张的关系是什么？==

It's not hard to notice that gSPT and igSPT both have **gapped sector**, corresponding to `exponential decaying energy splitting of edge modes`.

==为什么？==

### 1.3 pgSPT

It was first studied in [R. Verresen 2021](10.1103/PhysRevX.11.041059.).

It doesn't has a gapped sector, for `the energy splitting under OBC is polynomial`. $\Longrightarrow$ **Pure**

It does have a gapped counterpart, i.e. such topological properties can be realized in gapped SPT. $\Longrightarrow$ **Not Intrinsic**

### 1.4 ipgSPT

To be explored



### 1.5 Terminology Understanding

**Pure**  $\rightarrow$  The entire symmetries acting on the gapless sector / No gapped sector

**Intrinsic**  $\rightarrow$  The topological features that can not be realized by a gapped-SPT

![image-20250918153851732](C:\Users\WXC\AppData\Roaming\Typora\typora-user-images\image-20250918153851732.png)



### 1.6 Kennedy Tasaki Transformation

It was originally proposed as a *mapping between $\mathbb{Z}_2\times\mathbb{Z}_2$ SSB phase and SPT phase*, on a **spin-1 Haldane chain**:
$$
U_{KT} = \prod_{i>j}e^{i\pi S_i^zS_j^x}  ,
$$
which is highly non-local. We use the notation $U$ for it is unitary on OBC. Researchers then generalize it to PBC, where the unitarity vanishes.

On **PBC** systems (i.e. a ring), the KT transformation is a **non-unitary and non-invertible** duality operator, $\mathcal{N}_{KT}$. It becomes a unitary transformation under a suitable boundary condition on OBC ( i.e. an interval).

- In this note, we **focus on spin-1/2**, where there is an equivalent version of KT transformation. We review it in the following section.



## 2. Review on KT transformation

Through out this note, we focus on $\mathbb{Z}_2\times\mathbb{Z}_2$ symmetries, so we study following systems.

- $L$ sites ($\sigma_i$ or $s_i^\sigma$) and $L$ links ($\tau_{i-1/2}$ or $s_{i-1/2}^\tau$), on a **closed ring** unless otherwise specified

  > Closed Ring can be **PBC or ABC**. Be careful!

- Unit Cell $\rightarrow$ {$\sigma_i,\tau_i$}

- $\mathbb{Z}_2\times\mathbb{Z}_2$ Symmetry: 
  $$
  U_σ = \prod_{i=1}^L σ^x_i, \quad U_τ = \prod_{i=1}^L τ^x_{i-1/2}.
  $$

- **Symmetry sector** $\{u_\sigma, u_\tau\}$   $\longrightarrow$  The eigenvalue of ground state under each symmetry is $(-1)^u$
  - $u = 0$ corrsponds to symmetric sector
  - $u = 1$ corrsponds to catching a $-1$ phase

- **Twist sector** $\{t_\sigma, t_\tau\}$  $\longrightarrow$  How the state changes when going around the ring
  
  - $s_{i+L}^σ = s_i^σ + t_σ, \ \ \ \ s_{i-1/2+L}^τ = s_{i-1/2}^τ + t_τ$
  - $t=0$, PBC
  - $t=1$, ABC  $\Longrightarrow$  $\ket{0}_i\rightarrow\ket{1}_{i+L}, \text{vice versa}$

> 事实上，twisted sector看上去有些难以理解。在下面的例子里我们会发现，我们会**固定一个哈密顿量**，within it 有一些没有定义清楚的量，比如$\sigma_0^z$, 我们就必须把这个量联系到$\sigma_L^z$, where we **have to refer to twisted sector condition**. 在文献中，这被称为“we encode the boundary condition in the Hilbert space, and the Hamiltonian applies to arbitrary boundary conditions.”
>
> > 这有一点点像不同绘景之间的转换，我们总得固定一个不动的东西（Hamiltonian或者Hilbert Space）。很明显，在这种情况下固定Hamiltonian是方便的。

***<u>We will discuss ==Twisted Sector== with more details in Sec V!!!!</u>***

### 2.1 KT maps between different sectors

We use $[(u_\sigma, t_\sigma),(u_\tau, t_\tau)]$ to label the symmetry-twist sector.

> To be specific, the whole Hilbert space can be decomposes as:
> $$
> \mathcal{H} = \bigoplus_{u_\sigma,u_\tau,t_\sigma,t_\tau} \mathcal{H}_{(u_\sigma,u_\tau,t_\sigma,t_\tau)}.
> $$

W.L.O.G, we can suppose a state is within one particular sector  $\longrightarrow$  $\ket{\psi}_{[(u_\sigma, t_\sigma),(u_\tau, t_\tau)]}$

> **Subtlety**:
>
> $t$ 的确定是先验的，因为t的信息encode在Hilbert Space里面，可以看成是一种约定。
>
> $u$ 更加微妙。
>
> - 首先，如果有唯一基态，根据对称性的原理，$U\ket{\psi}\propto\ket{\psi}$, 因此定义$\ket{\psi}$的symmetry sector是合理的。- 
> - 其次，如果有SSB，对于任意一个基态，作用上去$U$之后还是基态，有：$U\ket{\psi_a} = \sum U_{ba}\ket{\psi_b}$。  也就是说，在GS subspace形成了$U$的一个表示（且因为SSB，这个表示不是1维的）。因为$[H,U] = 0$, 可以同时对角化。这样一来，GS space的对角基下，定义$\ket{\psi}$的symmetry sector是合理的。
>
> 所以，我们总是可以假定我们在研究one of the diagonal basis of GS subspace，因此u是良定义的。
>
> **我们上述的讨论实际上并没有用到“基态”的性质，故而适用于任何哈密顿量本征态。**

We note a very important property of KT transformation. It **changes sectors**.
$$
[(u_\sigma, t_\sigma),(u_\tau, t_\tau)] \overset{\mathcal{N}_{KT}}{\longrightarrow} [(u_\sigma, t_\sigma+u_\tau),(u_\tau, t_\tau+u_\sigma)],
$$
which means:
$$
\ket{\psi}_{[(u_\sigma, t_\sigma),(u_\tau, t_\tau)]}\overset{\mathcal{N}_{KT}}{\longrightarrow} \ket{\psi}_{[(u_\sigma, t_\sigma+u_\tau),(u_\tau, t_\tau+u_\sigma)]}
$$
Consider the transformation $\mathcal{N}_{KT}H = H'\mathcal{N}_{KT}$

We have the following relation for the **energy sepctrum**:
$$
E_{[(u'_\sigma, t'_\sigma), (u'_\tau, t'_\tau)]}^{H'} = E_{[(u_\sigma, t_\sigma), (u_\tau, t_\tau)]}^H = E_{[(u'_\sigma, t'_\sigma + u'_\tau), (u'_\tau, t'_\tau + u'_\sigma)]}^H.
$$
So we can `understand the coupled system from the original decoupled system`, to some extent.

### 2.2 Useful KT formulas

$$
\mathcal{N}_{\text{KT}} \tau^z_{i-\frac{1}{2}} \tau^z_{i+\frac{1}{2}} = \tau^z_{j-\frac{1}{2}} \sigma^x_j \tau^z_{j+\frac{1}{2}} \mathcal{N}_{\text{KT}}
$$

$$
\mathcal{N}_{\text{KT}} \tau^y_{i-\frac{1}{2}} \tau^y_{i+\frac{1}{2}} = \tau^y_{j-\frac{1}{2}} \sigma^x_j \tau^y_{j+\frac{1}{2}} \mathcal{N}_{\text{KT}}
$$

$$
\mathcal{N}_{\text{KT}} \sigma_i^x = \sigma_i^x \mathcal{N}_{\text{KT}},
$$

$$
\mathcal{N}_{\text{KT}} \sigma^z_{j-1} \sigma^z_j = \sigma^z_{j-1} \tau^x_{j-\frac{1}{2}} \sigma^z_j \mathcal{N}_{\text{KT}}
$$

## 3. Gapped SPT from KT transformation

$$
\mathbb{Z}_2^{\sigma} \text{ SSB} + \mathbb{Z}_2^{\tau} \text{ SSB} \xLeftrightarrow{\mathcal{N}_{\text{KT}}} \mathbb{Z}_2^{\sigma} \times \mathbb{Z}_2^{\tau} \text{ gapped SPT},
$$

### 3.1 Mapping SSB to SPT

Start from a decouples SSB Hamiltonian:
$$
H_{\text{SSB}} = -\sum_{i=1}^L \left( \sigma^z_{i-1} \sigma^z_i + \tau^z_{i-\frac{1}{2}} \tau^z_{i+\frac{1}{2}} \right),
$$
implement the KT transformation, we get:
$$
H_{\text{SPT}} = -\sum_{j=1}^L \left( \sigma^z_{j-1} \tau^x_{j-\frac{1}{2}} \sigma^z_j + \tau^z_{j-\frac{1}{2}} \sigma^x_j \tau^z_{j+\frac{1}{2}} \right).
$$

> **Subtlety:**
>
> It's worth mentioning that, in $H_{SPT}$, there include $\sigma_{0}^z$  and $\tau_{L+1/2}^z$, which is not originally defined on lattice.
>
> $i = 1,2,3,...,L$ ,       $i-\frac{1}{2} = \frac{1}{2},\frac{3}{2},...,L-\frac{1}{2}$
>
> Under TBC or PBC carry different signs. In calculations afterwards, we have to first map them to well-defined subindices and then discuss.

This is a mapping between a SSB to a SPT. (At least at the level of Hamiltonian) 

==如何从state的角度理解这样的mapping？SSB的两个基态怎么map到SPT的单一基态？==

==这个问题的答案是——KT mapping并不保证基态一定map到基态，另一个SSB基态map去了别的态==

The field theory description is:
$$
KT\  \text{operation}= STS
$$

> Here:
>
> - S corresponds to gauging the global symmetry 
> - T corresponds to implementing an entangler / adding a topological response term

### 3.2 Ground state charge under TBC

A key feature of the SPT is that <u>the ground state carries a non-trivial charge under twisted boundary conditions.</u>

We leave out the derivation here, and readers can refer to [Li 2025](https://scipost.org/10.21468/SciPostPhys.18.5.153) page 9.

We emphasize the main result, namely `the charge of SPT ground state under TBC`.

- Obviously the ground state of SPT is **unique** on a ring.
- $\mathbb{Z}_2^\sigma$-twisted ground state is $\mathbb{Z}_2^\tau$ charged
- $\mathbb{Z}_2^\tau$-twisted ground state is $\mathbb{Z}_2^\sigma$ charged
- The above results can be analyzed from decoupled SSB system via KT transformation properties. (i.e., analyzing the energy spectrum)



## 4. Gapless SPT from KT transformation

$$
\mathbb{Z}_2^{\sigma} \text{ Ising CFT} + \mathbb{Z}_2^{\tau} \text{ SSB} \xLeftrightarrow{\mathcal{N}_{\text{KT}}} \mathbb{Z}_2^{\sigma} \times \mathbb{Z}_2^{\tau} \text{ gapless SPT},
$$

### 4.1 Mapping "Ising CFT$\boxtimes$SSB" to "gSPT"

We start from stacking `critical Ising chain of the link` with `SSB Ising chain of the site`.
$$
H_{\text{Ising}+\text{SSB}} = -\sum_{i=1}^L \left( \tau^z_{i-\frac{1}{2}} \tau^z_{i+\frac{1}{2}} + \sigma^z_{i-1} \sigma^z_i + \sigma^x_i \right).
$$
We apply the KT transformation, and get:
$$
H_{\text{gSPT}} = -\sum_{j=1}^L \left( \tau^z_{i-\frac{1}{2}} \sigma^x_i \tau^z_{i+\frac{1}{2}} + \sigma^z_{i-1} \tau^x_{i-\frac{1}{2}} \sigma^z_i + \sigma^x_i \right),
$$
which looks like a **critical point** between cluster model and a transverse $X$ field.

If we restrict ourselves to the ground state manifold, notice that $\tau^z_{i-\frac{1}{2}} \sigma^x_i \tau^z_{i+\frac{1}{2}}$ commutes with every term and thus stabilize the ground state, together with low excitation states.

> This is because violating $\tau^z_{i-\frac{1}{2}} \sigma^x_i \tau^z_{i+\frac{1}{2}}$ causes energy penalty of $O(1)$, while the low energy exciation are 'gapless', scaling as $O(\frac{1}{L})$.

==疑问：我们怎么知道map之后的哈密顿量也是gapless的？？==

==我目前的回答是：因为KT变换在OBC下是Unitary的，所以不改变spectrum，外推到热力学极限，可知KT变换将gapped$\rightarrow$gapped, gapless$\rightarrow$gapless。==

Thus, if we only care about low-energy degrees of freedom, we can substitute $\tau^z_{i-\frac{1}{2}} \tau^z_{i+\frac{1}{2}} = \sigma^x_i$, and we get another effective gSPT Hamiltonian:
$$
H_{\text{gsPT}} \simeq -\sum_{j=1}^L \left( \tau^z_{i-\frac{1}{2}} \sigma^x_i \tau^z_{i+\frac{1}{2}} + \sigma^z_{i-1} \tau^x_{i-\frac{1}{2}} \sigma^z_i + \tau^z_{i-\frac{1}{2}} \tau^z_{i+\frac{1}{2}} \right).
$$

### 4.2 Field Theory Point of View

The original partition function is $Z_{\text{Ising}}[A_{\sigma}]Z_{\text{SSB}}[A_{\tau}],$ namely Ising CFT stacking a SSB.

After the KT mapping, effectively the partition funtion is: $Z_{\text{Ising}}[A_{\tau}] e^{i \pi \int_{X_2} A_{\sigma} A_{\tau}}.$

**Key points:**

- $\text{Ising CFT}_{\tau}\boxtimes \text{SSB}_{\sigma} \xrightarrow{\mathcal{N}_{\text{KT}}}\text{Ising CFT}_{\tau}\boxtimes \text{gapped-SPT}_{(\mathbb{Z}_2^\tau\times\mathbb{Z}_2^\sigma)}$
- $\mathbb{Z}_2^{\sigma}$ symmetry only acts on the gapped sector.

- Gapless degrees of freedom are those carrying $\mathbb{Z}_2^{\tau}$ charge.



### 4.3 Topological features of gapless SPT

As usual, we discuss:

- Symmetry charge of GS under TBC
- GSD under OBC

#### 4.3.1 Symmetry charge of ground state under TBC

We actually do not have good analytical methods to verify symmetry charge and degeneracy. So we need numerics.(There are some tricks though, but may not work if there're symmetric perturbations)

- **Under periodic boundary conditions (PBC):**
  - The ground state is **unique** (non-degenerate).
  - It is **even (neutral)** under both $\mathbb{Z}_2^{\sigma}$ and $\mathbb{Z}_2^{\tau}$.

- **Under twisted boundary conditions (TBC) of $\mathbb{Z}_2^{\tau}$:**
  - The ground state remains **unique**.
  - It becomes **odd** under $\mathbb{Z}_2^{\sigma}$ but still **even** under $\mathbb{Z}_2^{\tau}$.
- **Under twisted boundary conditions of $\mathbb{Z}_2^{\sigma}$:**
  - The ground state is related to the PBC ground state by conjugation with $\tau^z_{1/2}$.
  - As a result, it carries the **same $\mathbb{Z}_2^{\sigma}$ charge** as in PBC, but its **$\mathbb{Z}_2^{\tau}$ charge is flipped**.
  - That is, it becomes **odd** under $\mathbb{Z}_2^{\tau}$ but still **even** under $\mathbb{Z}_2^{\sigma}$.

#### 4.3.2 Degeneracy under open boundary condition

We choose such OBC conditions:

We only keep terms which has sub-indices     $i = 1,2,3,...,L$ ,       $i-\frac{1}{2} = \frac{1}{2},\frac{3}{2},...,L-\frac{1}{2}$

That is:
$$
H_{\text{gSPT}}^{\text{OBC}} = -\sum_{i=1}^{L-1} \tau^z_{i-\frac{1}{2}} \sigma^x_i \tau^z_{i+\frac{1}{2}} - \sum_{i=2}^L \sigma^z_{i-1} \tau^x_{i-\frac{1}{2}} \sigma^z_i - \sum_{i=1}^L \sigma^x_i.
$$
We actually avoided "TBC" subtlety, since every term in it is well-defined.

We have some "edge symmetries", which are operators localized at the edges.
$$
\tau^z_{\frac{1}{2}}, \quad \tau^z_{L-\frac{1}{2}} \sigma^x_L, \quad U_{\sigma}, \quad U_{\tau}.
$$
Because \( \{\tau^z_{\frac{1}{2}}, U_{\tau}\} = \{\tau^z_{L-\frac{1}{2}} \sigma^x_L, U_{\tau}\} = 0 \), the irreducible representation of the algebra (similar to clifford algebra) is two dimensional. Hence there are **at least** two degenerate ground states. Indeed, there are two degenerate ground states, which I have verified using numerics.

> 可以认为左右两端各有一个spin-1/2（described by eigenstates of $\tau^z_{\frac{1}{2}}$ and $\quad \tau^z_{L-\frac{1}{2}}$ respectively）。考虑到基态只有两重简并，这两个spin-1/2不是独立的。数值证明这两个spin方向是相同的，即$\ket{\uparrow\uparrow}$ 或者$\ket{\downarrow\downarrow}$。
>
> 另一件事情是，由于$U_\tau$和这两个effective的$Z$ operator都反对易，它实际上起到Pauli $X$的作用，其本征态是Bell state，即$\ket{\uparrow\uparrow}\pm\ket{\downarrow\downarrow}$

Under bulk perturbation, like $-h\sum_i \tau^x_{i-1/2}$, the edge degeneracy is lifted. `(Any GSD of finite system is nothing but coincidence.)`However, that gap decays exponentially with $L$, so the GS is still degenerate in the thermodynamic limit.

> 实际上，加入$U_\tau$ preserving的微扰后，不难想象基态正是$\ket{\uparrow\uparrow}\pm\ket{\downarrow\downarrow}$，which are seperated by an exponetially small gap。
>
> 在[T. Scaffidi 2017](10.1103/PhysRevX.7.041048)里，作者指出第一激发态对应于$\ket{\uparrow\downarrow}\pm\ket{\downarrow\uparrow}$
>
> (他们文章里没写成Bell state，但是我认为起码应该preserve $U_\tau$ symmetry)

### 4.4 Topological features from KT transformation

Using KT transformation, one can understand the `spectrum of gSPT` using the `already known results of Ising CFT and SSB phase`.

We leave out the discussion here. Readers may refer to  [Li 2025](https://scipost.org/10.21468/SciPostPhys.18.5.153) page 13.

One thing I do wanna emphasize is that, **in OBC**, KT transformation is **unitary**, and totally **preserves the spectrum**.





## 5. Intrinsically gapless SPT from KT transformation

We start with a SSB on the site and a XX model on the link, decoupled.
$$
H_{SSB+XX} = -\sum_{i=1}^{L} \left( \tau_{i-\frac{1}{2}}^z \tau_{i+\frac{1}{2}}^z + \tau_{i-\frac{1}{2}}^y \tau_{i+\frac{1}{2}}^y + \sigma_{i-1}^z \sigma_{i}^z \right).
$$

> Note that we use $\tau_{i-\frac{1}{2}}^z \tau_{i+\frac{1}{2}}^z + \tau_{i-\frac{1}{2}}^y \tau_{i+\frac{1}{2}}^y$ instead of the usual form $\tau_{i-\frac{1}{2}}^x \tau_{i+\frac{1}{2}}^x + \tau_{i-\frac{1}{2}}^y \tau_{i+\frac{1}{2}}^y$
>
> Thus the corrsponding rotation is along the $x$-axis

This Hamiltonian has a \( U(1)^\tau \times \mathbb{Z}_2^\sigma \) global symmetry, where \(\mathbb{Z}_2^\sigma\) is generated by :
$$
 U_\sigma = \prod_i\sigma^x_i 
$$


The $U^\tau(1)$ symmetry is generated by:
\[
\prod_{i=1}^{L} e^{\frac{i\alpha}{2}(1-\tau_{i-\frac{1}{2}}^x)}, \quad \alpha \simeq \alpha + 2\pi.
\]

> **Note:**
>
> In case the reader is not familiar with related algebra:
>
> Each term in the above $U^\tau(1)$ generator is composed of an irrelevant phase factor $e^{\frac{i\alpha}{2}}$ and a $\alpha$-rotation around the $x$-axis, $R_x(\alpha)_{i-\frac{1}{2}} = e^{-\frac{i\alpha}{2}\tau^x_{i-\frac{1}{2}}} =\cos(\frac{\alpha}{2})\,I - i\sin(\frac{\alpha}{2})\tau^x_{i-\frac{1}{2}}$
>
> We denote:$R_x(\alpha) = \prod_i e^{-i \frac{\alpha}{2} \tau^x_{i-\frac{1}{2}}}  $
> $$
> \tau^y \mapsto R_x(\alpha) \tau^y R_x(\alpha)^\dagger = \cos \alpha \, \tau^y + \sin \alpha \, \tau^z, \quad
> 
> 
> \tau^z \mapsto R_x(\alpha) \tau^z R_x(\alpha)^\dagger = \cos \alpha \, \tau^z - \sin \alpha \, \tau^y.
> $$
> One can explicitly verify the XX part is invariant under this rotation.

Specially, one can take out the normal subgroup of $U^\tau(1)$:

- $\alpha = \pi$, the generator is $ e^{\frac{i\alpha}{2}}R_x(\pi) = e^{\frac{i\pi}{2}}\prod_i e^{-i \frac{\pi}{2} \tau^x_{i-\frac{1}{2}}}= \prod_i \tau^x_{i-\frac{1}{2}} = U_\tau $    $\rightarrow$ Go back to $\mathbb{Z}_2^\tau$

- $\alpha = \pi/2$, we have the generator
  \[
  V_\tau = \prod_{i=1}^{L} e^{\frac{i\pi}{4}(1-\tau_{i-\frac{1}{2}}^x)},
  \]

And this is a **$\mathbb{Z}_4^\tau$ subgroup**

We would be interested in the  \( \mathbb{Z}_4^\tau \times \mathbb{Z}_2^\sigma \) symmetry, generated by \( V_\tau \) and \( U_\sigma \).

Then we apply the **KT transformation**. We get:
$$
H_{\text{igSPT}} = -\sum_{i=1}^{L} \left( \tau_{i-\frac{1}{2}}^z \sigma_{i}^x \tau_{i+\frac{1}{2}}^z + \tau_{i-\frac{1}{2}}^y \sigma_{i}^x \tau_{i+\frac{1}{2}}^y + \sigma_{i-1}^z \tau_{i-\frac{1}{2}}^x \sigma_{i}^z \right).
$$
Notice that $ U_\sigma$ and $ V_\tau$ only contains $\text{Pauli X}$ operators, which are invariant under $KT$ transformations. Thus, the resulting Hamiltonian $H_{\text{igSPT}}$ also has $ \mathbb{Z}_4^\tau \times \mathbb{Z}_2^\sigma $ symmetry, generated by $ U_\sigma$ and $ V_\tau$ respectively.

We also mention that, actually, $H_{\text{igSPT}}$ is protected by a "$\mathbb{Z}_4^\Gamma$" symmetry, generated by $ U_\sigma V_\tau$. But is worth emphasizing that the Hamiltonian itself has $ \mathbb{Z}_4^\tau \times \mathbb{Z}_2^\sigma $ symmetry.

### A Cut-in Section: Symmetry-Twist sector Revisited

We have dealt with Symmetry-Twist sectors in previous sections, but here I would like to revisit it.

##### Symmetry Sector

Generally we consider a 0-form symmetry $U$ that commmutes with the Hamiltonian. Thus, the eigenvalue of $U$ can be considered `Good Quantum Number`. We can find such a basis that every energy eigenstate is also the eigenstate of $U$. So we use $u$ to mark the symmetry sector of an energy eigenstate.

##### Twist Sector

Suppose we are considering **a ring of length $L$.**

We talk about whether symmetry $G$ is twisted or not, where we use an index $t$ to mark it. Note that $t$ can take value in the group $G$. We suppose the symmetry generator is $U$.

Twisting means the Hilbert space of site $i+L$ is different from the Hilbert space of site $i$, and the difference is related by $(U_i)^t$. Here $U_i$ is the onsite part of $U$.

If the state of site $i$ is $\ket{\psi_i}$, then:
$$
\ket{\psi_{i+L}} = U^t_i\ket{\psi_i}
$$


The operator is similarly transformed. The operator $A_i$ is transformed to $A_{i+L} = U_i^tA_i(U_i^t)^\dagger$.

We take $\mathbb{Z}_2$ symmetry for an example:

- $t = 0$, $U_i^t = I$, so $\ket{0}_i\rightarrow\ket{0}_{i+L},\ket{1}_i\rightarrow\ket{1}_{i+L}$

- $t=1$, $U_i^t = \sigma^x_i$ . Thus, $\ket{0}_{i}\rightarrow\ket{1}_{i+L},\ket{1}_{i}\rightarrow\ket{0}_{i+L}$

  Correspondingly, $\sigma_{i}^z\rightarrow  = \sigma^x_i\sigma_{i}^z (\sigma^x_i)^\dagger = -\sigma^z_i$

We can also take $\mathbb{Z}_4$ symmetry as an example:

- $t = 0$, the effective operator $V_i^0 = I$

- $t = 1$, the effective operator 
  $$
  V_i^1 =e^{\frac{i\pi}{4}(1-\tau_{i}^x)} =\begin{pmatrix} \tfrac12+\tfrac{i}{2} & \tfrac12-\tfrac{i}{2}\\[2pt]
  
  ​                              \tfrac12-\tfrac{i}{2} & \tfrac12+\tfrac{i}{2}\end{pmatrix}
  $$
  

- $t = 2$, the effective operator $V_i^2 = \sigma^x_i$

- $t = 3$, the effective operator 
  $$
  V_i^3=e^{\frac{i3\pi}{4}(1-\tau_{i}^x)}=\begin{pmatrix} \tfrac12-\tfrac{i}{2} & \tfrac12+\tfrac{i}{2}\\[2pt]
                                \tfrac12+\tfrac{i}{2} & \tfrac12-\tfrac{i}{2}\end{pmatrix}
  $$

==如果是Non-onsite symmetry要怎么定义Twist呢？==





