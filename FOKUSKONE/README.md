# FOKUSKONE

Keskittymisen työkalu ADHD-aivoille. Ajastin, reaaliajassa kasvava kasvi ja tekoälyapuri, joka pilkkoo jumin pienimmäksi mahdolliseksi ensiaskeleeksi.

Toimii selaimessa, puhelimessa ja työpöydällä. Ei tiliä, ei pilveä, ei seurantaa — kaikki data tallentuu vain omalle laitteelle.

---

## Julkaisu GitHubiin

1. Luo uusi repository, esim. `FOKUSKONE`.
2. Lataa sinne tämän kansion **kaikki tiedostot** (index.html, manifest.json, sw.js ja neljä png-ikonia).
3. Repositoryssa: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. Minuutin päästä osoite on `https://<käyttäjänimesi>.github.io/FOKUSKONE/`.

### Asennus laitteelle

- **iPhone / iPad:** avaa Safarissa → jakonappi → *Lisää kotivalikkoon*.
- **Android:** Chrome → valikko → *Asenna sovellus*.
- **Työpöytä:** Chrome/Edge → osoitepalkin asennuskuvake.

Asennettuna sovellus toimii myös ilman verkkoyhteyttä. Tekoälyapuri tarvitsee verkon, muu ei.

---

## Toiminnot

### Ajastin
Jaksot 5 / 10 / 25 / 45 / 90 min tai avoin jakso. Ajastin laskee aikaleimoista, joten se pysyy oikeassa vaikka vaihdat sovellusta tai ruutu sammuu.

### Visuaalinen dopamiini
Ruudulla kasvaa kasvi reaaliajassa: varsi nousee, lehdet aukeavat, lopussa puhkeaa kukka. Jokainen kasvi on siemenpohjainen, joten kahta samanlaista ei tule.

**Keskeinen ero Forestiin:** keskeytys **ei tapa kasvia**. Kasvi kasvaa täsmälleen niin pitkälle kuin ehdit ja jää puutarhaan. Rangaistus ei auta ADHD-aivoja, todiste edistymisestä auttaa.

### Apuri
Kuusi tilannetta: *Olen jumissa · Liian iso · Mitä ensin? · Ylikuormitus · Tylsä pakko · Suunnittele päivä*.

Apuri rakentaa kehotteen, jossa on mukana vireesi, päivän jaksot, putki ja tehtäväsi. Vastaus päättyy aina riviin `ASKEL:` — sovellus lukee sen ja tarjoaa nappia **"Aloita tämä nyt · 10 min"**, joka käynnistää ajastimen suoraan siitä. Jumista tekemiseen ilman välivaiheita.

Kaksi tapaa käyttää:

- **Ilman avainta (oletus):** kehote kopioituu leikepöydälle, viet sen Claudeen/Geminiin/ChatGPT:hen ja liität vastauksen takaisin.
- **Avaimella:** lisää ilmainen Gemini-avain ([aistudio.google.com/apikey](https://aistudio.google.com/apikey)) asetuksista, jolloin vastaus tulee suoraan sovellukseen. Avain säilyy vain omassa selaimessasi.

### Muut ADHD-tuet

| Toiminto | Mihin ongelmaan |
|---|---|
| **Vireystila** (🪫 / 🔋 / ⚡) | Sovellus ehdottaa vireeseen sopivia tehtäviä ja jakson pituutta. Terävää virettä ei kannata tuhlata sähköposteihin. |
| **Parkkipaikka** | Kesken jakson mieleen putkahtava ajatus napataan talteen ilman että jakso katkeaa. Ajatus lakkaa kiertämästä kun se on ulkona päästä. |
| **Aivotyhjennys** | Nopea kaatopaikka kaikelle mitä pyörii mielessä. Ajatuksen voi myöhemmin muuttaa tehtäväksi tai heittää pois. |
| **🐸 Sammakko** | Merkitse tehtävä jota vältät. Se nostetaan omaan laatikkoonsa muistutuksena: välttely maksaa enemmän energiaa kuin tekeminen. |
| **Aloitusrituaali** | Kolmen sekunnin lähtölaskenta madaltaa aloituskitkaa — vaikein kohta on aina alku. |
| **Keskeytyslaskuri** | Merkkaa keskeytykset yhdellä napilla. Tieto kertyy tilastoihin, ei syyllisyyteen. |
| **Hyperfokusvahti** | 45 minuutin välein muistutus juoda ja liikuttaa hartioita pitkissä jaksoissa. |
| **🆘 Hätäjarru** | Ylikuormitukseen: hengitysympyrä, pään tyhjennys ja pakotettu 5 minuutin mikrojakso. |
| **Taukoajastin** | Jakson jälkeen ohjattu 5 min tauko, jotta some ei syö juuri rakennettua fokusta. |
| **Anteeksiantava putki** | Aktiivisuusputki laskee päiviä, mutta yksikään näkymä ei rankaise keskeytyksestä. |

### Puutarha ja tilastot
Kokoelma kaikista kasveista, 12 viikon lämpökartta, viikkopalkit ja automaattiset havainnot: **paras keskittymistuntisi**, **kuinka suuren osan jaksoista viet loppuun**, **millä vireellä pisimmät jaksot syntyvät**. Jos loppuunvientiprosentti on matala, sovellus ehdottaa lyhyempää jaksoa.

---

## Näppäimet

- **Välilyönti** — aloita jakso
- **Esc** — sulje ikkuna

---

## Data

Kaikki tallentuu selaimen `localStorage`iin avaimella `fokuskone.v1`. Ota varmuuskopio asetuksista ennen laitteen tai selaimen vaihtoa — selaimen tyhjennys vie datan mukanaan.

---

## Muokkaus

Yksi tiedosto, ei riippuvuuksia, ei build-vaihetta. Avaa `index.html` editorissa ja muokkaa suoraan.

Hyödyllisiä kohtia:

- `:root` (rivi ~10) — värit
- `HINTS` — jakson aikana näkyvät lauseet
- `SITS` — apurin tilanteet ja niiden ohjeistus tekoälylle
- `VIRE_TIP` — vireystilan vinkit
- `drawPlant()` — kasvin ulkonäkö
- `buildPrompt()` — tekoälykehotteen runko

Jos muutat tiedostoja julkaisun jälkeen, nosta `sw.js`:n ensimmäisellä rivillä versionumeroa (`fokuskone-v1` → `v2`), muuten selain tarjoilee vanhaa välimuistiversiota.
