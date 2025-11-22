# 6-Stand Electrical Steel Cold Rolling Mill Simulator

[![Live Demo](https://img.shields.io/badge/demo-live-success)](https://pjkang2023-hub/cold-rolling-mill-simulator/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## 🎯 Overview

Advanced web-based simulation of a 6-stand cold rolling mill for electrical steel production. This interactive tool provides real-time physics-based calculations for temperature evolution, tension control, mass flow balance, and stand-by-stand performance analysis.

**🚀 [Launch Simulator →](https://pjkang2023-hub.github.io/cold-rolling-mill-simulator/)**


## ✨ Key Features

### 🏭 **Complete Mill Configuration**
- 6-stand tandem cold rolling mill
- 6-high roll configuration (backup, intermediate, work rolls)
- Realistic mill schematic with continuous strip visualization
- Individual stand control and monitoring

### 🌡️ **Thermal Modeling**
- Real-time temperature evolution for each stand
- Heat generation from deformation and friction
- Inter-stand cooling system simulation
- Roll temperature monitoring
- Radiation, convection, and conduction heat losses

### ⚡ **Advanced Tension Control**
- Inter-stand tension management (5 zones)
- Automatic tension control with PI loops
- Adaptive gain adjustment
- Real-time tension stress analysis
- Zone-by-zone tension error tracking

### 📊 **Process Control Systems**
- **AGC (Automatic Gauge Control)**: Thickness regulation
- **APC (Automatic Position Control)**: Roll gap positioning
- **Speed Control**: Master speed and speed ratio management
- **Threading Simulation**: Strip entry sequence through stands

### 🔬 **Physics-Based Calculations**
- Roll bite mechanics with forward slip
- Mass flow conservation (volume continuity)
- Deformation power and rolling force
- Enhanced roll bite model with neutral point
- Temperature-dependent material properties

### 📈 **Real-Time Visualization**
- Interactive charts for all process variables
- Stand-by-stand performance cards
- System diagnostics and monitoring
- Process equation reference guide

---

## 🎮 Quick Start

### Access Online
Simply visit the live demo - no installation required:
**(https://pjkang2023-hub.github.io/cold-rolling-mill-simulator/)**

### Run Locally
1. Download `index.html`
2. Open in any modern web browser
3. No server or dependencies needed - everything runs client-side

---

## 📖 Usage Guide

### Basic Operation

1. **Initialize System**
   - Set entry thickness (2.0-4.0 mm)
   - Set exit thickness target (0.18-0.35 mm)
   - Configure master speed (300-1200 m/min)
   - Select steel grade (M470-50A, M800-50A, etc.)

2. **Threading Process**
   - Click "Start Threading" to simulate strip entry
   - Watch as strip threads through each stand sequentially
   - Monitor thread status indicators

3. **Running Operation**
   - Observe real-time charts updating
   - Monitor stand-by-stand performance
   - Check tension control effectiveness
   - Track temperature evolution

4. **Advanced Features**
   - Enable enhanced roll bite physics
   - Activate roll temperature modeling
   - Enable radiation heat loss calculations
   - Adjust cooling system flow rates

### Control Panels

#### **Process Setup**
- Entry/exit thickness targets
- Master speed control
- Steel grade selection
- Strip width configuration

#### **Threading Control**
- Start/stop threading
- Thread speed adjustment
- Stand-by-stand engagement

#### **Speed Control**
- Speed ratio adjustments (Stands 2-6)
- Master speed presets (slow/medium/fast)

#### **Tension Control**
- Inter-stand tension targets (Zones 1-5)
- Entry/exit tension settings

#### **Cooling System**
- Individual zone flow rates (0-100 L/min)
- Coolant temperature

#### **Advanced Options**
- Enhanced roll bite model toggle
- Roll temperature simulation
- Radiation modeling
- Thermal enhancements

---

## 🔧 Technical Specifications

### Mill Configuration
| Parameter | Specification |
|-----------|--------------|
| Number of Stands | 6 |
| Roll Configuration | 6-High (Backup-Intermediate-Work) |
| Backup Roll Diameter | 1400 mm |
| Intermediate Roll Diameter | 900 mm |
| Work Roll Diameter | 600 mm |
| Strip Width Range | 800-1200 mm |
| Entry Thickness Range | 2.0-4.0 mm |
| Exit Thickness Range | 0.18-0.35 mm |
| Maximum Speed | 1200 m/min |
| Total Reduction | Up to 95% |

### Material Grades
- **M470-50A**: Premium electrical steel (470 MPa yield)
- **M800-50A**: High-strength electrical steel (800 MPa yield)
- **M600-50A**: Standard electrical steel (600 MPa yield)

### Control Systems
- **AGC Response Time**: ~100 ms
- **Tension Control**: PI with adaptive gains
- **Sampling Rate**: 50 Hz (20 ms cycle)
- **Threading Speed**: 10-30 m/min

---

## 🧮 Physics Models

### Roll Bite Mechanics
The simulator implements fundamental rolling theory:

- **Roll Pressure Distribution**: Approximated using modified von Kármán equation
- **Forward Slip**: $s_f = \frac{v_{exit} - v_{roll}}{v_{roll}} \times 100\%$
- **Rolling Force**: Based on deformation resistance and contact arc
- **Neutral Point**: Calculated from friction and reduction conditions

### Thermal Balance
Heat generation and dissipation:

$$Q_{total} = Q_{deformation} + Q_{friction} - Q_{cooling} - Q_{radiation} - Q_{convection}$$

- **Deformation Heat**: 95% of rolling power
- **Friction Heat**: 5% of rolling power
- **Cooling**: Convective heat transfer with spray cooling
- **Radiation**: Stefan-Boltzmann law (when enabled)

### Mass Flow Conservation
Volume flow continuity between stands:

$$h_i \times v_i \times w = h_{i+1} \times v_{i+1} \times w = \text{constant}$$

Where $h$ = thickness, $v$ = velocity, $w$ = width

### Tension Distribution
Tension affects roll bite mechanics:

- Back tension reduces rolling force
- Forward tension increases strip stress
- Inter-stand tension must stay below yield limit

---

## 📚 Documentation

### Tabs Overview

1. **Overview**: Main dashboard with mill schematic and key metrics
2. **Stands**: Individual stand performance and metrics
3. **Tension**: Inter-stand tension analysis and control
4. **Thermal**: Temperature evolution and cooling system
5. **Mass Flow**: Volume flow balance and speed ratios
6. **Diagnostics**: System status and equation reference
7. **Charts**: Real-time plotting of all variables

### Key Metrics Explained

- **Reduction Ratio**: $(h_{entry} - h_{exit}) / h_{entry} \times 100\%$
- **Elongation**: $h_{entry} / h_{exit}$
- **Roll Force**: Total force on work rolls (kN)
- **Motor Power**: Instantaneous power consumption (kW)
- **Strip Temperature**: Material temperature at stand exit (°C)
- **Tension Stress**: $\sigma = T / (h \times w)$ (MPa)

---

## 💻 Technology Stack

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Visualization**: [Chart.js](https://www.chartjs.org/) v3.9.1
- **Architecture**: Single-page application, no backend required
- **Physics Engine**: Custom JavaScript implementation
- **Control Systems**: Discrete-time PI controllers

---

## 🌐 Browser Compatibility

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Fully Supported |
| Edge | 90+ | ✅ Fully Supported |
| Firefox | 88+ | ✅ Fully Supported |
| Safari | 14+ | ✅ Fully Supported |
| Opera | 76+ | ✅ Supported |

**Requirements:**
- JavaScript enabled
- Modern ES6+ support
- Canvas API support (for Chart.js)

---

## 🚀 Performance

- **Load Time**: < 2 seconds on broadband
- **Memory Usage**: ~50-80 MB
- **Update Rate**: 20 Hz (50ms per cycle)
- **Responsive**: Works on desktop, tablet, and mobile devices

---

## 📁 Project Structure

```
cold-rolling-mill-simulator/
│
├── index.html              # Main simulator application
├── README.md              # This file
└── LICENSE                # MIT License
```

---

## 🎓 Educational Use

This simulator is ideal for:

- **Metallurgical Engineering Students**: Understanding cold rolling processes
- **Process Engineers**: Training on mill control systems
- **Researchers**: Testing control algorithms and optimization strategies
- **Industry Professionals**: Process visualization and troubleshooting

---

## 🤝 Contributing

Contributions are welcome! Areas for enhancement:

- Additional steel grades and material models
- More sophisticated cooling models
- Strip profile and flatness control
- Roll wear simulation
- Energy optimization algorithms
- Multi-language support

To contribute:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 [Pengju Kang]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Author

**Pengju Kang**
- Controls Engineer
- Specialization: Steel Manufacturing & Hot and Cold Rolling Mill Automation
- Expertise: Level 2 Control Systems, Physics-Informed Neural Networks

---

## 🙏 Acknowledgments

- Based on industrial cold rolling mill control systems
- Physics models derived from rolling theory literature
- Inspired by real-world electrical steel production facilities
- Built with modern web technologies for accessibility

---

## 📧 Contact & Support

- **Issues**: Use the [GitHub Issues](https://github.com/pjkang2023-hub/cold-rolling-mill-simulator/issues) page for bug reports
- **Discussions**: Use [GitHub Discussions](https://github.com/pjkang2023-hub/cold-rolling-mill-simulator/discussions) for questions
- **Email**: pjkang2023@gmail.com (optional)

---

## 🗺️ Roadmap

### Version 1.0 (Current)
- ✅ Basic 6-stand simulation
- ✅ Temperature and tension control
- ✅ Real-time visualization
- ✅ Physics-based calculations

### Version 2.0 (Planned)
- ⬜ Strip profile control (crown/flatness)
- ⬜ Work roll bending simulation
- ⬜ Advanced material models
- ⬜ Data export functionality
- ⬜ Historical data playback

### Version 3.0 (Future)
- ⬜ Machine learning-based optimization
- ⬜ Digital twin capabilities
- ⬜ Multi-user collaboration
- ⬜ API for external integration

---

## 📊 Citations

If you use this simulator in academic work, please cite:

```bibtex
@software{cold_rolling_simulator,
  author = {Pengju Kang},
  title = {6-Stand Electrical Steel Cold Rolling Mill Simulator},
  year = {2024},
  url = {https://github.com/pjkang2023-hub/cold-rolling-mill-simulator}
}
```

---

## ⭐ Star History

If you find this project useful, please consider giving it a star! ⭐

---

**Last Updated**: November 2024  
**Version**: 1.0.0  
**Status**: Active Development
