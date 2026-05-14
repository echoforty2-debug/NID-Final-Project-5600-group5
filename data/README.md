# Dataset Access Instructions

The raw CIC-IDS datasets are not included directly in this repository because the files are large external datasets. This folder explains how to access and organize the datasets used in the project.

## Datasets Used

### Primary Dataset

**CSE-CIC-IDS2018**  
Used for model training, validation, testing, calibration, threshold analysis, and same-year evaluation.

Official source:  
https://www.unb.ca/cic/datasets/ids-2018.html

### Drift Analysis Dataset

**CIC-IDS2017**  
Used to evaluate cross-dataset drift and robustness.

Official source:  
https://www.unb.ca/cic/datasets/ids-2017.html

## Expected Google Drive Folder Structure

After downloading the datasets, place the CSV files in Google Drive using this structure:

```text
MyDrive/
└── IDS/
    ├── CSE_CIC_IDS2018/
    │   ├── 02-14-2018.csv
    │   ├── 02-15-2018.csv
    │   ├── 02-16-2018.csv
    │   ├── 02-20-2018.csv
    │   ├── 02-21-2018.csv
    │   ├── 02-22-2018.csv
    │   ├── 02-23-2018.csv
    │   ├── 02-28-2018.csv
    │   ├── 03-01-2018.csv
    │   └── 03-02-2018.csv
    │
    └── CIC_IDS2017/
        ├── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv
        ├── Friday-WorkingHours-Afternoon-PortScan.pcap_ISCX.csv
        ├── Friday-WorkingHours-Morning.pcap_ISCX.csv
        ├── Monday-WorkingHours.pcap_ISCX.csv
        ├── Thursday-WorkingHours-Afternoon-Infilteration.pcap_ISCX.csv
        ├── Thursday-WorkingHours-Morning-WebAttacks.pcap_ISCX.csv
        ├── Tuesday-WorkingHours.pcap_ISCX.csv
        └── Wednesday-workingHours.pcap_ISCX.csv
```

## Notebook Paths

The Colab notebook expects these paths:

```python
DATA_DIR_2018 = '/content/drive/MyDrive/IDS/CSE_CIC_IDS2018'
DATA_DIR_2017 = '/content/drive/MyDrive/IDS/CIC_IDS2017'
```

## Notes

The notebook uses streamed loading and sampling to make the project feasible in Google Colab. The raw datasets must be downloaded separately from the official sources listed above.
