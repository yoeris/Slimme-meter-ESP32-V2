# Hardware Lijst - Slimme Meter ESP32 V2

## 📋 Overzicht Project Modules

Dit project bestaat uit 4 optionele modules die samen of apart kunnen werken:
1. **Interface Module** (VERPLICHT) - Leest de P1 poort van de slimme meter
2. **Relais Module** (OPTIONEEL) - Schakelt apparaten aan/uit bij injectie
3. **PWM Module** (OPTIONEEL) - Geleidelijke regeling voor boiler
4. **Display Module** (OPTIONEEL) - Lokale weergave van gegevens

---

## 🎯 Snelstart: Basisopstelling (Interface + Relais)

Voor wie direct wil beginnen met injectiedetectie en schakelaar:

### Totale Kosten: €35-45

| Aantal | Component | Prijs | Voor Module |
|--------|-----------|-------|-------------|
| 2x | ESP32 DevKit (30 pins) | €8 x 2 = €16 | Interface + Relais |
| 1x | 5V Relais module (30A) | €10 | Relais |
| 1x | BC547 transistor | €0.10 | Interface |
| 1x | RJ12 kabel met 6p6c connector | €3 | Interface |
| 3x | Weerstand 10kΩ (2x) + 2.2kΩ (1x) | €0.30 | Interface |
| 2x | 5V voeding (USB adapter 1A) | €5 x 2 = €10 | Beide modules |
| - | **TOTAAL** | **€39.40** | - |

**Link 5V Relais:** https://nl.aliexpress.com/item/4000185959463.html (kies 5V versie!)

---

## 📦 Complete Hardware Lijst per Module

### 1️⃣ MODULE 1: INTERFACE (Verplicht)

Deze module leest de P1 poort van je slimme meter.

#### Essentiële Componenten:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | ESP32 DevKit | 30 pins, WROOM module | €8 | AliExpress/Amazon |
| 1x | BC547 transistor | NPN transistor | €0.10 | Electronica winkel |
| 1x | RJ12 kabel | 6p6c connector + kabel | €3 | Of zelf maken |
| 1x | Weerstand 2.2kΩ | 1/4W, ±5% | €0.05 | Voor data signaal |
| 2x | Weerstand 10kΩ | 1/4W, ±5% | €0.10 | Pull-up weerstanden |

#### Voeding (kies OPTIE A of B):

**OPTIE A: Voeding via P1 poort (budget)**
| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 3x | Condensator 4700µF | 16V, electrolyten | €2.50 | Parallel schakelen |

**OPTIE B: Externe voeding (⭐ AANBEVOLEN)**
| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | 5V voeding | USB adapter, 1A minimum | €5 | Stabieler |

#### Optioneel - SD Kaart Data Opslag:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | Micro SD kaart module | 3.3V, SPI interface | €2 | Voor data logging |
| 1x | Micro SD kaart | 8GB of meer | €5 | Class 10 aanbevolen |
| 6x | Dupont kabels | Female-Female | €1 | Voor SD verbinding |

#### Optioneel - Status LED's:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | LED Groen | 3mm of 5mm | €0.10 | P1 data activiteit |
| 1x | LED Rood | 3mm of 5mm | €0.10 | SD kaart error |
| 1x | LED Blauw | 3mm of 5mm | €0.10 | Power indicator |
| 3x | Weerstand 20kΩ | 1/4W, ±5% | €0.15 | LED voorschakel |

**Module 1 Subtotaal (minimaal):** €11-14
**Module 1 Subtotaal (compleet):** €22

---

### 2️⃣ MODULE 2: RELAIS (Eenvoudige schakelaar)

Deze module schakelt apparaten AAN bij injectie.

#### Essentiële Componenten:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | ESP32 DevKit | 30 pins, WROOM module | €8 | AliExpress/Amazon |
| 1x | 5V Relais module | 30A, met optocoupler | €10 | Link hierboven |
| 1x | 5V voeding | USB adapter, 1A minimum | €5 | Voor ESP32 + relais |
| 1x | Behuizing | IP55, 220V geschikt | €10 | Veiligheid! |

#### 220V Bedrading (door elektricien):

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 2m | Elektriciteitskabel | 3x 2.5mm² (3-aderig) | €3 | Naar apparaat |
| - | Installatie elektricien | - | €50-100 | Veiligheid eerst! |

