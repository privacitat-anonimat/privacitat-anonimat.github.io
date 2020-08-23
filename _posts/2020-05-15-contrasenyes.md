---
title: Contrasenyes
author: privacitat-anonimat
date: 2020-05-15
categories: [Conceptes,Bàsics]
tags: [contrasenya]
---

Les persones són l'esglaó més dèbil en qualsevol sistema de seguretat i per extensió, les contrasenyes que escullen. La gran majoria mètodes amb els que es roben comptes de xarxes socials o fotografies personals, s'aconsegueixen mitjançant una sèrie d'atacs, que comentarem després, que només funcionen si la contrasenya és dèbil.

Per aquest motiu, és completament necessari i imprescindible que qualsevol persona que es preocupi per la seva privacitat sàpiga crear i utilitzi contrasenyes fortes.

# Paraula vs Frases
Un debat que sempre hi ha hagut és el de si és millor utiltizar una paraula supercomplexa o una frase fàcil de recordar. A continuació mostrem un còmic de XKCD que en fa una comparació:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-15-contrasenyes/comic.png)

Bàsicament s'ha d'aconseguir buscar una balança entre seguretat i usabilitat. És a dir, una contrasenya de 8 caràcters és molt fàcil d'esbrinar. Si es vol complicar i afegir números en lloc de vocals o signes de puntuació, és molt probable que l'usuari se n'oblidi.

En canvi, pensem una frase fàcil de recordar per nosaltres, el fet que tingui tants dígits ja incrementa molt la complexitat. Per tant, ja no seria necessari afegir tants signes de puntuació i números intercalats.

Per tant, recomanem utilitzar frases en lloc de contrasenyes tenint en compte el següent:
* Quatre paraules és suficient, però millor si en són cinc.
* No utilitzar paraules que siguin comunes i, per descomptat, no utilitzar frases fetes o frases conegudes que han sortit a pel·lícules, per exemple. Les paraules de la frase haurien de ser el màxim d'aleatòries possible.
* Utilitzar una frase diferent per cada compte. Així, si comprometen algun compte, no podran accedir a tots els comptes.

**Nota**: aprofitar per indicar que molts dels atacs per esbrinar contrasenyes, tenen contemplades els intercanvis de vocals per números. Per exemple, o per 0, a per 4, e per 3, etc. Això implica que el fet de canviar aquests caràcters no té un increment gaire elevat de complexitat.

# Atacs
La millor manera de saber com defensar-se és saber com ho fan els atacants per aconseguir robar contrasenyes. És per això, que a continuació posem un exemple d'un parell d'atacs.

Per un atacant hi ha dues maneres d'obtenir les contrasenyes dels usuaris. La primera és atacar el panell d'inici de sessió de la pàgina objectiu, però hi ha el problema que normalment aquests panells estan ben protegits amb controls per evitar aquests tipus d'atacs.

La segona manera, segur que n'has sentit a parlar, quan per les notícies expliquen que uns hackers han robat milions d'usuaris d'una pàgina web. El que fan és trobar un conjunt de vulnerabilitats que els hi permeten obtenir la base de dades. Si la pàgina té unes mesures de seguretat acceptables, no emmagatzemarà les contrasenyes dels usuaris en clar, sinó que només guardarà el seu [HASH](https://ca.wikipedia.org/wiki/Funci%C3%B3_hash). Per tant, els hackers no obtenen directament les contrasenyes.

No obstant això, com que ara ja no han d'atacar al servidor sinó que ho tenen tot en els seus ordinadors, poden llençar els atacs que expliquem a continuació sense que els controls de la pàgina web els molestin i amb més potencia de computació.

Per tant, si algun dia llegeixes que han robat usuaris d'una pàgina en el que en teniu un, és molt recomanable que canviïs la contrasenya, ja que tard o d'hora l'obtindran.

## Forca Bruta
Consisteix a provar totes les combinacions possibles donada una certa llargada. Per exemple, si fos una contrasenya de 4 caràcters, es provaria "aaaa", "aaab", "aaac", ..., "zzzz". Aquests atacs són lents però t'assegures de provar totes les combinacions possibles, així que si aconsegueixes acabar-lo tens un 100% de probabilitats de trobar la contrasenya.

Pels exemples següents es faran les següents suposicions:
* S'utilitzarà l'alfabet espanyol de 27 dígits
* Números del 0 al 9
* Signes de puntuació en seran 10
* Velocitat calculada és una aproximació. 

Quant de temps tardaria un atacant en endevinar-les:
* Contrasenya: **abcdefg**
	* Complexitat: 7 dígits només minúscules
	* Combinacions: 27 lletres
	* Temps en trencar-la: 0.29 mil·lisegons
* Contrasenya: **abcdefgh**
	* Complexitat: 8 dígits només minúscules
	* Combinacions: 27 lletres
	* Temps en trencar-la: 3 hores i 24 minuts
* Contrasenya: **abcdefg1**
	* Complexitat: 8 dígits alfanumèrics
	* Combinacions: 27 lletres + 10 números
	* Temps en trencar-la: 2 dies i 21 hores
* Contrasenya: **Abcdefgh**
	* Complexitat: 8 dígits amb majúscules i minúscules
	* Combinacions: 27 lletres minúscules + 27 lletres majúscules
	* Temps en trencar-la: 1 mes i 6 dies
* Contrasenya: **Abcdefg1**
	* Complexitat: 8 dígits alfanumèrics amb majúscules i minúscules
	* Combinacions: 27 lletres minúscules + 27 lletres majúscules + 10 números
	* Temps en trencar-la: 7 mesos i 1 setmana
