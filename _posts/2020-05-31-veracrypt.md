---
title: VeraCrypt
author: privacitat-anonimat
date: 2020-05-31
categories: [Eines,Programari]
tags: [xifratge,Windows,MacOS,Linux,USB]
---


VeraCrypt és un programa gratuït i lliure que serveix per xifrar discs durs o USB, mitjançant diversos tipus d'algorismes com AES, Serpent y Twofish.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/veracrypt_logo2.png)

VeraCrypt xifra "on-the-fly". És a dir, les dades i arxius es xifren automàticament just abans que es guardin i es desxifren just després que es carreguin, sense que l'usuari hagi d'intervenir. Qualsevol informació emmagatzemada en un volum xifrat només pot ser llegida (desxifrada) si es sap la contrasenya o es tenen les clau de desxifratge correctes.

Quan es xifra un disc dur o un USB, tot el disc queda xifrat: els noms dels fitxers, els noms de les carpetes, el continugt de cada fitxer, l'espai lliure, les meta dades... D'aquersta menera és impossible obtenir informació del contingut del disc sense desxifrar-lo.

Els fitxers es poden copiar i moure d'un volum de VeraCrypt com si fos un disc normal, ja que els fitxers es desxifren automàticament "on-the-fly" (en memoria/RAM) mentre l'usuari els llegeix i es tornen a xifrar quan l'usuari els guarda.

# Menú
Pot semblar complicat d'utilitzar a primera vista, però ja veuràs que en realitat és molt senzill. Bàsicament és com si fos el "Mi PC" o "Equipo" de Windows, on cada vegada que es connecta un USB, apareix i quan es vol treure, s'ha d'extreure amb seguretat.

Veracrypt té diversos apartats que explicarem detalladament. Començant de dalt a baix i d'esquerre a dreta:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/menu2.png)

Cada una de les files de la taula és un espai buit on pots muntar un USB o fitxer xifrat. Com pots veure, VeraCrypt és capaç de gestionar-ne molts a la vegada. Quan desxifris un USB, aquest apareixerà a la fila que hagis escollit.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/menu2.png)

Els botons de sota de la taula et permetran crear un volum xifrat, veure les propietats d'un volum muntat i eliminar la cache del volum seleccionat.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/menu3.png)

Quan vulguis carregar un fitxer o USB xifrat, ho pots fer des de l'apartat "Volume". Al clicar "Select File" o "Select Device", s'obrirà una finestra des d'on podràs seleccionar l'USB o el fitxer que vols desxifrar.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/menu4.png)

Per últim, el botó "Mount" muntarà i desxifrarà el fitxer o USB seleccionat a l'apartat anterior. Recorda que abans d'extreure l'USB, és necessari desmuntar-lo, sigui individualment o amb el botó "Dismount All". D'aquesta manera, es pot extreure amb seguretat i t'assegures que s'hagi xifrat correctament.

# Xifrar USB
Xifrar és la tècnica més utilitzada i més útil quan es vol protegir la informació d'atacs físics. Has de tenir en compte que un cop xifrat, serà quasi impossible de desxifrar si t'oblides de la contrasenya o perds les claus.

El temps que tarda VeraCrypt en xifrar el dispositiu varia molt depenent del rendiment de l'ordinador i la mida del disc o l'USB. Podria tardar des de 15 minuts a diversos dies. Tot i això, no et preocupis que un cop xifrat, el procés de xifrar i desxifrar serà molt més ràpid (pocs segons).

## Xifrar tot l'USB o disc dur
A continuació explicarem com xifrar un USB. Xifrar-lo implicarà que TOT el dispositiu quedarà absolutament xifrat i que, sense la contrasenya, no es podrà recuperar el contingut.

Primer de tot, clica "Create Volume" perquè sobri el menú de creació d'un nou volum:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb1.png)

Si vols xifrar un USB, has de seleccionar la segona opció, ja que la primera és per si vols crear un fitxer xifrat:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb2.png)

Normalment seleccionaràs sempre l'opció de volum estàndard. La carpeta fantasma explicarem més endavant què és:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb3.png)

A continuació, has d'escollir quin USB o disc dur vols xifrar. En Linux, els dispositius estaran a */dev/sdX* i en Windows o MacOS estaran identificats per una lletra, *D:* per exemple:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb4.png)

