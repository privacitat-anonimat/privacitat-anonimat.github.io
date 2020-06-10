---
title: Comunicacions i xifratge
author: privacitat-anonimat
date: 2020-05-07
categories: [Conceptes,Bàsics]
tags: [xifratge,privacitat,Internet]
---

Quan un usuari utilitza aplicacions que van per Internet per comunicar-se amb altres persones, es crea un canal de comunicació entre l'usuari que envia el missatge i el receptor. Tot i que aquest canal és invisible per l'usuari, la comunicació no es crea per art de màgia. Els missatges que s'intercanvien passen per un camí determinat i hi ha certs agents intermedis que poden veure la comunicació.

Partint de l'exemple de dues persones enviant-se missatges, a grans trets aquest seria el camí per on passarien els missatges:
1. L'usuari escriu el missatge i clica el botó d'enviar
2. El missatge surt del dispositiu de l'usuari i va cap al router (aparell que fa llumetes que dona Internet)
3. El router l'envia al ISP (Internet Service Provider), l'empresa que ofereix servei d'Internet a la casa de l'usuari. A Espanya, podria ser Telefònica, Vodafone...
4. El ISP envia el missatge al servidor de l'empresa que ha desenvolupat l'aplicació
5. El servidor mira el destinatari i l'envia
6. El missatge acaba arribant al ISP que té contractat el destinatari
7. El ISP envia el missatge al router del destinatari
8. Finalment el missatge acaba arribant al dispositiu del destinatari i aquest pot llegir el missatge

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-07-comunicacions_xifrat/isp.jpg)

Com pots veure, en aquest exemple hi ha 5 agents que intervenen en la comunicació (en realitat n'hi ha més, però no entrarem en tant detall):
* Dispositiu origen
* ISP origen
* Servidor
* ISP destí
* Dispositiu destí

Si et preocupa la privacitat, ràpidament hauràs detectat que la conversa privada entre dues persones en realitat no és tan privada com sembla.

# Comunicació no xifrada
En el pitjor dels casos, la comunicació no va xifrada. Això implica que els missatges no només els veuen els usuaris, sinó també les empreses que ofereixen el servei d'Internet (ISP), l'empresa que ha desenvolupat l'aplicació i altres agents intermedis com autoritats i governs, empreses d'espionatge i criminals.

Actualment, les aplicacions i programes més coneguts xifren totes les seves comunicacions. Moltes vegades perquè la normativa ho obliga.

# Comunicació xifrada punt a punt
L'immensa majoria d'aplicacions que xifren les seves comunicacions ho fan punt a punt (Point to Point Encryption, P2PE). Consisteix en el fet que el missatge va xifrat des de l'origen fins al servidor i des del servidor fins al destí.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-07-comunicacions_xifrat/p2pe.jpg)

Fixa't en el detall que el servidor el desxifra i el torna a xifrar. Això ho fan per poder veure qui és el destinatari del missatge per poder-li enviar, però també poden llegir el missatge.

Els missatges xifrats mitjançant aquesta tècnica estan protegits contra els agents intermedis com autoritats, governs, empreses d'espionatge i criminals. No obstant això, l'empresa que ha desenvolupat l'aplicació sí que pot veure'n el contingut i podria tenir pactes de compravenda d'informació amb tercers.

Alguns exemples:
* Telegram
* LINE
* Whatsapp fins al 2016
* Gmail
* Outlook

# Comunicació xifrada extrem a extrem
Per últim, les comunicacions xifrades extrem a extrem (End to End Encryption, E2EE) són les que només l'origen i el destinatari poden desxifrar els missatges.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-05-07-comunicacions_xifrat/e2ee.jpg)

D'aquesta manera, la comunicació està protegida contra qualsevol agent intermedi, ja que només els usuaris origen i destí tenen les claus necessàries per veure el contingut en clar.

Alguns exemples:
* Signal
* Wire
* Protonmail
* Tutanota
* Whatsapp a partir del 2016
* Telegram, només xats secrets

**Nota**: que les comunicacions es xifrin extrem a extrem, no vol dir que no existeixin altres tècniques que poden utilitzar les empreses que controlen l'aplicació per llegir els missatges. Ho indico per treure el dubte dels que penseu que el xifrat extrem a extrem ja fa que Whatsapp i Telegram siguin aplicacions segures que protegeixen la privacitat de l'usuari.

# Conclusions
Un indicador clau per saber si una aplicació es preocupa per la privacitat dels usuaris és si tenen implementat correctament el xifrat extrem a extrem. No hauries d'utilitzar cap aplicació que no tingui com a mínim E2EE.

No obstant això, també t'has de fixar amb altres coses com el país el on té la seu l'empresa per assegurar-te que no estigui dins dels "14 eyes", la política de privacitat, si tenen política "zero knowledge", etc.

# Referències
**Xifrat Whatsapp**: [enllaç](https://medium.com/@gzanon/no-end-to-end-encryption-does-not-prevent-facebook-from-accessing-whatsapp-chats-d7c6508731b2)