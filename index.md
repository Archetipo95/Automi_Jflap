# Automi e Linguaggi formali 17/18 {ignore=true}

`NON GARANTISCO LA CORRETTEZZA DEGLI ESERCIZI`

Il nome di ogni esercizio è dato dal numero della slide più il numero della pagina in cui si trova e da una lettera se presenti più esercizi nella stessa pagina.

## Raccolta esercizi {ignore=true}

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [Tutorato 01](#tutorato-01)
	* [Esercizio tut01A](#esercizio-tut01a)
	* [Esercizio tut01B](#esercizio-tut01b)
	* [Esercizio tut01C](#esercizio-tut01c)
	* [Esercizio tut01D](#esercizio-tut01d)
	* [Esercizio tut01E](#esercizio-tut01e)
	* [Esercizio tut01F](#esercizio-tut01f)
	* [Esercizio tut01G](#esercizio-tut01g)
* [01-intro-dfa](#01-intro-dfa)
	* [Esercizio 0122](#esercizio-0122)
	* [Esercizio 0123A](#esercizio-0123a)
	* [Esercizio 0123B](#esercizio-0123b)
	* [Esercizio 0123C](#esercizio-0123c)
	* [Esercizio 0123D](#esercizio-0123d)
	* [Esercizio 0124](#esercizio-0124)
* [02-03-nfa](#02-03-nfa)
	* [Esercizio 02-0305E](#esercizio-02-0305e)
	* [Esercizio 02-0307](#esercizio-02-0307)
	* [Esercizio 02-0312A](#esercizio-02-0312a)
	* [Esercizio 02-0312B](#esercizio-02-0312b)
	* [Esercizio 02-0312C](#esercizio-02-0312c)
	* [Esercizio 02-0313](#esercizio-02-0313)
	* [Esercizio 02-0323](#esercizio-02-0323)
	* [Esercizio 02-0324](#esercizio-02-0324)
	* [Esercizio 02-0325](#esercizio-02-0325)
* [04-epsilon](#04-epsilon)
	* [Esercizio 0402](#esercizio-0402)
	* [Esercizio 0404](#esercizio-0404)
	* [Esercizio 0418](#esercizio-0418)
* [05-regexp](#05-regexp)
	* [Esercizio 0512](#esercizio-0512)
	* [Esercizio 0514A](#esercizio-0514a)
	* [Esercizio 0514B](#esercizio-0514b)
	* [Esercizio 0514C](#esercizio-0514c)
	* [Esercizio 0515A](#esercizio-0515a)
	* [Esercizio 0515B](#esercizio-0515b)
	* [Esercizio 0515C](#esercizio-0515c)
	* [Esercizio 0520](#esercizio-0520)
* [06-esercizi-er](#06-esercizi-er)
	* [Esercizio 0607A](#esercizio-0607a)
	* [Esercizio 0607B](#esercizio-0607b)
	* [Esercizio 0607C](#esercizio-0607c)
	* [Esercizio 0608A](#esercizio-0608a)
	* [Esercizio 0608B](#esercizio-0608b)
	* [Esercizio 0608C](#esercizio-0608c)
	* [Esercizio 0608D](#esercizio-0608d)
* [07-dfa2re](#07-dfa2re)
	* [Esercizio 0707A](#esercizio-0707a)
	* [Esercizio 0707B](#esercizio-0707b)
	* [Esercizio 0708](#esercizio-0708)
* [08-pumpinglemma](#08-pumpinglemma)
	* [Esercizio 0811](#esercizio-0811)
	* [Esercizio 0812](#esercizio-0812)
	* [Esercizio 0813](#esercizio-0813)
* [Credits](#credits)

<!-- /code_chunk_output -->

## Tutorato 01

### Esercizio tut01A

DFA che accetta tutte le stringhe che iniziano o finiscono con 01.

@import "immagini/tut01a.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio tut01B

DFA che accetta tutte le stringhe che contengono almeno 2 zeri lunghe 5 caratteri.

@import "immagini/tut01b.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio tut01C

Trasformare da NFA a DFA.

@import "immagini/tut01cConsegna.png"- [Raccolta esercizi](#raccolta-esercizi)

@import "immagini/tut01c.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio tut01D

Vedi esercizio 25 slide 02. [LINK](#esercizio-02-0325)

### Esercizio tut01E

Trasformare da $\varepsilon$-NFA a DFA.

@import "immagini/tut01eConsegna.png"- [Raccolta esercizi](#raccolta-esercizi)

Chiusura = insieme di tutti gli stati in cui si può arrivare seguendo le $\varepsilon$-transizioni.

ENCLOSE ($q_0$)=$\{q_0,q_1,q_2\}$

|| a | b| c|
|-:|:-:|:-:|:-:|
|$\rightarrow \{q_0,q_1,q_2\}$|$\{q_0,q_1,q_2\}$|$\{q_1,q_2\}$|$\{q_2\}$
|*$\{q_1,q_2\}$|$\emptyset$|$\{q_1,q_2\}$|$\{q_2\}$
|*$\{q_2\}$|$\emptyset$|$\emptyset$|$\{q_2\}$
|$\emptyset$|$\emptyset$|$\emptyset$|$\emptyset$

@import "immagini/tut01e.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio tut01F

DFA che accetta multipli di 3 in binario.

@import "immagini/tut01f.png"- [Raccolta esercizi](#raccolta-esercizi)

In questo caso bisogna prendere il binario e dividerlo per 3 e poi osservare i resti.
Gli stati rappresentano:
* $q_0$ tutti i binari con resto 0
* $q_1$ tutti i binari con resto 1
* $q_2$ tutti i binari con resto 2

Ci interessa resto 0 per trovare i multipli di 3 quindi $q_0$ è lo stato finale.
Partendo da $q_0$ potrei trovare 0 (rimango in $q_0$) oppure 1 (mi sposto in $q_1$ $\rightarrow$ resto 1). Se sono in $q_1$ significa che prima ho trovato un 1 quindi trovando un altro 1 (ottenedo 11 che da resto 0 $\rightarrow$ torno in $q_0$) oppure 0 (ottenengo 10 che mi da resto 2 $\rightarrow$ vado in $q_2$). Essendo arrivato in $q_2$ ho trovato 10 e da qui posso trovare 0 (ottengo 100 che mi da resto 1 $\rightarrow$ vado in $q_1$) oppure 1 (ottengo 101 che mi da resto 2 $\rightarrow$ rimango in $q_2$).

### Esercizio tut01G

Espressioni regolari con:

* 2 oppure 3 `b` con $\Sigma$={a,b}
a\*ba\*ba\*(ba\*+$\varepsilon$)

* numero di zeri multiplo di 5 con $\Sigma$={0,1}
(1\*01\*01\*01\*01\*01\*)\*1\*

* lunghezza stringa multiplo di 3 con  $\Sigma$={a,b,c}\*
((a+b+c)(a+b+c)(a+b+c))\*

## 01-intro-dfa

### Esercizio 0122

Automa che accetta il linguaggio delle stringhe con 01 come sottostringa.

@import "immagini/0122.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0123A

Insieme di tutte e sole le stringhe con un numero pari di 0 e un numero pari di 1.

@import "immagini/0123A.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0123B

Insieme di tutte le stringhe che finiscono con 00.

@import "immagini/0123B.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0123C

Insieme di tutte le stringhe che contengono esattamente tre zeri (anche non consecutivi).

@import "immagini/0123C.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0123D

Insieme delle stringhe che cominciano o finiscono (o entrambe le cose) con 01.

@import "immagini/0123D.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0124

Modellare il comportamento di un distributore di bibite con un DFA. Il modello deve rispettare le seguenti specifiche:

* Costo della bibita: 40 centesimi
* Monete utilizzabili: 10 centesimi, 20 centesimi
* Appena le monete inserite raggiungono o superano il costo della bibita, il distributore emette una lattina
* Il distributore dà il resto (se serve) subito dopo aver emesso la lattina

@import "immagini/0124.png"- [Raccolta esercizi](#raccolta-esercizi)

## 02-03-nfa

### Esercizio 02-0305E

Insieme di tutte le stringhe che finiscono con 01.

@import "immagini/0205E.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0307

Riconosce le parole che terminano con 01 “scommettendo” se sta leggendo gli ultimi due simboli oppure no

@import "immagini/0207.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0312A

L’insieme delle parole sull’alfabeto {0, 1, . . . , 9} tali che la cifra finale sia comparsa in precedenza.

@import "immagini/0212A.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0312B

L’insieme delle parole sull’alfabeto {0, 1, . . . , 9} tali che la cifra finale non sia comparsa in precedenza.

@import "immagini/0212B.png"- [Raccolta esercizi](#raccolta-esercizi)
(Non vale per stringhe con solo 1 cifra ripetuta più di una volta)

### Esercizio 02-0312C

L’insieme delle parole di 0 e 1 tali che esistono due 0 separati da un numero di posizioni multiplo di 4 (0 è un multiplo di 4).

@import "immagini/0212C.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0313

Consideriamo l’alfabeto Σ = {a, b, c, d} e costruiamo un automa non deterministico che riconosce il linguaggio di tutte le parole tali che uno dei simboli dell’alfabeto non compare mai:

* tutte le parole che non contengono a
* +tutte le parole che non contengono b
* +tutte le parole che non contengono c
* +tutte le parole che non contengono d

@import "immagini/0213.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0323

Determinare il DFA equivalente all’NFA con la seguente tabella di transizione:

|| 0 | 1|
|-:|:-:|:-:|
|$\rightarrow q_0$|{$q_0$}|{$q_0$,$q_1$}|
|$q_1$|{$q_1$}|{$q_0$,$q_2$}|
|*$q_2$|{$q_1$,$q_2$}|{$q_0$,$q_1$,$q_2$}|

@import "immagini/0223.png"- [Raccolta esercizi](#raccolta-esercizi)

Qual è il linguaggio accettato dall’automa?

Tutte le stringhe che appartengono all'alfabeto (0,1) e che contengono almeno due 1.

### Esercizio 02-0324

Trasformare il seguente NFA in DFA.

@import "immagini/0224Consegna.png"- [Raccolta esercizi](#raccolta-esercizi)

@import "immagini/0224.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 02-0325

Determinare il linguaggio riconosciuto dall’automa.
Costruire un DFA equivalente.

@import "immagini/0225Consegna.png"- [Raccolta esercizi](#raccolta-esercizi)

Tutte le stringhe che terminano per 001 o 110.

@import "immagini/0225.png"- [Raccolta esercizi](#raccolta-esercizi)

## 04-epsilon

### Esercizio 0402

Convertire il seguente NFA in DFA:

|| 0 | 1|
|-:|:-:|:-:|
|$\rightarrow$A|{A,C}|{B}|
|*B|{C}|{B}|
|C|{B}|{D}|
|D|{$\emptyset$}|{$\emptyset$}|

@import "immagini/0402.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0404

Costruiamo un NFA che accetta numeri decimali:

* Un segno `+` o `−` (opzionale)
* Una stringa di cifre decimali {0, . . . , 9}
* Un punto decimale `.`
* Un’altra stringa di cifre decimali
* Una delle stringhe e può essere vuota, ma non entrambe

@import "immagini/0404.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0418

1. Costruiamo un ε-NFA che riconosce le parole costituite da:
   * zero o più a
   * seguite da zero o più b
   * seguite da zero o più c

   @import "immagini/0418.png"- [Raccolta esercizi](#raccolta-esercizi)

2. Calcolare ECLOSE di ogni stato dell’automa
   * ECLOSE(q0) = {q0, q1, q2}
   * ECLOSE(q1) = {q1, q2}
   * ECLOSE(q2) = {q2}
3. Convertire l’ε-NFA in DFA

Vedi esercizio E tutorato 01 [Link](#esercizio-tut01e)

## 05-regexp

### Esercizio 0512

Scriviamo l’espressione regolare per L = {w ∈ {0, 1}$^*$ : 0 e 1 alternati in w}.

(01)$^*$ + (10)$^*$ + 1(01)$^*$ + 0(10)$^*$

Oppure

($\varepsilon$ + 1)(01)$^*$($\varepsilon$ + 0)

### Esercizio 0514A

Costruire una ER sull’alfabeto {a, b, c} tale che tutte le stringhe w che contengono un numero pari di a;

(b+c)$^*$ (a(b+c)$^*$a(b+c)$^*$)$^*$

### Esercizio 0514B

Costruire una ER sull’alfabeto {a, b, c} tale che tutte le stringhe w che contengono 4k + 1 occorrenze di b, per ogni k ≥ 0.

(a+c)$^*$ (b(a+c)$^*$b(a+c)$^*$b(a+c)$^*$b(a+c)$^*$)$^*$

### Esercizio 0514C

Costruire una ER sull’alfabeto {a, b, c} tale che tutte le stringhe la cui lunghezza è un multiplo di 3.

((a+b+c)(a+b+c)(a+b+c))$^*$

### Esercizio 0515A

Costruire una ER sull’alfabeto {0, 1} tale che tutte le stringhe w che contengono la sottostringa 101.

(0+1)$^*$101(0+1)$^*$

### Esercizio 0515B

Costruire una ER sull’alfabeto {0, 1} tale che tutte le stringhe w che non contengono la sottostringa 101.

0$^*$(1+000$^*$)$^*$0$^*$

### Esercizio 0515C

Costruire una ER sull’alfabeto {0, 1} per il linguaggio di tutti i numeri binari multipli di 3.

0$^*$((1(01$^*$0)$^*$1)$^*$0$^*$)$^*$

### Esercizio 0520

Trasformare (0 + 1)$^*$1(0 + 1) in $\varepsilon$-NFA

@import "immagini/0520.png"- [Raccolta esercizi](#raccolta-esercizi)

## 06-esercizi-er

### Esercizio 0607A

Trasformiamo (0+1)$^*$1(0+1) in $\varepsilon$-NFA

@import "immagini/0607a.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0607B

Scrivere un’espressione regolare per rappresentare il linguaggio sull’alfabeto {a, b, c} che contiene tutte le stringhe che:
* iniziano con a e sono composte solo di a oppure b
* la stringa c

La prima condizione si potrebbe interpretare in 2 modi diversi.

1. a(a+b)$^*$+c
2. a(a*+b*)+c

### Esercizio 0607C

Trasformare l’espressione regolare dell’esercizio 2 in $\varepsilon$-NFA.

Primo caso:

@import "immagini/0607c1.png"- [Raccolta esercizi](#raccolta-esercizi)


Secondo caso:

@import "immagini/0607c2.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0608A

Scrivere una espressione regolare per tutte stringhe binarie che cominciano e finiscono per 1.

1(0+1)$^*$1+1

@import "immagini/0608a.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0608B

Scrivere una espressione regolare per le stringhe binarie che contengono almeno tre 1 consecutivi.

(0+1)$^*$ 111 (0+1)$^*$

### Esercizio 0608C

Scrivere una espressione regolare per le stringhe binarie che contengono almeno tre 1 (anche non consecutivi).

(0+1)$^*$ 1 (0+1)$^*$ 1 (0+1)$^*$ 1 (0+1)$^*$

### Esercizio 0608D

Scrivere una espressione regolare per stringhe di testo che descriva le date in formato GG/MM/AAAA.

(0+...+31)/(1+...+12)/(0+...+9)(0+...+9)(0+...+9)(0+...+9)

Ovviamente non controlla gli anni bisestili e nemmeno che ci siano 30 o 31 giorni in un determinato mese.

## 07-dfa2re

### Esercizio 0707A

Costruiamo l’espressione regolare equivalente al seguente NFA:

@import "immagini/0707AConsegna.png"- [Raccolta esercizi](#raccolta-esercizi)

Eliminando gli stati $q_1$ e $q_2$:
@import "immagini/0707A1.png"- [Raccolta esercizi](#raccolta-esercizi)
Eliminando gli stati $q_1$ e $q_3$:
@import "immagini/0707A2.png"- [Raccolta esercizi](#raccolta-esercizi)

Sommando le 2 espressioni precedenti si ottiene la ER cercata:
((0+1)$^*$1(0+1)(0+1))+(0+1($^*$1(0+1))
### Esercizio 0707B

Costruiamo l’espressione regolare equivalente al seguente NFA:

@import "immagini/0707BConsegna.png"- [Raccolta esercizi](#raccolta-esercizi)

@import "immagini/0707B.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 0708

Costruiamo l’espressione regolare equivalente al seguente NFA:

@import "immagini/0708Consegna.png"- [Raccolta esercizi](#raccolta-esercizi)

(1+0(10$^*$1+0)(1(10$^*$1+0))$^*$0)$^*$

## 08-pumpinglemma

### Esercizio 0811

Sia $L_{ab}$ il linguaggio delle stringhe sull’alfabeto {a, b} con un numero di b maggiore del numero di a. $L_{ab}$ è regolare?

No, $L_{ab}$ non è regolare:
* supponiamo per assurdo che lo sia
* sia $n$ la lunghezza data dal Pumping Lemma
* consideriamo la parola $w = a^nb^{n+1}$
* prendiamo un qualsiasi split $w = xyz$ tale che $y \ne \varepsilon$ e $\mid xy \mid ≤ n$:

   $w =
\underbrace{aa...}_{x}
\underbrace{...aa}_{y}
\underbrace{abbbbb}_{z}$

* per il Pumping lemma, anche $xy^2z$ ∈ Lab, ma contiene più a che b ⇒ **assurdo**.

### Esercizio 0812

Il linguaggio $L_{rev}$ = {$ww_R$ : w ∈ {a, b}$^*$} è regolare?

No, $L_{rev}$ non è regolare:
* supponiamo per assurdo che lo sia
* sia $n$ la lunghezza data dal Pumping Lemma
* consideriamo la parola $w = a^nbba^n$
* prendiamo un qualsiasi split $w = xyz$ tale che $y \ne \varepsilon$ e $\mid xy \mid ≤ n$:

   $w =
\underbrace{aa...}_{x}
\underbrace{...aa}_{y}
\underbrace{abbaaa..aa}_{z}$

* per il Pumping lemma, anche $xy^0z = xz ∈ L_{rev}$, ma non la posso spezzare in $ww^R$ ⇒ **assurdo**.

### Esercizio 0813

Il linguaggio $L_{nk}$ = {$a^nb^k : n$ è dispari oppure k è pari} è regolare?

Sì, $L_{nk}$ è regolare:
* è rappresentato dall’espressione regolare a(aa)$^*$b$^*$ + a$^*$(bb)$^*$
* e riconosciuto dall'automa

@import "immagini/0813.png"- [Raccolta esercizi](#raccolta-esercizi)

## Credits

* [JFLAP](http://www.jflap.org/ "Jflap official site")
* [MPE](https://shd101wyy.github.io/markdown-preview-enhanced/#/ "Markdown Preview Enhanced")
* [Link Repository](https://github.com/Archetipo95/Automi_Jflap) per contribuire o segnalare errori