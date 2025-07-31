# 0.25μm 64M DRAM (3rd Generation) Process Flow

> ⚠️ **Note**  
> This process table is a technical reconstruction based on Shinichi Samizo's manufacturing experience and memory from the late 1990s.  
> The content reflects the knowledge and conditions of that time and may differ from current technical documents or actual data.  
> It is not guaranteed to be accurate and should be used as reference information for educational or archival purposes only.

---

## 🔹 Key Features

| Item | Description |
|------|-------------|
| **Supply Voltage** | 3.3V for Memory Cell, Peripheral, and I/O |
| **Cell Capacitor Structure** | Stacked capacitor structure |
| **Well Structure** | Triple-well structure adopted in memory cell region |
| **Word Line** | Divided word-line structure with WSA-ALA connection |
| **Bit Line Formation** | Bit line and bit line contact formed simultaneously by WSB-CVD |
| **Storage Node Surface Treatment** | Surface roughening improved capacitance by 1.5–1.8× |

## Isolation and Well Formation

| Step Name   | Process Description              | Target Region               | Purpose                                                        | Condition                      | Notes                                                     |
|-------------|----------------------------------|------------------------------|----------------------------------------------------------------|-------------------------------|-----------------------------------------------------------|
| FS-DP       | SiON Oxynitride Deposition       | Whole Wafer                  | Interface protection before LOCOS                              | 200Å @ 700℃                   | Oxide/Nitride stack                                       |
| FSN-DP      | LOCOS Nitride Deposition         | Field Region                 | Field mask oxidation barrier                                   | 1500Å @ 750℃                  | Prevents LOCOS bird's beak                                |
| F-PH        | Field Lithography (KrF)          | Field Region                 | Define isolation area                                          | 0.35μm                         | Semi-recess pattern                                       |
| F-ET        | SIN + SION Etch                  | Field Region                 | Open field mask                                                | -                             | Removal of barrier layers                                 |
| F-OX        | LOCOS Field Oxidation            | Field Region                 | Field isolation oxide                                          | 4500Å @ 1000℃                 | Bird's beak suppression                                   |
| PRE-OX      | Sacrificial Oxide Formation      | Channel Region               | Channel protection                                              | 200Å @ 900℃                   | For gate oxide preparation                                |

## Deep N-Well / N-Well / P-Well Formation (Detailed with Multi-Purpose Implanting)

| Step Name   | Process Description              | Target Region               | Purpose                                                        | Condition                      | Notes                                                     |
|-------------|----------------------------------|------------------------------|----------------------------------------------------------------|-------------------------------|-----------------------------------------------------------|
| NWLA-PH     | Deep N-Well Lithography          | Memory Cell Region           | Define deep N-Well                                             | 1.5μm                         | For α-particle resistance                                 |
| NWLA-ION    | Deep N-Well Implant (MeV)        | Cell Deep N-Well             | Deep N-Well formation                                          | 1e13/cm² @ 1.2 MeV (P)         | High-energy for alpha immunity                            |
| NWLB-PH     | N-Well Lithography               | Peripheral Region            | Define peripheral N-Well                                       | 1.2μm                         | PMOS region                                                |
| NWLB-ION    | N-Well Implant (HC)              | Peripheral N-Well            | ① N-Well Formation<br>② PMOS Channel Doping                   | 1e13/cm² @ 300 keV (P)        | Dual-purpose (Well + Channel)                             |
| PWL-PH      | P-Well Lithography               | Cell & Peripheral Region     | P-Well Definition                                               | 1.0μm                         | Includes Cell/NMOS region and Field Stopper               |
| PWL-ION     | P-Well Implant (HC)              | P-Well (Cell/Peripheral)     | ① P-Well Formation<br>② Field Stopper<br>③ NMOS Channel Doping| 1e13/cm² @ 150 keV (B)        | Triple-purpose implant                                    |

## Gate Stack Formation

| Step Name   | Process Description              | Thickness   | CD/AR      | Temp     | Notes                                                     |
|-------------|----------------------------------|-------------|------------|----------|-----------------------------------------------------------|
| G-OX        | Gate Oxide Formation             | 80Å         | -          | 800℃     | High-quality thermal oxidation                            |
| PLYA-DP     | Doped Poly Deposition            | 2000Å       | -          | 620℃     | Gate Poly (LPCVD)                                         |
| WSA-DP      | WSi Deposition                   | 1500Å       | -          | 450℃     | Gate electrode formation                                  |
| BRAC-DP     | Barrier Cap Deposition           | 800Å        | -          | 400℃     | Oxide cap over gate                                       |
| WSA-PH      | Gate Pattern Lithography (KrF)   | -           | 0.25μm     | -        | High-resolution gate definition                           |
| WSA-ET      | Gate Etch                        | -           | -          | RT       | Maintain insulation via BRAC                              |