**Module 2 Subtotaal (alleen hardware):** €33
**Module 2 Subtotaal (met installatie):** €83-133

---

### 3️⃣ MODULE 3: PWM (Geavanceerde boilerregeling)

Deze module regelt geleidelijk een elektrische boiler met SSR.

#### Essentiële Componenten:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | ESP32 DevKit | 30 pins, WROOM module | €8 | AliExpress/Amazon |
| 1x | SSR (Solid State Relais) | 40A, 3-32V input, 220V AC output | €15 | Belangrijk: AC uitgang |
| 1x | 5V voeding | USB adapter, 1A | €5 | Voor ESP32 |
| 1x | Heatsink voor SSR | Minimaal 100x50mm | €5 | Koeling verplicht! |
| 1x | Thermische pasta | Voor SSR-heatsink | €3 | Warmteafvoer |
| 1x | Behuizing | IP55, met ventilatie | €15 | SSR wordt warm |

#### 220V Bedrading (door elektricien):

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 2m | Elektriciteitskabel | 3x 2.5mm² (3-aderig) | €3 | Naar boiler |
| - | Installatie elektricien | - | €50-100 | Veiligheid eerst! |

**Aanbevolen SSR:** Fotek SSR-40DA of compatible
**Link SSR:** https://nl.aliexpress.com/item/32817672858.html

**Module 3 Subtotaal (alleen hardware):** €51
**Module 3 Subtotaal (met installatie):** €101-151

---

### 4️⃣ MODULE 4: DISPLAY (Lokale weergave)

Deze module toont alle gegevens op een lokaal scherm.

#### Essentiële Componenten:

| Aantal | Component | Specificatie | Prijs | Opmerking |
|--------|-----------|--------------|-------|-----------|
| 1x | ESP32 DevKit | 30 pins, WROOM module | €8 | AliExpress/Amazon |
| 1x | TFT Display | 480x320, ILI9488 driver, SPI | €12 | 3.5" touchscreen |
| 1x | 5V voeding | USB adapter, 1A | €5 | Voor ESP32 + display |
| 8x | Dupont kabels | Female-Female | €1 | Voor display verbinding |

**Aanbevolen Display:** ILI9488 3.5" SPI TFT
**Link Display:** https://nl.aliexpress.com/item/32960241206.html

**Belangrijke Library:** TFT_eSPI (configuratie in User_Setup.h)

**Module 4 Subtotaal:** €26

---

## 🔧 Gereedschap & Algemene Benodigdheden

### Essentieel Gereedschap:

| Component | Prijs | Opmerking |
|-----------|-------|-----------|
| Soldeerbout | €15-30 | 30-60W, met temperatuurregeling |
| Soldeertin | €5 | 0.8mm, loodvrij |
| Stripboard / Perfboard | €2 | Voor vaste montage |
| Dupont kabels M-M, M-F, F-F | €5 | Assortiment voor prototyping |
| Multimeter | €15-30 | Voor testen en debuggen |
| Krimpkous assortiment | €5 | Voor isolatie soldeerverbindingen |
| Kabelbinders | €3 | Voor nette montage |

**Gereedschap Totaal:** €50-80 (eenmalig)

---

## 📱 Software & Programmeren

### Vereiste Software (GRATIS):

| Software | Versie | Opmerking |
|----------|--------|-----------|
| Arduino IDE | 2.x of hoger | Gratis downloaden |
| ESP32 Core | 3.0.x | **Let op: Versie 2.x werkt NIET** |
| AsyncTCP Library | Latest | Voor webserver |
| ESPAsyncWebServer | Latest | Voor webinterface |
| TFT_eSPI Library | Latest | Alleen voor display module |

**Library Links:**
- AsyncTCP: https://github.com/me-no-dev/AsyncTCP
- ESPAsyncWebServer: https://github.com/me-no-dev/ESPAsyncWebServer

### Programmeer Hardware:

| Component | Prijs | Opmerking |
|-----------|-------|-----------|
| USB micro kabel | €3 | Vaak meegeleverd met ESP32 |
| Computer | - | Windows/Mac/Linux |

---

## 💰 Kostenopbouw Verschillende Configuraties