Has de tenir en compte que durant el procés de xifratge és formateja el disc dur o l'USB. Per tant, és important que, si tens fitxers els guardis a algun altre lloc:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb5.png)

Per defecte, VeraCrypt selecciona l'algorisme AES i el HASH SHA-512. Persolament recomanem deixar-ho així, ja que AES és un algorisme de xifratge per blocs segur si s'utiltiza una clau suficientment gran. Respecte a l'algorisme de HASH, SHA està bé sempre que sigui 512 o superior, ja que s'ha demostrat que agencies d'espionatge poden arribar a trencar HASHES inferiors a 256:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb6.png)

Ara toca escollir una contrasenya. És important que sigui una contrasenya forta, ja que és l'únic punt dèbil del xifratge.

El [PIM](https://www.veracrypt.fr/en/Technical%20Details.html) és un valor que hauràs d'introduir, juntament amb la contrasenya, cada vegada que vulguis desxifrar el dispositiu. Si s'especifica un PIM, s'incrementa la seguretat però és ralentitza el procés de xifratge i desxifratge. Per defecte, si no selecciones la casella (no l'hauràs d'introduir), el PIM és 485 si s'utilitza SHA-512 o Whirlpool i 98 per la resta de casos.

En lloc de contrasenya també pots utilitzar claus. Les claus són fitxers que necessitaràs cada vegada que vulguis desxifrar el dispositiu. És molt important que les claus estiguin emmagatzemades a un lloc segur, ja que si un atacant les roba, podrà desxifrar el disc dur o USB.

En aquest exemple, posarem només la contrasenya:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb7.png)

Quan formateges un disc dur o un USB, és necessari especificar el tipus del sistema de fitxers. Un primer pas per fer-ho, és saber si emmagatzemaràs fitxers de més de 4GB. Si selecciones la primera opció, no podràs guardar fitxers de més de 4 GB, si selecciones la segona podràs guardar fitxers de la mida que vulguis:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb8.png)

Aquí és molt important que sàpigues quin sistema operatiu utilitzaràs. Per exemple, FAT32 és compatible amb tots els SO però no et deixa emmagatzemar fitxers més grans que 4GB. Si utilitzaràs Windows i/o Linux, NTFS és una bona opció. Si només utiltizes Linux, hauries d'escollir Ext3. Si vols que sigui compatible amb tots els sistemes operatius, la millor opció serà exFAT (tot i que hauràs d'instal·lar un paquet al Linux):

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/typus_format.png)

Un cop decidit, selecciona el tipus de sistema de fitxers:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb9.png)

Depenent de la teva decisió, selecciona la primera opció si només el vols utilitzar en un sistema operatius o la segona altrament:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb10.png)

Abans de xifrar, és necessari crear les claus que s'utilitzaran en l'algorisme. Per aconseguir el màxim d'aleatorietat possible, i per tant, més seguretat, has de moure el ratolí sense seguir cap patró fins que la barra estigui plena:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb11.png)

Aquest és l'últim pas abans de xifrar. Per això és important que sàpigues que tot el contingut del disc dur o USB s'esborrarà:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb12.png)

Per últim, toca esperar que VeraCrypt xifri el disc dur o USB:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb13.png)

## Fitxer xifrat
És possible que en comptes de xifrar un USB sencer, prefereixis tenir diversos fitxers xifrats. Un cas en el que seria útil xifrar fitxers és si volguessis compartir-los amb altres persones.

Primer de tot, clica "Create Volume" perquè sobri el menú de creació d'un nou volum:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb1.png)

A continuació, selecciona la primera opció per crear un fitxer xifrat:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file1.png)

En aquest exemple, farem el volum estàndard. El volum fantasma s'explica més endavant:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file2.png)

Selecciona el nom i carpeta on vols guardar el fitxer xifrat:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file3.png)

Per defecte, VeraCrypt selecciona l'algorisme AES i el HASH SHA-512. Persolament recomanem deixar-ho així, ja que AES és un algorisme de xifratge per blocs segur si s'utiltiza una clau suficientment gran. Respecte a l'algorisme de HASH, SHA està bé sempre que sigui 512 o superior, ja que s'ha demostrat que agencies d'espionatge poden arribar a trencar HASHES inferiors a 256:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file4.png)

