---
layout: default
title: "O projektu"
permalink: /about/
---

<h1 class="page__title">O projektu</h1>

<div class="page__body">

**Na današnji dan** je dnevni eksperiment v branju zgodovine.

Vsako jutro sistem pregleda današnje glavne novice (preko portala
[napovej.com](https://napovej.com)) in poišče tematsko sorodne članke iz
slovenskih zgodovinskih časopisov med leti **1771 in 1914**.

Izberemo enega — tistega, ki najbolj rezonira s sodobnim kontekstom — in
ga objavimo. Slogan: *Ne beri trenutnih novic. Vse se je že zgodilo.*

## Vir podatkov

Zgodovinski članki izhajajo iz korpusa
[**sPeriodika 1.0**](http://hdl.handle.net/11356/1881),
ki so ga pripravili Filip Dobranić, Bojan Evkoski in Nikola Ljubešić
(Inštitut za novejšo zgodovino, 2024).

Korpus vsebuje **149.000 dokumentov** iz **216 časopisov**, OCR-anih in
jezikovno anotiranih, in je objavljen pod licenco CC&nbsp;BY-SA&nbsp;4.0.

Naš izpeljani projekt podeduje to licenco.

## Kako deluje

1. **Današnje novice** se preberejo iz aktualnega feeda (filtri: politika,
   gospodarstvo, kultura, svet — črna kronika izpuščena).
2. **Hibridni iskalnik** poišče zgodovinske članke s podobnimi ključnimi
   besedami (PostgreSQL FTS) in podobnim semantičnim pomenom (embeddings
   `multilingual-e5-base`).
3. **Kurator** izbere en članek z najvišjim ujemanjem.
4. **Stran** zgenerira statični HTML in objavi.

Celotna koda je odprta:
[nadanasnjidan](https://github.com/davorinpavlica/nadanasnjidan).

## Kontakt

[nadanasnjidan@zvpl.com](mailto:nadanasnjidan@zvpl.com)

</div>
