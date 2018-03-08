# Automi e Linguaggi formali 17/18 {ignore=true}

NON GARANTISCO LA CORRETTEZZA DEGLI ESERCIZI
(prima bozza della pagina per il momento accetto solo suggerimenti per eventuali correzioni più avanti permetterò le pull request a chi vuole contribuire)

## Raccolta esercizi {ignore=true}

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

* [01-intro-dfa](#01-intro-dfa)
	* [Esercizio 22](#esercizio-22)
	* [Esercizio 23A](#esercizio-23a)
	* [Esercizio 23B](#esercizio-23b)
	* [Esercizio 23C](#esercizio-23c)
	* [Esercizio 23D](#esercizio-23d)
	* [Esercizio 24](#esercizio-24)
* [02-nfa](#02-nfa)
	* [Esercizio 05E](#esercizio-05e)
	* [Eercizio 07](#eercizio-07)
	* [Esercizio 12A](#esercizio-12a)
	* [Esercizio 12B](#esercizio-12b)
	* [Esercizio 12C](#esercizio-12c)
	* [Esercizio 13](#esercizio-13)
	* [Esercizio 23](#esercizio-23)
	* [Esercizio 24](#esercizio-24-1)
	* [Esercizio 25](#esercizio-25)
* [03-epsilon](#03-epsilon)
	* [Esercizio 04](#esercizio-04)

<!-- /code_chunk_output -->

Il nome di ogni esercizio è dato dal numero della pagina della slide in cui si trova e da una lettera se presenti più esercizi nella medesima pagina.

## 01-intro-dfa

### Esercizio 22

Automa che accetta il linguaggio delle stringhe con 01 come sottostringa.

@import "immagini/0122.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 23A

Insieme di tutte e sole le stringhe con un numero pari di 0 e un numero pari di 1.

@import "immagini/0123A.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 23B

Insieme di tutte le stringhe che finiscono con 00.

@import "immagini/0123B.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 23C

Insieme di tutte le stringhe che contengono esattamente tre zeri (anche non consecutivi).

@import "immagini/0123C.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 23D

Insieme delle stringhe che cominciano o finiscono (o entrambe le cose) con 01.

@import "immagini/0123D.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 24

Modellare il comportamento di un distributore di bibite con un DFA. Il modello deve rispettare le seguenti specifiche:

* Costo della bibita: 40 centesimi
* Monete utilizzabili: 10 centesimi, 20 centesimi
* Appena le monete inserite raggiungono o superano il costo della bibita, il distributore emette una lattina
* Il distributore dà il resto (se serve) subito dopo aver emesso la lattina

@import "immagini/0124.png"- [Raccolta esercizi](#raccolta-esercizi)

## 02-nfa

### Esercizio 05E

Insieme di tutte le stringhe che finiscono con 01.

@import "immagini/0205E.png"- [Raccolta esercizi](#raccolta-esercizi)

### Eercizio 07

Riconosce le parole che terminano con 01 “scommettendo” se sta leggendo gli ultimi due simboli oppure no

@import "immagini/0207.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 12A

L’insieme delle parole sull’alfabeto {0, 1, . . . , 9} tali che la cifra finale sia comparsa in precedenza.

@import "immagini/0212A.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 12B

L’insieme delle parole sull’alfabeto {0, 1, . . . , 9} tali che la cifra finale non sia comparsa in precedenza.

@import "immagini/0212B.png"- [Raccolta esercizi](#raccolta-esercizi)
(Non vale per stringhe con solo 1 cifra ripetuta più di una volta)

### Esercizio 12C

L’insieme delle parole di 0 e 1 tali che esistono due 0 separati da un numero di posizioni multiplo di 4 (0 è un multiplo di 4).

@import "immagini/0212C.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 13

Consideriamo l’alfabeto Σ = {a, b, c, d} e costruiamo un automa non deterministico che riconosce il linguaggio di tutte le parole tali che uno dei simboli dell’alfabeto non compare mai:

* tutte le parole che non contengono a
* +tutte le parole che non contengono b
* +tutte le parole che non contengono c
* +tutte le parole che non contengono d

@import "immagini/0213.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 23

Determinare il DFA equivalente all’NFA con la seguente tabella di transizione:

|| 0 | 1|
|-|-|-|
|$\rightarrow q_0$|{$q_0$}|{$q_0$,$q_1$}|
|$q_1$|{$q_1$}|{$q_0$,$q_2$}|
|*$q_2$|{$q_1$,$q_2$}|{$q_0$,$q_1$,$q_2$}|

@import "immagini/0223.png"- [Raccolta esercizi](#raccolta-esercizi)

Qual è il linguaggio accettato dall’automa?

### Esercizio 24

Trasformare il seguente NFA in DFA.

@import "immagini/0224Consegna.png"- [Raccolta esercizi](#raccolta-esercizi)

@import "immagini/0224.png"- [Raccolta esercizi](#raccolta-esercizi)

### Esercizio 25

Determinare il linguaggio riconosciuto dall’automa.
Costruire un DFA equivalente.

@import "immagini/0225Consegna.png"- [Raccolta esercizi](#raccolta-esercizi)

@import "immagini/0225.png"- [Raccolta esercizi](#raccolta-esercizi)

## 03-epsilon

### Esercizio 04

Costruiamo un NFA che accetta numeri decimali:

* Un segno `+` o `−` (opzionale)
* Una stringa di cifre decimali {0, . . . , 9}
* Un punto decimale `.`
* Un’altra stringa di cifre decimali
* Una delle stringhe e può essere vuota, ma non entrambe

@import "immagini/0304.png"- [Raccolta esercizi](#raccolta-esercizi)