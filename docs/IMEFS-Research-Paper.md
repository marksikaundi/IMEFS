# Design and Evaluation of a Low-Cost Integrated Mineral Exploration Field Station (IMEFS) for Portable Geophysical and Environmental Data Acquisition

**Author:** Mark Sikaundi  
**Affiliation:** _[University / Department — to be completed]_  
**Supervisor:** _[Name — to be completed]_  
**Document type:** Living research paper / dissertation draft  
**Version:** 0.1.0  
**Last updated:** 2026-06-27  
**Status:** Draft — active development

---

## How to Use This Document

This file is a **living research paper**. Update it as you learn, build, test, and analyze data. Treat each section like a chapter you refine over the three-year project timeline.

### Section status legend

| Status | Meaning |
|--------|---------|
| `[DRAFT]` | Written but needs review or expansion |
| `[TODO]` | Not started — fill in when you reach that project phase |
| `[DATA]` | Waiting on experimental or field data |
| `[REVIEW]` | Ready for supervisor or peer review |
| `[DONE]` | Section complete for current project stage |

### When to update

| Project event | Sections to update |
|---------------|-------------------|
| Finish a module (GPS, magnetometer, etc.) | §6, §7, §8, Appendix B |
| Run calibration tests | §7.3, §9, Appendix C |
| Conduct field survey | §8, §9, §10, Appendix D |
| Analyze results | §10, §11 |
| Build dashboard | §6.2, §8 |
| Read a new paper | §4, §15 |
| Supervisor feedback | Any flagged section + §16 changelog |

### Contribution log