Per a poder xifrar correctament el fitxer, és necessari que aquest tingui unes dimensions específiques. És per això que has d'indicar quina mida vols que tingui el fitxer:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file5.png)

Ara toca escollir una contrasenya. És important que sigui una contrasenya forta, ja que és l'únic punt dèbil del xifratge.

El [PIM](https://www.veracrypt.fr/en/Technical%20Details.html) és un valor que hauràs d'introduir, juntament amb la contrasenya, cada vegada que vulguis desxifrar el dispositiu. Si s'especifica un PIM, s'incrementa la seguretat però és ralentitza el procés de xifratge i desxifratge. Per defecte, si no selecciones la casella (no l'hauràs d'introduir), el PIM és 485 si s'utilitza SHA-512 o Whirlpool i 98 per la resta de casos.

En lloc de contrasenya també pots utilitzar claus. Les claus són fitxers que necessitaràs cada vegada que vulguis desxifrar el dispositiu. És molt important que les claus estiguin emmagatzemades a un lloc segur, ja que si un atacant les roba, podrà desxifrar el disc dur o USB.

En aquest exemple, posarem només la contrasenya:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file6.png)

Aquí és molt important que sàpigues quin sistema operatiu utilitzaràs. Per exemple, FAT32 és compatible amb tots els SO però no et deixa emmagatzemar fitxers més grans que 4GB. Si utilitzaràs Windows i/o Linux, NTFS és una bona opció. Si només utilitzes Linux, hauries d'escollir Ext3. Si vols que sigui compatible amb tots els sistemes operatius, la millor opció serà exFAT (tot i que hauràs d'instal·lar un paquet al Linux):

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/typus_format.png)

Un cop decidit, selecciona el tipus de sistema de fitxers:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file7.png)

Abans de xifrar, és necessari crear les claus que s'utilitzaran en l'algorisme. Per aconseguir el màxim d'aleatorietat possible, i per tant, més seguretat, has de moure el ratolí sense seguir cap patró fins que la barra estigui plena:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file8.png)

Per últim, es genera i es xifra el fitxer:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file9.png)

## Carpeta fantasma
VeraCrypt crea dues particions xifrades amb contrasenyes diferents, de tal manera que la partició fantasma és impossible de saber que existeix encara que es desxifri la primera. D'aquesta manera, depenent de la contrasenya que introdueixis, desxifraràs una partició o l'altra:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/hidden_volume.png)

Això pot ser molt útil en situacions on estiguis obligada a donar la contrasenya. Per exemple, si et posen una pistola al cap i t'obliguen a desxifrar l'USB, podries donar la contrasenya de la partició que tingués el contingut menys sensible.

Per explicar el procés, crearem la carpeta fantasma en un fitxer, però es pot fer de la mateixa manera amb USBs o disc durs.

Primer de tot, clica "Create Volume" perquè sobri el menú de creació d'un nou volum:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/usb1.png)

A continuació, selecciona la primera opció per crear un fitxer xifrat:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/file1.png)

Per crear la carpeta fantasma has de seleccionar la segona opció:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma1.png)

Selecciona el fitxer, USB o disc dur que vols xifrar:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma2.png)

Per defecte, VeraCrypt selecciona l'algorisme AES i el HASH SHA-512. Personalment recomanem deixar-ho així, ja que AES és un algorisme de xifratge per blocs segur si s'utilitza una clau suficientment gran. Respecte a l'algorisme de HASH, SHA està bé sempre que sigui 512 o superior, ja que s'ha demostrat que agencies d'espionatge poden arribar a trencar HASHES inferiors a 256:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma3.png)

Aquest apartat és molt important. Has d'indicar la mida màxima que tindrà la partició externa, tenint en compte que contindrà la fantasma. És a dir, la mida que tindrà el fitxer sumant ambdues particions. En el cas d'USBs o discs durs, es recomana posar el màxim de capacitat.

Per tant, si vols que la partició no sensible tingui 15MB i la partició fantasma 5MB, aquí hauràs de posar 20MB:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma4.png)

Ara toca escollir una contrasenya de la partició externa. És important que sigui una contrasenya forta, ja que és l'únic punt dèbil del xifratge.

