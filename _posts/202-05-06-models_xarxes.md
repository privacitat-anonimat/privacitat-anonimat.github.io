---
title: Models de xarxes
author: privacitat-anonimat
date: 2020-05-06
categories: [Conceptes,Bàsics]
tags: [introducció,programari]
---

Tots utiltizem aplicacions o serveis a través d'Internet. Per exemple, les xarxes socials, el correu electrònic o aplicacions de missatgeria instanània. El que segurament molts de vosaltres no us heu plantejat és per on viatgen els missatges que nosaltres enviem. 

Quan pensem en termes de privacitat i anonimat digital, és clau que ens plantegem per on es mou tota l'informació que intercanviem amb una persona o amb un servei. D'aquesta manera entendrem com la xarxa està estructurada i podrem identificar quins són els riscos i quina és la millor manera de protegir-nos.

Existeixen tres tipus de models de xarxes. La major diferència que tenen és per on passa l'informació i qui la controla.


# Centralitzat
A aquest model, tots els nodes són perifèrics i es connecten a un node central. D'aquesta manera, qualsevol comunicació entre els nodes haurà de passar si o si pel central.

Si per a qualsevol motiu el node central talla el fluxe de dades, ja sigui perquè ha deixat de funcionar o per decisió del qui el controla, tots els nodes perifèrics perdran la comunicació entre si.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-06-models_xarxes/centralitzada.png)

La majoria d'aplicacions del mercat funcionen amb models centralitzats. Per exemple, si volem enviar un correu electrònim amb Gmail, el correu anirà des del nostre ordinador fins als servidors de Google, Google mirarà el destinatari (SPOILER ALERT: també el llegeix) i l'enviarà a la persona de destí.

En termes de privacitat aquest és el pitjor dels tres models. Bàsicament perquè tota la comunicació i informació que intercanvien els usuaris està sota el control i domini de l'empresa que ofereix el servei. Això implica que no només saben l'origen i el destí de totes les comunicacions, sinó que també poden llegir-les o emmagatzemar-les.

Tampoc cal desanimar-se ara, ja que hi ha maneres de reduir o mitigar el risc que suposen els models centralitzats. Per exemple, l'ús de xifrat extrem a extrem o polítiques de "zero coneixement". 


# Descentralitzat
A diferència de les xarxes centralitzades, aquest model no té un únic node central, sinó que existeixen uns nodes centrals comunicats entre si. De tal manera que si un node central ser desconnecta, els nodes perifèrics podríen no perdre la connectivitat (dependria de la distribució de la xarxa).

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-06-models_xarxes/descentralitzada.png)

Aquest model és millor en termes de privacitat que el centralitzat sempre i quan els nodes centrals no siguin de domini d'una única empresa. Si continuem amb l'exemple de Gmail, està clar que Google té servidors distribuïts a diversos països el qual el converteix en un model de xarxa descentralitzada. No obstant, com ja haureu pensat, això no implica una millora en la privacitat de l'usuari.

Un bon exemple seria la xarxa social Mastodon, similar a Twitter però de codi obert i descentralitzada. On els nodes centrals que formen la xarxa són propietat de persones individuals majoritàriament. D'aquesta manera, no hi ha un monopoli per part d'una empresa i no hi ha cap node que controli tota l'informació.


# Distribuït
Aquest és el model més complicat d'implementar, ja que no existeix cap node central. Està fet de tal manera que si un node es desconnecta, no afecta a la connectivitat dels altres nodes, ja que no hi ha la necessitat de que tot passi per un node central.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-06-models_xarxes/distribuida.png)

Un exemple serien les aplicacions P2P (Peer to Peer) com les que s'utilitzen per descarregar Torrents. Quan un usuari es vol descarregar una pel·lícula mitjançant torrents, el fitxer en si no està a cap servidor. L'usuari es connecta a diversos usuaris que tenen la pel·lícula i es descarrega trossos de cada un d'ells fins a tenir-la al complet al seu ordinador.

Les xarxes distribuides són una molt bona manera de protegir la privacitat de l'usuari, ja que l'informació està distribuida entre tots els nodes i això evita que una empresa o persona la controli tota.

**Nota**: les aplicacions P2P tenen la contrapartida de que es pot filtrar l'IP de l'origen i el destí. Per tant, és un punt a tenir en compte si es prioritza l'anonimat.


# Conclusions
Quan busqueu aplicacions a utilitzar, sempre heu de prioritzar les descentralitzades i distribuides. No obstant això, a part del model, també és important tenir en compte altres punts com el xifrat, si és programari lliure o les polítiques de privacitat.

Us trobareu que hi ha molt poques aplicacions descentralitzades i les poques que hi ha, no acaben de funcionar com un esperava. Per exemple, aplicacions per fer videotrucades que durant la trucada hi ha petits talls o que si hi ha molts usuaris connectats a la vegada, es perdi la communicació.


# Referències
* **Secure Chat Guide**: [enllaç](https://securechatguide.org/)