* Contrasenya: **Abcdef1!**
	* Complexitat: 8 dígits alfanumèrics amb majúscules, minúscules i signes de puntuació
	* Combinacions: 27 lletres minúscules + 27 lletres majúscules + 10 números + 10 signes de puntuació
	* Temps en trencar-la: 9 anys i 6 mesos

Com pots comprovar, el fet d'afegir complexitat o tenir més longitud pot tenir un increment molt gran en el temps que un atacant tardaria a aconseguir-la. El teu objectiu ha de ser trobar aquest equilibri entre seguretat i usabilitat per fer una contrasenya el màxim de segura possible.

## Diccionari
Segur que has pensat que llavors la contrasenya "Casa1234!" és super segura perquè ho té tot i és llarga. Em sap greu decebre't, però no tot podia ser tan fàcil.

De la mateixa manera que el mètode anterior provava totes les combinacions possibles, hi ha un altre tipus d'atac que utilitza un diccionari. És a dir, donat un document amb paraules ja definides, les prova totes i a més a més, les combina. D'aquesta manera, es poden fer atacs molt més dirigits i encertar la contrasenya invertint menys temps que provant totes les combinacions.

Normalment, els atacants creen diccionaris personalitzats que contenen les següents paraules (per descomptat en l'idioma de l'objectiu):
* TOP contrasenyes més utilitzades
* Noms de familiars
* Noms de mascotes
* Dates importants
* Perfils de xarxes socials

Per fer l'atac més complet, existeixen programes que a part de combinar les paraules del diccionari, utilitzen regles per fer modificacions que normalment fan els usuaris quan volen incrementar la complexitat de les seves contrasenyes:
* Canviar números per lletres: canviar les e per 3, les a per 4...
* Afegir exclamacions al final
* Afegir punts entre paraules
* Posar la primera lletra de la frase o de cada paraula en majúscula

Els atacs de diccionari no tenen un 100% de fiabilitat però es poden dur a terme en un període de temps assequible si es realitza una investigació prèvia de la víctima.

# Gestor de contrasenyes
Un gran problema que tenen els usuaris que es preocupen per la seguretat i segueixen les recomanacions és que s'han de recordar de moltes contrasenyes llargues i complexes.

Se saben alguns casos on hackers han aconseguit entrar a una empresa i robar dades confidencials perquè algun treballador apuntava les seves contrasenyes en un post-it o en un fitxer al seu escriptori anomenat "contrasenyes.txt".

És per això, que recomanem molt fortament l'ús d'un gestor de contrasenyes per emmagatzemar-les de manera segura. Bàsicament, és un programa que permet distribuir amb carpetes i posar descripcions a les contrasenyes. A més a més, la base de dades on es guarden està xifrada, cosa que fa que sigui molt complicat obtenir les contrasenyes en clar si la contrasenya que s'ha escollit per xifrar la base de dades és segura.

Alguns gestors de contrasenyes recomanats:
* Bitwarden
* KeePass
* LastPass
* 1Password

El nostre preferit és KeePass, ja que és de programari lliure i sense connexió a Internet, així no cal que ens preocupem de si algú compromet els servidors de l'empresa del gestor de contrasenyes. No obstant això, si teniu la necessitat d'accedir a les contrasenyes des de qualsevol dispositiu a qualsevol hora, haureu de mirar un que les emmagatzemi a Internet.

# Com crear una contrasenya forta
La contrasenya més segura que podràs generar és les que generen els gestors de contrasenyes automàticament, ja que són llargues, aleatòries i complexes. El problema és que et serà impossible recordar-les, així que només les pots utilitzar quan tingueu accés al gestor.

Si el que vols és recordar-la, us recomanem utilitzar una frase i afegir-hi complexitat. Has de tenir present els atacs que hem explicat per evitar que la frase contingui paraules típiques o que es puguin deduir investigant les vostres xarxes socials. Per exemple, el nom del gos.

# Conclusions
Un dels principis de ProtonMail diu

> Security at the expense of usability comes at the expense of security.

És a dir, que si s'incrementa moltíssim el nivell de seguretat, fa que sigui tan complicat de gestionar pels usuaris que al final s'acaba tenint un nivell de seguretat més baix del que s'hagués obtingut sense incrementar tant el nivell.

Amb les contrasenyes passa exactament el mateix. És per això que s'ha de trobar un equilibri entre seguretat i usabilitat.

Recomanacions:
1. Més de 8 caràcters, utilitzar frases per recordar les contrasenyes més fàcilment
2. Alfanumèrica: lletres i números (o símbols)
3. Majúscules i minúscules
4. No repetir contrasenyes
5. Canviar contrasenyes freqüentment o si han compromès la pàgina on tens un usuari
6. Guardar-les a un gestor de contrasenyes

# Referències
* **Còmic XKCD**: [enllaç](https://xkcd.com/936/)
* **Discusió XKCD**: [enllaç](https://www.explainxkcd.com/wiki/index.php/936:_Password_Strength)
* **ProtonMail - Let's settle the password vs. passphrase debate once and for all**: [enllaç](https://protonmail.com/blog/protonmail-com-blog-password-vs-passphrase/)
* **ProtonMail - How long should your password be?**: [enllaç](https://protonmail.com/blog/how-long-should-my-password-be/)
* **ProtonMail - 3 safety tips to create a strong password**: [enllaç](https://protonmail.com/blog/how-to-create-a-strong-password/)
* **Estimació complexitat contrasenya**: [enllaç](https://www.betterbuys.com/estimating-password-cracking-times/)
* **Surveillance Self-Defense - Creando contraseñas seguras**: [enllaç](https://ssd.eff.org/es/module/creando-contrase%C3%B1as-seguras)