El [PIM](https://www.veracrypt.fr/en/Technical%20Details.html) és un valor que hauràs d'introduir, juntament amb la contrasenya, cada vegada que vulguis desxifrar el dispositiu. Si s'especifica un PIM, s'incrementa la seguretat però és ralentitza el procés de xifratge i desxifratge. Per defecte, si no selecciones la casella (no l'hauràs d'introduir), el PIM és 485 si s'utilitza SHA-512 o Whirlpool i 98 per la resta de casos.

En lloc de contrasenya també pots utilitzar claus. Les claus són fitxers que necessitaràs cada vegada que vulguis desxifrar el dispositiu. És molt important que les claus estiguin emmagatzemades a un lloc segur, ja que si un atacant les roba, podrà desxifrar el disc dur o USB.

En aquest exemple, posarem només la contrasenya:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma5.png)

Abans de xifrar, és necessari crear les claus que s'utilitzaran en els algorismes. Per aconseguir el màxim d'aleatorietat possible, i per tant, més seguretat, has de moure el ratolí sense seguir cap patró fins que la barra estigui plena:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma6.png)

Finalment, es crea la partició externa xifrada:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma7.png)

L'únic que queda ara és crear la interna. Veuràs que el procés és molt semblant:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma8.png)

Igual que amb l'externa, seleccionar els algorismes de xifratge i HASH:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma9.png)

Aquí has d'indicar la mida de la partició fantasma. Com pots veure, no pot ser més gran que la que has posat al crear la partició externa:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma10.png)

Introdueix la contrasenya:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma11.png)

Aquí és molt important que sàpigues quin sistema operatiu utilitzaràs. Per exemple, FAT32 és compatible amb tots els SO però no et deixa emmagatzemar fitxers més grans que 4GB. Si utilitzaràs Windows i/o Linux, NTFS és una bona opció. Si només utilitzes Linux, hauries d'escollir Ext3. Si vols que sigui compatible amb tots els sistemes operatius, la millor opció serà exFAT (tot i que hauràs d'instal·lar un paquet al Linux):

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma12.png)

Genera les claus de xifratge:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/fantasma13.png)

I ja hauràs acabat el procés per crear un fitxer, USB o disc dur xifrat amb una carpeta xifrada fantasma. Ara quan muntis el fitxer, només hauràs d'introduir la contrasenya corresponent per veure una partició o l'altre. El procés és completament idèntic al fet que tinguessis només una sola partició.

# Muntar
Un cop tens el disc dur, USB o fitxer xifrat, és molt fàcil d'utilitzar. Només els hauràs de muntar i ja els podràs utilitzar com si fossin una carpeta normal.

Primer de tot, selecciona una fila de la taula i clica "Select Device" si vols muntar un disc dur o un USB o "Select File" si és un fitxer, el procés és exactament el mateix:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/muntar1.png)

S'obrirà un menú amb els dispositius connectats a l'equip o una carpeta perquè seleccionis el fitxer:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/muntar2.png)

Una vegada seleccionat, clica "Mount" i introdueix la contrasenya:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/muntar3.png)

Si és correcta, apareixerà a la taula després que VeraCrypt l'hagi desxifrat:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/muntar4.png)

A partir d'aquí, apareixerà com si fos un USB normal i corrent i ja podràs treballar:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/muntar5.png)

# Desmuntar
Abans d'extreure el disc dur o USB o apagar l'ordinador, és necessari desmuntar-los. En tots els casos el procediment és el mateix.

Senzillament, selecciona a la taula el dispositiu i clica la telca "Dismount". Si en tinguessis varis de muntats, clicant "Dismount All" els pots desmuntar de cop.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/desmuntar.png)

Si tinguessis utilitzant algun fitxer del dispositiu que vols desmuntar, et sortirà un error. És necessari que tanquis tots els documents abans de desmuntar el dispositiu.

# Xifrar Disc Dur
Avui en dia és extremadament important que els ordinadors tinguin el disc dur xifrat, ja que és molt fàcil accedir a la informació emmagatzemada al disc dur sense necessitat de saber la contrasenya d'administrador. És més, et podrien clonar el disc dur o entrar com a administradors al teu ordinador en menys de 10 minuts.

