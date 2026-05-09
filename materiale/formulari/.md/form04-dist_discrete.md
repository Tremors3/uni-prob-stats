# Distribuzioni Notevoli Discrete

## Distribuzione Bernoulliana

Modella un singolo esperimento con due possibili esiti: successo o fallimento.

$$
X \sim \text{Ber}(p),\qquad X\in\{0,1\}
$$

dove:
- $X=1$ → successo
- $X=0$ → fallimento

#### Formula

$$
P(X=1)=p
$$

$$
P(X=0)=1-p
$$

con:

$$
0 \leq p \leq 1
$$

#### Parametri

- $p$ = probabilità di successo
- $1-p$ = probabilità di fallimento

#### Spiegazione intuitiva per utilizzo

Si usa quando si effettua **una sola prova** con due soli esiti possibili.

Esempi:
- lancio di una moneta (testa/croce)
- risposta corretta o errata
- componente funzionante o guasto

---

## Distribuzione Binomiale

Modella il numero di successi in $n$ prove indipendenti di Bernoulli.
$$
X \sim \text{Bin}(n,p)
$$

#### Formula

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

con:

$$
k=0,1,\dots,n
$$

#### Parametri

- $n$ = numero di prove
- $p$ = probabilità di successo in ogni prova

Assunzioni:
- prove indipendenti
- probabilità costante
- due soli esiti per prova

#### Spiegazione intuitiva per utilizzo

Si usa quando si vuole contare **quanti successi** avvengono in un numero fissato di prove.

Esempi:
- numero di teste in 10 lanci
- numero di risposte corrette in un test
- numero di prodotti difettosi in un campione

---

## Distribuzione Geometrica

Modella il numero di prove necessarie per ottenere il primo successo.

$$
X \sim \text{Geom}(p)
$$

#### Formula

$$
P(X=k)=(1-p)^{k-1}p
$$

con:

$$
k=1,2,3,\dots
$$

#### Parametri

- $p$ = probabilità di successo ad ogni prova

Assunzioni:
- prove indipendenti
- probabilità costante

#### Proprietà importante — Perdita di memoria

$$
P(X>s+t \mid X>s)=P(X>t)
$$

La probabilità futura non dipende dal passato.

#### Spiegazione intuitiva per utilizzo

Si usa quando interessa sapere **quanto bisogna aspettare** prima del primo successo.

Esempi:
- numero di lanci prima della prima testa
- numero di tentativi prima di vincere
- numero di chiamate prima della prima risposta

---

## Distribuzione Binomiale Negativa

Modella il numero di prove necessarie per ottenere il $r$-esimo successo.

$$
X \sim \text{NB}(r,p)
$$

#### Formula

$$
P(X=k)=\binom{k-1}{r-1}p^r(1-p)^{k-r}
$$

con:

$$
k=r,r+1,r+2,\dots
$$

#### Parametri

- $r$ = numero di successi desiderati
- $p$ = probabilità di successo ad ogni prova

Assunzioni:
- prove indipendenti
- probabilità costante

#### Spiegazione intuitiva per utilizzo

Si usa quando interessa sapere quante prove servono per raggiungere un certo numero di successi.

Esempi:
- quanti lanci servono per ottenere 3 teste
- quante telefonate servono per ottenere 5 risposte
- quanti tentativi servono per ottenere 2 vittorie

---

## Distribuzione Ipergeometrica

Modella il numero di successi in un campione estratto **senza reinserimento** da una popolazione finita.

$$
X \sim \text{Hyp}(N,K,n)
$$

#### Formula

$$
P(X=k)=
\frac{
\binom{K}{k}\binom{N-K}{n-k}
}{
\binom{N}{n}
}
$$

con:

$$
\max(0,n-(N-K)) \leq k \leq \min(n,K)
$$

#### Parametri

- $N$ = dimensione della popolazione
- $K$ = numero di elementi “successo” nella popolazione
- $n$ = numero di estrazioni
- $k$ = successi osservati nel campione

Assunzioni:
- popolazione finita
- estrazioni senza reinserimento
- due categorie possibili (successo/fallimento)

#### Spiegazione intuitiva per utilizzo

Si usa quando si estraggono elementi da una popolazione finita senza rimetterli dentro.

Esempi:
- carte da un mazzo
- pezzi difettosi da un lotto
- studenti scelti da una classe

---

## Distribuzione di Poisson

Modella il numero di eventi che avvengono in un intervallo di tempo, spazio o area.

$$
X \sim \text{Poisson}(\lambda)
$$

#### Formula

$$
P(X=k)=
e^{-\lambda}\frac{\lambda^k}{k!}
$$

con:
$$
k=0,1,2,\dots
$$

#### Parametri

- $\lambda$ = numero medio di eventi nell’intervallo (tasso), con $\lambda>0$

#### Assunzioni

Gli eventi:
- avvengono casualmente
- sono indipendenti
- hanno tasso medio costante
- non avvengono simultaneamente

#### Spiegazione intuitiva per utilizzo

Si usa per contare eventi rari distribuiti nel tempo o nello spazio.

Esempi:
- chiamate ricevute in un’ora
- incidenti in un giorno
- errori di stampa in una pagina
- clienti che arrivano in un negozio

---

# Relazioni tra Distribuzioni

Una Bernoulliana è una Binomiale con una sola prova:

$$
\text{Ber}(p)=\text{Bin}(1,p)
$$

Un solo esperimento.

---

La Geometrica modella l’attesa del primo successo:

$$
\text{Geom}(p)=\text{NB}(1,p)
$$

Un solo successo.

---

Binomiale come somma di Bernoulliane indipendenti

Se:

$$
X_i \sim \text{Ber}(p)
$$

indipendenti, allora:

$$
X=\sum_{i=1}^{n}X_i
\sim \text{Bin}(n,p)
$$

---

Poisson come approssimazione della Binomiale

Se:

- $n$ molto grande
- $p$ molto piccolo

e:

$$
\lambda=np
$$

allora:

$$
\text{Bin}(n,p)\approx \text{Poisson}(\lambda)
$$

---

Proprietà comune: somma di Poisson indipendenti

Se:

$$
X_1 \sim \text{Poisson}(\lambda_1)
$$

e:

$$
X_2 \sim \text{Poisson}(\lambda_2)
$$

indipendenti, allora:

$$
X_1+X_2
\sim
\text{Poisson}(\lambda_1+\lambda_2)
$$

---

Binomiale vs Ipergeometrica

- **Binomiale**:
  - estrazioni indipendenti
  - con reinserimento

- **Ipergeometrica**:
  - estrazioni dipendenti
  - senza reinserimento

---

Binomiale vs Binomiale Negativa

- **Binomiale**:
  - numero di prove fissato
  - si conta il numero di successi

    $$
    X \sim \text{Bin}(n,p)
    $$

    Domanda tipica:
    > Quanti successi ottengo in $n$ prove?

- **Binomiale Negativa**:
  - numero di successi fissato
  - si conta quante prove servono

    $$
    X \sim \text{NB}(r,p)
    $$

    Domanda tipica:
    > Quante prove servono per ottenere $r$ successi?

---