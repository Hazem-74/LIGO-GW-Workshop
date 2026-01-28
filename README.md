# LIGO Gravitational Wave Analysis Project

## Project Overview
This project provides a comprehensive analysis of gravitational wave data from the LIGO (Laser Interferometer Gravitational-Wave Observatory) collaboration. The code includes detailed analysis of the historic GW150914 event - the first direct detection of gravitational waves - along with three challenge datasets for educational purposes.

## Project Structure
The project consists of four main components:

1. **GW150914 Comprehensive Analysis**: A complete analysis of the first detected gravitational wave event
2. **Challenge #1**: Basic gravitational wave signal identification
3. **Challenge #2 (Rookie)**: Intermediate analysis with known signal parameters
4. **Challenge #3 (Intermediate)**: Advanced analysis using real LIGO data with simulated signals

## Prerequisites and Dependencies

### Required Python Packages
- NumPy (>=1.19.0)
- SciPy (>=1.5.0)
- Matplotlib (>=3.3.0)
- GWpy (>=2.0.0)
- PyCBC (>=1.18.0)

### Installation
```bash
# Create and activate a virtual environment
python -m venv ligo-env
source ligo-env/bin/activate  # On Windows: ligo-env\Scripts\activate

# Install required packages
pip install numpy scipy matplotlib
pip install gwpy pycbc
```

## Key Features

### GW150914 Analysis
- Multi-detector analysis using H1 (Hanford) and L1 (Livingston) data
- Comprehensive signal processing including band-pass filtering (30-300 Hz)
- Q-transform time-frequency analysis
- Matched filtering with template waveforms
- Signal consistency tests (chi-squared)
- Publication-quality visualizations
- Automated directory structure for organized outputs

### Challenge Analyses
1. **Challenge #1**: Basic signal identification and merger time estimation
2. **Challenge #2**: Template waveform generation and matched filtering for known parameters
3. **Challenge #3**: Real LIGO data analysis with advanced filtering techniques

## Usage Instructions

### Running the GW150914 Analysis
```bash
# Run the main GW150914 analysis
python -c "exec(open('path_to_gw150914_analysis.py').read())"
```

### Running Challenge Analyses
Each challenge can be run independently by executing the corresponding code section in the provided files.


## Technical Details

### Data Processing Pipeline
1. **Data Acquisition**: Download strain data from LIGO open data servers
2. **Preprocessing**: High-pass filtering and resampling to 2048 Hz
3. **Noise Characterization**: Power Spectral Density (PSD) calculation
4. **Signal Enhancement**: Band-pass filtering (30-300 Hz for GW150914)
5. **Time-Frequency Analysis**: Q-transforms for signal visualization
6. **Matched Filtering**: Cross-correlation with template waveforms
7. **Statistical Validation**: Signal-to-noise ratio (SNR) and chi-squared tests

### Signal Parameters for GW150914
- Primary black hole mass: 36.2 solar masses
- Secondary black hole mass: 29.1 solar masses
- Final black hole mass: 62.3 solar masses
- Radiated energy: 3.0 solar masses (5.3e47 Joules)
- Distance: 410 Mpc
- Peak strain: approximately 1e-21

## Educational Value
This code serves as an educational resource for:
- Understanding gravitational wave data analysis techniques
- Learning signal processing methods for noisy astrophysical data
- Practicing matched filtering and statistical detection methods
- Visualizing time-frequency representations of transient signals
- Working with real scientific data from LIGO observations

## Important Notes
1. The code requires internet access to download LIGO data (for GW150914 analysis)
2. Some challenge datasets are included locally
3. The GW150914 analysis may take several minutes to complete due to data download and processing
4. All generated plots are saved automatically in the organized directory structure
5. The code includes comprehensive error handling and debugging information

## References
1. Abbott et al. (2016) - Observation of Gravitational Waves from a Binary Black Hole Merger (GW150914)
2. LIGO Scientific Collaboration - Open data and software resources
3. PyCBC and GWpy documentation for gravitational wave data analysis

## Disclaimer
This code is provided for educational and research purposes. While it implements analysis techniques used by the LIGO collaboration, it represents a simplified educational version. For production-level gravitational wave analysis, refer to the official LIGO algorithms and software libraries.

## License
This educational code is provided under the MIT License for academic and research use.
