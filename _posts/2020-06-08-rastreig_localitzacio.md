---
title: Rastreig Geolocalització Telèfons Mòbils
author: privacitat-anonimat
date: 2020-06-08
categories: [Conceptes,Avançats]
tags: [espionatge,rastreig,mòbil]
---

Els telèfons mòbils són els grans desconeguts. Molta gent coneix els perills que té un ordinador connectat a Internet i sap com protegir-se, però poques coneixen els dels mòbils.

Has de tenir en compte que un telèfon mòbil no deixa de ser un mini ordinador on l'usuari té encara menys control. Això provoca que moltes utilitzin el dispositiu mòbil de manera no segura i desconeixen els perills reals que comporta tenir-ne un engegat a la butxaca.

L'objectiu d'aquesta entrada és aclarir una mica com es poden localitzar dispositius mòbils i si hi ha alguna manera de protegir-nos.

# Xarxa telefònica
## Cobertura
Una comunicació a través de telèfons mòbils és aquella en la que els dispositius no estan connectats físicament a la xarxa a través de cables. El mitjà de transmissió és l'aire i la comunicació es realitza a través d'ones electromagnètiques amb freqüències entre 900 i 2000 MHz.

La telefonia mòbil està formada bàsicament per dos components:
* **Xarxa de comunicacions**: composta per antenes repartides per la superfície terrestre.
* **Dispositius**: telèfons mòbils que accedeixen a aquesta xarxa.

Tant les antenes com els dispositius són emissors i receptors.

Per a poder donar servei a un territori sense que hi hagi zones sense cobertura, les xarxes sense fils operen dividint el territori en quadrícules anomenades cel·les. Cada cel·la pot cobrir des d'uns pocs carrers en ciutats amb alta densitat de població, fins a extensions de 200 km quadrats en zones poc poblades.

Generalment les cel·les són de forma hexagonal, ja que aquesta figura geomètrica permet cobrir una regió geogràfica amb el mínim números de cel·les possibles sense deixar zones sense cobertura, permetent a més a més que la distància entre les antenes de la cel·la sigui la mateixa a tot el territori, evitant així problemes de mala recepció de senyal.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/celulas-telefonia-movil.jpg)

Cada cel·la utilitza un conjunt de freqüències de ràdio per facilitar la comunicació dins de la seva àrea. La distància d'aquestes freqüències es limita a la cel·la on es dóna el servei i per tal d'evitar problemes d'interferències, una mateixa freqüència no pot ser utilitzada simultàniament en cel·les contigües però si properes.

Per exemple, a la següent imatge pots veure com la cel·la central opera a una certa freqüència però les cel·les contigües treballen amb una freqüència similar però diferent. No obstant això, a la cantonada superior hi ha una cel·la que opera a la mateixa freqüència que la central:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/freq.jpg)

Cada cel·la té una estació base que tindrà una o més antenes o repetidors amb amplitud suficient per emetre i rebre senyals en aquell hexàgon.

A més a més, cada cel·la té vàries desenes de canals diferents. Un canal és per on es poden emetre trucades, és a dir que cada cel·la pot emetre diverses trucades simultànies. Això és possible perquè cada canal té una freqüència, de tal manera que les ones electromagnètiques no es superposen.

A les àrees rurals, les antenes són omnidireccionals i se situen al centre de la cel·la, mentre que a àrees urbanes que tenen molts usuaris, les antenes s'acostumen a col·locara a tres vèrtexs no consecutiu de cada hexàgon:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/celes.jpg)

## Funcionament trucades
Cada operador en una determinada zona geogràfica té un centre de control (Mobile Telephone Switching Office, MTSO) que s'encarrega d'identificar i canalitzar totes les connexions telefòniques que es produeixen entre els usuaris i les estacions de cada cel·la.

Una trucada telefònica es produeix seguint els següents passos:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/trucada.jpeg)

