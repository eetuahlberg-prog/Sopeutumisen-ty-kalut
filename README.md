# Sopeutumisen työkalut – yhteinen GitHub Pages -sivusto

Käyttövalmis, staattinen Pohjois-Karjalan ilmastonmuutokseen sopeutumisen työkalusivusto. Sivustolla on yhteinen aloitussivu ja kaksi olemassa oleviin työkaluihin perustuvaa, toisistaan riippumatonta näkymää. Aloitussivun ingressi on: "Työkalut auttavat kuntia ja yrityksiä tunnistamaan omaan toimintaansa vaikuttavia ilmastoriskejä ja löytämään käytännön toimenpiteitä niihin varautumiseksi."

## Sivurakenne

```
index.html              Yhteinen aloitussivu: valitse Kunnille tai Yrityksille
style.css               Aloitussivun ulkoasu: metsäkuva, punainen/valkoinen brändi
GITHUB-JULKAISUOHJE.md    Erillinen lyhyt julkaisuohje
assets/                 Aloitussivun logot ja metsätaustakuva (metsa.jpg)
kunta/index.html        Kuntien Sopeutumispolku
kunta/app.js            Kuntien työkalun alkuperäinen toiminnallisuus
kunta/data.js           Kuntien kysymykset ja toimet
kunta/style.css         Kuntien työkalun alkuperäinen tyyli + paluulinkki
kunta/assets/           Kuntien alkuperäiset logot
yritys/index.html       Yrityksen ilmastoriskit
yritys/app.js            Yritysten työkalun alkuperäinen toiminnallisuus
yritys/data.js           Yritysten kysymykset ja toimet
yritys/export-xlsx.js    Yritysten Excel-vienti
yritys/style.css         Yritysten työkalun alkuperäinen tyyli + paluulinkki
yritys/assets/           Yritysten alkuperäiset logot
yritys/research/         Yritystyökalun lähde- ja testiaineistot
.nojekyll               GitHub Pagesin asetus
```

Molemmat mikrotyökalut ovat 8.10.2026 valmistuneista julkaisu-ZIP-paketeista. Niiden `app.js`, `data.js` ja yrityksen `export-xlsx.js` sekä niiden omat kuvat ovat **muuttumattomat**. Työkalujen HTML:ään on lisätty yksi paluunavigaatio ja poistettu paikallisen fontin esilataus. CSS:n loppuun on lisätty vain paluulinkin tyylit ja alkuperäiset `@font-face`-määritykset on poistettu, koska fonttitiedostoja ei jaeta. Työkalujen kysymykset, kohdennus, tilanhallinta ja tallennus-/tulostustoiminnot säilyvät sellaisinaan. Versiotiedot pysyvät mikrosovellusten omissa näkymissä.

## GitHub Pages – julkaisu

1. Kirjaudu GitHubiin ja luo yksi uusi **julkinen** repositorio: oikean yläkulman **+ → New repository**. Anna nimeksi esimerkiksi `sopeutumisen-tyokalut`, valitse **Public** ja paina **Create repository**. Voit käyttää myös olemassa olevaa repositoriota, mutta **älä korvaa toimivaa julkaisua ennen kuin uusi versio on testattu**.
2. Pura toimitettu ZIP tietokoneelle (Windows: napsauta ZIPiä hiiren oikealla → **Pura kaikki**). Avaa luotu kansio ja siirrä **sen sisältö** GitHubin repositorion `main`-haaran juureen. GitHubissa **Add file → Upload files** (tyhjässä repositoriossa **uploading an existing file**), raahaa kansiot `assets`, `kunta` ja `yritys` sekä juuren tiedostot `index.html`, `style.css`, `.nojekyll` ja README. **Älä lataa ZIP-tiedostoa sellaisenaan, eikä ylimääräistä pääkansiota.**
3. Kirjoita sivun alareunan **Commit changes** -kenttään esimerkiksi "Julkaise Sopeutumisen työkalut" ja tallenna tiedostot. Avaa **Settings → Pages**. Valitse **Source: Deploy from a branch**, haaraksi **main** ja kansioksi **/(root)**. Paina **Save** ja odota julkaisua.
4. Avaa **Settings → Pages → Visit site**. Osoite on yleensä `https://KAYTTAJA.github.io/sopeutumisen-tyokalut/` (jos repositoriolla on tuo nimi). Julkaisu voi kestää muutaman minuutin. Jos näet vanhan version, kokeile Ctrl+F5.
5. Tarkista aloitussivun molemmat valintakortit, kuntien ja yritysten paluulinkit sekä kummankin työkalun raportti- ja vientitoiminnot. Tarkista myös mobiilinäkymä. Julkaisun jälkeiset tarkistukset löytyvät `TESTAUS.txt`-tiedostosta.

