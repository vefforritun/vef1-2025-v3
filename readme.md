# Vefforritun 1, 2025: Verkefni 3, CSS #1

## Markmið

- Tengja CSS við HTML.
- Aðlaganir á HTML fyrir CSS.
- Notkun á grunn CSS með box model; visual formatting model og; letri og litum.

## Verkefni 2–6

Í verkefnum 2–6 munum við vinna áfram með sama verkefni og byggja ofan á það:

- [Verkefni 2](https://github.com/vefforritun/vef1-2025-v2) skilgreinir grunn HTML og síður.
- [Verkefni 3](https://github.com/vefforritun/vef1-2025-v3) bætir við grunn viðmóti.
- [Verkefni 4](https://github.com/vefforritun/vef1-2025-v4) setur upp útlit (e. layout).
- [Verkefni 5](https://github.com/vefforritun/vef1-2025-v5) setur upp grind og gerir útlit skalanlegt (e. responsive).
- [Verkefni 6](https://github.com/vefforritun/vef1-2025-v6) setur upp tól til að hjálpa við skipulag og vinnu.

## Lýsing

Verkefnið er framhald af [verkefni 2](https://github.com/vefforritun/vef1-2025-v2), nýtir það efni sem uppsett er í því, og fylgir þeirri verkefnalýsingu. Leyfilegt er að nota [sýnilausn að verkefni 2](https://github.com/vefforritun/vef1-2025-v2-synilausn), sem gefin verður út föstudaginn 5. september.

Nú skal bæta við einföldu útliti á efnið með CSS. Allt útlitið skal vera í `./styles.css` og **allar** HTML skrár skulu vísa í nákvæmlega þá skrá.

Bæta þarf við auka elementum við lausn/sýnilausn til að geta náð fram útliti, sjá grunn sem gefinn er fyrir HTML.

Þar sem allt útlit skal útfæra í einni CSS skrá, skal huga að cascade og erfðum, þó er fullkomlega eðlilegt að endurtaka eigindi, en t.d. fyrir málsgreinar (`<p>`) þarf aðeins að taka fram einu sinni hvert margin þeirra er.

### Grunnur

Gefinn er HTML grunnur í `index.html` sem byggir á sýnilausn en ekki er allt til staðar sem er í sýnilausn.

Gefið er `styles.css` skjal með grunn að lausn og athugasemdum.

Almennt skal gilda:

- Nota skal gefið „reset“ og `box-sizing` breytingu (merkt sérstaklega), það má ekki fjarlægja.
- Nota skal leturgerðirnar:
  - [Atkinson Hyperlegible Mono](https://fonts.google.com/specimen/Atkinson+Hyperlegible+Mono) frá Google fonts fyrir fyrirsagnir, eingöngu í _regular_.
  - [Gelasio](https://fonts.google.com/specimen/Gelasio) frá Google fonts sem _variable font_ fyrir allt annað, bæði _regular_ (þyngd `400`) og _bold_ (þyngd `700`).
  - Sækja skal leturgerðirnar (download) _ekki_ með vísun og nota `@font-face` í CSS.
- Gefin er stærð á letri sem `16px` (sem merkir að `1rem == 16px`), því skal ekki breyta. Í framhaldi af lýsingu er `eitt bil = 1rem`, `hálft bil = 0.5rem` o.s.fr.
- Gefin er hjálparklasi `.sr-only` sem skal setja á `Beint í efni` tengil.
- Aðeins skal nota `px` í grunnleturstærð og á `border` skilgreiningar, annars skal nota hlutfallslegar einingar (`em`, `rem`, eða `%`)
- Allt efni (málsgreinar, myndir, form element) skal hafa eitt bil fyrir neðan sig.
  - Á fyrirmyndum gæti þetta verið óljóst og þarf ekki að vera nákvæmlega eins og á fyrirmyndum. Í nákvæmri lýsingu á útliti kemur fram ef vikið er frá þessu.
- Almennt er bakgrunns litur hvítur (`#ffffff`) og texta litur svartur (`#000000`).
- Allir litir: `#ff9999`, `#000000` og `#ffffff`.
- CSS skal vera án villna og **viðvarana** þegar keyrt í gegnum [CSS validator](https://jigsaw.w3.org/css-validator/), einnig hægt að keyra gegnum W3C Validator extension.

Allt sem gildir í verkefni 2 gildir áfram í þessu verkefni.

## Útlit

Fyrirmynd að útliti er í `fyrirmynd/` möppu. Öll skjáskot eru tekin í `1000px` breiðum Firefox vafra. Útlit þarf eingöngu að virka vel í þeirri breidd, sérstaklega í minniskjám má lausn vera brotin.

### Meginmál

Gefinn er `flexbox` skilgreining sem sett er utan um allt efni, sjá athugasemdir í `styles.css`. Setja þarf `<div class="wrapper">` eftir `<body>` og `</div>` fyrir neðan allt efni. Athugið að til þess að fá fasta valmynd þarf að breyta uppsetningu í HTML, sjá uppsetningu í `index.html`.

Þetta mun sjá til þess að efni fylli nákvæmlega út í skjá, fótur sé alltaf neðst og efni taki allt auka pláss. Nánar um þetta í viku 4.

Allt efni á að vera að hámarki `900px` breitt og miðjað í vafra, auka pláss vinstra og hægra megin skal sjálfkrafa vera útdeilt.

### Valmynd

- Valmynd er föst efst á síðu og fylgir þegar skrunað (scroll) er.
- Valmynd skal ná yfir alla breidd skjásins.
- Leturgerð skal vera Atkinson Hyperlegible.
- Leturstærð skal vera 24px, skilgreint í `rem`.
- Texti í valmynd skal vera miðjuð (centered), hér skal nota `inline-block` og `text-align` til að ná því fram.
- Þegar tengill í valmynd er valinn með því að nota tab (`active`) eða sveimað er yfir (`hover`) skal setja undirstrik undir viðkomandi tengil.
- Núverandi síða skal vera með undirlínu (og er ekki tengill).

### Haus síðu

Haus (header) síðu skal vera með heiti síðu miðjað og leturstærð 48px, skilgreint í `rem`.

### Fótur

Efni í fæti skal vera skipt í þrennt með bili á milli og:

- Bakgrunnur skal vera með litnum `#ff9999`.
- Bil frá efni skal vera á allar hliðar innan fætar eitt bil.
- Eitt bil skal vera undir hverri fyrirsögn og milli staða í „Hafa samband“.

### Forsíða

[Sjá skjáskot af útliti forsíðu](./fyrirmynd/forsida.png).

Haus er öðruvísi á forsíðu:

- Allan skjá skal hylja með [bakgrunnsmynd](./myndir/background.jpg):
  - Lýsing á mynd: Stakur sófi snýr að vegg, á veggnum eru mjög mörg listaverk í allskonar römmum. Einnig sést í vegg hægra megin við sófann, á honum eru líka mörg listaverk.
  - [Frá Unsplash](https://unsplash.com/photos/brown-loveseat-surrounded-by-photo-frame-lot-VbI0LMaGMlg?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) eftir [Mick Haupt](https://unsplash.com/@rocinante_11?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash).
- Þegar skrollað er niður síðu skal bakgrunnsmynd vera föst (fixed).
- Mynd skal birta frá (position) miðju hennar, ekki frá efra vinstra horni.
- Myndin skal hylja allt pláss (cover) og ekki endurtaka sig (repeat).
- Yfir mynd en undir efni (stilla með z-index) skal vera hálfgegnsætt lag sem gerir það að verkum að texti er læsilegur (annars er erfitt að lesa hvítan texta ofan á myndinni þar sem partur af henni er hvítur).
- Efni skal vera nokkurnveginn miðjað með því að nota `margin`, frá toppi um `20rem`.
- Eftir fyrirsögnum skal vera bil, um `4rem`.

Eftir haus á síðu birtist efni í tveim kortum (cards) með fyrirsagnirnar „Núverandi sýningar“ og „Skráðu hópinn þinn á sýningu“, þar sem:

- „Kicker“ er fyrir ofan fyrirsögn og er í hástöfum í minna letri, `12px` en skilgreint í `rem`, ekki skal breyta HTML og setja stafi í hástafi heldur nota CSS
- Fyrirsögn
- Jafntölu kort skal hafa myndina vinstra megin og efni hægra megin, öfugt fyrir oddatölu. Ekki þarf að passa upp á að mynd og texti séu jafnskipt.
- Fyrir neðan skal hafa tengil.

### Um síða

[Sjá skjáskot af útliti um síðu](./fyrirmynd/um.png).

Eftir fyrirsagnir skal ekki vera bil. Milli svæða skal vera eitt bil.

### Sýningarsíða

[Sjá skjáskot af útliti sýningarsíðu](./fyrirmynd/syningar.png).

- Fyrirsagnir skulu vera fyrir ofan töflu.
- Milli tafla skal vera eitt bil.
- Fyrirsagnir á töflum skulu vera feitletraðar.
- Allt efni í töflu skal vera vinstrijafnað.
- Önnur hver röð í töflunni skal hafa bakgrunnslitinn `#ff9999`.

### Skráningarsíða

[Sjá skjáskot af útliti skráningarsíðu](./fyrirmynd/skraning.png).

- Milli svæða skal vera eitt bil.
- Fyrirsagnir svæða skulu vera 24px, skilgreint í `rem`.
- Allir reitir skulu vera að hámarki `450px` breiðir.
- Allir form reitir skulu hafa hálft bil vinstra og hægra megin, hafa hvítan bakgrunn (`#ffffff`) og `1px` svartan (`#000000`) border.
- Þar sem tjékkbox eru notuð skulu þau vera á undan texta.
- Takki til að senda skal hafa bakgrunnslitinn `#ff9999`.

# Takmarkanir

Aðeins skal nota eftirfarandi eigindi, og ef tekið fram, viðeigandi gildi:

- `@font-face` til að fella inn leturgerðir
- `background` og nánari skilgreiningar:
  - `background-attachment`
  - `background-color`
  - `background-image`
  - `background-position`
  - `background-repeat`
  - `background-size`
- `border` og nánari skilgreiningar
- `border-spacing: 0;` (fyrir töflur)
- `box-sizing` (en þó bara það sem gefið er)
- `color`
- `float` og `clear`
- `display: block;`, `display: inline-block;`
- `font-family`
  - `src` til að vísa í skrár fyrir leturgerðir
- `font-style`
- `font-size`
- `font-weight`
- `list-style: none;`
- `margin` og nánari skilgreiningar
- `padding` og nánari skilgreiningar
- `width`, `height`, `min-width`, `max-width`, `min-height`
- `position`
- `left`, `right`, `top`, `bottom`
- `text-align`
- `text-decoration`
- `text-transform`
- `vertical-align: top;` í efni í fæti
- Þau eigindi notuð í `.sr-only` og ekki tiltekin hér ætti ekki að nota í annað.
- `display: flex;`, `flex-direction` og `flex` (í `.wrapper`) ætti eingöngu að nota þar.

Nota ætti `type` og `class` selectora og í einhverju tilfelli pseudo-selectora. Í gefnu efni er universal selector (`*`), ekki ætti að nota hann í öðru í lausn. Ekki ætti að nota `id` selectora.

## Netlify

Setja skal upp verkefni á Netlify með því að hlaða upp skrám með „manual deploy“ _eða_ tengja GitHub repo. Einnig er leyfilegt að nota aðra hýsingu en heyrið í kennara.

## Mat

- 10% – Snyrtilega uppsett og gilt CSS.
- 15% – Aðeins leyfileg eigindi og gildi notuð.
- 20% – Almennt útlit, haus, valmynd, meginmál og fótur.
- 20% – Útlit forsíðu eftir forskrift.
- 5% – Útlit un síðu eftir forskrift.
- 10% – Útlit sýningarsíðu eftir forskrift.
- 20% – Útlit skráningarsíðu eftir forskrift.

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 1. september 2025.

## Skil

Skila skal í Canvas, seinasta lagi fyrir lok dags fimmtudaginn 11. september 2025.

Skilaboð skulu innihalda bæði:

- zip skrá með öllum skrám og möppum í lausn á verkefni (eða hlekkur á GitHub).
- slóð á verkefni keyrandi á Netlify, sett sem athugasemd við skil á Canvas.

Athugið að það er **ekki nóg** að eingöngu setja athugasemd, skila þarf verkefni sérstaklega. Verkefnum sem ekki er skilað fá ekki einkunn.

## Aðstoð

Leyfilegt er að ræða, og vinna saman að verkefni en **skrifið ykkar eigin lausn**. Ef tvær eða fleiri lausnir eru mjög líkar þarf að færa rök fyrir því, annars munu allir hlutaðeigandi hugsanlega fá 0 fyrir verkefnið.

Ekki er heimilt að nota stór mállíkön til að vinna verkefni í námskeiðinu, [sjá nánar um notkun](https://github.com/vefforritun/vef1-2024/blob/main/mallikon.md).

## Verkefni og einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

> Útgáfa 0.1

## Útgáfusaga

| Útgáfa | Lýsing                     |
| ------ | -------------------------- |
| 0.1    | Fyrsta útgáfa verkefnisins |