Record meaningful updates in [Appendix E](#appendix-e-document-changelog).

---

## Abstract `[DRAFT]`

Mineral exploration fieldwork often requires geologists to carry multiple instruments for magnetic surveying, positioning, environmental monitoring, and conductivity measurement. Commercial geophysical equipment is accurate but expensive, heavy, and typically operated by specialist teams. This research proposes and evaluates the **Integrated Mineral Exploration Field Station (IMEFS)** — a portable, low-cost embedded system that integrates MEMS-based magnetometry, GPS positioning, environmental sensing, and prototype soil conductivity measurement into a single data-logging platform.

The system uses an Arduino-based microcontroller to acquire sensor readings, timestamp and geotag measurements, store data locally on SD card in CSV format, and export datasets to a web dashboard for mapping, visualization, and report generation. The research investigates whether low-cost consumer-grade sensors can be combined into a practical field instrument suitable for preliminary mineral exploration workflows in resource-rich regions such as Zambia's Copperbelt and North-Western Province.

_[TODO: Add quantitative results after field testing — e.g., sensor accuracy vs reference instruments, survey point count, anomaly detection case study.]_

**Keywords:** mineral exploration, geophysics, embedded systems, magnetometer, electrical conductivity, GPS surveying, data logging, low-cost instrumentation, Zambia

---

## 1. Introduction `[DRAFT]`

### 1.1 Background

Mineral exploration is a data-intensive process. Geologists and geophysicists collect magnetic, electrical, environmental, and positional measurements to identify geological structures and mineralization targets. Professional surveys use specialized magnetometers, resistivity meters, and high-precision GPS receivers — equipment that is often beyond the budget and portability requirements of student researchers, small exploration teams, and early-stage field programs.

Recent advances in MEMS sensors, low-cost GPS modules, and open-source embedded platforms (Arduino, Raspberry Pi) have made it possible to prototype field instruments at a fraction of commercial cost. However, integrating multiple sensors into a reliable, calibrated, field-ready system remains an engineering and scientific challenge.

### 1.2 Motivation

Zambia's mining sector — including operators such as Mopani, Konkola Copper Mines (KCM), First Quantum Minerals, and Barrick Lumwana — depends on effective exploration to sustain production. There is a need for affordable tools that support field data collection, particularly for:

- Undergraduate and postgraduate research
- Community and junior exploration programs
- Teaching geophysics and field instrumentation
- Prototyping decision-support systems before commercial investment

This project addresses that gap by designing IMEFS as a **research-driven field instrument**, not merely a hobby electronics build.

### 1.3 Research gap

_[TODO: Expand after literature review with specific citations comparing commercial vs low-cost systems.]_

Existing literature covers individual topics — magnetic surveys, resistivity methods, embedded data acquisition — but fewer studies evaluate an **integrated, multi-sensor, geotagged platform** built from low-cost components for mineral exploration in developing-economy field conditions (heat, dust, limited power, rough terrain).

---

## 2. Problem Statement `[DRAFT]`

Field geologists and exploration students often lack access to integrated, portable instrumentation that simultaneously records:

1. Magnetic field components (X, Y, Z and total field)
2. GPS coordinates (latitude, longitude, altitude, time)
3. Environmental conditions (temperature, humidity, pressure)
4. Soil electrical conductivity (proxy for resistivity surveying)
5. Consistent, exportable data tied to location and time

Carrying separate devices increases cost, weight, training burden, and data synchronization errors. The problem this research addresses is:

> **Can a low-cost, Arduino-based integrated field station provide geotagged geophysical and environmental data of sufficient quality to support preliminary mineral exploration workflows?**

---

## 3. Research Objectives `[DRAFT]`

### 3.1 Primary objective

To design, build, calibrate, and evaluate a portable Integrated Mineral Exploration Field Station (IMEFS) capable of logging multi-parameter field data with GPS coordinates.

### 3.2 Specific objectives

| ID | Objective | Target milestone |
|----|-----------|------------------|
| O1 | Develop modular sensor interfaces (magnetometer, GPS, environmental, conductivity) | Year 2 |
| O2 | Implement reliable SD-card data logging in standardized CSV format | Year 1–2 |
| O3 | Design custom PCB and battery-powered enclosure for field deployment | Year 3 |
| O4 | Build web dashboard for upload, mapping, visualization, and PDF reporting | Year 3 |
| O5 | Calibrate each sensor against reference measurements | Year 2–3 |
| O6 | Conduct field validation survey and compare with known geological context | Year 3 |
| O7 | Document limitations, error sources, and suitable application domains | Year 3 |

---

## 4. Research Questions `[DRAFT]`

| ID | Question |
|----|----------|
| RQ1 | How accurate are low-cost MEMS magnetometers compared with reference magnetometers or published regional field values? |
| RQ2 | Can GPS, magnetic, environmental, and conductivity data be reliably synchronized and geotagged on a single embedded platform? |
| RQ3 | What calibration and signal processing techniques (filtering, averaging, outlier rejection) most improve data quality? |
| RQ4 | Can a prototype soil conductivity sensor provide useful relative measurements for exploration screening? |
| RQ5 | What are the practical limitations of IMEFS in real field conditions (temperature drift, EMI, battery life, enclosure)? |
| RQ6 | Does the integrated dataset support identification of magnetic or conductivity anomalies when visualized on a map? |

---

## 5. Literature Review `[TODO]`

_Complete this section incrementally as you read. Aim for 15–25 references by dissertation submission._

### 5.1 Exploration geophysics fundamentals

_[TODO: Summarize magnetic surveying, electrical resistivity, and their role in mineral exploration.]_

**Papers to read and summarize:**

- [ ] Introduction to Exploration Geophysics — _[Author, Year]_
- [ ] Magnetic Survey Methods — _[Author, Year]_
- [ ] Electrical Resistivity Survey — _[Author, Year]_

**Notes:**

```
[Add summary, key equations, and relevance to IMEFS here]
```

### 5.2 Magnetic surveying and anomaly detection

_[TODO: Cover total field measurement, diurnal variation, sensor orientation, anomaly thresholds.]_

**Notes:**

```
```

### 5.3 Electrical resistivity and soil conductivity

_[TODO: Relate resistivity method to simplified conductivity probe design.]_

**Notes:**

```
```

### 5.4 GIS and spatial data in mineral exploration

_[TODO: WGS84, UTM, map visualization, interpolation methods (e.g., IDW).]_

**Notes:**

```
```

### 5.5 Embedded data acquisition systems

_[TODO: Arduino/embedded logging, SD storage, serial protocols I²C/SPI/UART.]_

**Notes:**

```
```

### 5.6 Sensor calibration and signal processing

_[TODO: Offset calibration, temperature compensation, moving averages, Kalman filtering if applicable.]_

**Notes:**

```
```

### 5.7 Low-cost geophysical instrumentation

_[TODO: Find 3–5 papers on DIY or low-cost geophysical tools. Compare with IMEFS approach.]_

| Reference | Instrument | Sensors | Cost | Findings | Gap IMEFS fills |
|-----------|------------|---------|------|----------|-----------------|
| _[TODO]_ | | | | | |

### 5.8 Synthesis — research gap statement

_[TODO: After review, write 1–2 paragraphs stating exactly what IMEFS contributes that prior work does not.]_

---

## 6. System Design `[DRAFT]`

### 6.1 Design requirements

| Requirement | Description | Priority |
|-------------|-------------|----------|
| FR1 | Log magnetic field (X, Y, Z, total) | High |
| FR2 | Log GPS position and timestamp | High |
| FR3 | Log temperature, humidity, pressure | Medium |
| FR4 | Log soil conductivity (prototype) | Medium |
| FR5 | Store data on SD card as CSV | High |
| FR6 | Display live readings on OLED | Medium |
| FR7 | Operate on battery power ≥ 4 hours | High |
| FR8 | Export data via USB (Bluetooth optional) | Medium |
| FR9 | Weather-resistant field enclosure | High |
| NFR1 | Unit cost under ZMW 3,500 total | High |
| NFR2 | Single-operator use | High |
| NFR3 | Readable datasheets and reproducible design | Medium |

### 6.2 System architecture

```
                 Integrated Mineral Exploration Field Station

                    ┌─────────────────────────┐
                    │      Arduino Uno        │
                    │   (or compatible MCU)   │
                    └────────────┬────────────┘
                                 │
         ┌──────────────┬─────────┴───────────┬───────────────┐
         │              │                     │               │
    Magnetometer   GPS Module         Conductivity Sensor  Temp/Humidity
    (MEMS 3-axis)  (UART/NMEA)        (prototype)          (I²C)
         │              │                     │               │
         └──────────────┴──────────┬──────────┴───────────────┘
                                   │
                             SD Card Logger
                                   │
                              OLED Display
                                   │
                           USB / Bluetooth
                                   │
                         Web Dashboard
                                   │
                     Maps • Graphs • Reports • CSV
```

### 6.3 Hardware modules

#### Module 1 — Magnetometer `[TODO: specify part numbers after procurement]`

| Parameter | Planned specification |
|-----------|----------------------|
| Sensor | _[e.g., HMC5883L / QMC5883L / LIS3MDL — TBD]_ |
| Outputs | X, Y, Z (µT), total field (µT) |
| Interface | I²C |
| Sampling rate | _[TBD Hz]_ |
| Research focus | Detect magnetic anomalies associated with iron-rich formations |

#### Module 2 — GPS `[TODO]`

| Parameter | Planned specification |
|-----------|----------------------|
| Sensor | _[e.g., NEO-6M / NEO-M8N — TBD]_ |
| Outputs | Latitude, longitude, altitude, UTC time |
| Coordinate systems | WGS84 (log), UTM (dashboard conversion) |
| Interface | UART |

#### Module 3 — Environmental `[TODO]`

| Parameter | Planned specification |
|-----------|----------------------|
| Sensor | _[e.g., BME280 — TBD]_ |
| Outputs | Temperature (°C), humidity (%), pressure (hPa) |
| Additional | Light level, battery voltage |
| Interface | I²C |

#### Module 4 — Conductivity (prototype) `[TODO]`

| Parameter | Planned specification |
|-----------|----------------------|
| Method | _[Two-electrode or four-electrode — TBD]_ |
| Output | Conductivity (mS/cm) or resistance (Ω) |
| Note | Not a replacement for professional resistivity meters |

#### Module 5 — Data logger and display

| Component | Role |
|-----------|------|
| Micro SD module | Primary field storage |
| OLED display | Live readings and status |
| Push buttons | Start/stop logging, mark waypoints |
| RTC module (optional) | Timestamp when GPS fix unavailable |

### 6.4 Software architecture

#### 6.4.1 Embedded firmware (Arduino / C++)

_[TODO: Add state machine diagram and pseudocode as firmware matures.]_

Planned functions:

- Sensor initialization (I²C, UART, SPI)
- Periodic sampling loop with configurable interval
- GPS fix validation before logging
- CSV row formatting and SD write
- Button interrupts for user control
- Low-battery warning

#### 6.4.2 Web dashboard (Next.js or Spring Boot)

| Feature | Description | Status |
|---------|-------------|--------|
| CSV upload | Parse IMEFS field files | `[TODO]` |
| Map view | Plot geotagged points, color by magnetic field | `[TODO]` |
| Time-series graphs | Temperature, conductivity, magnetic field vs time | `[TODO]` |
| Statistics | Mean, max, min, std dev per survey | `[TODO]` |
| PDF report | Survey summary for field team | `[TODO]` |
| Anomaly highlighting | Flag points above threshold | `[TODO]` |

### 6.5 Data schema

Standard CSV format (see [Appendix B](#appendix-b-csv-data-schema)):

```csv
survey_id,point_id,timestamp_utc,latitude,longitude,altitude_m,mag_x_uT,mag_y_uT,mag_z_uT,mag_total_uT,temperature_c,humidity_pct,pressure_hpa,conductivity_mS_cm,battery_v,notes
```

---

## 7. Methodology `[DRAFT]`

### 7.1 Research approach

This study follows a **design science and experimental evaluation** approach:

1. **Design** — Define requirements and architecture
2. **Build** — Implement modules incrementally (Years 1–3)
3. **Calibrate** — Compare against reference values
4. **Deploy** — Conduct controlled and field surveys
5. **Evaluate** — Analyze accuracy, reliability, and usability
6. **Report** — Document findings and limitations

### 7.2 Development methodology

Development follows the three-year roadmap:

| Phase | Duration | Focus |
|-------|----------|-------|
| Phase 1 | Year 1 | Arduino fundamentals, GPS logger, environmental monitor |
| Phase 2 | Year 2 | Individual instrument modules with calibration |
| Phase 3 | Year 3 | PCB integration, enclosure, dashboard, field validation |

### 7.3 Calibration methodology `[TODO]`

Document calibration procedure for each sensor before field use.

#### Magnetometer calibration

| Step | Procedure | Result |
|------|-----------|--------|
| 1 | Hard-iron / soft-iron calibration (figure-8 motion or known method) | `[TODO]` |
| 2 | Compare total field with IGRF model for survey location | `[TODO]` |
| 3 | Compare with reference magnetometer if available | `[TODO]` |

#### GPS validation

| Step | Procedure | Result |
|------|-----------|--------|
| 1 | Log fixed point for 30 min, compute position scatter | `[TODO]` |
| 2 | Compare altitude with known elevation | `[TODO]` |

#### Environmental sensors

| Step | Procedure | Result |
|------|-----------|--------|
| 1 | Compare temperature/humidity with reference hygrometer | `[TODO]` |

#### Conductivity probe

| Step | Procedure | Result |
|------|-----------|--------|
| 1 | Calibrate with standard conductivity solutions | `[TODO]` |

### 7.4 Signal processing `[TODO]`

Techniques to evaluate and document:

- [ ] Moving average filter (window size: ___ samples)
- [ ] Outlier rejection (threshold: ___ σ)
- [ ] Temperature compensation for magnetometer drift
- [ ] GPS fix quality gate (minimum satellites: ___)
- [ ] _[Optional: Kalman filter for sensor fusion]_

### 7.5 Field survey protocol `[TODO]`

Define before Year 3 field campaign.

| Parameter | Planned value |
|-----------|---------------|
| Survey area | _[e.g., Solwezi / campus test site — TBD]_ |
| Grid spacing | _[e.g., 10 m — TBD]_ |
| Walking speed | Consistent pace, pause at each point |
| Point dwell time | _[e.g., 5 s averaging — TBD]_ |
| Weather conditions | Record temperature, cloud cover, wind |
| Ground conditions | Record soil type, moisture, topography |

---

## 8. Implementation Progress `[TODO]`

_Update this table as modules are completed._

| Module | Design | Prototype | Calibrated | Field-tested | Notes |
|--------|--------|-----------|------------|--------------|-------|
| GPS logger | ☐ | ☐ | ☐ | ☐ | |
| SD data logger | ☐ | ☐ | ☐ | ☐ | |
| Environmental monitor | ☐ | ☐ | ☐ | ☐ | |
| Magnetometer | ☐ | ☐ | ☐ | ☐ | |
| Conductivity probe | ☐ | ☐ | ☐ | ☐ | |
| OLED + buttons UI | ☐ | ☐ | ☐ | ☐ | |
| Custom PCB | ☐ | ☐ | ☐ | ☐ | |
| Battery + enclosure | ☐ | ☐ | ☐ | ☐ | |
| Web dashboard | ☐ | ☐ | ☐ | ☐ | |
| Integrated IMEFS v1 | ☐ | ☐ | ☐ | ☐ | |

---

## 9. Experimental Design `[TODO]`

### 9.1 Experiment 1 — Sensor accuracy (lab)

**Hypothesis:** Low-cost sensors produce readings within acceptable error bounds for screening-level exploration when calibrated.

| Sensor | Independent variable | Dependent variable | Reference instrument |
|--------|---------------------|-------------------|---------------------|
| Magnetometer | Known field / IGRF | Total field (µT) | _[TBD]_ |
| Temperature | Controlled range | Reading (°C) | Reference thermometer |
| Conductivity | Standard solutions | Conductivity (mS/cm) | Calibrated meter |

### 9.2 Experiment 2 — Data logging reliability

**Hypothesis:** IMEFS logs ≥ 99% of sample intervals without data loss over a 4-hour session.

| Metric | Target | Measured |
|--------|--------|----------|
| Missing rows | 0% | `[TODO]` |
| Timestamp monotonicity | 100% | `[TODO]` |
| GPS fix rate | ≥ 95% outdoors | `[TODO]` |

### 9.3 Experiment 3 — Field survey (case study)

**Hypothesis:** Geotagged magnetic data from IMEFS reveals spatial variation correlating with geological context or known anomalies.

_[TODO: Define survey site, expected geology, and comparison data source.]_

---

## 10. Results `[DATA]`

_Replace placeholders with actual measurements as experiments complete._

### 10.1 Magnetometer calibration results

| Condition | IMEFS (µT) | Reference (µT) | Error (%) |
|-----------|-------------|----------------|-----------|
| _[TODO]_ | | | |

### 10.2 GPS accuracy

| Metric | Value |
|--------|-------|
| Horizontal scatter (CEP) | _[TODO] m_ |
| Altitude error | _[TODO] m_ |

### 10.3 Environmental sensor comparison

| Sensor | IMEFS | Reference | Error |
|--------|-------|-----------|-------|
| Temperature | _[TODO]_ | _[TODO]_ | _[TODO]_ |
| Humidity | _[TODO]_ | _[TODO]_ | _[TODO]_ |

### 10.4 Conductivity calibration curve

_[TODO: Insert table or describe linear fit equation.]_

### 10.5 Field survey summary

| Parameter | Value |
|-----------|-------|
| Survey ID | _[TODO]_ |
| Location | _[TODO]_ |
| Points collected | _[TODO]_ |
| Duration | _[TODO]_ |
| Average magnetic field | _[TODO] µT_ |
| Maximum magnetic field | _[TODO] µT_ |
| Average conductivity | _[TODO] mS/cm_ |
| Average temperature | _[TODO] °C_ |

### 10.6 Map and visualization

_[TODO: Insert map screenshot or link to dashboard export after field test.]_

```
[Placeholder for anomaly map — red = high magnetic field, blue = low]
```

---

## 11. Discussion `[TODO]`

_Answer each research question explicitly using results from §10._

### 11.1 RQ1 — Magnetometer accuracy

_[TODO]_

### 11.2 RQ2 — Multi-sensor integration

_[TODO]_

### 11.3 RQ3 — Signal processing impact

_[TODO]_

### 11.4 RQ4 — Conductivity prototype utility

_[TODO]_

### 11.5 RQ5 — Field limitations

_[TODO: Discuss temperature drift, EMI from power lines, battery life, enclosure durability.]_

### 11.6 RQ6 — Anomaly detection utility

_[TODO]_

### 11.7 Comparison with commercial systems

| Aspect | Commercial instrument | IMEFS | Implication |
|--------|----------------------|-------|-------------|
| Cost | _[TODO]_ | ~ZMW 3,100 | |
| Accuracy | _[TODO]_ | _[TODO]_ | |
| Portability | _[TODO]_ | _[TODO]_ | |
| Training required | _[TODO]_ | _[TODO]_ | |

---

## 12. Limitations `[DRAFT]`

Acknowledged limitations of the current design:

1. **Sensor grade** — MEMS magnetometers are not replacement for proton precession or fluxgate magnetometers used in professional surveys.
2. **Conductivity probe** — Prototype measures near-surface soil conductivity, not full electrical resistivity tomography.
3. **Environmental interference** — Power lines, vehicles, and ferrous objects affect magnetic readings.
4. **GPS accuracy** — Consumer GPS modules lack survey-grade precision (cm-level).
5. **Single-point sampling** — No continuous profiling along traverses unless post-processed.
6. **Platform constraints** — Arduino memory and processing limit advanced on-board filtering.
7. **Geological interpretation** — IMEFS provides data; geological conclusions require expert analysis.

---

## 13. Future Work `[DRAFT]`

### 13.1 Hardware improvements

- Upgrade to higher-sensitivity magnetometer
- Add Bluetooth Low Energy for wireless data transfer
- Design ruggedized IP-rated enclosure
- Integrate solar charging

### 13.2 Software and analytics

- Real-time anomaly alerts on OLED
- Inverse distance weighting (IDW) interpolation for contour maps
- Export to GeoJSON / Shapefile for QGIS
- Automated quality-control flags in dashboard

### 13.3 Machine learning extension (post-graduation)

Train a model to predict mineralization probability from field features:

| Input features | Output |
|----------------|--------|
| Magnetic field, conductivity, elevation, temperature | Probability of mineralization |

This would evolve IMEFS from a **data collection tool** into an **intelligent decision-support system**.

### 13.4 Publication targets

| Venue type | Example | When |
|------------|---------|------|
| Undergraduate dissertation | University submission | Year 3 |
| Local engineering conference | _[TBD]_ | Year 3 |
| IEEE / instrumentation workshop | _[TBD]_ | Post-graduation |
| Mining/geophysics journal | _[TBD]_ | If results are strong |

---

## 14. Conclusion `[TODO]`

_[Write after field validation — summarize problem, approach, key findings, and contribution to low-cost exploration instrumentation.]_

---

## 15. References `[TODO]`

_Use IEEE or APA format consistently. Expand as you read._

1. _[Author, A. A.] ([Year]). [Title]. [Journal/Publisher]._
2. _[Author, B. B.] ([Year]). [Title]. [Journal/Publisher]._
3. Reynolds, J. M. ([Year]). *An Introduction to Applied and Environmental Geophysics*. _[Edition, publisher — verify]_.
4. _[Magnetic survey methods reference — TBD]_
5. _[Electrical resistivity survey reference — TBD]_
6. _[GIS for mineral exploration — TBD]_
7. _[Embedded data acquisition — TBD]_
8. _[Sensor calibration — TBD]_
9. _[IGRF model documentation — NOAA/GFZ — TBD]_
10. _[Low-cost geophysical instrument paper — TBD]_

---

## Appendix A — Bill of Materials Template `[TODO]`

| Component | Part number | Qty | Unit cost (ZMW) | Year | Purchased |
|-----------|-------------|-----|-----------------|------|-----------|
| Arduino Uno | | 1 | | 1 | ☐ |
| GPS module | | 1 | | 1 | ☐ |
| Micro SD module | | 1 | | 1 | ☐ |
| OLED display | | 1 | | 1 | ☐ |
| Magnetometer | | 1 | | 2 | ☐ |
| BME280 (env.) | | 1 | | 2 | ☐ |
| Conductivity probe parts | | 1 | | 2 | ☐ |
| PCB fabrication | | 1 | | 3 | ☐ |
| Battery + charger | | 1 | | 3 | ☐ |
| Enclosure | | 1 | | 3 | ☐ |
| **Total** | | | **~3,100** | | |

---

## Appendix B — CSV Data Schema `[DRAFT]`

| Column | Type | Unit | Description |
|--------|------|------|-------------|
| `survey_id` | string | — | Survey identifier (e.g., `SURVEY-001`) |
| `point_id` | integer | — | Sequential point number |
| `timestamp_utc` | ISO 8601 | — | UTC timestamp from GPS or RTC |
| `latitude` | float | degrees | WGS84 latitude |
| `longitude` | float | degrees | WGS84 longitude |
| `altitude_m` | float | m | Altitude above sea level |
| `mag_x_uT` | float | µT | Magnetic field X-axis |
| `mag_y_uT` | float | µT | Magnetic field Y-axis |
| `mag_z_uT` | float | µT | Magnetic field Z-axis |
| `mag_total_uT` | float | µT | Total magnetic field magnitude |
| `temperature_c` | float | °C | Air temperature |
| `humidity_pct` | float | % | Relative humidity |
| `pressure_hpa` | float | hPa | Atmospheric pressure |
| `conductivity_mS_cm` | float | mS/cm | Soil conductivity |
| `battery_v` | float | V | Battery voltage |
| `notes` | string | — | Operator notes or waypoint label |

**Example row:**

```csv
SURVEY-001,42,2026-06-27T10:30:00Z,-12.123456,26.456789,1285.2,18.4,-5.2,42.1,45.8,26.4,65.2,1013.2,12.8,3.92,clear sky
```

---

## Appendix C — Calibration Log Template `[TODO]`

| Date | Sensor | Method | Reference value | IMEFS reading | Correction applied | Operator | Notes |
|------|--------|--------|-----------------|---------------|-------------------|----------|-------|
| | | | | | | | |

---

## Appendix D — Field Survey Log Template `[TODO]`

| Field | Value |
|-------|-------|
| Survey ID | |
| Date | |
| Location / area name | |
| Coordinates (centre) | |
| Operator(s) | |
| Weather | |
| Equipment version | IMEFS v___ |
| Firmware version | |
| Grid spacing | |
| Total points | |
| Start time | |
| End time | |
| Issues encountered | |
| Data file name(s) | |

**Site sketch / photo references:**

```
[Attach photos or link to /data/field-surveys/ folder when created]
```

---

## Appendix E — Document Changelog

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1.0 | 2026-06-27 | Mark Sikaundi | Initial living paper scaffold from Journey and Roadmap |

---

## Appendix F — Milestone Alignment

Maps paper sections to the project roadmap.

| Roadmap milestone | Paper sections to update |
|-------------------|-------------------------|
| Months 1–6: Arduino, GPS, environmental monitor | §6.3, §8, Appendix A |
| Months 7–12: Compass, SD logger, calibration | §7.3, Appendix C |
| Months 13–18: Magnetometer module | §6.3, §9.1, §10.1 |
| Months 19–24: Conductivity + integrated logging | §6.3, §9, §10.4 |
| Months 25–30: PCB, enclosure, battery | §6.2, §8, §12 |
| Months 31–36: Dashboard, field test, dissertation | §6.4, §9.3, §10–§14 |

---

*This document is part of the [IMEFS](../README.md) project repository.*