Tots aquests atacs físics es mitiguen, o es compliquen moltíssim, si el disc dur està xifrat. La recomanació és xifrar TOT el disc dur, perquè així s'anul·la el risc que hi hagi filtracions d'informació. Per exemple, si només xifres un document, és probable que a l'ordinador quedin rastres de quan l'has obert i editat, es pugui obtenir el nom del document o inclús recuperar algun fragment. Si tot el disc dur està xifrat, això no és possible, ja que no es pot veure el contingut del disc dur.

Abans de xifrar res, fes una còpia de seguretat i assegura't que el teu sistema operatiu és compatible: [enllaç](https://www.veracrypt.fr/en/Supported%20Operating%20Systems.html)

**Nota**: com que no podem ensenyar com xifrar un disc dur pas per pas, per raons òbvies, utilitzarem imatges extretes d'[aquest blog](https://www.online-tech-tips.com/computer-tips/how-to-encrypt-your-windows-hard-drive-with-veracrypt/) que poden variar lleugerament en l'aspecte del VeraCrypt, ja que són versions més antigues. No obstant això, el procediment és el mateix i molt similar a l'explicat en anteriors apartats d'aquesta entrada.

## Windows
Windows és un sistema operatiu de programari privat. Com no podia ser de cap altra manera, tenen el seu propi programa de xifratge, també de programari privat, anomenat [Bitlocker](https://support.microsoft.com/en-us/help/4028713/windows-10-turn-on-device-encryption).

Bitlocker és molt fàcil de configurar i d'utilitzar. A més a més, és molt ràpid perquè està dissenyat especialment per xifrar i desxifrar sistemes Windows. No obstant això, com que el codi font no està publicat, no ha sigut possible analitzar-lo i no se sap amb certesa si existeix una clau mestre. És a dir, una clau capaç de desxifrar qualsevol Windows encara que no se sàpiga la contrasenya.

A més a més, Bitlocker només està disponible si has comprat la versió de "Windows Professional", ja que no està disponible a la versió de "Home Edition".

Així i tot, s'ha de trencar una llança a favor de Bitlocker i és que dóna moltes facilitats a empreses. El departament de IT poden monitorar i gestionar el sistema de xifratge de tots els treballadors: detecten si un disc dur no està xifrat o poden desbloquejar el compte si un usuari ha oblidat la seva contrasenya.

Anem al gra. El procés és molt similar al de xifrar un USB, però amb un parell més de passos. Primer de tot, selecciona que vols crear un nou volum:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows1.png)

Has de seleccionar el tercer apartat per xifrar tot el sistema de fitxers:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows2.png)

Recomanem utilitzar el sistema de xifratge "Normal", ja que es tracta de xifrar el sistema operatiu i així evites complicacions:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows3.png)

Normalment, tindràs instal·lat el Windows en un disc dur i no tindràs particions. És a dir, que si vas a "Equipo", només et surt el disc "C:". Si aquest és el teu cas, és indiferent quina opció seleccionar.

Si per el contrari, ets un usuari amb més coneixements d'informàtica i tens una o més particions al disc dur, pots escollir que xifrar. La primera opció només xifrarà la partició que té el sistema operatiu mentre que la segona les xifrarà totes. Nosaltres recomanem sempre xifrar-ho tot per evitar filtracions.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows4.png)

Si al teu ordinador només hi tens instal·lat el Windows, selecciona la primera opció. Si per lo contrari tens el Windows juntament amb un altre sistema operatius, hauràs de seleccionar la segona. Personalment, mai hem provat xifrar un disc amb múltiples sistemes operatius amb VeraCrypt.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows5.png)

Tal com s'explica en altres apartats, la millor configuració es deixa la de per defecte. A la següent imatge, al ser antiga, utilitzen SHA-256. Recomanem utilitzar com a mínim SHA-512:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows6.png)

Després d'especificar la contrasenya, hauràs de generar les claus de xifratge movent el ratolí per la pantalla sense seguir cap patró:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows7.png)

Els següents passos són diferents respecte els que hem explicat als apartats anteriors. En xifrar un disc dur sencer amb el sistema operatiu, VeraCrypt recomana crear un disc de recuperació per si falla el procés de xifratge. Si hi hagués algun error, aquest disc restauraria les opcions de BOOT i podries iniciar sessió al sistema operatiu.

No et preocupis però que el disc no implica un problema de seguretat, ja que per utilitzar-lo hauràs d'introduir la contrasenya que has escollit.

