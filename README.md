# HRFEST 2026 – Submission 96

## Design and Experimental Evaluation of a Dual-Microcontroller IoT System for Plasma Freezer Monitoring in Healthcare Facilities

This repository contains the experimental dataset, data-processing notebook, and generated results associated with the HRFEST 2026 paper:

**“Design and Experimental Evaluation of a Dual-Microcontroller IoT System for Plasma Freezer Monitoring in Healthcare Facilities.”**

The study presents and experimentally evaluates **MHUTEMP-ULT**, an IoT monitoring system developed for plasma-freezer temperature monitoring in a healthcare facility.

The prototype uses a three-wire PT100 resistance temperature detector interfaced through a MAX31865 RTD-to-digital converter. A dual-ESP32 architecture functionally separates sensing and local processing from Wi-Fi and WebSocket communication.

---

## Repository Structure

```text
hrfest2026-96/
│
├── Raw-Data/
│   └── bio_data_10mindata_ult26_250926.csv
│
├── Analysis/
│   └── hrfest_96.ipynb
│
├── Results/
│   ├── ULT26_001_Group1_clean.csv
│   └── Fig5_ULT26_001_Group1_18days_600dpi.png
│
├── README.md
└── ...
```

### Raw-Data

The `Raw-Data/` directory contains the original CSV file exported from the MHUTEMP-ULT database before the preprocessing and selection procedures used for the paper.

**File:**

`bio_data_10mindata_ult26_250926.csv`

This file is preserved as the original data source used to obtain the experimental subset analyzed in the study.

### Analysis

The `Analysis/` directory contains the Jupyter notebook used for data preprocessing and analysis.

**File:**

`hrfest_96.ipynb`

The notebook can be opened using Jupyter Notebook or Google Colab.

### Results

The `Results/` directory contains the processed dataset and the temperature-profile figure generated from the experimental data.

**Files:**

`ULT26_001_Group1_clean.csv`

Clean dataset corresponding to the field-monitoring period analyzed in the paper.

`Fig5_ULT26_001_Group1_18days_600dpi.png`

Temperature profile generated from the experimental dataset and used as Fig. 5 in the paper.

<img width="4229" height="1980" alt="Fig6_ULT26_001_Group1_18days_600dpi" src="https://github.com/user-attachments/assets/f09a26a2-25df-4dd0-9450-3ab2b10ad49c" />

---

## Experimental Dataset

The experimental data correspond to the **ULT26-001** MHUTEMP-ULT monitoring node installed on an operational plasma freezer in a healthcare facility.

The field-monitoring period analyzed in the paper extends from **August 21 to September 8, 2026**, corresponding to approximately **18.1 days** of monitoring.

Database records were generated at approximately one-minute intervals.

The analyzed dataset contains:

| Parameter | Result |
|---|---:|
| Monitoring duration | 18.1 days |
| Database records | 26,073 |
| Valid temperature records | 26,071 |
| Temperature range | −32.1 to −28.2 °C |
| Mean temperature | −30.58 °C |
| Standard deviation | 0.68 °C |
| Median inter-record interval | 60.0 s |
| Inter-record intervals ≤ 90 s | 99.98% |
| Inter-record intervals > 90 s | 6 |
| Maximum inter-record gap | 136 s |

The repository provides both the original database export and the processed dataset used for the analysis to support reproducibility of the reported results.

---

## Data Processing

The `hrfest_96.ipynb` notebook contains the data-processing workflow used to obtain the experimental results reported in the paper.

The main processing steps include:

1. Loading the original CSV database export.
2. Identification of records corresponding to monitoring node `ULT26-001`.
3. Selection of the field-monitoring period used in the study.
4. Validation and cleaning of temperature records.
5. Evaluation of time differences between consecutive database records.
6. Calculation of descriptive temperature statistics.
7. Generation of the plasma-freezer temperature profile.

Preliminary commissioning records with irregular acquisition intervals were excluded from the field-monitoring period analyzed in the paper.

---

## Temperature Profile

The figure generated from the processed dataset shows the plasma-freezer temperature profile during the approximately 18.1-day field-monitoring period.

**File:**

`Results/Fig5_ULT26_001_Group1_18days_600dpi.png`

The temperature measurements are displayed according to their original database timestamps.

No moving-average smoothing or temporal interpolation was applied to the temperature profile.

The recorded temperature ranged from **−32.1 °C to −28.2 °C**, with a mean temperature of **−30.58 °C** and a standard deviation of **0.68 °C**.

Recurring temperature variations can be observed throughout the monitoring period. Detailed characterization of their periodic behavior is outside the scope of the associated HRFEST 2026 paper.

---

## Reproducibility

This repository provides the materials required to inspect and reproduce the data-processing workflow associated with the experimental evaluation.

The following resources are included:

- Original database export.
- Processed experimental dataset.
- Jupyter/Google Colab analysis notebook.
- Generated temperature-profile figure.

The notebook can be used to inspect the preprocessing procedure and reproduce the descriptive statistics and temperature profile reported in the paper.

---

## Scope of the Dataset

The data were collected during the experimental evaluation of the MHUTEMP-ULT monitoring prototype on a plasma freezer.

The dataset is provided to support the reproducibility and verification of the monitoring-system evaluation.

The data and results should not be interpreted as validation of plasma-storage safety, plasma quality, or clinical compliance of the monitored freezer.

---

## Associated Paper

This repository accompanies the following HRFEST 2026 submission:

**Submission 96**

**Title:**  
*Design and Experimental Evaluation of a Dual-Microcontroller IoT System for Plasma Freezer Monitoring in Healthcare Facilities*

The complete bibliographic information will be added after publication of the conference proceedings.

---

## Citation

If you use the dataset, analysis workflow, or other materials contained in this repository, please cite the associated HRFEST 2026 paper after its publication.

Temporary citation:

```text
I. Lon-kan et al., “Design and Experimental Evaluation of a
Dual-Microcontroller IoT System for Plasma Freezer Monitoring
in Healthcare Facilities,” HRFEST 2026, 2026.
```

Repository:

https://github.com/storres20/hrfest2026-96

---

## Authors

**Italo Lon-kan**  
Faculty of Engineering and Architecture  
Universidad Autónoma del Perú  
Lima, Peru

This repository contains research materials associated with collaborative work reported in the corresponding HRFEST 2026 paper.

---

## Contact

For questions regarding the dataset, analysis, or associated research:

**Italo Lon-kan**  
Universidad Autónoma del Perú  
Lima, Peru

Email: ilonkanp@autonoma.edu.pe

---

## License

The licensing terms applicable to the dataset, analysis notebook, and other materials in this repository should be reviewed before reuse or redistribution.

Unless a specific license file is provided, the availability of the repository should not be interpreted as granting unrestricted permission for reuse or redistribution.