1. A l'encendre el telèfon mòbil, aquest busca un senyal per confirmar que el servei està disponible. Quan rep el senyal de l'estació més propera, el dispositiu s'hi connecta i s'identifica perquè la xarxa pugui verificar que l'usuari està adscrit a la companyia telefònica. Aquest procés és automàtic i es realitza quan l'usuari encén el mòbil.
2. Un cop verificat, el telèfon mòbil envia un missatge a l'estació indicant que vol comunicar-se amb el número de telèfon amb qui l'usuari vol parlar. El missatge el rep el MTSO que controla la zona.
3. El MTSO busca el telèfon mòbil sol·licitat enviant missatges a diverses estacions. Una vegada localitzada l'estació més propera al telèfon receptor, el MTSO accepta la trucada i decideix quins canals poden utilitzar ambdós dispositius per comunicar-se.
4. El MTSO estableix la connexió entre els dos telèfons mòbils a través de les estacions a les quals estan connectats cada un.
5. A partir d'aquí, els usuaris ja es poden comunicar.
6. A mesura que un usuari es mou i entra a una nova cel·la, l'estació notarà que la intensitat de senyal emesa pel mòbil varia. Mentrestant, l'estació de la cel·la a la qual s'està acostant, notarà que el senyal és més intensa. Les dues estacions és coordinaran entre si a través del MTSO i en un moment determinat, el telèfon rep el senyal que indica que canviï de freqüència per connectar-se amb la nova estació. Aquest canvi evita que la connexió entre els dos dispositius mòbils s'interrompi.

## Tipus de xarxes
El primer país que va instal·lar una xarxa de comunicacions per telèfons mòbils va ser Japó el 1979. A Europa, els països escandinaus van ser els primers l'any 1981 i EEUU van començar a funcionar el 1983. L'evolució històrica de les xarxes mòbils i les seves característiques són les següents:

* **Primera Generació 1G**: utilitza canals de comunicació analògics i s'utilitzava exclusivament per transmetre missatges de veu, amb una escassa seguretat i mala transferència al passar d'una cel·la a l'altra.
* **Segona Generació 2G**: va arribar al començament de la dècada dels 90 i va ser el primer a utilitzar protocols de comunicacions digitals, el més famós és GSM (Global System for Mobile communications). Va ser el primer a permetre la transmissió de dades (SMS), a part de trucades telefòniques amb un cert nivell de xifratge.
* **Tercera Generació 3G**: va sorgir com a resposta a la necessitat de tenir més velocitat de transmissió de dades i més capacitat. Va permetre oferir als usuaris, a part d'enviar missatges de veu i dades, accés a Internet. El protocol europeu es denomina UMTS (Universal Mobile Telecommunications System).
* **Quarta Generació 4G**: comercialitzada per les operadores des de 2010, ofereix millor seguretat i qualitat de servei, juntament amb més velocitat de transmissió que les generacions anteriors. Aquest sistema s'ha estès gràcies a l'ús massiu dels smartphones. La tecnologia 4G ha permès l'ús d'aplicacions com Whatsapp o Telegram, videojocs o navegació a Internet.
* **Cinquena Generació 5G**: s'espera que estigui disponible el 2020. La seva característica principal serà la millor velocitat de transferència de dades i imatges.

