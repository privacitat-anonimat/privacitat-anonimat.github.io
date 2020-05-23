---
title: Sistemes Operatius
author: privacitat-anonimat
date: 2020-05-23
categories: [Conceptes,Bàsics]
tags: [Windows,Linux,MacOS,Whonix,Tails,QubesOS,virtualització]
---

Els sistemes operatius són programes que permeten a l'usuari interactuar de manera gràfica amb l'ordinador. Tots els programes que executem, com el navegador, els documents, inclús el que teclegem, els gestiona el sistema operatiu.

És per això, que el sistema operatiu té un gran pes quan parlem de privacitat i seguretat, ja que és el que té el control absolut sobre què passa a l'ordinador.

# Sistemes operatius genèrics
Actualment, el mercat està dominat pel sistema operatiu Windows, desenvolupat per Microsoft, principalment per la facilitat que dóna a l'usuari en utilitzar-lo.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/marketshare2.png)

Aquests són els percentatges segons la font consultada:
* Windows: 76.52%
* OS X: 18.99%
* Linux: 1.61%
* Chrome OS: 1.12%
* Altres: 1.76%

## Windows
És el sistema operatiu amb més quota de mercat. És mundialment utilitzat gràcies a l'esforç que ha realitzat Microsoft en dissenyar un sistema que és molt fàcil d'utilitzar, inclús per persones sense coneixements informàtics.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/windows2.jpg)

Malauradament, com que moltíssima gent l'utilitza, és el sistema operatiu preferit pels criminals. Això implica que existeixen una gran quantitat d'atacs dirigits (programari maliciós) contra usuaris de Windows. És per això que recomanem utilitzar un antivirus, sigui el Windows Defender o un de pagament.

En termes de privacitat, el sistema és de programari privatiu. És a dir, el codi font és privat i no sabem ven bé que fa el Windows per darrere. Alguns investigadors han demostrat que el Windows envia moltíssima informació sobre l'usuari a Microsoft, inclòs on clica l'usuari o quines tecles prem.

És per això, que Windows és el sistema opratiu menys recomanat en termes de privacitat i seguretat.

## Mac OS
És el segon sistema operatiu més utilitzat, tot i que amb bastant diferència respecte a Windows. Apple també s'ha centrat en la usabilitat i el disseny, però a diferència de Microsoft, la seva estratègia de màrqueting és vendre que és un producte exclusiu. D'aquí l'elevat preu dels seus productes.

Com a punt positiu de l'exclusivitat, tots els programes i hardware estan dissenyats exclusivament per aquest sistema operatiu. Això millora moltíssim el rendiment de l'ordinador i els dispositius, pel que l'usuari pot utilitzar un ordinador Apple amb menys potencia que un de Windows, però que li funcioni més de pressa.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/osx.png)

En tenir menys quota de mercat i l'alt cost dels seus productes, no hi ha tants virus com a Windows. No obstant això, es veu que hi ha un petit increment constant tant de popularitat com de virus desenvolupats per atacar-lo.

Mac OS utilitza el kernel de Linux, però aclarir que això no implica que sigui programari lliure. De fet, excepte el kernel, tot és privatiu. Igual que Windows, els usuaris i investigadors no tenim accés al codi font i per tant, és possible que el sistema operatiu enviï informació sobre l'usuari a Apple.

Tampoc és gaire recomenat si et preocupa la privacitat.

## Linux
És un sistema operatiu que té molt poca quota de mercat perquè, antigament, els usuaris havien de tenir coneixements elevats d'informàtica per utilitzar-lo.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/linux2.png)

Linux és de programari lliure i ha estat desenvolupat per empreses o persones sense ànim de lucre. Per tant, podem estar segurs que, no envia informació de l'usuari a cap empresa. A més a més, és completament gratuït i no té gaires virus ja que és poc utilitzat.

### Distribucions
El millor de què sigui programari lliure és que al llarg dels anys, empreses i particulars, han agafat el codi font i li han fet modificacions per aconseguir un sistema operatiu personalitzat.

Aquestes modificacions s'han traduït en diverses versions de Linux, anomenades distribucions. Són essencialment un Linux però amb diferències d'aspecte o algunes funcionalitats o programes instal·lats per defecte.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/linux1.png)

Tot i que en general és un sistema operatiu una mica més complicat d'utilitzar, existeixen distribucions com Ubuntu que estan dissenyades per a persones que no han utilitzat abans un Linux, ja que és molt semblant al Windows.

