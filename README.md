###**README.md**

```markdown
# Gravitational Wave Analysis: GW150914

<p align="right">
  <img src="Zewail-City.png" width="200">
</p>

This repository contains a complete Jupyter notebook-based analysis of the historic gravitational wave event **GW150914**, the first direct detection of gravitational waves by the LIGO collaboration on September 14, 2015.

---

## Overview

This project replicates and extends standard LIGO analysis techniques to:
- Download and preprocess strain data from both LIGO detectors (H1 and L1)
- Visualize the time-domain and time-frequency characteristics of the signal
- Generate a theoretical waveform template for a binary black hole merger
- Perform matched filtering to compute signal-to-noise ratio (SNR)
- Validate signal consistency using chi-squared tests
- Combine information across detectors for robust detection

The analysis demonstrates the characteristic "chirp" signal of a binary black hole inspiral, merger, and ringdown — confirming Einstein's general relativity prediction a century after its proposal.

---


## Requirements

Install the required Python packages:

```bash
pip install numpy matplotlib scipy gwpy pycbc
```

> **Note**: `PyCBC` may require additional system dependencies (e.g., FFTW, GSL). Please refer to the [PyCBC installation guide](https://pycbc.org/pycbc/latest/html/install.html).

All code is compatible with **Python 3.8+**.

---

## Usage

1. Clone or download this repository.
2. Ensure all dependencies are installed.
3. Open `GW150914_Analysis.ipynb` in Jupyter Lab or Jupyter Notebook.
4. Run all cells sequentially.

> **Internet Access Required**: Data is fetched in real-time from the [Gravitational Wave Open Science Center (GWOSC)](https://www.gw-openscience.org).

The notebook will:
- Automatically create the `plots/` directory
- Download 32 seconds of strain data around GW150914
- Generate 10+ high-quality diagnostic plots
- Save a comprehensive text summary

**Total runtime**: ~3–10 minutes (depending on internet speed and hardware).

---

## Key Results

| Parameter               | Value                     |
|------------------------|---------------------------|
| Primary BH Mass        | ~36 M☉                    |
| Secondary BH Mass      | ~29 M☉                    |
| Final BH Mass          | ~62 M☉                    |
| Radiated Energy        | ~3 M☉ c² (~5 × 10⁴⁷ J)    |
| Distance               | ~410 Mpc                  |
| Redshift               | ~0.09                     |
| H1 Peak SNR            | >24                       |
| L1 Peak SNR            | >20                       |
| Network SNR            | >32                       |
| H1–L1 Time Delay       | ~7 ms                     |
| Frequency Band         | 35 Hz → 250 Hz            |
| Signal Duration        | ~0.2 seconds              |

The analysis confirms:
- A clear "chirp" in both detectors
- Excellent match to numerical relativity templates
- Reduced chi-squared ≈ 1 (validating signal consistency)
- Arrival time difference consistent with sky localization

---

## Example Outputs

- **Q-transforms** showing time-frequency evolution  
- **Matched filter SNR** time series with peak detection  
- **Whitened strain data** overlaid with theoretical template  
- **Publication-quality figure** combining all diagnostics  
- **SNR vs χ² scatter plots** for glitch rejection  

All figures are saved in `plots/` with **300 DPI resolution**.

---

## References

1. Abbott et al. (2016). *Observation of Gravitational Waves from a Binary Black Hole Merger*. [Phys. Rev. Lett. 116, 061102](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.116.061102).  
2. LIGO Open Science Center (GWOSC): https://www.gw-openscience.org  
3. PyCBC Documentation: https://pycbc.org  
4. GWpy Documentation: https://gwpy.github.io  

---

## License

This educational code is released under the **MIT License**.  
Gravitational wave data is publicly available via the GWOSC under open-access terms.

---
