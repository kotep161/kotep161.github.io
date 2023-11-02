---
title: Videoeditointi
layout: default
parent: "Teema 2: Opetusvideot ja videoiden editointi"
---

# Videoeditointi DaVinci Resolve -ohjelmalla

{: .no_toc }

Tällä oppitunnilla tutustumme...
{: .fs-5 }

---

<details open markdown="block">
  <summary>
    Sisällysluettelo
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

![Mies kuvaa videota](assets/images/opetusvideot/videomies-pieni.png)

Tässä osiossa käsitellään videoeditoinnin perusteita. Joitain videoeditointiin liittyviä perustaitoja on käsitelty <a href="https://peda.net/jyu/it/perusopinnot/dop/tervetulosivu/videoeditointi/openshot">**ITKP1011 Digitaalisen oppimisen perusteet -opintojaksolla**</a> (tai ITKP101 Tietokone ja tietoverkot työvälineenä). Käy tarvittaessa kertaamassa sen opintojakson materiaalia.

Tämän osion osaamistavoitteita ovat:

<ol>
    <li>Videoeditoinnin perustoiminnot
        <ol style="list-style-type: lower-latin;">
            <li>Materiaalin (video, äänet, kuvat) tuonti projektiin</li>
            <li>Aikajanan käyttö</li>
            <li>Leikkaaminen</li>
            <li>Siirtymät, häivytys</li>
            <li>Äänentasojen muuttaminen ja normalisointi</li>
            <li>Tekstin lisääminen videoon</li>
        </ol>
    </li>
    <li>Valmiin videotiedoston toimittaminen
        <ol style="list-style-type: lower-latin;">
            <li>Videon tiedostomuodot</li>
            <li>Pakkaus ja tiedostokoko</li>
        </ol>
    </li>
    <li>Laadukkaan videomateriaalin tuottaminen, johon sisältyy muun muassa seuraavien käsitteiden ymmärtämin
        <ol style="list-style-type: lower-latin;">
            <li>Videon tarkkuus (resoluutio) ja kuvataajuus (ruutua sekunnissa, frames per second, fps)</li>
            <li>Alkuperäisen kuvamateriaalin ja lopullisen videon suhde</li>
        </ol>
    </li>
</ol>

Tällä kurssilla suosittelemme käyttämään **DaVinci Resolve** -ohjelmistoa. Myös **OpenShot** (käytetty Digitaalisen osaamisen perusteet -opintojaksolla) ja **Shotcut** ovat hyviä vaihtoehtoja. Monet periaatteet ovat hyvin samanlaisia eri ohjelmien välillä. Eroavaisuuksia kuitenkin on, ja Resolve on näistä ohjelmista edistynein.

Ilmoitathan luennoitsijalle jos havaitsette oppimateriaalissa puutteita tai vanhentuneita asioita, linkkejä tms.

## Lataaminen ja asentaminen

<a href="https://www.blackmagicdesign.com/products/davinciresolve/">**Lataa ja asenna Davinci Resolve -ohjelmisto**</a>. Kyseessä on kaupallinen ohjelmisto josta saa kuitenkin ladattua maksuttoman version omaa käyttöä varten. **Huom! Älä lataa ohjelman Studio-versiota**, sillä se on maksullinen sovellus.

Lataussivu pyytää antamaan henkilötiedot rekisteröitymistä varten. Voit omatuntosi mukaan antaa tiedot tai jättää antamatta. Voit esimerkiksi syöttää vaikka vain yhden kirjaimen kuhunkin kenttään (sähköpostiin kelpaa vaikka <code>a@a.a</code>).

**Huomautus 1**: Suosittelen vahvasti kytkemään pois käytöstä erilliset virustorjunta- ja tietoturvaohjelmistot, kuten McAfee, Norton jne. Resolven käyttämisen ajaksi. Nämä erilliset tietoturvaohjelmistot saattavat merkittävästi haitata ohjelman käyttämistä tai jopa estää käynnistymisen. Käyttöjärjestelmän omat tietoturvaominaisuudet (esimerkiksi Windowsissa Asetukset -&gt; Päivittäminen ja suojaus -&gt; Windowsin suojaus) kannatta jättää päälle.

