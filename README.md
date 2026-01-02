# ⚠️ Legal & Responsible Use Notice

> **This repository is published solely for cybersecurity education, research integrity, and lawful testing.**  
> Use of these materials implies acceptance of all applicable laws and the conditions below:
>  
> - Any use on systems, vehicles, or radio devices **not owned or explicitly authorized** is illegal under acts such as the *CFAA (U.S.)*, *UK Computer Misuse Act 1990*, and *EU Cybercrime Convention*.  
> - The author and contributors **do not promote, endorse, or support** exploitation, unauthorized access, or signal cloning outside controlled research.  
> - All files are supplied **“as is,”** without warranties or guarantees of functionality, safety, or fitness for purpose.  
> - You assume all responsibility for compliance, actions, and any resulting consequences.  
>
> **If legality or intent is uncertain, you must not use, modify, or distribute this software.**  
>
> Maintained to advance open knowledge, security testing transparency, and responsible research.
>
> “Real security comes from transparency, testing, and open eyes - not from hiding keys.fz under the rug.”
---

# Unleashed 2.0 – Full Files Repository ![Visitor Counter](https://komarev.com/ghpvc/?username=uhbur8-lgtm&label=Repo%20Views&color=0e75b6&style=for-the-badge)

This repository hosts the complete set of files for **Unleashed 2.0** software.  
The original upload was made on **December 31**, and due to unforeseen issues, this is the **re‑upload** of that release.

---

## About

These files are provided **as‑is** and were verified functional at the time of upload.  
I am **not responsible** for their contents, performance, or condition.  
This repository exists to **make the files publicly accessible** following gatekeeping within the community.

---

## Disclaimer

Use these files **at your own discretion and risk.**  
No warranties, guarantees, or support are provided.

*Uploaded and shared for transparency and accessibility.*

---

# Private Unleashed 2.0 – Flipper Zero Firmware

## Overview

**Private‑Unleashed‑2.0‑FlipperZero‑Firmware**  
Focus: *Rolling Code Exploitation and Relay Attack Research*

---

### Rolling Code Mechanics

- Records legitimate key fob transmissions.  
- Analyzes signal sequences to predict future unlock codes.  
- Injects predicted codes to emulate authorized access.  

This effectively allows learning of authentication patterns through observation.

---

### Relay Attack Process

1. Captures a vehicle’s “key nearby” signal.  
2. Relays it to the genuine key located elsewhere.  
3. Sends the genuine key’s reply back to the vehicle.  
4. The vehicle unlocks, believing the key is present.  

**Note:** This process does *not* enable driving or starting the vehicle.

---

## Warnings

- For **educational and experimental use only** on devices or vehicles **you own.**  
- **Illegal use is strictly prohibited.**  
- The author is **not responsible** for damage or misuse.  
- Requires **Unleashed Firmware v0.84+**.

---

## Technical Notes

### Modulation Reference

| Manufacturer / System | Typical Modulation | Notes |
|------------------------|--------------------|-------|
| Kia, Hyundai, Mitsubishi, Suzuki | FM476 *(older pre‑2014: AM650)* | Common OEM systems |
| VW, Skoda, Seat, Audi, Ford, Subaru, FCA | AM650 | Standard |
| Aftermarket alarms (e.g., Scher‑Khan) | FM238 / FM476 | Varies |
| Barriers | AM650 *(some FM / custom FSK)* | Exceptions exist |
| PSA systems | Custom presets *(in development)* | Special handling required |

---

### Working with Signals

- Always **save captured signals** before emulation.  
- Direct emulation (from RX) works but sends only the received command.  
- To use all buttons (lock / unlock / trunk / panic), emulate from a saved signal.  
- Hold the emulation button for **at least 2 seconds** to complete transmission.  

**Button Map:**  
- Center: Received command  
- Up: Unlock or secondary  
- Down: Trunk or tertiary  

---

### Copying FAAC SLH / BFT

1. Record two consecutive presses per button without gaps.  
2. Capture screenshots from receiver info (key, fix, hop, etc.).  
3. Data is manually calculated to generate valid counter values for Sub‑GHz “Add Manually” mode.

---

## Changelog

### 1 December 2025

- Added support for older Audi models.  
- Improved CC1101 drivers, HAL, and Sub‑GHz modules:  
  - Fixed freezes and crashes under high‑speed presets.  
  - Optimized PSA brute‑force performance.  
- Improved private protocol stability.  
- Merged updates from OFW and public Unleashed firmware.

---

## Coming Soon

- Ford, Land Rover, Jaguar, Lincoln, Mercury (up to 2023, FSK & Keyless‑Go)  
- BMW and Mini Cooper  
- Honda  
- Mazda

---

## Supported Vehicle Models (As of November 2025)

### KIA (Up to 2025)

