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

