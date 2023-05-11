---
date: "2023-05-11"
highlight: true
tags:
- swirl
title: Tutorial Swirl
type: book
weight: 30
---

Installare e aggiornare i tutorial Swirl

<!--more-->

{{< icon name="clock" pack="fas" >}} 15 minuti

## Introduzione

Per un apprendimento graduale delle basi del linguaggio abbiamo adottato [Swirl](https://swirlstats.com/) come piattaforma per praticare R in modo interattivo, direttamente all'interno della console R.

## Installare il pacchetto Swirl

I pacchetti possono essere installati dall'interfaccia di RStudio nella scheda 'Packages' in basso a destra.<br> In alternativa è possibile installare da riga di comando con il comando `install.packages()`.<br> Il codice seguente, che può essere eseguito direttamente nella console di R, installa il pacchetto solamente se non è già disponibile:<br>

``` r
if(!require(swirl)){
  install.packages("swirl")
}
```

## Installare il corso base Swirl

Abbiamo tradotto e adattato (semplificando alcuni argomenti e aggiungendone altri) il corso [R programming](https://github.com/swirldev/R_Programming_E), disponibile come repository GitHub [R base course in Italian](https://github.com/uvesco/R-base-course-in-Italian/).<br> Il corso può essere installato con il seguente codice:

``` r
library(swirl)
install_course_github("uvesco", "R-base-course-in-Italian")
```

## Aggiornare il corso base Swirl

Per aggiornare il corso all'ultima versione presente su [GitHub](https://github.com/uvesco/R-base-course-in-Italian/) si può eseguire il seguente codice:

``` r
# carica il pacchetto swirl dal repository CRAN
library(swirl)
# disinstalla il corso se già installato
uninstall_course("R-base-course-in-Italian")
# installa l'ultima versione del corso dal repository personale di U Vesco
install_course_github("uvesco", "R-base-course-in-Italian")
```

E' prevista l'aggiunta di nuovi contenuti al corso e la correzione di bugs.

## Segnalare bugs

Il modo migliore per segnalare bugs al codice è aprire una issue direttamente sull'[apposita pagina](https://github.com/uvesco/R-base-course-in-Italian/issues) del repository Github. Tutte le lezioni e le domande sono state numerate per consentire di specificare dove si presenta l'errore o il testo non risulta comprensibile.
