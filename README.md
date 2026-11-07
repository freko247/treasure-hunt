# Operation Søndermarken: Agent Felt-Terminal

Interaktiv web-app bygget til en 10-års fødselsdagsskattejagt i **Søndermarken, København**. Indeholder **indbygget OpenStreetMap**, GPS-geofencing (30 meters tjek-ind for at åbne gåder), prikket kurslinje, pointfradrag og fuld lokal lagring af fremgang.

---

## 🚀 Sådan tester du den lige nu

### Mulighed A: Åbn direkte i browseren på din Mac
Dobbeltklik på `index.html` eller kør:
```bash
open /Users/freko/treasure-hunt/index.html
```

### Mulighed B: Start lokal webserver (test på mobilen via Wi-Fi)
```bash
cd /Users/freko/treasure-hunt
python3 -m http.server 8000
```
Besøg derefter `http://localhost:8000` på din computer eller `http://<din-mac-ip>:8000` i browseren på telefonen.

---

## 🛰️ Fysisk Tjek-Ind & Afstandscheck (30 Meters Radius)

1. **Gåderne er låst undervejs:**
   * Når drengene navigerer mod en post, er spørgsmålet og svarfeltet låst.
   * Kortet viser dem vej med den pulserende radarnål og en prikket kurslinje.
2. **Tjek Ind på Posten (Gratis når man er fremme!):**
   * Når de ankommer, trykker de på **`📍 TJEK IND PÅ POSTEN`**.
   * Hvis deres GPS-position er **under 30 meter** fra postens koordinater, låser missionsordren og svarfeltet automatisk op med grøn status og fanfare — **helt gratis (0 point fradrag)**!
   * Hvis de trykker på knappen mens de er mere end 30 meter væk, trækkes **-25 point**, og displayet viser den præcise afstand (f.eks. *`⛔ I er ~68 meter væk (-25 point). Gå 38 meter tættere på!`*), så de ikke gætter eller tjekker for tidligt.

---

## 📜 Regler & Vejledning (📜 Ikon i Headeren)
* Tryk på **📜-ikonet** øverst i bjælken når som helst for at åbne introen og reglerne igen undervejs i missionen.

---

## 🗺️ De 7 Poster i Søndermarken & Hængelåsens Kodesum

| # | Post | Koordinater (DMS) | Koordinater (Decimal) | Gåde / Opgave | Godkendte Svar | Hemmeligt Kodetal |
|---|---|---|---|---|---|:---:|
| **1** | **Kildegrotten** *(Stengrotten)* | `55°40'10.6"N 12°31'09.8"E` | `55.669611, 12.519389` | Hvilket element strømmede ud fra kilden: ILD, VAND eller VIND? | `VAND`, `WATER` | **+1.000** |
| **2** | **Zoo Udsigtspunktet** *(Savannen)* | `55°40'13.2"N 12°31'09.4"E` | `55.670333, 12.519278` | Rovdyret der kaldes 'dyrenes konge' bag muren | `LØVE`, `LION` | **+2.000** |
| **3** | **Den Kinesiske Pavillon** *(Lysthuset)* | `55°40'10.4"N 12°31'16.2"E` | `55.669544, 12.521179` | Hvilket asiatisk land har inspireret lysthuset med det svungne tag? | `KINA`, `CHINA` | **+3.000** |
| **4** | **Cisternerne** *(De Hemmelige Pyramider)* | `55°40'10.1"N 12°31'27.1"E` | `55.669472, 12.524194` | Tæl de trekantede glassider på pyramiden | `4`, `FIRE`, `FOUR` | **+4.000** |
| **5** | **Det Norske Hus** *(Bjælkehytten)* | `55°40'13.2"N 12°31'36.7"E` | `55.670333, 12.526861` | Materialet denne skovhytte er bygget af | `TRÆ`, `TRAE`, `WOOD` | **+5.000** |
| **6** | **Hundeparken** *(Fritløbsområdet)* | `55°40'07.1"N 12°31'34.5"E` | `55.668650, 12.526255` | Kæledyret der må løbe frit omkring og lege uden snor | `HUND`, `HUNDE`, `DOG` | **+6.000** |
| **7** | **Toilethuset** *(Den Gule Bygning)* | `55°40'06.2"N 12°31'21.8"E` | `55.668398, 12.522713` | Farven på facadens mure (GUL, BLÅ eller RØD) | `GUL`, `GULT`, `YELLOW` | **+0** |

### 🔐 Beregning af Hængelåsens 5 Cifre:
$$1.000 + 2.000 + 3.000 + 4.000 + 5.000 + 6.000 + 0 = \mathbf{[fjernet]}$$
* **Hængelåsens 5 hjul indstilles til:** `[fjernet]`
* **Skattekistens placering:** *I [fjernet]* (`[fjernet]`)

---

## ⭐ Pointsystem & Pointfradrag

* **Startscore:** 1000 point
* **Tjek-ind ved posten (< 30 m):** `0 PTS` (Gratis når de er fremme!)
* **Positionsopslag for langt væk (> 30 m):** `-25 PTS`
* **Forkert svar:** `-25 PTS` hver gang der indtastes et forkert svar.
* **Hint fra basen:** `-50 PTS` hvis patruljen beder om hjælp til opgaven.

### Spion-Rang på Sejrsskærmen:
* 🏆 **900+ point:** Mester-Spion *(Legendarisk)*
* 🎖️ **750 – 899 point:** Elite-Agent *(Fremragende)*
* 🕵️ **500 – 749 point:** Felt-Spion *(Godkendt)*
* 🔎 **Under 500 point:** Rekrut *(Gennemført)*

---

## ⚙️ Forældrekontrol (⚙️ Tandhjulet øverst til højre)
Tryk på tandhjulet for at:
* Se patruljens telemetri: aktuel score, rang, nuværende post, fundne kodelås-cifre og antal fejl/hints/GPS-opslag (uden at afsløre gådernes facit).
* Springe frem til næste post i nødstilfælde.
* Installere appen på startskærmen (PWA).
* Nulstille hele spillet og scoren (tilbage til 1000 point) inden festen starter.
