## Layout

```
bento-board/
├── kicad/              KiCad source projects (open the .kicad_pro)
│   ├── library/        Shared symbol + footprint library
│   ├── rev0/           SUB-00156 REV00
│   └── rev1/           SUB-00156 REV01
├── schematic/          Schematic exports (PDF, SVG), per revision
│   ├── rev0/
│   └── rev1/
├── layout/             Board renders and fabrication outputs, per revision
│   ├── rev0/
│   └── rev1/
├── firmware/           Prebuilt firmware images
│   └── blinky/
└── test/               PLT test plans
    └── flash-blinky/
```

Each `kicad/revN/` directory is a complete KiCad project; the schematic and
PCB must stay together for KiCad's project linking to work. `schematic/` and
`layout/` hold generated outputs only.

## Revisions

| Rev | Changes |
|---|---|
| REV00 | Initial release |
| REV01 | Tag-Connect footprint moved away from relay; added 4.7 µF capacitor |

## License

![Open Source Licenses](oshw-licenses.svg)

| Component | License |
|---|---|
| Hardware design files (KiCad) | [CERN-OHL-P-2.0](LICENSE-HARDWARE) |
| Firmware | Apache-2.0 ([firmware repo](https://github.com/bcdevices/example-projects/tree/main/bento-board/firmware/blinky)) |
| Documentation | [CC-BY-4.0](LICENSE-DOCS) |

## Credits

Derived from the Golioth Aludel Elixir (CERN-OHL-P-2.0), designed by
Chris Gammell, which itself descends from Jared Wolff's nRF9160 Feather.
Changes: RP2350B + ESP32-C3 architecture, OKW IN-BOX form factor,
sensor/relay/buzzer sections, and DFT test features.
