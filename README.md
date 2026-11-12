# Heart and brain: analysing EEG and ECG together with BrainAccess
 
Your heartbeat leaves a mark on your EEG. This short tutorial shows how to analyse synchronized EEG and ECG recorded with BrainAccess devices: you compute heart rate and heart-rate variability (HRV), then look at EEG activity locked to each heartbeat.
 
📖 Read the full blog post [here](https://www.brainaccess.ai/heart-and-brain-together-analysing-eeg-and-ecg-with-brainaccess/). 
 
## What you will learn
 
- Load an EEG recording with heartbeat annotations in [MNE-Python](https://mne.tools)
- Compute heart rate and two standard HRV measures (SDNN and RMSSD) from the heartbeat times
- Average the EEG around every heartbeat to reveal the cardiac field artefact and the window where heartbeat-evoked potentials are studied
- Visualize every heartbeat at once to see why averaging matters
## Repository contents
 
```
├── heart_and_brain.ipynb   # the tutorial notebook
└── data/
    └── mini_heartbeat_raw.fif # example recording used in the notebook
```
 
## The data
 
About 6 minutes of EEG recorded with a **BrainAccess MINI** (Fp1, Fp2, O1, O2, sampled at 250 Hz). An ECG was recorded at the same time with a **BrainAccess ExG** device, and each heartbeat (R-peak) was added to the EEG file as an `R_peak` annotation, so both signals share one timeline. The EEG is already band-pass filtered at 1–40 Hz.
 
## Getting started

You need Python 3.10 or newer. With pip in your own Python 3.10+ environment:
 
```bash
git clone https://github.com/martinaberto/heart-and-brain-tutorial.git
cd heart-and-brain-tutorial
pip install -r requirements.txt
jupyter lab
 ```

Open `heart_and_brain.ipynb`
 
Run the cells from top to bottom. The notebook reads the recording from `data/`, so start Jupyter from the repository folder.
 
## Going further: live data
 
The notebook works on a saved recording. To stream data live from BrainAccess devices, install the [BrainAccess SDK](https://www.brainaccess.ai) or use BrainAccess Board; the last section of the notebook shows how. The SDK and Board are separate products with their own licences and are not needed to run the tutorial.
 
## Learn more
 
- Park, H.-D., & Blanke, O. (2019). Heartbeat-evoked cortical responses: Underlying mechanisms, functional roles, and methodological considerations. *NeuroImage, 197*, 502–511.
- Task Force of the European Society of Cardiology and the North American Society of Pacing and Electrophysiology (1996). Heart rate variability: Standards of measurement, physiological interpretation, and clinical use. *Circulation, 93*(5), 1043–1065.

## Licence
 
- **Code** in this repository is licensed under the [MIT License](LICENSE).
- **Text, figures and the example data** in `data/` are licensed under [Creative Commons Attribution 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You are free to share and adapt them, as long as you credit BrainAccess.

## Contact
 
Questions or feedback? Open an issue or contact us at brainaccess@neurotechnology.com.
 
BrainAccess is developed by [Neurotechnology](https://www.neurotechnology.com).
 