Selecciona on vols que s'emmagatzemi el disc de recuperació. No és recomanable seleccionar la casella "Skip Rescue Disk verification", ja que si alguna cosa surt malament hauràs de reinstal·lar el sistema operatiu de nou i és possible que perdis tot.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows8.png)

A continuació has de gravar el disc de recuperació a un CD de 700MB. Si l'ordinador no disposa de gravadora de CDs, hauràs de gravar-ho tu a un USB i seleccionar l'opció de no verificar el disc de recuperació. Això és degut al fet que un CD és de només lectura però un USB és de lectura i escriptura. VeraCrypt no vol tenir la responsabilitat de gravar-ho a un dispositiu on hi hagi perill que la imatge es corrompi.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows9.png)

Abans de xifrar el disc dur, VeraCrypt fa un procés de prova on instal·larà tot el necessari perquè quan iniciïs l'ordinador, hagis d'introduir la contrasenya que has escollit abans que el sistema operatiu es carregui. Si la contrasenya és correcte, s'iniciarà el Windows, si no et tornarà a demanar la contrasenya.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows10.png)

Quan l'ordinador és reinici, veuràs que apareixerà una pantalla en negre on et demanarà que introdueixis una contrasenya. Aquí és on hauràs d'escriure la contrasenya que has escollit en passos anteriors:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows11.jpg)

Quant inicis sessió, VeraCrypt començarà a xifrar tot el disc dur. És molt important que no tanquis l'ordinador durant aquest procés per evitar que es corrompin les dades. Depenent de la mida del disc dur, VeraCrypt pot tardar diverses hores en xifrar-lo:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/windows12.png)

Un cop acabat, ja tindràs el disc dur xifrat. Només podràs llegir el contingut d'aquest si saps la contrasenya, així que no te l'oblidis.

Veuràs que cada vegada que engeguis l'ordinador, hauràs d'introduir la contrasenya per desxifrar i després la teva de l'usuari amb el qual vulguis iniciar sessió.

## MacOS
Igual que Windows, MacOS disposa del programa [FileVault](https://support.apple.com/en-us/HT208344) per xifrar el disc dur. És de programari privat i per tant, no sabem si Apple té una clau mestre. Hi ha hagut casos on l'FBI ha demanat a Apple la clau mestre però ells no li han donat. No obstant això, no podem saber si no els hi han donat perquè no existeix o simplement per publicitat.

Per defecte, FileVault no està activat, tot i que és un procés molt senzill activar-lo. A l'estar dissenyat per Apple, el procés de xifrar i desxifrar el disc és molt ràpid.

El procés per xifrar el disc dur amb VeraCrypt és el mateix que el de Windows. Així que no tornarem a copiar-ho tot. Dona un cop d'ull a l'apartat anterior.

## Linux
Linux utilitza [LUKS](https://support.apple.com/en-us/HT208344) per xifrar el disc dur. LUKS és de programari lliure i és compatible amb tots els sistemes Linux.

Per xifrar el sistema amb LUKS és recomana fer-ho durant la instal·lació, ja que és l'opció més senzilla i automàtica per l'usuari:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-31-veracrypt/luks.png)

Si vols xifrar amb LUKS després de la instal·lació, ho tens complicat, ja que no és possible fer-ho de manera senzilla: [enllaç](https://askubuntu.com/questions/366749/enable-disk-encryption-after-installation)

Recomanem utilitzar LUKS si tens un Linux, ja que anirà més de pressa i és 100% compatible. Així i tot, si volguessis utilitzar VeraCrypt, el procés a seguir és el mateix que hem explicat a l'apartat de Windows.

# Conclusions
Al contrari del que pensa la majoria d'usuaris, xifrar un disc dur no és complicat, només requereix temps. A més a més, no se li dóna gaire importància en xifrar el disc dur, ja que la majoria no són conscients que un atacant que aconseguís accés a l'ordinador físicament, podria entrar com a administrador en menys de 10 minuts si el disc dur no està xifrat.

Pensa que hi ha dos tipus de seguretat, la lògica i la física. L'absència d'una pot comprometre completament l'altra. És per això que recomanem molt fortament que xifris els discs durs i USB.

# Referències
* **Pàgina oficial**: [enllaç](https://www.veracrypt.fr/en/Home.html)