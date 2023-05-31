
Creating Exercises with H5P-Solfege  Libraries
==========

## About

*H5P-Solfege* is a project to develop libraries for creating ear training exercises in  https://sisuloome.e-koolikott.ee/ or similar H5P content system.

The software is developed at Georg Ots Tallinna Music School, now Tallinn College of Music and Ballet for project "Digitaalse muusikateooria ja solfedžo õppevara täiustamine ja arendamine"   with the support of European Social Fund (Euroopa Sotsiaalfond).

![Euroopa Sotsiaalfond](img/eu_small.jpg)

Since e-koolikott is meant mostly for Estonian schools, the instructions below will be only in Estonian. The libraries can be used in Estonian, English and Russian though, if the platform supports it.

<br>

## Harjutuste loomine

### Sisenemine e-koolikoti sisuloomesse


E-koolikoti sisuloome asub aaderssil: https://sisuloome.e-koolikott.ee/


Sisenemiseks on vajalik HarID (Haridus-ID) konto. Kui olete Tahvli, eKooli, Opiq jpm kasutaja, siis on see teil tõenäoliselt olemas. Kui mitte, looge konto aadressil https://harid.ee/et/users/sign_up


Kui olete sisenenud, vajutage nuppu "Loo uus materjal"

![](img/loo-uus-materjal.png)

<br>

### Sisutüübi valimine

**H5P** on interaktiivse veebimaterjali loomise süsteem, millele e-koolikott on rajatud. H5P teeke (ingl.k *libraries*) nimetatakse sisutüüpideks.

**H5P-Solfege** võimaldab hetkel luua 2 (peatselt 3) tüüpi harjutusi -  **astmediktaadid** (*degree dictations*), **harmoonilised funktsioonid** (*harmonic functions*) (+ peatselt: meloodilised diktaadid).

Sisestage harjutuse pealkiri, mille järgi saab seda hiljem leida. Nt "Astmediktaadid - test"

Valige seejärel H5P Sisu tüüp. Otsingu ribale tuleb sisestada tüübi ingliskeelne nimetus või üks osa sellest. Nt *degree* või *harmon*

 
![](img/vali-sisu-tyyp.png)


Klõpsake valitud tüübile ning avaneb vorm, nn *H5P-Editor*, mille abil saate harjutuse koostada. Vaatleme erinevaid tüüpe allpool eraldi.

<br>

### Astmediktaadid

Kõigepealt tuleb sisestada harjutuse pealkiri. Nt "Astmeline liikumine, väiksed hüpped"

Märguanne "See ei ole ametlik H5P.org sisutüüp. Probleemide korral pöörduge autori poole: tarmo.johannes@muba.edu.ee " tähendab, et tegemist ei ole H5P.org  enda välja töötatud sisutüübiga ning e-koolikott/H5P ei võta vastutust, kui selle juures on mingeid tõrkeid. Seda ei olnud võimalik kuvada kuidagi elegantsemalt.

Harjutus võib sisaldada üks või mitu astmediktaati. Need saate sisestada "Harjutuse andmed" all:

- konkreetse diktaadi pealkiri (läheb harjutuses rippmenüüsse). Nt "1" või "Astmeline" vms
- määratlege tunnetuslikult harjuse raskusaste oma sihtgruppi silmas pidades. See pole nii oluline - siin ei ole ühtset standardit.
- valige laad, nt "Dooria"
- sisestage astmed. Meloodia peab koosnema 7 noodist, so iga kast peab olema täidetud. Astmed tuleb sisestada numbritena - 1, 2, .. 8. 8 tähendab "ülemine 1". Vastuses on "1" selle koha peal õige, kuid süsteem ei teaks muidu, kumma 1. astmega on tegemist. Toonikas allapoole saab minna kuni 5. astmeni, selleks tuleb sisestada astmed miinusmärgiga: -7, -6, -5. Vastates, miinust pole vaja. Kui teete midagi valesti, siis see kastike märgitakse punasega. Kui kõik on korras, siis nuppu "Valideeri" tegelikult polegi vaja vajutada.
- Kui soovite sisestada järgmise meloodia, vajutage nuppu "Lisa diktaat" ning täitke sarnased väljad.
- "Teksti asendused ja tõlge" võite jätta nii nagu on või kui soovite lihvida mõne välja tõlget, saate seda siin teha.


 ![](img/astmediktaadid.png)


Kui kõik on valmis, vajutage "Salvesta". Seejärel saate harjutust üle vaadata, läbi teha ning vajadusel sisse viia vajalikud muudatused/täiendused. (Nupp ülal -  "Muuda"). 

Et õpilane saaks seda harjutust teha, tuleb see avaldada. Selleks on kõige mugavam võimalus vajutada nuppu "Avalda e-koolikotis". Vt peatükk "Avaldamine e-koolikotis" allpool.