Forte, Magentis, Sedona, Rio, Mohave, Sorento, Rio X‑Line, Optima, Soul, Carnival, Picanto, Sportage, Cerato, Ceed, Stonic, Cerato Coupe, Ceed JD, Venga, Bongo

### HYUNDAI (Up to 2025)

Accent, HB20, i35, Solaris, Avante, H1, i40, Sonata, Creta, i10, iMax, Starex, Elantra, i20, iLoad, Trajet, Getz, i25, iX20, Tucson, KRX 2025, i30, iX25, Veloster, Mistra, i35, iX30, Verna, Santa Fe, iX35, iX40, iX45

### SUBARU

B9 Tribeca, Legacy, XV, Forester, Outback, Impreza

### LAND ROVER (Up to 2016)

### FIAT (Up to 2012)

Cronos, Doblo, Ducato

### LANCIA / FCA

Delta, Momo, Ypsilon, and other FCA vehicles

### FORD (Up to 2016)

B‑Max, C‑Max, Edge, Escape, Expedition, Explorer, Fiesta, Flex, Focus, Fusion, Galaxy, Grand, Kuga, Mondeo, Mustang, Ranger, S‑Max, Taurus, Tourneo, Transit, Transit Connect, Transit Custom, Transit Grand, Transit MK4, F150–F450, EconoLine

### LINCOLN / MERCURY (Up to 2016)

### MITSUBISHI

ASX, Pajero Sport, L200, Colt, Galant, Pajero, Grandis

### SUZUKI (Up to 2015)

Grand Vitara, SX‑4, Swift

### PEUGEOT (2004–2016+)

2008, 207, 208, 307, 308, 3008, 4008, 408, 407, 408–508, 301, 5008, 607, 3008+, RCZ, Partner, Expert, Triumph, Xsara, Elysée, DS5, Quatre, Picasso

### CITROËN (2004–2018)

C2, C3, C3XR, C4, C4L, C4 Cactus, C4 Coupé, C4 Grand Picasso, C5, C8, CTR3, DS4, DS5, Berlingo, Jumpy, Picasso, Elysée, Xsara

### JAGUAR (Up to 2016)

### VOLKSWAGEN (Up to 2024)

Amarok, Beetle, Bora, Caddy, California, Caravelle, Crafter, Eos, Golf (4‑7), Jetta, LT, Lupo, Multivan, Passat (B5–CC), Polo, Scirocco, Sharan, Suran, Tiguan, Touran, Transporter, Up!, e‑Up!

### SKODA (Up to 2024)

Citigo, Fabia, Octavia, Rapid, Roomster, Superb, Yeti

### SEAT (Up to 2024)

Alhambra, Altea, Arosa, Cordoba, Ibiza, Leon, Mii, Toledo

### AUDI (Up to 2024)

A1 (8X), A2, A3 (8P), A4, A6, A8, Q3 (U8), TT (MK1, 8J), RS3, RS4, S1, S3, S4

---

## Supported Alarms

Alligator, APS‑1100, APS‑2550, B6–B9, Cenmax ST‑5, Cenmax ST‑7, CFM, Faraon, Harpoon, Jaguar, KGD, KeeLoq, Leopard, Mongoose, Pantera (CLK, XS), Pro‑1, Pro‑2, Reff, Scher‑Khan, Sheriff, Tomahawk (9010), TZ‑9030, ZX Series (3‑5, 1070, 730, 750, 755, 930, 940, 1090)

---

## Supported Barriers

AirForce, Allmatic, Alutech AT‑4N, Ansonic, Aprimatic, Beninca, Beninca VA AES‑128, Bett, BFT, Came (Atomo, Atomo TOP44RBN, Space, Static, Twee/Twin), Chamberlain Code, Clemsa, Comunello, Dickert MAHS, Doitrand, Dooya, DoorHan, DTM Neo, EcoStar, Elmes Poland, Elplast, FAAC (RX/XT, SLH, Spa), Feron, GateTX, GBiDi, Genius Bravo & Echo, GuardRF 311A, Harpoon, Honeywell, Honeywell WDB, Hörmann (BiSecur beta, HSM), iDo, InterTechno V3, IronLogic, JCM Tech, Jolly Motors, KingGates Stylo 4K, Linear Delta‑3, Magellan, Marantec, MasterCode, MegaCode, Merlin, Monarch, MotorLine, MutanCode, Nero Radio, Nero Sketch, Nice Flo, Nice FloR‑S, Nice One, Nice Smilo, Novoferm, Pantera, Pecninin, Phoenix V2, Power Smart, Prastel, Princeton, Rosh, Roger, Rossi, SEA, SecPlus (V1 & V2), SMC‑5326, Somfy (Keytis & Telis), Stilmatic, SteelMate, Teco, Tomahawk 9010, and others under Sub‑GHz categories.

---

*Compiled and released for research, testing, and educational use only.*
