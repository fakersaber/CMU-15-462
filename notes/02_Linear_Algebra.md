# 02_Linear_Algebra

**Linear Map**

- A map f is linear if it maps vectors to vectors, and if for all vectors u,v and scalars A we have:
  $$
  f(u+v) = f(u)+f(v)\\
  f(au) = af(u)
  $$
  (不仅仅是向量满足该运算，如果函数满足上述条件也称为线性运算)



**Linear Map in Coordinates**

- A Map is linear if it can be expressed as

$$
f(u_{1},...u_{m}) = \sum_{i=1}^n u_i a_i
$$

- 图像表示一个已经存在的Vector线性组合可以由新的向量集合表示

  ![1571366487394](assets/1571366487394.png)

**Affine Maps**

- Affine is not a linear, eg. f(x) = ax + b

- 仿射变换满足加权和（preserve weighted sums）
  $$
  f(w_1 x_1 + ... + w_nx_n) = \sum_i w_i f(x_i)\\
  其中\sum_i w_i = 1
  $$
  

**span**

- the span is the set of all vectors that can be written as a linear combination of u and v.  show blow:
  $$
  au+bv\\
  span(u1,...,uk) = \lbrace x\subset|x=\sum_{i=1}^k a_iu_i, a_1,...a_k\subset R \rbrace
  $$

**Orthonormal Basis**

- if e1,...,en are our basis vectors then:
  $$
  <e_i,e_j> = \begin{cases}
  	1, i=j\\
  	0, otherwise\\
   \end{cases}
  $$
  即<ei,ej>表示ei在ej上的投影

**Gram-schmidt**

- normalize the first vector(divide by its length)
- subtract any component of the 1st vector from the 2nd one
  - 即将任何vector1在vector2上的分量减去

- normalize the 2nd one
- 经过以上步骤得到两个正交的向量

![1571405126482](assets/1571405126482.png)

**Bilinear And Quadratic Forms**
$$
B(ax+by,z) = aB(x,z) +bB(y,z)\\
B(x,ay+bz) = aB(x,y) +bB(x,z)
$$
A quadratic form is any map 
$$
Q : Rn → R
$$
 that satisﬁes 
$$
Q(ax) = a^2Q(x)
$$
记
$$
Q(x) = B(x,x) = ax_1^2+bx_1x_2+cx_2^2
$$
所以有
$$
B(x,y) := \frac12 (Q(x+y)−Q(x)−Q(y)).
$$
