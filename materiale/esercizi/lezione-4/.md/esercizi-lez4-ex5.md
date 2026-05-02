## $$ \textcolor{red}{\text{Esercizi Lez. 4 - Ex 5}} $$

#### Esercizio 1

Uno studente studia con probabilità $\frac{1}{2}$. Gli viene presentato un quiz con 4 risposte possibili. Se ha studiato da certamente la risposta esatta, se non ha studiato sceglie a caso una delle 4 risposte. Supponiamo che abbia dato risposta esatta: con che probabilità ha studiato davvero?

##### Risoluzione

Definiamo i due eventi:

$\begin{aligned}
E &= \{\text{"Lo studente ha dato la risposta esatta}"\} \\
S &= \{\text{"Lo studente ha studiato"}\}
\end{aligned}$

Calcoliamo $P(E)$ con la **legge della Probabilità Totale**:

$$\begin{aligned}
P(S) &= P(S') = 0.50 \\
P(E\cap S) &= P(E\mid S)\cdot P(S) = 1\cdot0.50 = 0.50 \\
P(E\cap S') &= P(E\mid S')\cdot P(S') = \frac{1}{4}\cdot0.50 = 0.125 \\
P(E) &= P(E\cap S) + P(E\cap S') = 0.50 + 0.125 = 0.625
\end{aligned}$$

Calcoliamo $P(S\mid E)$ tramite l'applicazione della **legge di Bayes**:

$$\begin{aligned}
P(S\mid E) &= \frac{P(E\mid S)\cdot P(S)}{P(E)} \\
&= \frac{0.50}{0.625} = \boxed{0.8} \;.
\end{aligned}$$

> **Nota**. Dati $A_1,A_2,\dots,A_n$ eventi **disgiunti due a due** ($A_i\cap A_j=\emptyset$) che compongono una **partizione** di $\Omega$ ($A_1\cup\dots\cup A_n = \Omega$). La formula della legge della probabilità totale dice che:
>
> $$\begin{aligned}
> P(D) &= P(D\cap A_1) + \dots + P(D\cap A_n) \\
> &= P(D\mid A_1)\cdot P(A_1) + \dots + P(D\mid A_n)\cdot P(A_n) \\
> &= \sum_{i=1}^n P(D\mid A_i)\cdot P(A_i)
> \end{aligned}$$

> **Nota**. Se voglio **invertire il condizionamento** degli eventi posso sfruttare la proprietà di simmetria. La formula della legge di Bayes dice che:
>
> $$\begin{aligned}
> P(B\mid A) &= \frac{P(A\mid B)\cdot P(B)}{P(A)}
> \end{aligned}$$
>
> Unendo la legge di Bayes con la probabilità totale otteniamo:
>
> $$\begin{aligned}
> P(C_i\mid D) &= \frac{P(D\mid C_i)\cdot P(C_i)}{\sum_{k=1}^n P(D\mid C_k)\cdot P(C_k)}
> \end{aligned}$$

---

#### Esercizio 2

In una regione una malattia colpisce il 5 per mille della popolazione. Un test è affidabile con probabilità 0.99 tanto sui sani quanto sui malati. *Cioè: per un malato il test è postivo con probabilità 0.99; per un sano il test è negativo con probabilità 0.99*.
- (a) Se il risultato di una persona è positivo, trova la probabilità che la persona sia realmente malata.
- (b) Se il risultato è negativo, trova la probabilità che la persona sia in realtà malata.

##### Risoluzione

Definiamo gli eventi:

$\begin{aligned}
M &= \{\text{"La persona ha contratto la malattia"}\} \\
N &= \{\text{"L'esito del test è risultato negativo"}\}
\end{aligned}$

Abbiamo che:

$\begin{aligned}
P(M) = 0.005, &\qquad P(M') = 0.995 \\
P(N'\mid M) = 0.99, &\qquad P(N'\mid M') = 0.01 \\
P(N\mid M') = 0.99, &\qquad P(N\mid M) = 0.01  
\end{aligned}$

- **(a)** Calcoliamo $P(M\mid N')$ applicando la **legge di Bayes**:

    $$\begin{aligned}
    P(M\mid N') &= \frac{P(N'\mid M)\cdot P(M)}{P(N'\mid M)\cdot P(M) + P(N'\mid M')\cdot P(M')} \\
    &= \frac{0.99\cdot 0.005}{0.99\cdot 0.005 + 0.01\cdot 0.995} = \boxed{33.22\%} \;.
    \end{aligned}$$

- **(b)** Calcolare $P(M\mid N)$ applicando la **legge di Bayes**:

    $$\begin{aligned}
    P(M\mid N) &= \frac{P(N\mid M)\cdot P(M)}{P(N\mid M)\cdot P(M) + P(N\mid M')\cdot P(M')} \\
    &= \frac{0.01\cdot 0.005}{0.01\cdot 0.005 + 0.99\cdot 0.995} \approx \boxed{5.075\times 10^{-5}} \;.
    \end{aligned}$$

---

#### Esercizio 3



##### Risoluzione



---

#### Esercizio 4



##### Risoluzione



---

#### Esercizio 5



##### Risoluzione



---