### ⚡ Configuratie 1: Minimaal Relais Systeem
**Voor wie: Simpel schakelaar bij injectie**

| Module | Kosten |
|--------|--------|
| Interface (basis) | €14 |
| Relais | €33 |
| Gereedschap (eenmalig) | €50 |
| **TOTAAL** | **€97** |

---

### ⚡ Configuratie 2: Compleet Relais + Display
**Voor wie: Schakelaar + lokale weergave**

| Module | Kosten |
|--------|--------|
| Interface (compleet met SD) | €22 |
| Relais | €33 |
| Display | €26 |
| Gereedschap (eenmalig) | €50 |
| **TOTAAL** | **€131** |

---

### ⚡ Configuratie 3: PWM Boilerregeling
**Voor wie: Optimale boilerregeling met overschot**

| Module | Kosten |
|--------|--------|
| Interface (compleet met SD) | €22 |
| PWM | €51 |
| Gereedschap (eenmalig) | €50 |
| **TOTAAL** | **€123** |

---

### ⚡ Configuratie 4: Volledig Systeem
**Voor wie: Alles inclusief**

| Module | Kosten |
|--------|--------|
| Interface (compleet met SD) | €22 |
| Relais | €33 |
| PWM | €51 |
| Display | €26 |
| Gereedschap (eenmalig) | €50 |
| **TOTAAL** | **€182** |

*Prijzen zijn exclusief 220V installatie door elektricien*

---

## 🛒 Aanbevolen Winkels

### Online (goedkoop, langere levertijd):
- **AliExpress** - ESP32, relais, SSR, displays (~2-4 weken)
- **Banggood** - Electronica componenten (~2-4 weken)
- **Amazon** - Snellere levering, iets duurder

### Lokaal (sneller, iets duurder):
- **Farnell** - Professionele componenten
- **Conrad** - Winkels + online
- **Kiwi Electronics** (NL) - ESP32 specialist
- **Hobbyelectronica.nl** - Nederlandse webshop

### Voor weerstanden/transistoren:
- Lokale electronica winkel (goedkoopst)
- eBay assortimenten (100+ stuks voor €3-5)

---

## 📦 Handige Assortimenten (voor meerdere projecten)

Als je vaker met electronica werkt:

| Assortiment | Inhoud | Prijs | Opmerking |
|-------------|--------|-------|-----------|
| Weerstand kit | 1Ω-10MΩ, 30 waarden x 20 stuks | €8 | Voor jaren voorraad |
| Condensator kit | 1pF-4700µF, diverse types | €10 | Handig assortiment |
| Transistor kit | BC547/BC557 + anderen | €5 | 100+ stuks |
| LED assortiment | Diverse kleuren + maten | €5 | 200+ stuks |
| Dupont kabel set | 3x 40 stuks M-M, M-F, F-F | €8 | Essentieel |

**Assortimenten Totaal:** €36 (eenmalig, jaren voorraad)

---

## ⚠️ Belangrijke Opmerkingen

### Veiligheid:
1. ❌ **NOOIT zelf 220V aansluiten zonder bevoegdheid**
2. ✅ Laat 220V installatie doen door erkend elektricien
3. ✅ Gebruik altijd IP-beschermde behuizing voor 220V
4. ✅ Test eerst met 12V voor je 220V aansluit
5. ✅ SSR modules worden HEET - altijd heatsink gebruiken

### Compatibiliteit:
1. ⚠️ ESP32 Core **3.0.x vereist** - versie 2.x werkt NIET
2. ⚠️ Check dat relais modules **5V input** zijn (niet 12V)
3. ⚠️ SSR moet **AC output** hebben voor 220V
4. ⚠️ P1 poort moet geactiveerd zijn via Fluvius/Netbeheerder

### Meterkast Overweging:
- Zorg voor 5V voeding bij meterkast
- WiFi signaal moet voldoende sterk zijn
- Eventueel WiFi repeater nodig (€20-30)

---

## 🔗 Links & Bronnen

### GitHub Repository:
https://github.com/thieu-b55/Slimme-meter-ESP32-V2

