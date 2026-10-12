# Kuntien sopeutumistyökalu

Kuntien työkalu on osa [Sopeutumisen työkalut](../README.md) -sivustoa. Se auttaa tunnistamaan kunnan toimintaympäristöön liittyviä sopeutumistarpeita, tarkastelemaan toimenpide-ehdotuksia ja kokoamaan oman toimenpidesuunnitelman.

Työkalun sisältöpohjana ovat Pohjois-Karjalan ilmastonmuutokseen sopeutumisen tiekartta ja sen seutukuntaliite (2025). Kunnan tilanteen perusteella muodostuvat ehdotukset ovat valmistelun apuvälineitä: toteutuksen tarkoituksenmukaisuus arvioidaan kunnassa erikseen.

## Toiminnot

- Kunnan tilanteen arviointi ja esimerkkikunnan kokeilu.
- Soveltuvien sopeutumistoimien tarkastelu perusteluineen ja lähteineen.
- Oman toimenpidesuunnitelman kokoaminen ja muokkaaminen.
- Suunnitelman vienti TXT- ja CSV-tiedostoksi sekä tulostaminen PDF-muotoon selaimessa.

## Toteutus

- `index.html`: sovelluksen käyttöliittymän perusrakenne.
- `style.css`: ulkoasu sekä navigointi takaisin yhteiselle aloitussivulle.
- `app.js`: käyttöliittymän toiminta ja toimenpiteiden kohdentaminen.
- `data.js`: kysymys- ja toimenpideaineisto.
- `assets/`: sovelluksessa käytettävät tunnukset ja kuvat.

Vastaukset säilyvät vain avoimen sivun muistissa. Tallenna suunnitelma ennen sivulta poistumista. Työkalu ei lähetä vastauksia palvelimelle.

**Julkaisu ja ylläpito:** Kuntien työkalua ei julkaista erillisenä repositoriona, vaan yhteisen sivuston `/kunta/`-hakemistossa. Ks. [yhteinen README](../README.md) ja [julkaisuohje](../GITHUB-JULKAISUOHJE.md).

## Yhteinen ylätunniste ja vastuuhuomautus

Työkalu kuuluu yhteiseen Sopeutumisen työkalut -sivustoon. Ylätunnisteen mitoitus ja vastuuhuomautuksen ulkoasu on määritelty tiedostossa `../shared/tool-header.css`. Verkkosivun alatunniste sisältää hankkeen rahoituslausekkeen ja vastuuhuomautuksen.
