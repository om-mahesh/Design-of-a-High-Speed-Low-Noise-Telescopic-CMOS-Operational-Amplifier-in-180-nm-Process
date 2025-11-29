# Design of a High-Speed, Low-Noise Telescopic CMOS Operational Amplifier in 180 nm Process

A comprehensive design and analysis of a telescopic operational amplifier implemented in 180nm CMOS technology, optimized for high-speed applications with low noise characteristics.

## 📋 Table of Contents
- [Overview](#overview)
- [Specifications](#specifications)
- [Design Architecture](#design-architecture)
- [Simulation Results](#simulation-results)
- [Repository Structure](#repository-structure)
- [Tools Used](#tools-used)
- [How to Use](#how-to-use)
- [Author](#author)

## 🔍 Overview

This project presents the design and implementation of a telescopic operational amplifier using 180nm CMOS technology. The design focuses on achieving:
- High-speed operation
- Low noise performance
- Optimal power efficiency
- High gain and bandwidth

The telescopic architecture is chosen for its excellent high-frequency performance and lower power consumption compared to conventional two-stage amplifiers.

## ⚡ Specifications

| Parameter | Value |
|-----------|-------|
| **Technology** | 180 nm CMOS |
| **Supply Voltage (VDD)** | 1.8V |
| **Gain** | 40 dB |
| **Bandwidth** | 1 GHz |
| **Phase Margin** | 85° |
| **Slew Rate** | 3.12 V/ns |
| **Power Consumption** | 5.12 mW |
| **Input-Referred Noise** | 100 uV/√Hz |
| **CMRR** | 37 dB |
## 🏗️ Design Architecture

### Circuit Topology

The telescopic amplifier consists of:
1. **Input Differential Pair** - NMOS/PMOS input stage for differential signal processing
2. **Cascode Load** - PMOS cascode configuration for high output impedance
3. **Current Source** - Tail current source for biasing
4. **Bias Network** - Precision biasing for optimal operating point

### Key Features

- **Single-stage architecture** for minimal power consumption
- **Cascode configuration** for enhanced gain
- **Optimized transistor sizing** for noise and speed trade-offs
- **Robust biasing network** for process variation tolerance

## 📊 Simulation Results

### Gain and Phase Response
- DC Gain: 41 dB
- Unity Gain Bandwidth: 1.01 GHz
- Phase Margin: 85°

![Gain-Phase Plot](simulation_results/gain_phase_plot.png)


![Slew Rate](slew_rate_plot.png)

### Noise Analysis
- Input-referred noise at 1kHz: 100 uV/√Hz
![Error/Noise Plot](error_plot.png)

### Layout
The complete layout includes:
- Optimized transistor placement
- Matched differential pairs
- Guard rings for isolation
- Metal routing with minimal parasitic

![Layout](layout.png)
![Layout (BW)](layout_bw.png)

## 📁 Repository Structure

```
.
├── README.md                   # Project documentation
├── opamp_report.pdf           # Detailed design report
├── opamp_report.tex           # LaTeX source for report
│
├── circuits/
│   ├── 1.png                  # Schematic diagram 1
│   ├── 2.png                  # Schematic diagram 2
│   ├── circuit.png            # Main circuit schematic
│   ├── telescopic.png         # Telescopic amplifier topology
│   └── telescopic_bw.png      # Telescopic amplifier (B&W)
│
├── symbols/
│   ├── symbol.png             # Circuit symbol
│   └── symbol_bw.png          # Circuit symbol (B&W)
│
├── layout/
│   ├── layout.png             # Complete layout design
│   └── layout_bw.png          # Layout (B&W)
│
├── simulation_results/
│   ├── gain_phase_plot.png    # Frequency response
│   ├── gain_phase.csv         # Frequency response data
│   ├── slew_rate_plot.png     # Slew rate analysis
│   ├── slew_rate.csv          # Slew rate data
│   ├── error_plot.png         # Error/noise analysis
│   └── ERROR.csv              # Error data
│
└── docs/
    └── opamp_report.pdf       # Complete project report
```

## 🛠️ Tools Used

- **Circuit Design & Simulation**: Cadence Virtuoso / LTspice / [Your tool]
- **Layout Design**: Cadence Virtuoso Layout Editor
- **Verification**: DRC, LVS, PEX
- **Documentation**: LaTeX, Python (for plotting)
- **Technology**: TSMC 180nm CMOS Process

## 💻 How to Use

### Prerequisites
- Cadence IC Suite (Virtuoso)
- 180nm PDK (Process Design Kit)
- Basic knowledge of analog circuit design

### Steps
1. Clone this repository
   ```bash
   git clone https://github.com/om-mahesh/Design-of-a-High-Speed-Low-Noise-Telescopic-CMOS-Operational-Amplifier-in-180-nm-Process.git
   cd Design-of-a-High-Speed-Low-Noise-Telescopic-CMOS-Operational-Amplifier-in-180-nm-Process
   ```

2. Open the schematic files in Cadence Virtuoso

3. Run simulations:
   - DC Operating Point
   - AC Analysis (Gain, Phase)
   - Transient Analysis
   - Noise Analysis

4. Review the layout and verify with DRC/LVS

5. Check the detailed report: `opamp_report.pdf`

## 📖 Documentation

For detailed design methodology, calculations, and analysis, please refer to the complete project report: [`opamp_report.pdf`](opamp_report.pdf)

## 🎯 Future Work

- [ ] Post-layout simulation with parasitic extraction
- [ ] Monte Carlo analysis for process variations
- [ ] Corner analysis (SS, FF, SF, FS)
- [ ] Temperature variation analysis
- [ ] Comparison with other topologies

## 📝 License

This project is available for educational and research purposes.

## 👤 Author

**Om Mahesh**

- GitHub: [@om-mahesh](https://github.com/om-mahesh)
- Project: [Design of High-Speed Low-Noise Telescopic CMOS Op-Amp](https://github.com/om-mahesh/Design-of-a-High-Speed-Low-Noise-Telescopic-CMOS-Operational-Amplifier-in-180-nm-Process)

## 🙏 Acknowledgments

- TSMC for the 180nm process technology
- [Your Institution/University]
- [Advisor/Professor name if applicable]

---

⭐ If you find this project useful, please consider giving it a star!

*Last Updated: November 2025*