# Tècniques de geolocalització
Una sentència del [Tribunal Supremo](https://cadenaser.com/ser/2016/06/15/tribunales/1465991267_436541.html) espanyol va dictaminar que la policia no necessita autorització judicial per accedir a la geolocalització i al número de targeta d'un mòbil. Només s'han de dirigir a les operadores per aconseguir aquestes dades.

Per tant, és possible localitzar a una persona sense necessitat d'ordre judicial. L'únic que la policia no podrà saber és si el dispositiu el té titular o no.

La manera que té la policia per verificar que el mòbil el tenia el titular és accedint al registre de trucades i missatges. En aquest cas, la policia sí que necessita una ordre judicial que l'autoritzi a accedir a aquestes dades. A Espanya, les forces de seguretat no només tenen accés a les trucades i missatges entrants i sortints, sinó que també poden veure'n el contingut gràcies a la creació de SITEL.

El Sistema Integrat d'Interceptació Telefònica (SITEL) va ser encarregat pel Ministerio de Interior el 2001, tot i que no es va posar en marxa fins al 2004. A través d'aquest sistema, les forces de seguretat de l'estat poden escoltar i/o gravar totes les comunicacions de qualsevol telèfon, sempre amb l'autorització d'un jutge.

Una vegada obtenen el permís, l'operador que ofereix el servei a la línia afectada desvia una còpia de totes les trucades i missatges a un ordinador central de la Guardia Civil, CNI i un altre de la Policia Nacional, als que els investigadors poden accedir.

S'ha de tenir en compte que aquest mètode només funciona amb trucades i missatges convencionals. No serveix per accedir a trucades i converses d'aplicacions de missatgeria instantània com Whatsapp, Telegram o Signal.

## Triangulació
Aquest mètode permet localitzar un dispositiu que estigui connectat a la xarxa telefònica. No és necessari que l'usuari tingui cap mena d'aplicació especial instal·lada, només cal que el telèfon mòbil estigui engegat i tingui cobertura.

Si es fa només utilitzant una antena d'una cel·la, es pot arribar a saber la distància respecte a l'antena dibuixant un cercle al voltant d'aquesta, però no la localització exacta. No obstant això, si s'utilitzen tres antenes, es pot arribar a determinar la localització exacta del dispositiu, amb un cert marge d'error, mitjançant les següents variables:
* La distància entre les torres de telefonia
* El temps que tarda el senyal entre el dispositiu i cada una de les torres
* La intensitat del senyal rebuda a cada torre.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/torres.jpg)

La triangulació és més efectiva en zones urbanes que en rurals, ja que com més distància hi hagi entre les antenes, més marge d'error hi ha.

## Tower dump
És una tècnica que permet a la policia obtenir informació sobre la identitat, activitat i geolocalització de qualsevol telèfon mòbil que es connecti a una antena de telefonia determinada durant un període de temps.

Tot i que no poden escoltar les trucades o llegir els SMS, sí que poden obtenir l'identificador del telèfon i demanar la informació de més d'una torre de telèfon.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/tower_dump.jpeg)

## Simuladors de torres telefòniques (IMSI-Catcher)
Els IMSI-Catcher simplement emmagatzemen els IMSIs dels dispositius mòbils propers fent-se passar per una torre telefònica autèntica.

IMSI, International Mobile Subscriber Identity en anglès, és un identificador únic enllaçat amb la targeta SIM que utilitza el telèfon mòbil per autenticar-se a la xarxa de telefonia.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/imsi0.png)

Una tècnica que poden utilitzar les forces de seguretat per localitzar i identificar dispositius mòbils és utilitzant un simulador de torre telefònica. Hi ha tres tipus d'atacs diferents que es poden dur a terme amb un simulador:
1. Localització
2. Interceptació de comunicacions
3. Denegació de servei

