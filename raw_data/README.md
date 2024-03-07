# RAW_DATA
## Obtaining the data
In this project the database used is CHB-MIT Scalp EEG Database (https://physionet.org/content/chbmit/1.0.0/). The raw data in this directory can be downloaded from https://physionet.org/files/chbmit/1.0.0/
using the following command:
```bash
 wget -r -N -c -np https://physionet.org/files/chbmit/1.0.0/
```
This will download the following directory:
```
physionet.org
├── ANNOTATORS
├── files
│   └── chbmit
│     ├── chb01
│     ├── chb02
│     ├── chb03
│     ├── chb04
│     ├── chb05
│     ├── chb06
│     ├── chb07
│     ├── chb08
│     ├── chb09
│     ├── chb10
│     ├── chb11
│     ├── chb12
│     ├── chb13
│     ├── chb14
│     ├── chb15
│     ├── chb16
│     ├── chb17
│     ├── chb18
│     ├── chb19
│     ├── chb20
│     ├── chb21
│     ├── chb22
│     ├── chb23
│     └── chb24
├── index.html
├── README.md
├── RECORDS
├── RECORDS-WITH-SEIZURES
├── robots.txt
├── SHA256SUMS.txt
├── shoeb-icml-2010.pdf
└── SUBJECT-INFO
```
Where chb01, ..., chb24 are directories containing the .edf files with the data for each patient. 

After downloading the data, all the chb* directories should be moved to the raw_data/patients directory:
 ```bash
    mv physionet.org/files/chbmit/* raw_data/patients/
 ```


## Methods for obtaining the data
This is extracted from the original web (https://physionet.org/content/chbmit/1.0.0/).

_Recordings, grouped into 23 cases, were collected from 22 subjects (5 males, ages 3–22; and 17 females, ages 1.5–19). (Case chb21 was obtained 1.5 years after case chb01, from the same female subject.)_

_Each case (chb01, chb02, etc.) contains between 9 and 42 continuous .edf files from a single subject. Hardware limitations resulted in gaps between consecutively-numbered .edf files, during which the signals were not recorded; in most cases, the gaps are 10 seconds or less, but occasionally there are much longer gaps. In order to protect the privacy of the subjects, all protected health information (PHI) in the original .edf files has been replaced with surrogate information in the files provided here._

_Dates in the original .edf files have been replaced by surrogate dates, but the time relationships between the individual files belonging to each case have been preserved. In most cases, the .edf files contain exactly one hour of digitized EEG signals, although those belonging to case chb10 are two hours long, and those belonging to cases chb04, chb06, chb07, chb09, and chb23 are four hours long; occasionally, files in which seizures are recorded are shorter._

_All signals were sampled at 256 samples per second with 16-bit resolution. Most files contain 23 EEG signals (24 or 26 in a few cases). The International 10-20 system of EEG electrode positions and nomenclature was used for these recordings. In a few records, other signals are also recorded, such as an ECG signal in the last 36 files belonging to case chb04 and a vagal nerve stimulus (VNS) signal in the last 18 files belonging to case chb09. In some cases, up to 5 “dummy” signals (named "-") were interspersed among the EEG signals to obtain an easy-to-read display format; these dummy signals can be ignored._


## Data description
This is extracted from the original web (https://physionet.org/content/chbmit/1.0.0/).

_The RECORDS file contains a list of all 664 .edf files included in this collection, and the RECORDS-WITH-SEIZURES file lists the 129 of those files that contain one or more seizures. The SUBJECT-INFO file contains the gender and age of each subject. (Case chb24 was added to this collection in December 2010, and is not currently included in SUBJECT-INFO.)_

_In all, these records include 198 seizures (182 in the original set of 23 cases); the beginning ([) and end (]) of each seizure is annotated in the .seizure annotation files that accompany each of the files listed in RECORDS-WITH-SEIZURES. In addition, the files named chbnn-summary.txt contain information about the montage used for each recording, and the elapsed time in seconds from the beginning of each .edf file to the beginning and end of each seizure contained in it._
