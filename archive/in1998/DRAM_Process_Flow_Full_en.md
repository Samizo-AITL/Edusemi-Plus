## 📘 64M DRAM (0.25μm Node) Full Process Flow List

> This document reconstructs the process structure of 64M DRAM (3rd Generation, 0.25μm technology) as of 1998, for educational purposes.  
> Film thickness, critical dimensions, temperature, and implantation conditions are listed as estimated representative values.  
> It is designed to help understand mask layout, KrF lithography adaptation, implant profiles, and connection structures.  
> The flow is **reconstructed from the memory of Shinichi Samizo** and intended for use in training and learning materials.

| Step Name | Process Description | Thickness | CD | Temp | Notes | Mask |
|-----------|----------------------|-----------|-----|------|-------|------|
| FS-DP | SiON Deposition | 200Å | - | 700℃ | Interface protection | - |
| FSN-DP | LOCOS Nitride Mask | 1500Å | - | 750℃ | Field mask usage | - |
| F-PH | Field Lithography (KrF) | - | 0.35μm | - | Semi-recess pattern | F |
| F-ET | Open SIN + SION | - | - | - | Field Isolation formation | - |
| F-OX | LOCOS Field Oxidation | 4500Å | - | 1000℃ | Bird's beak suppression | - |
| PRE-OX | Sacrificial Oxide | 200Å | - | 900℃ | Channel protection | - |
| NWLA-PH | Deep N-Well Litho | - | 1.5μm | - | Cell/MV Area | NWLA |
| NWLA-ION | Deep N-Well Implant | - | - | RT | 1) Deep N-Well for Cell (MV)<br>2) Alpha-particle resistance<br>3) Est. Dose: 1e13 /cm² @ 1.2 MeV (P) | - |
| NWLB-PH | N-Well Litho | - | 1.2μm | - | Peripheral PMOS Area | NWLB |
| NWLB-ION | N-Well Implant | - | - | RT | 1) N-Well for peripheral PMOS<br>2) PMOS channel doping<br>3) Est. Dose: 1e13 /cm² @ 300 keV (P) | - |
| PWL-PH | P-Well Litho | - | 1.0μm | - | NMOS / Stopper Area | PWL |
| PWL-ION | P-Well Implant | - | - | RT | 1) P-Well for Cell & Peripheral NMOS<br>2) Stopper under LOCOS<br>3) Channel doping<br>4) Est. Dose: 1e13 /cm² @ 150 keV (B) | - |
| G-OX | Gate Oxide Growth | 80Å | - | 800℃ | High-quality oxidation | - |
| PLYA-DP | Doped Poly Deposition | 2000Å | - | 620℃ | Gate Poly (LPCVD) | - |
| WSA-DP | WSi CVD Deposition | 1500Å | - | 450℃ | Gate Electrode Formation | - |
| BRAC-DP | Barrier Cap Deposition | 800Å | - | 400℃ | SiO₂ Cap Layer | - |
| WSA-PH | Gate Litho (KrF) | - | 0.25μm | - | High-resolution pattern | WSA |
| WSA-ET | Gate Etch | - | - | RT | Maintain BRAC insulation | - |
| THA-DP | TEOS Deposition | 4000Å | - | 650℃ | V1 interlayer | - |
| THA-PH | V1 Contact Litho (KrF) | - | AR=2 | - | Avoid WSA overlap | THA |
| THA-ET | V1 Contact Etch | - | - | RT | Contact Hole Open | - |
| PLYB-DP | Doped Poly Deposition | 2500Å | - | 620℃ | Bit Line Base | - |
| WSB-DP | WSi Deposition (CVD) | 1800Å | - | 450℃ | WSi-CVD from 0.25μm node | - |
| WSB-PH | Bit Line Litho (KrF) | - | 0.25μm L/S | - | High-density wiring | WSB |
| WSB-ET | Bit Line Etch | - | - | RT | Maintain insulation via BRAC | - |
| THB-DP | TEOS Deposition | 6000Å | - | 650℃ | Storage Node Insulation | - |
| THB-PH | V2 Litho (KrF) | - | AR=8 | - | High AR Contact | THB |
| THB-ET | V2 Contact Etch | - | - | RT | Deep contact formation | - |
| PLYC-DP | Thick Poly Deposition | 8000Å | - | 620℃ | Bottom Electrode | - |
| PLYC-PH | Bottom Electrode Litho | - | 0.25μm | - | Patterning | PLYC |
| PLYC-ET | Bottom Electrode Etch | - | - | RT | Residue → Short risk | - |
| PLYC2-DP | Roughening | - | - | 700℃ | Capacitance +1.5~1.8x | - |
| SIN-DP | SiN Dielectric Deposition | 150Å | - | 750℃ | ONO Dielectric Prep | - |
| SIN-OX | SiN Oxidation | - | - | 800℃ | Form ONO Stack | - |
| PLYD-DP | Top Electrode Deposition | 2000Å | - | 620℃ | Poly or TiN | - |
| PLYD-PH | Top Electrode Litho | - | 0.3μm | - | Maintain isolation | PLYD |
| PLYD-ET | Top Electrode Etch | - | - | RT | Cell Plate Formation | - |