En aquesta entrada nosaltres ens centrarem exclusivament a explicar el funcionament bàsic i com poden identificar i localitzar un dispositiu mòbil, ja que si no l'entrada seria massa extensa. Pots obtenir més informació visitant aquesta entrada anomenada [
Gotta Catch 'Em All: Understanding How IMSI-Catchers Exploit Cell Networks
](https://www.eff.org/wp/gotta-catch-em-all-understanding-how-imsi-catchers-exploit-cell-networks) de Electronic Frontier Foundation.

En xarxes GSM, els mòbils es connectaran a l'antena de telefonia que tingui el senyal més forta. Una vegada el dispositiu ha identificat l'antena, comença la negociació per connectar-s'hi. L'estació telefònica demana al mòbil que enviï els algorismes de xifratge que pot utilitzar. Després, l'estació envia el seu identificador i el mòbil respon enviant el seu IMSI. El telèfon l'envia perquè d'aquesta manera la companyia telefònica pot validar que l'usuari d'aquella targeta SIM és client i està pagant les quotes.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/imsi.png)

Si hi ha un simulador pel mig, el procediment és exactament el mateix. Bàsicament, el mòbil fa tota la negociació amb el simulador i el simulador, a la vegada, la fa amb la torre telefònica. Quan el mòbil envia el seu IMSI, el simulador l'emmagatzema i es desconnecta del telèfon, perquè aquest es connecti a la xarxa real, i comença la negociació amb el següent dispositiu mòbil que s'hi connecti.

Si les forces de seguretat capturen IMSIs que consideren rellevant en un moment donat, per exemple durant una manifestació, després els poden utilitzar per obrir processos legals.

**Nota**: en protocols més nous com 4G o LTE, els dispositius mòbils són més intel·ligents i no es connecten a qualsevol torre telefònica que tingui senyal més forta. Així i tot, existeixen tècniques més avançades per a poder dur a terme l'atac.

## Wifi
Quan un dispositiu té el Wifi activat, encara que l'usuari no estigui connectat a cap Wifi, el telèfon mòbil anirà escanejant tots els punts d'accés Wifi per veure si s'hi pot connectar.

Durant el procés previ a l'autenticació, el dispositiu mòbil envia la seva direcció MAC. Media Access Control (MAC) és un identificador únic de cada dispositiu, també es coneix com a direcció física i té aquesta forma: D4:BE:D9:8D:46:9A.

Aquesta direcció física no es pot canviar fàcilment, per tant es podria considerar una manera senzilla d'identificar un dispositiu.

Qualsevol punt d'accés Wifi tindrà un llistat de totes les MAC que s'hi han intentat connectar. Per tant, es queda registrat l'hora en la qual un dispositiu ha passat a una distància de menys de 40 metres de l'accés Wifi.

## Bluetooth
En el cas de la tecnologia Bluetooth la identificació es produeix si el dispositiu està a una distància de menys de 3 metres de l'emissor. No obstant això, a diferència del Wifi, durant l'aparellament de dos dispositius amb Bluetooth, no es transmet la MAC, sinó un identificador generat en aquell moment.

Per tant, identificar un dispositiu físic que s'ha connectat amb Bluetooth és molt més complicat que no pas amb el Wifi.

## GPS
El GPS és un sistema de posicionament multisatelital que utilitza uns receptors col·locats al dispositiu mòbil que capten emissions d'uns satèl·lits en concret.

A part dels satèl·lits que formen el GPS, hi ha països que han desenvolupat els seus propis sistemes:
* GLONASS a Rússia
* BeiDou a la Xina
* Galileo a Europa

Quan un dispositiu vol saber la seva ubicació a través de GPS, el primer que fa és capturar el màxim de senyals possibles per així posicionar-se de manera fiable. Durant el procés veuràs que l'aplicació anirà acotant la localització fins a arribar als 4-16 metres. El senyal tarda un temps d'ençà que surt del satèl·lit fins que arriba al receptor del mòbil. Donat que la velocitat és constant, el mòbil pot calcular la distància precisa que hi ha entre els satèl·lits i el dispositiu.

Quan el mòbil ha capturat el menys quatre senyals de diferents satèl·lits, ja pot posicionar-se en les tres dimensions utilitzant una tècnica anomenada Trileració. El mòbil traça una circumferència al voltant de cada satèl·lit i el punt on es creuen totes les circumferències és la localització actual del dispositiu.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/satelit.jpg)

Com més senyals obtingui, més precís i amb menys marge d'error serà la localització que calculi.