## Bit Line & V1 Contact Formation

| Step Name   | Process Description              | Notes                                                     |
|-------------|----------------------------------|-----------------------------------------------------------|
| THA-DP      | TEOS Deposition (V1)             | 4000Å @ 650℃                                               |
| THA-PH      | V1 Lithography (KrF)             | AR=2, layout avoiding gate interference                    |
| THA-ET      | V1 Contact Etch                  | Contact hole formation                                     |
| PLYB-DP     | Doped Poly Deposition (BL)       | 2500Å @ 620℃                                               |
| WSB-DP      | WSi Deposition (Bit Line)        | 1800Å @ 450℃                                               |
| WSB-PH      | Bit Line Lithography (KrF)       | 0.25μm L/S                                                 |
| WSB-ET      | Bit Line Etch                    | Isolation maintained via BRAC                              |

## Capacitor Formation (Lower Electrode to Upper Electrode)

| Step Name   | Process Description              | Notes                                                     |
|-------------|----------------------------------|-----------------------------------------------------------|
| THB-DP      | TEOS Deposition (V2)             | 6000Å @ 650℃                                               |
| THB-PH      | V2 Lithography (KrF)             | AR=8, for deep contact                                     |
| THB-ET      | V2 Etch                          | Deep contact hole                                          |
| PLYC-DP     | Thick Poly Deposition            | 8000Å @ 620℃ lower electrode                               |
| PLYC-PH     | Lower Electrode Lithography      | 0.25μm                                                     |
| PLYC-ET     | Lower Electrode Etch             | Residue = short risk                                       |
| PLYC2-DP    | Surface Roughening               | 700℃, increases capacitance 1.5–1.8×                      |
| SIN-DP      | SiN Dielectric Deposition        | 150Å @ 750℃                                                |
| SIN-OX      | SiN Oxidation                    | 800℃, ONO dielectric structure                             |
| PLYD-DP     | Upper Electrode Deposition       | 2000Å Poly                                                 |
| PLYD-PH     | Upper Electrode Lithography      | 0.3μm                                                      |
| PLYD-ET     | Upper Electrode Etch             | Cell plate formation                                       |

## Interlayer Dielectric / W-Plug / M1-M2 Interconnect

| Step Name   | Process Description              | Notes                                                     |
|-------------|----------------------------------|-----------------------------------------------------------|
| F2-DP       | BPSG Deposition                  | 1.0μm @ 750℃ smoothing topography                         |
| F2-ANL      | BPSG Reflow                      | 850℃ planarization                                        |
| CNT-PH      | Component Lithography (KrF)      | AR=6, half-tone mask                                      |
| CNT-ET      | W Contact Etch                   | Connect N+/P+                                             |
| TI-SP       | Ti Barrier Sputtering            | 300Å LT sputtering                                        |
| LAMP-ANL    | LAMP Anneal                      | 400℃ activate TiN & junction                              |
| CW-DP       | W Plug Deposition (CVD WF₆)      | 4000Å                                                      |
| CW-ET       | W Etch-back                      | No CMP                                                    |

## M1/M2 Metallization, Pad & Passivation

| Step Name   | Process Description              | Notes                                                     |
|-------------|----------------------------------|-----------------------------------------------------------|
| ALA-SP      | M1 Sputter (Ti/AlCu/TiN)         | 6000Å / 0.4μm L/S                                          |
| HL1-DP      | ILD1 Deposition                  | 7000Å                                                      |
| HL-SOG      | SOG Coating                      | 5000Å                                                      |
| HL2-DP      | ILD2 Deposition                  | 7000Å                                                      |
| HL-PH       | Via Lithography                  | AR=4 M1→M2                                                 |
| HL-ET       | Via Etch                         | Open ILD                                                   |
| ALB-SP      | M2 Sputter (Ti/AlCu/TiN)         | 6000Å / 0.4μm L/S                                          |
| ALB-PH      | M2 Lithography                   | 0.35μm                                                     |
| ALB-ET      | M2 Etch                          | Final wiring                                               |
| PAD-DP      | Passivation Deposition (SiN/PI)  | 5000Å @ 350℃                                               |
| PAD-PH      | Pad Lithography                  | 60μm                                                       |
| PAD-ET      | Pad Etch                         | Aluminum exposure                                          |
| AL-SNT      | Hydrogen Sinter                  | 450℃, reduces metal leakage                                |
| POP-PH      | PI Coat Lithography              | 60μm, for optical PI                                       |
| POP-CUR     | PI Cure                          | 300℃, harden final film                                    |
| E-TEST      | Electrical Testing               | TEG measurement (RT)                                       |

---