Alguns exemples:
* **Distribucions estables**
	* [Debian](https://www.debian.org/index.es.html)
	* [Fedora](https://getfedora.org/)
	* [ArchLinux](https://www.archlinux.org/)
* **Recomenat a usuaris novells**
	* [Ubuntu](https://ubuntu.com/)
	* [Linux Mint](https://www.linuxmint.com/)

# Sistemes operatius específics
A continuació, mostrem alguns sistemes operatius que estan dissenyats per obtenir un alt nivell de seguretat, privacitat i anonimat. Tots ells, com no podia ser de cap altra manera, estan basats en Linux i per tant, són de programari lliure.

## Whonix
És una distribució basada en Linux, específicament en Debian, que té com a objectiu proporcionar privacitat, seguretat i anonimat.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/whonix.png)

Aquest sistema operatiu és una mica diferent al que estem acostumats, ja que combina tecnologies com la virtualització, Tor i l'aïllament de les aplicacions.

Whonix està dividit en dues màquines. Per una banda, hi ha la "Workstation", el sistema que utilitza l'usuari per treballar y per l'altra banda el "Gateway", una màquina que únicament té la funció de fer de porta d'enllaç entre la "Workstation" i Internet.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/whonix2.jpeg)

Aquesta estructura assegura a l'usuari que qualsevol programa executat dins de la "Workstation" utilitzarà Tor. A més a més, si algun atacant intenta atacar a l'usuari, la màquina "Gateway" farà de bloqueig i no aconseguirà arribar a la "Workstation", ja que estan aïllades gràcies a la virtualització i a les configuracions de seguretat de Whonix.

És un sistema operatiu que recomanem molt i us animem que el provis. No obstant això, en aquest cas si que es necessiten alguns coneixements d'informàtica per instal·lar el programa de virtualització, com [Virtualbox](https://www.virtualbox.org/), i configurar el Whonix.

**Nota**: si l'instal·les, recorda obrir primer la "Gateway" i després la "Workstation", ja que sinó no tindràs connexió a Internet.

## Tails
És una distribució basada en Línux, específicament en Debian, però que té una particularitat respecte al que entenem com a sistema operatiu. Permet a l'usuari utilitzar-lo sense necessitat d'instal·lar-lo a l'ordinador.

És a dir, pots convertir el teu ordinador en una màquina segura sense necessitat d'eliminar ni instal·lar res al disc dur.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/tails.png)

Per utilitzar-lo, només és necessari instal·lar-lo a un USB. El procés d'instal·lació dura aproximadament 30 minuts i a la [pàgina oficial]((https://tails.boum.org/install/index.es.html)) està molt ben explicat. No es necessiten gaires coneixements per poder-ho fer.

Un cop instal·lat, només cal que, a l'engegar l'ordinador, indicar-li que s'inici des de l'USB en lloc del disc dur.

Tails té les següents característiques:
* **Amnesia**: sempre començarà al mateix estat. És a dir, tot el que facis a Tails, desapareixerà en el moment que el desconnectis de l'ordinador. No es guarda res a l'USB, a no ser que ho especifiquis, així que no queda rastre.
* **[Volum Persistent Xifrat](https://tails.boum.org/doc/first_steps/persistence/index.es.html)**: dóna l'opció de crear una partició xifrada perquè puguis emmagatzemar documents dins del USB.
* **[Programes instal·lats](https://tails.boum.org/doc/about/features/index.es.html)**: Tails ja té instal·lat alguns programes que et permeten treballar i comunicar-te de manera segura.
* **No deixar rastre a Internet**: Tails està configurat per utilitzar sempre Tor. D'aquesta manera, utilitzis l'aplicació que utilitzis, sempre navegaràs a través de Tor. És a dir, la connexió estarà xifrada i serà anònima.

Per tant, Tails és una gran opció a tenir en compte. Sempre recomanem que tinguis a casa un USB amb Tails per si algun dia has de treballar, al teu ordinador o al d'algú altre, en quelcom sensible i no tinguis un sistema segur preparat.

**Nota**: a l'estar instal·lat a un USB, és complex instal·lar més programes dels que venen per defecte. Es pot fer però no és recomanable, ja que els programes instal·lats no hauran estat configurats i supervisats per Tails.

## Qubes OS
És una distribució basada en Linux, específicament en Xen i Fedora. És un sistema operatiu centrat en la seguretat a través de l'aïllament de les aplicacions. A diferència de Whonix, Qubes OS virtualitza a nivell de hardware.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/qubesos.png)

És a dir, Qubes OS virtualitzarà cada una de les aplicacions que utilitzi l'usuari. Això permet incrementar moltíssim la seguretat, ja que cada aplicació estarà aïllada de la resta.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-23-sistemes_operatius/qubesos2.png)

Per exemple, pots obrir dos navegadors a la vegada. En un entrar al correu de la feina i a l'altra buscar coses per comprar. Ni l'empresa del correu electrònic ni el de la botiga sabran que estàs connectat a la vegada (normalment, les pàgines web poden saber a quines altres pàgines es connecta l'usuari des d'un mateix navegador). A més a més, si tinguéssis la mala sort d'infectar-te amb un virus mentre esttàs comprant, la virtualització evitarà que el virus s'estengui a l'ordinador i a les altres aplicacions que tinguis obertes. Per tant, només afectarà el navegador que estiguis utilitzant per comprar.

Qubes OS també permet personalitzar el sistema operatiu. És a dir, podries utilitzar el sistema de seguretat de Qubes OS i fusionar-lo amb Whonix, aconseguin així també privacitat i anonimat.

Aquest és un sistema operatiu espectacular. No obstant això, cal remarcar que es necessiten uns coneixements d'informàtica una mica avançats i que no es pot instal·lar a tots els ordinadors, ja que té una gran [dependència del hardware](https://www.qubes-os.org/hcl/). A més a més, a causa de la virtualització és possible que el rendiment sigui inferior.

# Conclusions
Escollir el sistema operatiu és una decisió complexa, sobretot si estàs preocupada per la teva privacitat. La nostra recomenació és que utilitzis un Linux, independenment de la distribució. Ja veuràs que no és tant complicat d'utilitzar.


# Referències
* **Distribucions Linux**: [enllaç](https://www.genbeta.com/linux/31-distribuciones-linux-para-elegir-bien-que-necesitas-1)
* **Whonix**: [enllaç](https://www.whonix.org/)
* **Virtualització**: [Virtualbox](https://www.virtualbox.org/)
* **Virtualització**: [VMWare](https://www.vmware.com/)
* **Tails**: [enllaç](https://tails.boum.org/)
* **Qubes OS**: [enllaç](https://www.qubes-os.org/)