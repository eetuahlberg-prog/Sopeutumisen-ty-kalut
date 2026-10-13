# Yritysten sopeutumistyökalu

Yritysten työkalu on osa [Sopeutumisen työkalut](../README.md) -sivustoa. Sen avulla yritys voi arvioida toimintaansa vaikuttavia sää- ja ilmastoriippuvuuksia, fyysisiä ilmastoriskejä ja varautumisen nykytilaa sekä koota itselleen ensimmäiset varautumistoimet.

Työkalussa on toimialaan ja valittuihin riippuvuuksiin mukautuva arviointi. Se toimii alustavan riskienhallinnan ja keskustelun tukena, eikä korvaa yksityiskohtaista riskianalyysiä. Menetelmän lähdeperusta ja rajaukset kuvataan tiedostossa [LAHTEET-JA-RAKENNE.md](research/LAHTEET-JA-RAKENNE.md).

## Toiminnot

- Yrityksen riippuvuuksien ja ilmastoon liittyvien häiriöiden arviointi.
- Nykyisten varautumistoimien ja kehittämistarpeiden tarkastelu.
- Ensitoimien, vastuiden ja aikataulujen kokoaminen toimintalistaksi.
- Toimintalistan vienti Excel- tai tekstitiedostoksi sekä tulostaminen PDF-muotoon selaimessa.
- Koko arvion tallentaminen tekstitiedostoksi ja esimerkkitilanteen kokeilu.

## Toteutus

- `index.html`: sovelluksen käyttöliittymän perusrakenne.
- `style.css`: ulkoasu sekä navigointi takaisin yhteiselle aloitussivulle.
- `app.js`: arvioinnin käyttöliittymä ja toimintalogiikka.
- `data.js`: kysymys- ja toimenpideaineisto.
- `export-xlsx.js`: Excel-tiedoston muodostaminen selaimessa.
- `assets/`: sovelluksessa käytettävät tunnukset ja kuvat.
- `research/`: lähdeperusta, aineistorakenne ja kehittäjän automaattiset tarkistukset.

Vastaukset säilyvät vain avoimen sivun muistissa. Tallenna toimintalista tai arvio ennen sivulta poistumista. Työkalu ei lähetä vastauksia palvelimelle.

**Julkaisu ja ylläpito:** Yritysten työkalua ei julkaista erillisenä repositoriona, vaan yhteisen sivuston `/yritys/`-hakemistossa. Ks. [yhteinen README](../README.md) ja [julkaisuohje](../GITHUB-JULKAISUOHJE.md).

## Yhteinen ylätunniste ja vastuuhuomautus

Työkalu kuuluu yhteiseen Sopeutumisen työkalut -sivustoon. Ylätunnisteen mitoitus ja vastuuhuomautuksen ulkoasu on määritelty tiedostossa `../shared/tool-header.css`. Verkkosivun alatunniste sisältää hankkeen rahoituslausekkeen ja vastuuhuomautuksen.

## Ulkoasu

Fonttiperhe on **Corbel** (varafontit Segoe UI ja Arial). Fonttikoot
tulevat yhteisestä `../shared/typography.css`-tiedostosta. Yritysten pääväri on vihreä `#ADB150` (RGB 173, 177, 80).
Erillinen `theme.css` sisältää vihreän käyttöliittymäteeman.
