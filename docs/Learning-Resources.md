# IMEFS Learning Resources

Curated books, YouTube channels, and websites to support the Integrated Mineral Exploration Field Station project. Use this alongside [`Journey.md`](../Journey.md), [`Roadmap.md`](../Roadmap.md), and the [Research Paper](IMEFS-Research-Paper.md).

**How to track progress:** Check off items as you complete them. When you finish a book or course module, add notes to the matching section in [Research Paper §5](IMEFS-Research-Paper.md#5-literature-review-todo).

---

## Quick start (buy / subscribe first)

| Action | Resource |
|--------|----------|
| Buy one book | *Make: Electronics* **or** *Arduino Workshop* |
| Subscribe | [Paul McWhorter](https://www.youtube.com/@paulmcwhorter), [DroneBot Workshop](https://www.youtube.com/@DroneBotWorkshop) |
| Bookmark | [Adafruit Learn](https://learn.adafruit.com/), [Microcontrollers Lab](https://microcontrollerslab.com/) |
| Save for Year 2 | *Geophysics for the Mineral Exploration Geoscientist* (Dentith & Mudge) |

---

## When to use what

| Phase | Focus | Priority resources |
|-------|-------|-------------------|
| Months 1–6 | Arduino, electronics, GPS + SD logging | Make: Electronics, Paul McWhorter, Microcontrollers Lab |
| Months 7–12 | I²C/SPI, displays, sensors | Arduino Workshop, Adafruit/SparkFun, DroneBot Workshop |
| Year 2 | Magnetometer, environmental, conductivity | Dentith & Mudge, sensor tutorials, IGRF calculator |
| Year 3 | PCB, enclosure, dashboard, field analysis | Phil's Lab (KiCad), QGIS, Next.js + Leaflet |

---

## Books

### Tier 1 — Start here (Year 1)

- [ ] **Make: Electronics** (3rd ed.) — Charles Platt  
  Hands-on experiments; best first book for breadboarding, LEDs, transistors, relays.

- [ ] **Arduino Workshop** (2nd ed.) — John Boxall  
  65 projects including GPS (Ch. 16), SD logging, displays, wireless.  
  [No Starch Press](https://nostarch.com/arduino-workshop-2nd-edition)

- [ ] **Getting Started in Electronics** — Forrest M. Mims III  
  Cheap, visual quick reference for Ohm's law, dividers, basic circuits.

### Tier 2 — Reference as you build (Year 1–2)

- [ ] **Practical Electronics for Inventors** (4th ed.) — Paul Scherz & Simon Monk  
  Deep reference for ADCs, op-amps, MOSFETs, power supplies.

- [ ] **Make: Encyclopedia of Electronic Components** (Vol 1–3) — Charles Platt  
  Look up any part before you buy (GPS, SD card, magnetometer, etc.).

- [ ] **Arduino Project Handbook** (Vol 1–2) — Mark Geddes  
  Short visual project recipes for quick wins between modules.  
  [No Starch Press](https://nostarch.com/arduinohandbook)

### Tier 3 — Geophysics & research (Year 2–3)

_Complete summaries in [Research Paper §5](IMEFS-Research-Paper.md#5-literature-review-todo)._

- [ ] **Geophysics for the Mineral Exploration Geoscientist** — Michael Dentith & Stephen T. Mudge  
  **Best fit for IMEFS** — magnetic surveys, resistivity, real deposit examples.  
  → Paper §5.1, §5.2, §5.3  
  [Cambridge University Press](https://www.cambridge.org/highereducation/books/geophysics-for-the-mineral-exploration-geoscientist/07D392D5911F891FE400B84D2D49D1F4)

- [ ] **An Introduction to Applied and Environmental Geophysics** (2nd ed.) — John M. Reynolds  
  Broader field geophysics context for magnetic and electrical methods.  
  → Paper §5.1, §5.3  
  [Wiley](https://www.wiley.com/en-us/An+Introduction+to+Applied+and+Environmental+Geophysics%2C+2nd+Edition-p-9780471485360)

- [ ] **Mining Geophysics** (2nd ed.) — D.S. Parasnis  
  Classic intro to ore prospecting methods.  
  → Paper §5.1  
  [Elsevier](https://shop.elsevier.com/books/mining-geophysics/parasnis/978-0-444-41077-1)

### Tier 4 — Software & data (Year 2–3)

- [ ] **Python for Data Analysis** — Wes McKinney  
  CSV analysis, pandas, statistics for field data.

- [ ] **QGIS Training Manual** (free online)  
  Map geotagged survey points.  
  → Paper §5.4  
  [qgis.org](https://qgis.org/en/docs/training_manual/)

- [ ] **Next.js documentation** or **Spring Boot tutorials** (pick one for dashboard)  
  → Paper §6.4.2

### Reference later (not for Year 1)

- [ ] **The Art of Electronics** — Horowitz & Hill  
  Excellent but advanced; use as Year 3+ reference only.

---

## YouTube channels

### Arduino & embedded (Year 1 core)

- [ ] [Paul McWhorter](https://www.youtube.com/@paulmcwhorter) — Structured Arduino course from zero
- [ ] [DroneBot Workshop](https://www.youtube.com/@DroneBotWorkshop) — Sensor projects, I²C/SPI deep-dives
- [ ] [GreatScott!](https://www.youtube.com/@greatscottlab) — Power, batteries, MOSFETs, portable devices
- [ ] [Afrotechmods](https://www.youtube.com/@afrotechmods) — Transistors, capacitors, basic EE concepts
- [ ] **Exploring Arduino** (Jeremy Blum) — Search on YouTube; companion to a well-known textbook series

### Module-specific tutorials

| Topic | Resource | IMEFS milestone |
|-------|----------|-----------------|
| GPS + SD logger | [Microcontrollers Lab — GPS Data Logger](https://microcontrollerslab.com/gps-data-logger-arduino-micro-sd-card/) | Year 1 Semester 1 |
| Portable GPS tracker | [Maker Portal — Arduino GPS Tracker](https://makersportal.com/blog/2019/9/4/arduino-gps-tracker) | Year 1 Semester 2 |
| Magnetometer / compass | Search: `HMC5883L Arduino` or `QMC5883L Arduino` | Year 2 Module 1 |
| Environmental sensors | [Random Nerd Tutorials](https://randomnerdtutorials.com/) — BME280, DHT22 | Year 2 Module 3 |
| I²C & SPI | DroneBot Workshop — search "I2C" and "SPI" | Year 1 Semester 2 |
| OLED displays | Paul McWhorter or DroneBot — search "OLED Arduino I2C" | Year 1–2 |

### PCB design (Year 3)

- [ ] [Phil's Lab](https://www.youtube.com/@PhilsLab) — Best KiCad resource
  - [KiCad 6 STM32 Full Tutorial](https://www.youtube.com/watch?v=aVUqaB0IMh4) (~1h40m, end-to-end)
  - [How To Learn PCB Design](https://www.youtube.com/watch?v=aODkA2mrimQ)
  - [KiCad 9 Tutorial Part 1 — Schematic](https://www.youtube.com/watch?v=O-zNn5k5Bn4)
  - [KiCad 9 Tutorial Part 2 — PCB Layout](https://www.youtube.com/watch?v=igQWdVGZGpI)

### Electronics fundamentals (supporting)

- [ ] [Electronoobs](https://www.youtube.com/@electronoobs) — Sensor projects, clear wiring diagrams
- [ ] [Andreas Spiess](https://www.youtube.com/@AndreasSpiess) — GPS, SD cards, IoT logging, low power
- [ ] [W2AEW](https://www.youtube.com/@w2aew) — Multimeter and oscilloscope; calibration work
- [ ] [EEVblog](https://www.youtube.com/@EEVblog) — EE mindset, datasheets, debugging

### Geophysics & GIS (Year 2–3)

- [ ] [QGIS Training Manual](https://qgis.org/en/docs/training_manual/) — Plot CSV survey data
- [ ] Search YouTube: `magnetic survey geophysics explained`
- [ ] Search YouTube: `introduction to geophysical exploration`

### Web dashboard (Year 3)

- [ ] **Traversy Media** — Next.js crash course
- [ ] **Net Ninja** — Next.js playlist
- [ ] **Leaflet.js** docs + YouTube tutorials — interactive maps from lat/lng
- [ ] **Chart.js** tutorials — time-series graphs
- [ ] **Amigoscode** or **Java Brains** — Spring Boot (if using Java instead of Next.js)

### Book overview video

- [ ] [Learn Electronics in 2025: Best Beginner-Friendly Books](https://www.youtube.com/watch?v=7YLouJfW5ss) — 15-min guide to which books to buy first

---

## Free websites

| Site | URL | IMEFS use | Paper § |
|------|-----|-----------|---------|
| Adafruit Learn | [learn.adafruit.com](https://learn.adafruit.com/) | GPS, magnetometer, SD, OLED guides | §5.5 |
| SparkFun Learn | [learn.sparkfun.com](https://learn.sparkfun.com/) | I²C/SPI, sensor hookup | §5.5 |
| Random Nerd Tutorials | [randomnerdtutorials.com](https://randomnerdtutorials.com/) | Arduino/ESP32 sensor projects | §5.5 |
| Microcontrollers Lab | [microcontrollerslab.com](https://microcontrollerslab.com/) | GPS logger, SD card projects | §5.5 |
| Arduino Reference | [arduino.cc/reference](https://www.arduino.cc/reference/en/) | Language reference | — |
| KiCad Documentation | [docs.kicad.org](https://docs.kicad.org/) | PCB design | §6.2 |
| IGRF Calculator | [NOAA Geomag](https://www.ngdc.noaa.gov/geomag/calcsgf.shtml) | Validate magnetometer vs expected field | §7.3, §10.1 |
| Hackster.io | [hackster.io](https://www.hackster.io/) | GPS tracker, weather station projects | — |
| Instructables | [instructables.com](https://www.instructables.com/) | Step-by-step project builds | — |

---

## 12-month learning plan

### Months 1–3: Foundations

- [ ] Read *Make: Electronics* Experiments 1–15
- [ ] Watch Paul McWhorter Lessons 1–20
- [ ] Build: blink LED → button → temperature sensor
- [ ] Build: **GPS + SD logger** ([Microcontrollers Lab tutorial](https://microcontrollerslab.com/gps-data-logger-arduino-micro-sd-card/))

### Months 4–6: Sensors & protocols

- [ ] Work through *Arduino Workshop* display + GPS chapters
- [ ] Watch DroneBot Workshop I²C and SPI videos
- [ ] Build: LCD display, environmental monitor, SD CSV logger

### Months 7–12: Exploration prep

- [ ] Start *Dentith & Mudge* Chapters 1–3
- [ ] Build: digital compass (magnetometer), portable weather station
- [ ] Learn Python pandas for CSV analysis
- [ ] Set up Git/GitHub for project code

### Year 2: Modules + geophysics

- [ ] Finish magnetic and electrical method chapters in Dentith & Mudge
- [ ] Watch W2AEW multimeter videos — document calibration in [Appendix C](IMEFS-Research-Paper.md#appendix-c--calibration-log-template-todo)
- [ ] Use IGRF calculator for magnetometer validation
- [ ] Complete QGIS training manual — first map from field CSV

### Year 3: Product + dashboard

- [ ] Phil's Lab KiCad tutorial → design IMEFS PCB
- [ ] GreatScott! battery/charging videos
- [ ] Next.js + Leaflet — upload CSV, plot points, color by magnetic field
- [ ] Write results in [Research Paper §10–11](IMEFS-Research-Paper.md#10-results-data)

---

## Map resources to research paper sections

| Research Paper § | Topic | Primary resources |
|------------------|-------|-------------------|
| §5.1 | Exploration geophysics fundamentals | Dentith & Mudge, Reynolds |
| §5.2 | Magnetic surveying | Dentith & Mudge Ch. 3, IGRF calculator |
| §5.3 | Resistivity / conductivity | Dentith & Mudge, Reynolds, Parasnis |
| §5.4 | GIS & spatial data | QGIS Training Manual |
| §5.5 | Embedded data acquisition | Arduino Workshop, Adafruit, SparkFun, Paul McWhorter |
| §5.6 | Calibration & signal processing | W2AEW, Practical Electronics for Inventors |
| §6.2–6.3 | Hardware design | Make: Electronics, Phil's Lab |
| §6.4.2 | Web dashboard | Next.js docs, Leaflet, Chart.js |
| §7.3 | Calibration methodology | W2AEW, IGRF calculator, Appendix C |
| §10–11 | Results & discussion | Python for Data Analysis, QGIS |

---

## Bookmark these first projects

Direct links to videos and tutorials that match your earliest milestones:

1. [Paul McWhorter — Arduino Lesson 1](https://www.youtube.com/@paulmcwhorter)
2. [GPS Data Logger — Microcontrollers Lab](https://microcontrollerslab.com/gps-data-logger-arduino-micro-sd-card/)
3. [Arduino GPS Tracker — Maker Portal](https://makersportal.com/blog/2019/9/4/arduino-gps-tracker)
4. YouTube search: **HMC5883L Arduino compass** (Year 2 magnetometer)
5. [Phil's Lab — KiCad STM32 Tutorial](https://www.youtube.com/watch?v=aVUqaB0IMh4) (Year 3)
6. [Learn Electronics: Best Beginner Books](https://www.youtube.com/watch?v=7YLouJfW5ss)

---

*Part of the [IMEFS](../README.md) project. Last updated: 2026-06-27.*
