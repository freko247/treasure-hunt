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

## 🗺️ Rækkefølge af Poster i Søndermarken

| # | Post | Koordinater (DMS) | Koordinater (Decimal) | Gåde / Opgave | Godkendte Svar | Låser op for |
|---|---|---|---|---|---|:---:|
| **1** | **Kildegrotten** *(Stengrotten)* | `55°40'10.6"N 12°31'09.8"E` | `55.669611, 12.519389` | Hvilket element strømmede ud fra kilden: ILD, VAND eller VIND? | `VAND`, `WATER` | Ciffer 1 |
| **2** | **Zoo Udsigtspunktet** *(Savannen)* | `55°40'13.2"N 12°31'09.4"E` | `55.670333, 12.519278` | Rovdyret der kaldes 'dyrenes konge' bag muren | `LØVE`, `LION` | Ciffer 2 |
| **3** | **Cisternerne** *(De Hemmelige Pyramider)* | `55°40'10.1"N 12°31'27.1"E` | `55.669472, 12.524194` | Tæl de trekantede glassider på pyramiden | `4`, `FIRE`, `FOUR` | Ciffer 3 |
| **4** | **Det Norske Hus** *(Bjælkehytten)* | `55°40'13.2"N 12°31'36.7"E` | `55.670333, 12.526861` | Materialet denne skovhytte er bygget af | `TRÆ`, `TRAE`, `WOOD` | Ciffer 4 & Slutkode |

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