A diferència de la xarxa de telefonia, l'operadora no pot utilitzar la informació GPS calculada pel dispositiu per obtenir la localització d'aquest, ja que no en té accés. No obstant això, les coordenades GPS poden ser utilitzades pel sistema operatiu o aplicacions de tercers, aplicacions que l'usuari ha instal·lat i ha donat permisos o inclús per certes pàgines d'Internet mentre l'usuari navega.

Per tant, has de tenir en compte que si dones permisos a una aplicació perquè utilitzi el GPS, aquesta pot enviar les coordenades al servidor i l'empresa que ha desenvolupat l'aplicació sabrà la teva localització real.

# Exemples reals
## Malte Spitz
L'advocat i polític alemany Malte Spitz va sol·licitar a la seva companyia telefònica, Deutsche Telekom (T-Mobile), que li entregués tota la informació que havia guardat d'ell durant sis mesos. La companyia s'hi va negar i Spitz va decidir anar per la via legal. Spitz mai va guanyar el judici. Tampoc va tenir la necessitat, ja que durant el procés judicial, el Tribunal Constitucional alemany va considerar que la retenció de dades era inconstitucional i s'oposava al concepte anunciat el 1983: l'autodeterminació informativa. El Tribunal va crear un precedent internacional i va motivar a T-Mobile a entregar la informació.

Spitz va rebre un [document](https://docs.google.com/spreadsheets/d/1PMjIkymwzYNGhENCi9BZst63H-UPagYgPO6DwHVdskU/edit?authkey=COCjw-kG&hl=en_GB&hl=en_GB&authkey=COCjw-kG#gid=0) amb més de 35000 línies d'informació: a qui trucava, qui li trucava, el consum de dades d'Internet i les posicions geogràfiques de les antenes a les quals es connectava el seu telèfon mòbil.

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/malte_spitz_dades.png)