**Huom.** Julkaisu ei tapahdu automaattisesti tätä ZIP-tiedostoa lataamalla. Yksikään GitHub-repositorio ei muutu, ennen kuin viet tiedostot sinne.

## Paikallinen kokeilu

Pura ZIP ja avaa sen juuren `index.html` selaimessa. Molempien työkalujen tavalliset näkymät toimivat myös tiedostosta käsin. Joidenkin selainten leikepöytäominaisuudet voivat edellyttää HTTPS:ää tai paikallista HTTP-palvelinta. Voit kokeilla suoraan HTTP-palvelimella:

```bash
python -m http.server 8000
```

Avaa sitten `http://localhost:8000/`.

## Tiedot, lataukset ja navigointi

- Arvion tiedot ovat kunkin avoimen työkalusivun muistissa. **Aloitussivulle palaaminen tai sivun päivitys hävittää keskeneräiset tiedot.** Siksi tallenna raportti ensin. Alkuperäisiin sovelluksiin ei lisätty automaattista tallennusta.
- Kunnan työkalusta saa oman suunnitelman TXT-/CSV-muodossa tai selaimen PDF-tulosteena. Yrityksen työkalussa ovat sen nykyiset Excel-/teksti-/PDF-viennit.
- Työkalut eivät lähetä käyttäjän vastauksia palvelimelle, eivätkä käytä erillistä tietokantaa, palvelinlogiikkaa, kirjautumista tai ulkoisia JavaScript-kirjastoja.
- Sivuston eri polut käyttävät **suhteellisia** asset-polkuja. Se toimii GitHub Pagesin repositorio-osoitteessa myös ilman omaa verkkotunnusta.
- Yhteisen sivun Ilmastovisio-logo on toimitetusta alkuperäisestä läpinäkyvästä PNG-tiedostosta. Pohjois-Karjalan ja EU:n tunnukset on kopioitu alkuperäisistä työkaluista. Aloitussivun metsätaustakuva on käyttäjän toimittamasta Metsä 1.jpg -kuvasta. Ylätunnukset ovat punaisella ja valkoisella pohjalla, rahoitusteksti on alapalkissa. Aloitussivun valintojen näkyvät nimet ovat "Kunnille" ja "Yrityksille"; työkalujen sisäisiä alkuperäisiä tuotenimiä ei muutettu, jotta niiden toiminta pysyy ennallaan. Varsinaisia fonttitiedostoja ei jaeta paketissa; selaimet käyttävät asennettua Ubuntu-fonttia tai alkuperäisen CSS:n varafontteja.

## Päivitykset jatkossa

Päivitä kunnan työkalu vaihtamalla tiedostot **vain** `kunta/`-kansioon, ja yrityksen työkalu vaihtamalla tiedostot **vain** `yritys/`-kansioon. Vältä yhden työkalun `app.js`-/`data.js`-tiedostojen siirtämistä toisen kansioon. Säilytä yhdistetyissä `index.html`-tiedostoissa `suite-nav`-navigaatio ja `style.css`-tiedostojen lopussa siihen liittyvät tyylit, kun korvaat tiedostoja myöhemmillä versioilla.

Jos nykyisiin kahteen erilliseen GitHub Pages -sivustoon on jo jaettu linkkejä, päätä niiden uudelleenohjauksista erikseen. Tämän paketin sisältö ei tee muutoksia vanhoihin verkkosivustoihin eikä luo automaattisia uudelleenohjauksia.

## Testaus

Yhdistetyn sivuston kolme sivupolkua ja 18 HTML-linkki-/resurssiviitettä tarkistettiin paikallisella HTTP-palvelimella. Kuntien ja yritysten alkuperäiset JavaScript- ja aineistotiedostot varmistettiin muuttumattomiksi, ja yritystyökalun mukana olevat Node.js-testit läpäisivät tarkistukset. Varsinainen graafinen Chromium-selaintestaus estyi testiympäristön käyttörajoituksiin. Tarkista ulkoasu, mobiilikäyttö ja vientitoiminnot julkaistulla GitHub Pages -sivustolla. GitHub Pages -julkaisu on testattava käyttäjän omassa repositoriossa. Yritystyökalun alkuperäiset testit sijaitsevat `yritys/research/`-kansiossa: `node research/check.mjs` ja `node research/check-exports.mjs`, suoritettuna `yritys`-kansiossa.

Työkalut ovat valmistelu- ja keskustelutukea, eivät sertifioituja ilmastoriskien arviointijärjestelmiä.
12.10.2026