### Documentatie:
- [START_HIER.md](START_HIER.md) - Welk document heb ik nodig?
- [EENVOUDIG_RELAIS_SCHEMA.md](EENVOUDIG_RELAIS_SCHEMA.md) - Simpel relais
- [COMPLETE_PINOUT_DIAGRAM.md](COMPLETE_PINOUT_DIAGRAM.md) - Alle pinouts
- [Slimme meter ESP32 V2.pdf](Slimme%20meter%20ESP32%20V2.pdf) - Volledige handleiding

### Handige Video's (YouTube):
- "ESP32 getting started"
- "How to solder electronics"
- "P1 poort uitlezen"

---

## ✅ Bestelchecklists

### 📝 Checklist: Basis Relais Systeem (€40)

```
Hardware:
☐ 2x ESP32 DevKit (30 pins)
☐ 1x 5V Relais module (30A, let op: 5V versie!)
☐ 1x BC547 transistor
☐ 1x RJ12 kabel met 6p6c connector
☐ 1x Weerstand 2.2kΩ
☐ 2x Weerstand 10kΩ
☐ 2x 5V voeding (USB adapter, 1A)
☐ 1x Behuizing (IP55)

Gereedschap (als je nog niet hebt):
☐ Soldeerbout + tin
☐ Dupont kabels assortiment
☐ Multimeter
☐ USB micro kabel
```

### 📝 Checklist: PWM Boiler Systeem (€75)

```
Hardware:
☐ 2x ESP32 DevKit (30 pins)
☐ 1x SSR 40A (3-32V input, 220V AC output)
☐ 1x Heatsink voor SSR (100x50mm)
☐ 1x Thermische pasta
☐ 1x BC547 transistor
☐ 1x RJ12 kabel met 6p6c connector
☐ 1x Weerstand 2.2kΩ
☐ 2x Weerstand 10kΩ
☐ 2x 5V voeding (USB adapter, 1A)
☐ 1x Behuizing met ventilatie (IP55)
☐ 1x Micro SD kaart module (optioneel)
☐ 1x Micro SD kaart 8GB (optioneel)

Gereedschap (als je nog niet hebt):
☐ Soldeerbout + tin
☐ Dupont kabels assortiment
☐ Multimeter
☐ USB micro kabel
```

### 📝 Checklist: Volledig Systeem (€180)

```
Hardware:
☐ 4x ESP32 DevKit (30 pins)
☐ 1x 5V Relais module (30A, 5V versie)
☐ 1x SSR 40A (3-32V input, 220V AC output)
☐ 1x Heatsink voor SSR (100x50mm)
☐ 1x Thermische pasta
☐ 1x TFT Display 3.5" ILI9488 SPI
☐ 1x BC547 transistor
☐ 1x RJ12 kabel met 6p6c connector
☐ 1x Weerstand 2.2kΩ
☐ 2x Weerstand 10kΩ
☐ 3x Weerstand 20kΩ (voor LEDs)
☐ 3x LED (groen, rood, blauw)
☐ 4x 5V voeding (USB adapter, 1A)
☐ 1x Micro SD kaart module
☐ 1x Micro SD kaart 8GB
☐ 2x Behuizing (IP55)
☐ Dupont kabels (40+ stuks)
☐ Krimpkous assortiment

Gereedschap (als je nog niet hebt):
☐ Soldeerbout + tin
☐ Stripboard / perfboard
☐ Multimeter
☐ USB micro kabel
☐ Kabelbinders
```

---

## 🎓 Upgradepad (start klein, bouw uit)

### Fase 1: Monitoring (€20)
- Alleen Interface module
- Zie verbruik op webpagina

### Fase 2: Schakelaar (+ €35)
- Voeg Relais module toe
- Schakel apparaten bij injectie

### Fase 3: Boilerregeling (+ €50)
- Vervang relais door PWM + SSR
- Geleidelijke boilerregeling

### Fase 4: Lokale weergave (+ €25)
- Voeg Display module toe
- Zie alles zonder WiFi

**Voordeel:** Je kunt klein beginnen en later uitbreiden!

---

## 📞 Support & Community

### Bij vragen:
1. Lees eerst de PDF documentatie
2. Check de GitHub Issues
3. Nederlands Arduino forum
4. Tweakers Forum - Gathering of Tweakers

### Originele Auteur:
**thieu-b55** - GitHub: https://github.com/thieu-b55

---

**Veel succes met je slimme meter project!** ⚡☀️

*Versie 1.0 - November 2024*
