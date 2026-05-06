Let

\[
T(x)=\lfloor x\rfloor \,\langle x\rangle ,\qquad
\langle x\rangle =x-\lfloor x\rfloor ,\qquad x\in\mathbb {R}.
\]

The sequence is defined by \(a_{i+1}=T(a_{i})\;(i\ge 0)\).
Denote

\[
n_i=\lfloor a_i\rfloor ,\qquad f_i=\langle a_i\rangle\;(=a_i-n_i\in[0,1)).
\]

--------------------------------------------------------------------
### 1.  Non‑negative initial values

Assume \(a_0\ge 0\).
If \(n_i=0\) then \(a_{i+1}=0\) and the sequence stays equal to \(0\) forever, so
\(a_{i+2}=a_i\) for all large \(i\).

Suppose \(n_i\ge 1\).  Then

\[
a_{i+1}=n_i f_i\quad\text{with }0\le f_i<1,
\]

hence \(a_{i+1}<n_i\).  Because \(n_i\) is an integer,
\[
\lfloor a_{i+1}\rfloor\le n_i-1 .
\]
Thus the integer part drops at least by one at every step as long as it is
positive.  After at most \(n_0+1\) steps we reach an index \(k\) with
\(n_k=0\); consequently \(a_k=0\) and for every \(j\ge k\)

\[
a_j=0,\qquad a_{j+2}=a_j .
\]

--------------------------------------------------------------------
### 2.  Negative initial values

Now let \(a_0<0\).  Write

\[
a_i= -m_i+r_i ,\qquad m_i\in\mathbb N,\; r_i\in[0,1),
\]
so that \(\lfloor a_i\rfloor =-m_i\) and \(\langle a_i\rangle =1-r_i\).
Hence

\[
a_{i+1}= \lfloor a_i\rfloor \langle a_i\rangle
        =-m_i(1-r_i)=-(m_i- m_i r_i).
\tag{1}
\]

Put \(b_i:=-a_i\;(>0)\).  From (1)

\[
b_{i+1}=m_i(1-r_i)=\bigl\lceil b_i\bigr\rceil\,
               \bigl\{b_i\bigr\},\qquad b_i>0 .
\tag{2}
\]

--------------------------------------------------------------------
#### Lemma

For every \(b>0\) the sequence defined by (2) reaches the interval \((0,1]\)
after at most two steps.

*Proof.*
Let \(b\in (k,k+1]\;(k\in\mathbb N)\).  Then \(\lceil b\rceil =k+1\) and
\(\{b\}=b-k\in(0,1]\).  Consequently

\[
b_1=(k+1)(b-k)\le k+1 .
\]

If \(b_1\le 1\) we are done.  If \(b_1>1\) then \(b_1\in(k, k+1]\) with
\(k\le 1\); thus \(k=1\) and \(b_1\in(1,2]\).  Applying (2) once more gives

\[
b_2=2(b_1-1)\le 2,
\]

and the same argument shows \(b_2\le 1\).  ∎



Applying the Lemma to \(b_i=-a_i\) we obtain an index \(N\) such that

\[
-1<a_N<0 .
\tag{3}
\]

--------------------------------------------------------------------
#### Behaviour on \((-1,0)\)

If \(x\in(-1,0)\) then \(\lfloor x\rfloor=-1\) and \(\langle x\rangle =1+x\); hence

\[
T(x) = -1\,(1+x)= -1-x .
\]

Therefore for every \(x\in(-1,0)\)

\[
T^{2}(x)=T(T(x))=T(-1-x)=-1-(-1-x)=x .
\tag{4}
\]

Thus every point of \((-1,0)\) is a 2‑cycle (the point \(-\tfrac12\) is a fixed
point, which also satisfies (4)).

--------------------------------------------------------------------
### 3.  End of the proof

From Sections 1 and 2 we have shown:

* if \(a_0\ge 0\) then after finitely many steps the sequence becomes constantly
  \(0\);
* if \(a_0<0\) then after finitely many steps it enters the interval
  \((-1,0)\), and on that interval the map satisfies \(T^{2}= \text{id}\).

Consequently there exists an integer \(N\) (depending on \(a_0\)) such that

\[
a_{i+2}=a_i\qquad\text{for all } i\ge N .
\]

Hence the sequence is eventually periodic with period \(2\) (the period may
degenerate to \(1\) when the limit is \(0\)). ∎

\[
\boxed{\displaystyle\text{For every real }a_0,\; a_{i+2}=a_i\text{ for all
sufficiently large }i.}
\]