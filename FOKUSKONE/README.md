# FOKUSKONE

Keskittymisen työkalu ADHD-aivoille. Ajastin, reaaliajassa kasvava kasvi ja tekoälyapuri, joka pilkkoo jumin pienimmäksi mahdolliseksi ensiaskeleeksi.

Toimii selaimessa, puhelimessa ja työpöydällä. Ei tiliä, ei pilveä, ei seurantaa — kaikki data tallentuu vain omalle laitteelle.

---

## Julkaisu GitHubiin

Vie **tämän kansion kaikki tiedostot** repositoryn juureen, ei alikansioon.

1. Luo repository, esim. `FOKUSKONE`.
2. Raahaa tiedostot yksitellen latausikkunaan. Koko kansion raahaaminen säilyttää kansiorakenteen ja johtaa 404-virheeseen.
3. **Settings → Pages → Deploy from a branch → main → / (root) → Save**.
4. Osoite on minuutin päästä `https://<käyttäjänimesi>.github.io/FOKUSKONE/`.

### Asennus laitteelle

- **iPhone tai iPad:** avaa Safarissa, paina jakonappia ja valitse *Lisää kotivalikkoon*.
- **Android:** Chrome → valikko → *Asenna sovellus*.
- **Työpöytä:** Chrome tai Edge → osoitepalkin asennuskuvake.

Asennettuna sovellus toimii myös ilman verkkoyhteyttä. Vain tekoälyapuri tarvitsee verkon.

---

## Toiminnot

### Ajastin

Jaksot 5, 10, 25, 45 ja 90 minuuttia tai avoin jakso. Ajastin laskee aikaleimoista, joten se pysyy oikeassa, vaikka vaihtaisit sovellusta tai ruutu sammuisi.

### Niitty

Jakson aikana ruudulla kasvaa kasvi reaaliajassa: varsi nousee, lehdet aukeavat ja lopuksi puhkeaa kukka. Kukka jää niitylle.

Laji määräytyy jakson pituuden mukaan ja pysyy aina samana:

| Jakso | Laji |
|---|---|
| alle 10 min | ketoneilikka, kissankello |
| 10–20 min | päivänkakkara, ruiskaunokki |
| 21–49 min | ahdekaunokki, nurmikaunokki |
| 50 min tai yli | maarianohdake |

Niityllä lentää perhonen jokaista täyttä putkiviikkoa kohden, enintään viisi.

Napauta kukkaa, niin näet mistä jaksosta se kasvoi.

**Keskeinen ero Forestiin:** keskeytys **ei tapa kasvia**. Kukka kasvaa täsmälleen niin pitkälle kuin ehdit ja jää niitylle sellaisena. Rangaistus ei auta ADHD-aivoja, mutta todiste edistymisestä auttaa.

### Apuri

Kuusi tilannetta: *Olen jumissa · Liian iso · Mitä ensin? · Ylikuormitus · Tylsä pakko · Suunnittele päivä*.

Apuri rakentaa kehotteen, jossa on mukana vireesi, päivän jaksot, putki ja tehtäväsi. Vastaus päättyy aina riviin `ASKEL:`, jonka sovellus lukee ja tarjoaa nappia **"Aloita tämä nyt · 10 min"**. Se käynnistää ajastimen suoraan siitä askeleesta — jumista tekemiseen ilman välivaiheita.

Kaksi tapaa käyttää:

- **Ilman avainta (oletus):** kehote kopioituu leikepöydälle, viet sen Claudeen, Geminiin tai ChatGPT:hen ja liität vastauksen takaisin.
- **Avaimella:** lisää ilmainen Gemini-avain ([aistudio.google.com/apikey](https://aistudio.google.com/apikey)) asetuksista, jolloin vastaus ilmestyy suoraan sovellukseen. Avain säilyy vain omassa selaimessasi.

### Muut ADHD-tuet

| Toiminto | Mihin ongelmaan |
|---|---|
| **Vire** (🪫 / 🔋 / ⚡) | Sovellus ehdottaa vireeseen sopivia tehtäviä ja jakson pituutta. Terävää virettä ei kannata tuhlata sähköposteihin. |
| **Parkkipaikka** | Kesken jakson mieleen putkahtava ajatus napataan talteen ilman että jakso katkeaa. Ajatus lakkaa kiertämästä, kun se on ulkona päästä. |
| **Aivotyhjennys** | Nopea kaatopaikka kaikelle, mikä pyörii mielessä. Ajatuksesta voi myöhemmin tehdä tehtävän tai päästää siitä irti. |
| **🐸 Sammakko** | Merkitse tehtävä, jota vältät. Se nostetaan omaan laatikkoonsa muistutukseksi: välttely syö enemmän energiaa kuin tekeminen. |
| **Aloitusrituaali** | Kolmen sekunnin lähtölaskenta madaltaa aloituskynnystä. Vaikein kohta on aina alku. |
| **Keskeytyslaskuri** | Merkitset keskeytykset yhdellä napilla. Tieto kertyy tilastoihin, ei syyllisyyteen. |
| **Hyperfokusvahti** | Muistuttaa 45 minuutin välein juomaan ja liikuttamaan hartioita pitkissä jaksoissa. |
| **🆘 Hätäjarru** | Ylikuormitukseen: hengitysympyrä, pään tyhjennys ja pakotettu viiden minuutin mikrojakso. |
| **Taukoajastin** | Jakson jälkeen ohjattu viiden minuutin tauko, jotta some ei syö juuri rakennettua keskittymistä. |
| **Anteeksiantava putki** | Putki laskee päiviä, mutta yksikään näkymä ei rankaise keskeytyksestä. |

### Tilastot

Kahdentoista viikon lämpökartta, viikkopalkit ja automaattiset havainnot: **paras keskittymistuntisi**, **kuinka suuren osan jaksoista viet loppuun** ja **millä vireellä pisimmät jaksot syntyvät**. Jos loppuunvientiprosentti on matala, sovellus ehdottaa lyhyempää jaksoa.

---

## Näppäimet

- **Välilyönti** — aloita jakso
- **Esc** — sulje ikkuna

---

## Data

Kaikki tallentuu selaimen `localStorage`iin avaimella `fokuskone.v1`. Ota varmuuskopio asetuksista ennen laitteen tai selaimen vaihtoa: selaimen tyhjennys vie datan mukanaan.

---

## Muokkaus

Yksi tiedosto, ei riippuvuuksia, ei build-vaihetta. Avaa `index.html` editorissa.

Hyödyllisiä kohtia:

- `:root` — värit
- `HINTS` — jakson aikana näkyvät lauseet
- `SITS` — apurin tilanteet ja niiden ohjeistus tekoälylle
- `VIRE_TIP` — vireen vinkit
- `TIERSP` ja `TIERR` — jakson pituutta vastaavat lajit ja kukkien koot
- `drawHead` — yksittäisten lajien piirto
- `drawMeadow` — niityn sommittelu, heinät, siitepöly ja perhoset
- `drawPlant` — jakson aikana kasvava kasvi
- `buildPrompt` — tekoälykehotteen runko

Jos muutat tiedostoja julkaisun jälkeen, nosta `sw.js`:n ensimmäisellä rivillä versionumeroa (`fokuskone-v1` → `v2`). Muuten selain tarjoilee vanhaa välimuistiversiota.
