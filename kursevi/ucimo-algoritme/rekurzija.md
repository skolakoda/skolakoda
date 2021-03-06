---
title: Šta je rekurzija?
layout: lekcija-algoritmi
author: damjan
permalink: /rekurzija
image: https://upload.wikimedia.org/wikipedia/commons/3/30/Cuncha_GFDL_Galicia4.jpg
---

![]({{page.image}})

***Rekurzija je zanimljiva pojava u prirodi, koja ima osobinu beskonačnog ponavljanja. Počela je da me privlači nakon što sam je otkrio u kodu.***

Rekurzija je beskonačno skalirajuće ponavljanje istog obrasca (rastuće ili smanjujuće). Ako se obrazac samoreprodukuje, kao što je slučaj u računarskim programima, onda je rekurzija beskonačno skalirano ponavljanje sebe.

## Beskonačnost rekurzije

Ideja rekurzije je uvek beskonačna, a ograničavaju je isključivo spoljnji faktori. Na primer, puževa kućica je rekurzija koja se neprestano ponavlja, ograničena isključivo smrću puža. Bez ometajućih faktora, rekurzija je beskonačna, kao u slučaju međusobno ogledajućih ogledala, gde se isti obrazac ponavlja doslovno u beskonačnost.

![](//68.media.tumblr.com/59f43c03ca0e9ede45b8b71f79b44268/tumblr_inline_ntx0langcg1r1aqjj_1280.jpg)

## Rekurzija u prirodi

Rekurzija u prirodi je uočljiva u rastućem ponavljanju spiralnih obrazaca, kod školjki i raznih vrsta biljaka. Trajanje biljnih i životinjskih rekurzija je u konačnici ograničeno trajanjem života domaćina.

![](//spacecollective.org/userdata/zdP3mVy7/_cimg/1197601200.jpg)

![](https://upload.wikimedia.org/wikipedia/commons/c/c4/Aloe_polyphylla_spiral.jpg)

![](https://s-media-cache-ak0.pinimg.com/564x/88/86/e1/8886e11fcba6c5be0801609f397e4068.jpg)

## Ljudske rekurzije

Često se neke ljudske tvorevine, kao ruske matruške ili spiralne građevine, navode kao primer rekurzije. Ljudske rekurzije su uvek konačne, ograničene ne samo dužinom života, već veličinom nakon koje je dalja obrada nemoguća.

![](https://qph.ec.quoracdn.net/main-qimg-4742a03d87ef68cbb642d6798f588a66-c)

## Rekurzija u programiranju

U programiranju, rekurzija je funkcija koja poziva samu sebe, sa uvećanom ili umanjenjenom vrednošću.

![](https://upload.wikimedia.org/wikipedia/commons/8/8a/RecursiveFunction1_execution.png)

Rekurzija u kodu je, inicijalno, beskonačna. Prekida se tek prestankom rada računara, ili kočnicom (uslovom) koju postavimo. Bez kočnice, beskonačna rekurzija će veoma brzo pojesti resurse i blokirati računar. Kada sliku beskonačnog ogledanja, koja postoji u stvarnosti, pokušamo reprodukovati na računaru, dolazi do momentalnog pada sistema (autor isprobao).

Da bi rekurzija radila na računaru, moramo je ograničiti.
