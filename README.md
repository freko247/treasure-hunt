# Operation Søndermarken: Agent Felt-Terminal

Interaktiv web-app bygget til en 10-års fødselsdagsskattejagt i **Søndermarken, København**. Indeholder **indbygget OpenStreetMap**, live GPS-sporing med prikket kurslinje, pointfradrag og fuld lokal lagring af fremgang.

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

## 🗺️ Ny Rækkefølge af Poster i Søndermarken

Ruten starter ved stengrotten mod sydvest og bevæger sig naturskønt gennem parken:

| # | Post | Koordinater (DMS) | Koordinater (Decimal) | Gåde / Opgave | Godkendte Svar | Låser op for |
|---|---|---|---|---|---|:---:|
| **1** | **Kildegrotten** *(Stengrotten)* | `55°40'10.6"N 12°31'09.8"E` | `55.669611, 12.519389` | Hvilket element strømmede ud fra kilden: ILD, VAND eller VIND? | `VAND`, `WATER` | Ciffer 1 |
| **2** | **Zoo Udsigtspunktet** *(Savannen)* | `55°40'13.2"N 12°31'09.4"E` | `55.670333, 12.519278` | Rovdyret der kaldes 'dyrenes konge' bag muren | `LØVE`, `LION` | Ciffer 2 |
| **3** | **Cisternerne** *(De Hemmelige Pyramider)* | `55°40'10.1"N 12°31'27.1"E` | `55.669472, 12.524194` | Tæl de trekantede glassider på pyramiden | `4`, `FIRE`, `FOUR` | Ciffer 3 |
| **4** | **Det Norske Hus** *(Bjælkehytten)* | `55°40'13.2"N 12°31'36.7"E` | `55.670333, 12.526861` | Materialet denne skovhytte er bygget af | `TRÆ`, `TRAE`, `WOOD` | Ciffer 4 & Slutkode |

---

## ⭐ Pointsystem & Pointfradrag

* **Startscore:** 1000 point
* **Forkert svar fradrag:** `-25 PTS` hver gang der indtastes en forkert kode.
* **GPS-opslagsfradrag:** `-25 PTS` hver gang patruljens placering og kurslinje opdateres.
* **Hint-fradrag:** `-50 PTS` hvis patruljen anmoder om satellit-hjælp fra basen.

### Spion-Rang på Sejrsskærmen:
* 🏆 **900+ point:** Mester-Spion *(Legendarisk)*
* 🎖️ **750 – 899 point:** Elite-Agent *(Fremragende)*
* 🕵️ **500 – 749 point:** Felt-Spion *(Godkendt)*
* 🔎 **Under 500 point:** Rekrut *(Gennemført)*

---

## ⚙️ Forældrekontrol (⚙️ Tandhjulet øverst til højre)
Tryk på tandhjulet for at:
* Se patruljens aktuelle score, antal fejl, hints og GPS-opslag.
* Se facitlisten med alle koder.
* Nulstille hele spillet og scoren (tilbage til 1000 point) inden festen starter.
