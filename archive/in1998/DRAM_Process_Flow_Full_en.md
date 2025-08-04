# 0.25μm 64M DRAM (3rd Generation) Process Flow

> ⚠️ **Note**  
> This process table is a technical reconstruction based on Shinichi Samizo's manufacturing experience and memory from the late 1990s.  
> The content reflects knowledge and conditions of that time and may differ from current technical documents or actual data.  
> It is not guaranteed to be accurate and should be used as reference information for educational or archival purposes only.

---

## 🔹 Key Features

| Item | Description |
|------|-------------|
| **Supply Voltage** | 3.3V for Memory Cell, Peripheral, and I/O |
| **Cell Capacitor Structure** | Stacked capacitor structure |
| **Well Structure** | Triple-well adopted in memory cell region |
| **Word Line Structure** | Divided word-line structure with WSA-ALA connection |
| **Bit Line Formation** | Bit line and bit line contact formed simultaneously by WSB-CVD |
| **Storage Node Treatment** | Surface roughening improved capacitance by 1.5–1.8× |

---

## 🟫 Device Isolation Formation

| Step | Process Description | Target Area | Purpose | Conditions | Notes |
|------|----------------------|-------------|---------|------------|-------|
| **FS-DP** | SiON deposition | Whole wafer | Pre-LOCOS interface protection | 200Å @ 700℃ | Improved interface quality |
| **FSN-DP** | Field Nitride deposition | Field area | LOCOS oxidation mask | 1500Å @ 750℃ | Main hard mask before oxidation |
| **F-PH** | Field lithography (KrF) | Field area | Patterning LOCOS region | 0.35μm | Semi-recess LOCOS layout |
| **F-ET** | Etching SIN + SiON | Field area | Open field oxide region | - | Selective removal of multilayer mask |
| **F-OX** | Thermal field oxidation (LOCOS) | Field area | Field oxide isolation | 4500Å @ 1000℃ | Bird’s beak minimization |
| **PRE-OX** | Sacrificial oxidation | Channel region | Channel surface protection | 200Å @ 900℃ | Cleaning and surface smoothing |

---

## 🧪 Well & Channel Doping (Deep/N/P-Well, Channel Doping)

| Step | Process Description | Target Area | Purpose | Conditions | Notes |
|------|----------------------|-------------|---------|------------|-------|
| **NWLA-PH** | Deep N-Well lithography | Memory cell region | Define Deep N-Well | 1.5μm | Deep region for α-particle immunity |
| **NWLA-ION** | Deep N-Well implantation (MeV) | Memory cell region | Form high-resistance N-Well | 1e13/cm² @ 1.2 MeV (P⁺) | Exclusive to memory cell area |
| **NWLB-PH** | N-Well lithography | Peripheral region | Define N-Well | 1.2μm | For peripheral PMOS devices |
| **NWLB-ION** | N-Well implantation (HC) | Peripheral region | (1) Form N-Well<br>(2) PMOS channel doping | 1e13/cm² @ 300 keV (P⁺) | Combines two functions in one step |
| **PWL-PH** | P-Well lithography | Cell + Peripheral | Define P-Well | 1.0μm | Includes Field Stopper region |
| **PWL-ION** | P-Well implantation (HC) | Same as above | (1) Form P-Well<br>(2) Field Stopper<br>(3) NMOS channel doping | 1e13/cm² @ 150 keV (B⁺) | Three functions integrated in one step |

---

## 🟦 Gate Oxide & Gate Electrode Formation (Word Line WSA)

| Step | Process Description | Thickness | CD | Temp | Notes |
|------|----------------------|-----------|----|------|-------|
| **G-OX** | Gate oxide formation | 80Å | - | 800℃ | High-quality thermal oxide by LPCVD |
| **PLYA-DP** | Doped poly-Si deposition | 2000Å | - | 620℃ | Poly-Si for gate electrode |
| **WSA-DP** | WSi deposition (CVD) | 1500Å | - | 450℃ | Tungsten silicide on poly-Si |
| **BRAC-DP** | Barrier cap deposition (SiO₂) | 800Å | - | 400℃ | Etch protection and insulation |
| **WSA-PH** | Gate lithography (KrF) | - | 0.25μm | - | High-resolution patterning |
| **WSA-ET** | Gate etching | - | - | RT | Keeps BRAC layer for insulation |

---

## ⚙️ Source & Drain Formation

| Step | Process Description | Target Area | Purpose | Conditions | Notes |
|------|----------------------|-------------|---------|------------|-------|
| **NLD-PH**    | NMOS LDD lithography | Peripheral | Define LDD region | 0.35μm | High-precision patterning |
| **NLD-ION**   | NMOS LDD implantation | Peripheral | Form shallow N⁻ diffusion | 5e13/cm² @ 40 keV (As⁺) | For low electric field |
| **NLDC-PH**   | NMOS Cell LDD lithography | Cell | Define LDD for memory cell | 0.3μm | Avoid WSA interference |
| **NLDC-ION**  | NMOS Cell LDD implantation | Cell | Shallow N⁻ for memory cell | 5e13/cm² @ 30 keV (As⁺) | Low current control |
| **PLD-PH**    | PMOS LDD lithography | Peripheral | Define LDD region for PMOS | 0.35μm | — |
| **PLD-ION**   | PMOS LDD implantation | Peripheral | Form shallow P⁻ diffusion | 3e13/cm² @ 30 keV (BF₂⁺) | — |
| **SW-DP**     | Spacer deposition (oxide/nitride) | Global | Spacer stack for S/D mask | SiO₂: 600Å, SiN: 400Å | CVD process |
| **SW-ET**     | Spacer etching | Global | Form oxide/nitride spacers | Dry etch @ RT | Material-selective etching |
| **NLD2-PH**   | NMOS deep S/D lithography | Peripheral | Define N⁺ S/D | 0.35μm | — |
| **NLD2-ION**  | NMOS deep S/D implantation | Peripheral | Form deep N⁺ S/D | 5e15/cm² @ 60 keV (As⁺) | Activated by anneal |
| **NLDC2-PH**  | NMOS Cell deep S/D lithography | Cell | Define N⁺ S/D for cell | 0.3μm | — |
| **NLDC2-ION** | NMOS Cell deep S/D implantation | Cell | Form deep N⁺ in memory cell | 5e15/cm² @ 50 keV (As⁺) | — |
| **PLD2-PH**   | PMOS deep S/D lithography | Peripheral | Define P⁺ S/D | 0.35μm | — |
| **PLD2-ION**  | PMOS deep S/D implantation | Peripheral | Form deep P⁺ S/D | 3e15/cm² @ 50 keV (BF₂⁺) | — |

---

## 🟩 Bit Line Formation (THA to WSB)

| Step | Process Description | Notes |
|------|----------------------|-------|
| **THA-DP**  | TEOS deposition (THA base layer) | 4000Å @ 650℃ |
| **THA-PH**  | Through-hole lithography (KrF) | AR=2, layout avoids WSA interference |
| **THA-ET**  | THA contact hole etching | Contact hole for bit line |
| **PLYB-DP** | Doped poly-Si deposition (BL base) | 2500Å @ 620℃ |
| **WSB-DP**  | WSi deposition (CVD) | 1800Å @ 450℃ |
| **WSB-PH**  | Bit line lithography (KrF) | 0.25μm L/S for high-density interconnect |
| **WSB-ET**  | Bit line etching | BRAC cap maintains bottom insulation |


---