### Harmoonilised funktsioonid

Seda tüüpi harjutuse sisuks on, et süsteem esitab väikse helifaili ning kasutaja peab taktide kaupa kirja panema, milline harmooniline funktsioon -  toonika, subdominant, dominant või mediant  - seal on.

Harjutuse koostaja peab seega kõigepealt valima ja ettevalmistama vastavad helifailid - kas ise salvestama või valima katkendeid olemasolevast muusikast.

Ka selle sisutüübi juures võib sisestada ühes harjutuses mitu erinevat funktsioonidiktaati. Selleks:

- andke igale diktaadile pealkiri, mis kuvatakse harjutuse juures rippmenüüs (võib olla ka lihtsatl "1", "2", "3" jne)
- seejärel sisestage funktsioonid tähtetega t, d, s, m taktide kaupa, üks sisestusväli vastab ühele taktile. Sobivad nii suur- kui väiketähed. Tihti on ühes taktis ainult üks funktsioon, aga kui neid on mitu (tüüpiliselt 2), siis tuleb lahtrisse sisestada mitu tähte, nt "t d", tühikud pole olulised, võib sisestada ka "td".
- laadige üles helifail. Veenduge, et teil on selle kasutamiseks õigus! (vaba litsentsiga, enda loodud helifail või olemasolevate teoste lühikesed katkendid)
- kui teil on võtta, võite lisada ka notatsiooni pildifailina (.jpg või .png vormingus).

![](img/e-koolikott-harmoonilised-funktsioonid.png)

Kui kõik on valmis, vajutage "Salvesta". Seejärel saate harjutust üle vaadata, läbi teha ning vajadusel sisse viia vajalikud muudatused/täiendused. (Nupp ülal -  "Muuda"). 

Et õpilane saaks seda harjutust teha, tuleb see avaldada. Selleks kõige mugavam võimalus on nupp "Avalda e-koolikotis".

<br>

## Avaldamine e-koolikotis

NB! On tähtis mõista, et **e-koolikott** ja **e-koolikoti sisuloome** on kaks eri keskkonda. **e-koolikott** on sisuliselt õppematerjalide kogu,  mis on loodud nendest harjutustest, mis on tehtud **sisuloomes**. Üks e-koolikoti materjal võib kombineerida endas mitu sisuloome harjutust, koondada neid peatükkidesse, lisada tutvustavat teksti.


Logige sisse e-koolikotti (nt HarID abil).

Mõistlik on hoida **e-koolikott** ja **sisuloome** kahes aknas või vahelehel eraldi lahti.

Vajutage nuppu "Lisa uus õppematerjal" või kui te olite vajutanud nuppu "Avalda e-koolis" sisuloomes, siis peakski olema uue materjali loomise vorm avatud. Sisestage materjali pealkiri ning kirjeldus.


![](img/e-koolikott-lisamine1.png)


Seejärel avage lahter "Lisa sisu". Kui te vajutasite Sisuloomes "Avalda e-koolikotis", peaks see olema eeltäidetud. Vastasel juhul tuleb kasutada nuppu "Poogi link", leidke sisuloome keskkonnas vastav harjutus, vajutage seal nuppu "Kopeeri link" ning kopeerige see e-koolikotis väljale "Lisa link", seejärel "Lisa"

![](img/e-koolikott-lisa-sisu.png)


Võite kasutada ka nuppusid "Lisa tekst", kui tahate midagi kommenteerida või "Lisa uus peatükk", kui materjal on ulatuslikum ja vajab liigendamist. "Poogi link" abil saate lisada veel teisi harjutusi. 


### Tee materjal lihtsamini leitavaks. 

Täita see osa, on väga oluline!

Valige otsingu järgi "muusika" õppekava, mille juurde see materjal sobib ning märkige ära vastavad kastikesed. Valige ka vähemalt üks üldpädevustest, nt "Kultuuri- ja väärtuspädevus". H5P-Solfege sisutüübid on kasutatavad ka pimedatele muusikaõppijatele, võite valida ka "Muu erivajadus".

Materjali tüüp peaks olema "Harjutus või tööleht", lisada võib ka
"Heli".


**NB!!!** Võtmesõnade juurde **märkige kindlasti "digitaalne õppevara - nutikas õppimine"** (ESF nõue)! Lisada võiks ka võtmesõna "solfedžo"

![](img/e-koolikott-lihtsamini-leitavaks.png)


Soovituslik on lisada pilt, mille järgi materjal ära tunneb, nt see:

<img src="img/h5p-solfege.png" width="400">


Seejärel märkige ära kasitke, et nõustute *Creative Commons* litsentsiga ning salvestage materjal.

Ongi valmis!









