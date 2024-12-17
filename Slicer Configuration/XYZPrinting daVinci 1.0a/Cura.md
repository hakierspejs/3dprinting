# Cura configuration
Printer settings:
- X (Width): 200.0 [mm]
- Y (Depth): 200.0 [mm]
- Z (Height): 200.0 [mm]
- Build plate shape: Rectangular
- Heated bed
- G-code flavor: Repetier

Printhead settings:
- X min: -20 [mm]
- Y min: -10 [mm]
- X max: 10 [mm]
- Y max: 10 [mm]
- Gantry Height: 200.0 [mm]
- One Extruder
- Apply Extruder offsets to Gcode

Start G-code:
```
G21
G28 ;Home
G92 E0
M82
G92 Z0
G1 Z15.0 F6000 ;Move the platform down 15mm
;Prime the extruder
G1 F200 E3
G92 E0
```

End G-code:
```
M104 S0
M140 S0
;Retract the filament
;G92 E1
G1 Z185
;G1 E-1 F300
;G28 X0 Y0
G92 E0		;reset extruder count
M107		;fan off
M84
```

Nozzle Settings:
- Nozzle size: 0.4 [mm]
- Compatible material diameter: 1.75 [mm]
- Nozzle offset X: 0.0 [mm]
- Nozzle offset Y: 0.0 [mm]
- Cooling Fan number: 1

