# DRAM to VSRAM Case Study (Historical Yield Ramp-up)

## Part I (1998): 0.25µm 64M DRAM Ramp-up
- 3rd generation, from scratch (floppiesから立ち上げ)  
- Initial yield ~65%, pause-refresh failures dominant  
- Plasma damage root cause → countermeasures:  
  - Wet resist strip  
  - Body back-bias -1V → -3V  
- Yield improved to ~80%, passed long-term reliability  

## Part II (2001): 0.25µm VSRAM
- Same stack capacitor, but added self-refresh & 90℃ margin  
- Problems:  
  - Pause-refresh → mitigated (gate residue, back-bias)  
  - Disturb-refresh → gate dimension control required  
- Margin much tighter than DRAM  

## Part III (0.18µm): Trench Capacitor VSRAM
- Spec same as 0.25µm  
- Larger junction area → leakage current↑  
- Self-refresh + high-T margin → yield collapse → project abandoned  

## Discussion
- DRAM → pause-refresh critical, disturb-refresh not dominant  
- VSRAM → new challenges (self-refresh, high-T) expose hidden failure modes  
- Trench → leakage made continuation impossible  
- Lessons: process vs device vs architecture interplay  

## Conclusion
- Ramp-up frameworks remain valuable today  
- Failure mechanisms (pause, disturb) echo modern retention & rowhammer  
- Educational value in showing limits of 1T–1C memories
