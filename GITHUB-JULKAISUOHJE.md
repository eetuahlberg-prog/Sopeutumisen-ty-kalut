# GitHub Pages - julkaisuohje

## GitHub Pages – julkaisu

1. Kirjaudu GitHubiin ja luo yksi uusi **julkinen** repositorio: oikean yläkulman **+ → New repository**. Anna nimeksi esimerkiksi `sopeutumisen-tyokalut`, valitse **Public** ja paina **Create repository**. Voit käyttää myös olemassa olevaa repositoriota, mutta **älä korvaa toimivaa julkaisua ennen kuin uusi versio on testattu**.
2. Pura toimitettu ZIP tietokoneelle (Windows: napsauta ZIPiä hiiren oikealla → **Pura kaikki**). Avaa luotu kansio ja siirrä **sen sisältö** GitHubin repositorion `main`-haaran juureen. GitHubissa **Add file → Upload files** (tyhjässä repositoriossa **uploading an existing file**), raahaa kansiot `assets`, `kunta` ja `yritys` sekä juuren tiedostot `index.html`, `style.css`, `.nojekyll` ja README. **Älä lataa ZIP-tiedostoa sellaisenaan, eikä ylimääräistä pääkansiota.**
3. Kirjoita sivun alareunan **Commit changes** -kenttään esimerkiksi "Julkaise Sopeutumisen työkalut" ja tallenna tiedostot. Avaa **Settings → Pages**. Valitse **Source: Deploy from a branch**, haaraksi **main** ja kansioksi **/(root)**. Paina **Save** ja odota julkaisua.
4. Avaa **Settings → Pages → Visit site**. Osoite on yleensä `https://KAYTTAJA.github.io/sopeutumisen-tyokalut/` (jos repositoriolla on tuo nimi). Julkaisu voi kestää muutaman minuutin. Jos näet vanhan version, kokeile Ctrl+F5.
5. Tarkista aloitussivun molemmat valintakortit, kuntien ja yritysten paluulinkit sekä kummankin työkalun raportti- ja vientitoiminnot. Tarkista myös mobiilinäkymä. Julkaisun jälkeiset tarkistukset löytyvät `TESTAUS.txt`-tiedostosta.

**Huom.** Julkaisu ei tapahdu automaattisesti tätä ZIP-tiedostoa lataamalla. Yksikään GitHub-repositorio ei muutu, ennen kuin viet tiedostot sinne.

Lisätiedot: [README.md](README.md). Julkaisun jälkeinen testaus: `TESTAUS.txt`.