**Huomautus 2**: Videoeditointi on tietokoneen tehojen kannalta melko vaativaa työskentelyä. Keskusmuistia tulisi olla vähintään 8 gigatavua, mutta 16 gigatavua on suositeltava. Myös prosessorin teholla on merkitystä siihen kuinka sujuvasti editointi onnistuu. Mikäli näyttää siltä, että koneesi ei jaksa kunnolla pyörittää Resolvea, voit kokeilla (1) käyttää Shotcutia, joka on hieman kevyempi ohjelmisto, tai (2) pienentää editoitavien videoiden resoluutiota esimerkiksi 720p-resoluutioon ja enintään 30 fps kuvataajuuteen (ks. [ohjevideo YouTubessa](https://youtu.be/KlzqDhXuFlo)).

## Projektin luominen ja projektin asetukset

[Katso video YouTubessa (kesto 01:13).](https://youtu.be/N4WaQ2Ilvek?si=kPpcbjsfwF7nJUG3)

<iframe width="560" height="315" src="https://www.youtube.com/embed/N4WaQ2Ilvek" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

**Projektin asetukset**

Ennen kuin aloitetaan työskentelemään varsinaisen editoinnin parissa, on päätettävä lopullisen tuotantovideon asetuksista muutama asia, tärkeimpänä **tarkkuus** ja **kuvataajuus**. Aikajanan kuvataajuuden muuttaminen jälkikäteen on haastavaa. Tarkkuutta voi kylläkin vielä muuttaa, mutta siitä huolimatta se kannattaa asettaa alussa oikeaksi. Niinpä paneutuminen näihin asetuksiin alussa on tärkeää.
Valitse oikeasta alalaidasta rattaan kuva. Katsotaan sitten tarkemmin paria asetusta.
**Projektin kuvatarkkuus (resoluutio)**
Valitse **Timeline Resolution** -kohdasta 1920 x 1080 HD. Tätä tarkkuutta kutsutaan ns. Full HD -tarkkuudeksi, joka on tällä kurssilla riittävä ja sopiva. Luonnollisesti voit valita paremmankin tarkkuuden (esimerkiksi Ultra HD, 4K), jos kuvamateriaalisi
on riittävän tarkkaa, ja tietokoneesi on riittävän tehokas. Ihanteellisessa tilanteessa kaikki lähdemateriaali on tällöin vähintään Full HD -resoluution tasoista materiaalia. Materiaalin resoluutio voi olla videoprojektin resoluutiota tarkempaa, ja siitä voi olla hyötyäkin esimerkiksi tilanteessa, jossa videota halutaan zoomata / rajata osa kuvasta.

<table style="border: 2px solid black;">
    <thead style="text-align: center;">
        <tr>
            <th>
                <img src="assets/images/opetusvideot/resoluutiot.jpg" alt="Resoluutiot">
            </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <i>Kuvio 1: 4K-tarkkuus sisältää nelinkertaisen määrän kuvapikseleitä verrattuna Full HD (1920 x 1080) tarkkuuteen.
                </i>
            </td>
        </tr>
    </tbody>
</table>

### Projektin kuvataajuus (frame rate)

Valitse _Timeline Frame Rate_ -kohdasta kuvataajuus.

Kuvataajuudella voi olla merkittävä vaikutus lopputulemaan ja katselukokemukseen. Alla on vertailu materiaalista, josta vasen on 25 fps (televisiossa käytettävä kuvataajuus) ja oikea on 60 fps (tyypillinen nykykameroiden kuvataajuus). Kannattaa katsoa video koko ruudun kokoisena, niin eron näkee paremmin.

[Katso video YouTubessa (kesto 00:13).](https://youtu.be/PRrcLdj6lZM)

<iframe width="560" height="315" src="https://www.youtube.com/embed/PRrcLdj6lZM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

Korkein mahdollinen kuvataajuus ei kuitenkaan ole itseisarvo. Kuvataajuuden valintaan vaikuttaa muutama asia, jotka tulee ottaa huomioon.

<ol>
    <li>Lähdemateriaalin kuvataajuus. Mikäli lähdemateriaali on kuvattu tietyllä kuvataajuudella, on hyvä lähtökohta valita kyseinen kuvataajuus myös projektille. Vain harvoissa tilanteissa on hyötyä valita sitä korkeampaa kuvataajuutta. Esimerkiksi jos kaikki
        lähdevideot on kuvattu 30 fps:llä, projektin määritteleminen 60 fps:ksi tulee kasvattamaan lopullisen videon kokoa noin kaksinkertaiseksi. Teoriassa tässä ainoa näkyvä hyöty (verrattuna 30 fps:ään) olisi transitioiden ja efektien sulavampi liike.
    </li>
    <li>Videon tarkoitus. Elävää kuvaa ja paljon liikettä sisältävät videot halutaan yleensä toistaa korkeammalla kuvataajuudella (esimerkiksi 60 fps), jotta liike toistuu luonnollisena, olettaen että lähdemateriaali on kuvattu riittävän korkealla kuvataajuudella.
        Powerpoint-esityksessä, joka ei sisällä runsaasti liikettä, kuvataajuus on kuitenkin likimain yhdentekevä, joten alhainenkin kuvataajuus (esimerkiksi 15 fps) saattaa riittää kohdeyleisölle hyvin.</li>
    <li>Kohdealustan rajoitukset esimerkiksi tiedostokoolle. Kuvataajuuden vaikutus videon tiedoston kokoon on suora: Taajuuden kaksinkertaistaminen (esim. 15 -&gt; 30, tai 30 -&gt; 60) likimain tuplaa videotiedoston koon. Mikäli tiedoston koko halutaan saada
        mahdollisimman pieneksi, voi kuvataajuutta joutua pienentämään. Tiedostokokoa voi pienentää myös lisäämällä pakkauksen tehokkuutta (ks. alaluku deliver>Valmiin videon toimittaminen</a>)</li>
</ol>

Selvitä lähdemateriaalisi kuvataajuus ennen videoprojektin kuvataajuuden päättämistä.

Jotkin kamerat valitettavasti piilottavat kuvaushetkellä videon kuvataajuuden tehokkaasti. iPhone-puhelimessa kuvataajuus näkyy uudessa iOS-versiossa selkeästi Kamera-sovelluksessa, mikä on positiivinen uudistus. Läheskään kaikissa kameroissa näin ei kuitenkaan ole. Mikäli et ole varma millä kuvataajuudella lähdemateriaali on kuvattu, voit selvittää sen käyttöjärjestelmän tiedostoselaimesta:

- Windows: Klikkaa tiedostoa hiiren oikealla -&gt; Ominaisuudet (Properties) -&gt; Tiedot -&gt; Kuvataajuus.</li>
- macOS: Avaa video Quicktime Playerissa -&gt; Ikkuna -&gt; Näytä elokuvainspektori.</li>

Mikäli lähdemateriaalisi on kuvattu usealla eri kuvataajuudella, pohdi yllä olevan listan kohtia 2 ja 3 ja valitse kuvataajuus niiden perusteella.

Mielenkiintoista kyllä, Resolvessa ei toimitettavan videon kuvataajuutta voi myöskään alentaa Deliver-kohdassa (ks. alaluku Deliver). Periaatteessa kuvataajuutta voi alentaa jälkikäteen muilla keinoilla, kuten pakkaamalla videon uudelleen Handbrake-ohjelmalla.

On kuitenkin parasta tähdätä alusta alkaen siihen kuvataajuuteen, joka projektille halutaan.

Muihin asetuksiin ei tarvitse tämän kurssin puitteissa koskea. Jos tietokoneellasi on vaikeuksia pyörittää projektin esikatselukuvaa, voit kokeilla laskea Video Monitoring -kohdasta Video format -valintaa alhaisemmalle tarkkuudelle (oletuksena HD 1080i
60).

## Resolve-ohjelman käyttöliittymä

Alalaidassa olevilla painikkeilla (Media, Cut, Edit, ...) siirrytään projektissa tilasta toiseen. Työskentely alkaa alkuperäisen materiaalin tuomisella (Media), jonka jälkeen siirrytään leikkausvaiheeseen (Cut). Tämän jälkeen alkaa tarkempi editointi
(Edit) ja niin edelleen. Viimeisenä vaiheena on valmiin videon toimittaminen lopulliseksi videotiedostoksi (Deliver). Tässä materiaalissa käsitellään vain osa näistä toiminnoista.

Resolve-ohjelmaan on tullut muutamia päivityksiä näiden videoiden julkaisemisen jälkeen, joten käyttöliittymä ei välttämättä näytä täysin samalta kaikin osin.

## Materiaalin tuominen projektiin (Media)

Lähdemateriaali tuodaan Media Pool -kokoelmaan, josta se sitten myöhemmin järjestellään aikajanalle. Materiaalin tuomiseksi Media Pool -kokoelmaan valitse File -&gt; Import file -&gt; Import media. Voit myös raahata tiedostoja Resurssienhallinnasta / Finderista suoraan mediakokoelmaan.

[Katso video YouTubessa (kesto 01:29).](https://youtu.be/gIOev483QXw)

<iframe width="560" height="315" src="https://www.youtube.com/embed/gIOev483QXw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

## Vielä lähdemateriaalista ja kuvataajuudesta

Kun ensimmäisen kerran tuot lähdemateriaalia Media Pool -kokoelmaan, ohjelma saattaa ilmoittaa:

> The clip(s) have a different frame rate than the current project settings. Would you like to change your timeline frame rate and video format to match?

Tämä tarkoittaa sitä että tuodun materiaalin kuvataajuus ja projektin aikajanan kuvataajuus eivät täsmää. Jos vastaat tähän kysymykseen Change (eli kyllä), aikajanan kuvataajuus muutetaan samaksi kuin lähdemateriaalisi kuvataajuus. Mikäli valitset Don't Change (eli ei), aikajanan kuvataajuus jätetään siihen asetukseen joka se alunperinkin oli, ja tällöin materiaalin kuvataajuus ei vastaa aikajanaa. **Tämä on tärkeä kohta, ja on tärkeää, että tiedostat millä tavalla valitseminen vaikuttaa lopulliseen videoon.** Jos et ole varma mitä sinun tulisi valita, palaa tämän ohjeen kohtaan Projektin kuvataajuus ja pohdi asiaa uudelleen. Todennäköisesti turvallisin valinta tässä on kuitenkin Kyllä.

## Aikajanan käyttö ja leikkaaminen (Edit)

Resolvessa editointia voi tehdä sekä Cut- että Edit-toiminnoissa. Cut on tarkoitettu nopeaan ja suoraviivaiseen editointiin. Edit-toimintoa käytetään, kun halutaan tehdä hieman monimutkaisempaa editointia, kuten lisätä tekstejä, siirtymiä ja käyttää avainruutuja. Tässä ohjeessa keskitytään **Edit-toimintoon**, mutta voit omatoimisesti kokeilla myös Cut-toimintoa.

**Materiaalin lisääminen aikajanalle**

Siirry Edit-tilaan.Raahaa video tai kuva aikajanalle (alla olevassa videossa ei ole ääntä). Voit raahata videon haluamallesi videoraidalle. Mikäli videoraitaa (ja vastaavasti audioraitaa) ei ole olemassa, uusi raita luodaan lennosta. Ylemmällä raidalla oleva materiaali (suurempi raidan tunniste, esimerkiksi Video 2) näkyy alemmalla raidalla (esimerkiksi Video 1) olevan materiaalin päällä. Audioraidoissa taas eri raidat summautuvat yhteen.

[Katso video YouTubessa (kesto 00:20).](https://youtu.be/_zWWJaOO-9I)

<iframe width="560" height="315" src="https://www.youtube.com/embed/_zWWJaOO-9I" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

Aikajanaa katsellaan painamalla play-painiketta tai välilyöntiä näppäimistöllä. Saat aikajanan koko näytön kokoiseksi esikatseluksi painamalla näppäimistöltä P. Paina uudestaan P niin pääset takaisin.

**Leikkaaminen**

Voit leikata joko (i) raahaamalla klippien päistä, tai (ii) käyttämällä partaterä-työkalua (Blade Edit Mode).

Leikkauksen jälkeen klippien väliin saattaa jäädä tyhjää. Voit poistaa sen klikkaamalla tyhjästä kohdasta hiiren oikealla ja sitten Ripple Delete.

[Katso video YouTubessa (kesto 01:48).](https://youtu.be/JMq_jZyi7bI)

<iframe width="560" height="315" src="https://www.youtube.com/embed/JMq_jZyi7bI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

**Klipin siirtäminen aikajanalla**

Pidä näppäimistöllä pohjaan painettuna Ctrl- ja Shift-näppäimet (macOS:ssa Cmd ja Shift) ja raahaa haluamasi klippi / klipit valitsemaasi kohtaan.

[Katso video YouTubessa (kesto 01:49).](https://youtu.be/jPXwaqA9Zd8)

<iframe width="560" height="315" src="https://www.youtube.com/embed/jPXwaqA9Zd8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

**Materiaalin lisääminen aikajanalle, kun resoluutio tai kuvasuhde ei täsmää**

Jos lisättävän materiaalin resoluutio tai kuvasuhde ei täsmää projektin asetusten kanssa, materiaali ei täytä koko videon kuva-alaa, tai materiaalista voi epätoivotusti leikkautua osa pois. Tällaisessa tilanteessa voit skaalata materiaalin haluamallasi tavalla. Valitse skaalattava klippi, sitten Inspector -&gt; Retime and Scaling -&gt; Scaling. Hyvä nyrkkisääntö on valita Fill, joka skaalaa materiaalin täyttämään koko aikajanan resoluution, mutta osa materiaalista saattaa leikkautua kuvan ulkopuolelle. Voit kokeilla myös muita skaalausmenetelmiä:<i>Fit</i>mahduttaa alkuperäisen kuvan videolle muuttamatta kuvasuhdetta, mutta reunoille voi jäädä mustat palkit.<i>Stretch</i>säilyttää alkuperäisen kuvan materiaalin, mutta muuttaa kuvasuhdetta (eli venyttää kuvaa).<i>Fill</i>säilyttää kuvan muodon/kuvasuhteen, mutta, kuten sanottu, hävittää osan kuvamateriaalista.

Huomaa, että aina kun videon kokoa muutetaan, sen laatu väistämättä heikkenee. Parasta olisi, mikäli kaikki materiaali on resoluutioltaan (vähintään) yhtä tarkkaa, kuin aikajanan tarkkuus.

[Katso video YouTubessa (kesto 02:26).](https://youtu.be/Zrij7HHeXXE")

<iframe width="560" height="315" src="https://www.youtube.com/embed/Zrij7HHeXXE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

Voit halutessasi asettaa kaikille tuotaville materiaaleille saman "resolution mismatch" -asetuksen kohdasta File -&gt; Project Settings -&gt; Image scaling -&gt; Mismatched resolution files.

## Siirtymät ja tehosteet

**Siirtymä, ristihäivytys (crossfade)**

Yksinkertainen mutta tyylikäs tapa siirtyä klipistä toiseen on ristihäivytys (crossfade). Ristihäivytyksen (ja ylipäätään siirtymän) tekemiseksi lähde- ja kohdemateriaali tulee olla eri videoraidoilla. Aikajanalle syntyy automaattisesti uusi video- ja ääniraita, kun raahaat videon edellistä videoraitaa hieman ylemmäksi.

Ristihäivytys tehdään muokkaamalla ylemmällä videoraidalla olevan materiaalin läpinäkyvyyttä. Videon vasemmassa (ja oikeassa) yläreunassa on pienet säätimet, jolla videon läpinäkyvyyttä voidaan säätää ajan suhteen. Raahaa vasemman yläreunan säädintä oikealle päin säätääksesi ristihäivytyksen pituutta. Tuloksena on lineaarinen ristihäivytys, jossa läpinäkyvyysarvo muuttuu tasaisesti nollasta (täysin läpinäkymättömästä) sataan (täysin läpinäkyvään).

[Katso video YouTubessa (kesto 02:00).](https://youtu.be/TEHXHQ-j8pc")

<iframe width="560" height="315" src="https://www.youtube.com/embed/TEHXHQ-j8pc" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

**Siirtymätehosteet**

Siirtymätehosteet löytyvät Toolbox -&gt; Video Transitions -kohdasta. Käytä näitä harkiten, sillä siirtymätehosteet tekevät videon vaikutelmasta hyvin helposti amatöörimäisen.

Alla esimerkki, jossa edellä tehty crossfade-siirtymä otetaan pois ja tilalle laitetaan siirtymätehoste.

[Katso video YouTubessa (kesto 01:30).](https://youtu.be/96PyHWJiNBU")

<iframe width="560" height="315" src="https://www.youtube.com/embed/96PyHWJiNBU" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

**Nopeuden muuttaminen**

Voit nopeuttaa tai hidastaa videota klikkaamalla klipin päällä hiiren oikea -&gt; Retime Controls. Valitse prosenttilukeman vieressä oleva pieni kolmio ja haluamasi toistonopeus sieltä. Alle 100 prosentin nopeus hidastaa ja sitä suurempi nopeuttaa videota.

[Katso video YouTubessa (kesto 01:22).](https://youtu.be/elvl-XUg3Ig")

<iframe width="560" height="315" src="https://www.youtube.com/embed/elvl-XUg3Ig" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

## Äänen muokkaaminen

On varsin tärkeää, että ääniraita ei ole liian hiljainen tai voimakas. Valitettavasti Edit-välilehdellä ei ole helppoa tapaa tarkastella onko ääni "sopivan" voimakas. Tämä tapahtuukin käyttämällä Fairlight-välilehteä (musiikki-ikoni). Tarkkaillaan Loudness-mittaria, jonka pitäisi pysytellä mahdollisimman lähellä 0-tasoa. Otetaan esimerkki Taso 3 -tehtävän ääniraidasta (tässä ei kuulu ääni vaan näkyy vain pelkkä kuva):

<img src="assets/images/opetusvideot/loudness-1.gif" alt="Loudness-1" /><br>

Huomataan, että mittari on jatkuvasti keltaisen puolella, mikä on huono asia, koska musiikki on tällöin liian kovalla suhteessa standardiäänentasoon (lisätietoa kiinnostuneille: oletuksena Resolvessa on käytössä ITU-R BS.1770-1 standardin loudness; Jos haluat, voit myös klikata kolmen pisteen kautta Youtube-loudnessin käyttöön joka sallii vähän kovemman äänenpaineen).

Käydään säätämässä Edit-välilehden puolella äänen voimakkuutta. Muutetaan audioraidan voimakkuutta raahamalla audioraidan päällä olevaa käyrää alaspäin. Tämä muuttaa äänenvoimakkuutta koko klipin matkalla. Tehdään noin 10-12 desibelin hiljennys äänenvoimakkuuteen. Tässä joutuu vähän kokeilemaan mikä taso olisi sopiva ja tsekkaamaan tilanteen Loudness-mittarista

<img src="assets/images/opetusvideot/loudness-2.gif" alt="loudness-2" />

Palataan nyt Fairlight-välilehdelle.

<img src="assets/images/opetusvideot/loudness-3.gif" alt="loudness-2"/>

Nyt näyttää paljon paremmalta. Mittari kyllä käy välillä keltaisella, mutta tämä on OK, kunhan se ei siellä ole kovin pitkään. Huomautus 1.11.2023: Äänentason loudness-tarkastelu kyllä tehtiin mallivideossa (ääniraitaa hiljennettiin n. 13dB), mutta sitä ei videossa näytetty. Päivitän malliratkaisun videon myöhemmin...

Kiinnitä huomiota myös siihen, että äänenvoimakkuus pysyy tasaisena eri klippien välillä, ja hiljennä tai voimista eri klippejä tarpeen mukaan.

Audioraidan äänenvoimakkuuden muuttaminen yhden klipin sisällä (esim. fade in tai fade out -tyyppiset tilanteet): Pidä alt-näppäin (Windows) tai option-näppäin (macOS) painettuna. Lisää avainpisteitä käyrälle ja muuta äänenvoimakkuutta haluamaksesi.

<img src="assets/images/opetusvideot/hiljenna-audio-2.gif" alt="Audio keyframes" />

Voit myös poistaa linkityksen videon ja audion väliltä. Klikkaa videoklippiä hiiren oikealla ja klikkaa Link clips (jolloin valinta poistuu siitä kohdasta). Tämän jälkeen voit siirtää pelkkää audioraitaa irrallaan videoraidasta tai vaikkapa poistaa audioraidan kokonaan.

**Äänenvoimakkuuden normalisointi:** Äänenvoimakkuuden normalisoinnilla tarkoitetaan muuttamista tasolle, joka on "tyypillinen" normaalitaso. Siirry Fairlight-välilehdelle (alareunassa nuotin näköinen kuvake), klikkaa ääniraitaa ja valitse Normalize Audio Levels. Voit käyttää oletusvalintoja ja klikata Normalize. Tämä nostaa/laskee koko ääniraidan äänenvoimakkuuden oletuksena ns. -23 LUFS -tasolle. Tämä on tyypillinen taso, johon esim. podcastit ja voiceoverit normalisoidaan. Mikäli asia kiinnostaa enemmän, niin voit omatoimisesti tutkia netistä lisää Loudness-käsitteestä.

Jos et halua normalisoida koko ääniraitaa, voit toki tehdä sen haluamallesi klipille erikseen.

## Tekstit (Title)

Tekstejä kutsutaan videoeditoinnissa termillä Title. Tekstitystekstejä (Subtitles) emme tässä käsittele.

[Katso video YouTubessa (kesto 03:12).](https://youtu.be/-WLQlsHnEVw")

<iframe width="560" height="315" src="https://www.youtube.com/embed/-WLQlsHnEVw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

Lue lisätietoja tekstien lisäämisestä seuraavan linkin kautta (englanniksi).

<a href="https://motionarray.com/learn/davinci-resolve/davinci-resolve-titles-tutorial/#part-1-add-titles-to-a-davinci-resolve-project">https://motionarray.com/learn/davinci-resolve/davinci-resolve-titles-tutorial/#part-1-add-titles-to-a-davinci-resolve-project</a>

## Avainruudut (Keyframes)

Avainruutujen avulla halutun parametrin muutos voidaan tarkasti määrittää ajan suhteen. "Parametri" voi olla melkein mikä tahansa sellainen asia, jonka videolle pystyy tekemään, esimerkiksi sijainti, koko, kierto, tai vaikkapa efektin voimakkuus. Otetaan yksinkertainen esimerkki.

<img src="assets/images/opetusvideot/lääkäri.gif" alt="Lääkäri" />

Tehdään klippiin kierto siten, että lähtötilanteessa kierto on 0 astetta (eli "normaali"), sitten klippi kiertyy 180 astetta, palaten takaisin 0 asteeseen. Katso oheinen video.

[Katso video YouTubessa (kesto 01:38).](https://youtu.be/UvpLiHwMnBs")

<iframe width="560" height="315" src="https://www.youtube.com/embed/UvpLiHwMnBs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

Voit lisätä klippiin useisiin eri parametreihin kohdistuvia avainruutuja. Voit esimerkiksi muuttaa yhtäaikaisesti sekä kiertoa että sijaintia. Kokeile!

## Valmiin videon toimittaminen (Deliver)

Kun video on valmis katseltavaksi, valitse Deliver-kohta alapalkista.

Laita tiedostollesi sopiva nimi (Filename) ja valitse haluamasi sijainti omalla tietokoneellasi (Location).

Tiedostomuodoksi (Format) suositellaan tällä kurssilla mp4, koska se on hyvin yhteensopiva erilaisten järjestelmien kanssa. Koodeksiksi (Codec) valitaan H.264.

Resoluutio ja kuvataajuus tulevat automaattisesti aikajanan asetusten mukaisesti, joten niihin ei tarvitse koskea.

Quality-kohdassa valitaan videon bittivirran nopeus. Bittivirran nopeudella määritellään se kuinka paljon videota pakataan, eli kuinka iso osa videon yksityiskohdista hävitetään ja kuinka iso osa säilytetään alkuperäisessä muodossaan. Tällä valinnalla on suuri vaikutus videon laatuun.

Kohdassa on valittavana Automatic, jossa on karkea valikoima erilaisia laatuvalintoja (Best, Medium, Low ...). Bittivirran voi myös rajoittaa tiettyyn enimmäismäärään. Mitä pienempi luku, sitä pienempi tiedosto, ja huonompi laatu. Vastaavasti mitä suurempi luku, sitä isompi tiedosto, mutta myös parempilaatuinen video.

Tähän ei voi antaa mitään absoluuttista oikeaa lukua, mutta eläviin videoihin joissa on liikettä, esimerkiksi 5000 Kb/s tai 10000 Kb/s voi olla hyvä valinta. Ruutukaappausvideoihin, joissa tapahtuu vain "vähän asioita", kuten esimerkiksi powerpoint-esitys, voi hyvinkin riittää 1000 Kb/s ja video näyttää silti erinomaiselta.

Valittuasi haluamasi asetukset, klikkaa Add to Render Queue, ja sitten oikealta Start Render. "Renderöinnin" nopeus riippuu koneesi tehoista.

Seuraava video havainnollistaa videon pakkaamista ja bittinopeutta.

[Katso video YouTubessa (kesto 04:19).](https://youtu.be/r6Rp-uo6HmI")