Malte Spitz va donar [aquest document](https://docs.google.com/spreadsheets/d/1PMjIkymwzYNGhENCi9BZst63H-UPagYgPO6DwHVdskU/edit?authkey=COCjw-kG&hl=en_GB&hl=en_GB&authkey=COCjw-kG#gid=0) a una empresa de tractament de dades perquè fessin una aplicació per visualitzar-les de manera més senzilla.

El resultat és un [mapa interactiu](https://www.zeit.de/datenschutz/malte-spitz-data-retention), publicat el 2011, on pots veure tot el que la companyia de telefonia Deutsche Telekom sabia sobre la vida de Malte Spitz. Només per tenir un smartphone a la butxaca, la companyia ja sabia on vivia, quan dormia, on treballava, quan viatjava, quan agafava el tren o el cotxe, quan tenia una cita o organitzava protestes públiques. A una xerrada a Ted el 2012, Spitz ho va resumir amb la frase: "*Era la meva vida*".

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/malte_spitz_mapa.png)

A part de la geolocalització, l'empresa de telefonia també obté molta altra informació com les trucades, SMS, ús d'internet, a qui truques més sovint o a qui menys. Tota aquesta informació la van tractar i van fer [diagrames interactius](https://public.tableau.com/views/MalteSpitzCallData/MalteSpitzcalldatadashboard?:embed=y&:showVizHome=no) perquè fos més fàcil de veure:

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/malte_spitz_diagrames.png)

Malte Spitz va començar un activisme dedicat a la defensa de l'autodeterminació informativa i protecció de les dades personals. El 2014 va publicar un llibre anomenat *What are you doing with my data?*.

## Protestes Ucraina 2013
Durant les [protestes a Ukraina](https://es.wikipedia.org/wiki/Euromaid%C3%A1n) que van començar el novembre de 2013, el govern va utilitzar la tècnica "Tower Dump", explicada anteriorment, per a poder identificar a tots els manifestants que participaven en una protesta antigovernamental.

Des d'òrgans policials, van demanar a la companyia de telefonia que els hi donés els dispositius que s'havien connectat a les torres telefòniques més properes a les protestes.

D'aquesta manera, el govern Ucraïnès va utilitzar les tecnologies per a identificar a tots els manifestants que estaven a les protestes sense que ni ells en fossin conscients. Uns dies després, n'hi va haver molts que van rebre un SMS al seu telèfon mòbil amb el missatge "*Has sigut identificat com a participant d'una protesta massiva*":

![](https://raw.githubusercontent.com/privacitat-anonimat/privacitat-anonimat.github.io/master/img/2020-06-08-rastreig_localitzacio/ucraina.png)

Tot i que la policia utilitza aquesta tècnica freqüentment, el fet que el govern enviés aquest missatge va tenir grans implicacions psicològiques entre els manifestants. Les protestes van anar escalant i el govern Ucraïnès va aprofitar per canviar la legalitat de diverses activitats que els manifestants havien dut a terme durant mesos.

# Conclusions
Recomanem tenir el GPS, Wifi i Bluetooth apagats a no ser que els estiguis utilitzant. A més a més, si vas a manifestacions recomanem que deixis el telèfon a casa o, si no fos possible, el posis en mode avió. I sobretot, és molt important que sàpigues quines aplicacions tens instal·lades al mòbil i no donar més permisos dels necessaris.

Per exemple, si instal·les una aplicació de Movistar i li dónes permisos per utilitzar el GPS, quan l'activis Movistar podrà saber la teva localització. Passa exactament el mateix amb els mapes de Google o Apple.

Després de llegir aquesta entrada i adonar-te que les forces de seguretat i agències d'espionatge tenen moltes maneres d'espiar-te sense tenir una ordre judicial, potser penses que ells no tenen cap motiu per espiar-te a tu en concret, perquè no has fet res. Has de tenir en compte que als nostres vigilants no els importa que no siguem ningú, perquè són algorismes. El nostre perfil és automàtic, existeix encara que ningú el miri. I el dia que algú el miri, el teu historial passa a convertir-se en els teus antecedents.

No et vigilen per no ser ningú, sinó que et vigilen per si algun dia ets algú.

# Referències
* **Document científic localització Wi-Fi**: [enllaç](https://dialnet.unirioja.es/descarga/articulo/5101924.pdf)
* **Blog telefonia mòbil**: [enllaç](https://blogs.publico.es/ignacio-martil/2017/02/24/como-funcionan-las-redes-inalambricas-de-telefonia-movil/)
* **Marta Peirano - TED Talk**: [enllaç](https://www.youtube.com/watch?v=NPE7i8wuupk&feature=youtu.be)
* **Malte Spitz - TED Talk**: [enllaç](https://www.ted.com/talks/malte_spitz_your_phone_company_is_watching)
* **Malte Spitz - Diagrames**: [enllaç](https://public.tableau.com/views/MalteSpitzCallData/MalteSpitzcalldatadashboard?:embed=y&:showVizHome=no)
* **Malte Spitz - Geolocalització**: [enllaç](https://www.zeit.de/datenschutz/malte-spitz-data-retention)
* **Malte Spitz - Informació companyia telefònica**: [enllaç](https://docs.google.com/spreadsheets/d/1PMjIkymwzYNGhENCi9BZst63H-UPagYgPO6DwHVdskU/edit?authkey=COCjw-kG&hl=en_GB&hl=en_GB&authkey=COCjw-kG#gid=0)
* **Malte Spitz - Blog personal**: [enllaç](https://www.malte-spitz.de/english/)
* **SITEL**: [enllaç](https://www.xataka.com/moviles/asi-es-como-la-policia-del-siglo-xxi-situa-al-sospechoso-en-la-escena-del-crimen)
* **Gotta Catch 'Em All: Understanding How IMSI-Catchers Exploit Cell Networks - EFF**: [enllaç](https://www.eff.org/wp/gotta-catch-em-all-understanding-how-imsi-catchers-exploit-cell-networks)
* **GPS**: [enllaç](https://elandroidelibre.elespanol.com/2018/12/informacion-gps-satelites-conexion-cobertura.html)